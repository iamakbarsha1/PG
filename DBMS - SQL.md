### 1. Create the following tables with the mapping given below.
	1. emp_details (emp_no, emp_name, DOB, address, doj, mobile_no, dept_no, salary).
		1. Display the months between the doj and till date.
		2. Display the emp_name getting highest salary.
		3. Alter the table emp_details to add a primary key constraint on emp_no.
		4. Create a view emp1 from emp_details such that it contains only emp_no and emp_name.
		5. Write a pl/sql program to display the salary of a particular employee using functions.

```sql
-- Create emp_details table
CREATE TABLE emp_details (
    emp_no INT,
    emp_name VARCHAR(255),
    DOB DATE,
    address VARCHAR(255),
    doj DATE,
    mobile_no VARCHAR(15),
    dept_no INT,
    salary DECIMAL(10, 2)
);

-- Display the months between doj and till date
SELECT emp_no, emp_name, MONTHS_BETWEEN(SYSDATE, doj) AS months_worked
FROM emp_details;

-- Display the emp_name getting the highest salary
SELECT emp_name
FROM emp_details
WHERE salary = (SELECT MAX(salary) FROM emp_details);

-- Alter the table emp_details to add a primary key constraint on emp_no
ALTER TABLE emp_details
ADD CONSTRAINT pk_emp_details PRIMARY KEY (emp_no);

-- Create a view emp1 from emp_details with emp_no and emp_name
CREATE VIEW emp1 AS
SELECT emp_no, emp_name
FROM emp_details;

-- PL/SQL program to display the salary of a particular employee using functions
CREATE OR REPLACE PROCEDURE get_employee_salary(p_emp_no INT) AS
    v_salary DECIMAL(10, 2);
BEGIN
    SELECT salary INTO v_salary
    FROM emp_details
    WHERE emp_no = p_emp_no;
    
    DBMS_OUTPUT.PUT_LINE('Salary of Employee ' || p_emp_no || ': ' || v_salary);
END;
/
```


### 2. Create the following tables with the mapping given below.
	b. emp_details(emp_no, emp_name, DOB, address, doj, mobile_no, dept_no, salary).
	c. dept_details(dept_no,dept_name, location).
		(i) Select dept_no from dept_details and not in emp_details using both the tables.
		(ii) Display the emp_name getting highest salary.
		(iii) Display the emp_name and dept_name by implementing a left outer join. 
		(iv) Display the employee address in Chennai city.
		(v) Write a pl/sql program to find the largest of two numbers. 
		
```sql
-- Create emp_details table
CREATE TABLE emp_details (
    emp_no INT,
    emp_name VARCHAR(255),
    DOB DATE,
    address VARCHAR(255),
    doj DATE,
    mobile_no VARCHAR(15),
    dept_no INT,
    salary DECIMAL(10, 2)
);

-- Create dept_details table
CREATE TABLE dept_details (
    dept_no INT,
    dept_name VARCHAR(255),
    location VARCHAR(255)
);

-- Select dept_no from dept_details not in emp_details using both tables
SELECT d.dept_no
FROM dept_details d
LEFT JOIN emp_details e ON d.dept_no = e.dept_no
WHERE e.dept_no IS NULL;

-- Display the emp_name getting the highest salary
SELECT emp_name
FROM emp_details
WHERE salary = (SELECT MAX(salary) FROM emp_details);

-- Display emp_name and dept_name by implementing a left outer join
SELECT e.emp_name, d.dept_name
FROM emp_details e
LEFT JOIN dept_details d ON e.dept_no = d.dept_no;

-- Display the employee address in Chennai city
SELECT emp_name, address
FROM emp_details
WHERE address LIKE '%Chennai%';

-- PL/SQL program to find the largest of two numbers
CREATE OR REPLACE PROCEDURE find_largest(p_num1 NUMBER, p_num2 NUMBER) AS
    v_largest NUMBER;
BEGIN
    IF p_num1 > p_num2 THEN
        v_largest := p_num1;
    ELSE
        v_largest := p_num2;
    END IF;

    DBMS_OUTPUT.PUT_LINE('The largest of ' || p_num1 || ' and ' || p_num2 || ' is: ' || v_largest);
END;
/
```

### 3. Create the following tables with the mapping given  below.
	a. emp_details (emp_no,emp_name,DOB,address,doj,mobile_no,dept_no,salary).
	b. dept_details (dept_no,dept_name,location).
		(i) List all employees which starts with either B or C.
		(ii) Select dept_no from dept_details and not in emp_details using both the tables.
		(iii) Display the emp_name and dept_name by implementing a right outer join.
		(iv) Display the name of employees order by Salary.
		(v) Write PL/SQL Program to generate even numbers.

```sql
-- Create emp_details table
CREATE TABLE emp_details (
    emp_no INT,
    emp_name VARCHAR(255),
    DOB DATE,
    address VARCHAR(255),
    doj DATE,
    mobile_no VARCHAR(15),
    dept_no INT,
    salary DECIMAL(10, 2)
);

-- Create dept_details table
CREATE TABLE dept_details (
    dept_no INT,
    dept_name VARCHAR(255),
    location VARCHAR(255)
);

-- List all employees which start with either B or C
SELECT * FROM emp_details WHERE emp_name LIKE 'B%' OR emp_name LIKE 'C%';

-- Select dept_no from dept_details not in emp_details using both tables
SELECT d.dept_no
FROM dept_details d
LEFT JOIN emp_details e ON d.dept_no = e.dept_no
WHERE e.dept_no IS NULL;

-- Display emp_name and dept_name by implementing a right outer join
SELECT e.emp_name, d.dept_name
FROM emp_details e
RIGHT JOIN dept_details d ON e.dept_no = d.dept_no;

-- Display the name of employees ordered by Salary
SELECT emp_name, salary
FROM emp_details
ORDER BY salary;

-- PL/SQL program to generate even numbers
CREATE OR REPLACE PROCEDURE generate_even_numbers(p_limit NUMBER) AS
BEGIN
    FOR i IN 2..p_limit BY 2 LOOP
        DBMS_OUTPUT.PUT_LINE(i);
    END LOOP;
END;
/
```

### 4. Create the following tables with the mapping given below.
	emp_details (emp_no, emp_name, DOB, address, doj, mobile_no, salary). 
		(i) Add a column dept_no(department number). 
		(ii) List all employees which starts with either B or C.
		(iii) Display the details of those who draw the salary greater than the average salary.
		(iv) Create a view emp1 from emp_details such that it contains only emp_no and emp_name.
		(v) Write a PL/SQL program to find the greatest of 3 numbers.

```sql
-- Create emp_details table
CREATE TABLE emp_details (
    emp_no INT,
    emp_name VARCHAR(255),
    DOB DATE,
    address VARCHAR(255),
    doj DATE,
    mobile_no VARCHAR(15),
    salary DECIMAL(10, 2)
);

-- Add a column dept_no
ALTER TABLE emp_details
ADD dept_no INT;

-- List all employees starting with B or C
SELECT * FROM emp_details WHERE emp_name LIKE 'B%' OR emp_name LIKE 'C%';

-- Display details of those with salary greater than average
SELECT * FROM emp_details WHERE salary > (SELECT AVG(salary) FROM emp_details);

-- Create a view emp1 with only emp_no and emp_name
CREATE VIEW emp1 AS
SELECT emp_no, emp_name FROM emp_details;

-- PL/SQL program to find the greatest of 3 numbers
CREATE OR REPLACE PROCEDURE find_greatest(p_num1 NUMBER, p_num2 NUMBER, p_num3 NUMBER) AS
    v_greatest NUMBER;
BEGIN
    v_greatest := GREATEST(p_num1, p_num2, p_num3);
    DBMS_OUTPUT.PUT_LINE('The greatest number is: ' || v_greatest);
END;
/
```

### 5. Create the following tables with the mapping given below.
	a.  emp_details(emp_no, emp_name, DOB, address, doj, mobile_no, dept_no, salary).
	b.  dept_details(dept_no, dept_name, location).
		(i) Select dept_no from dept_details and not in emp_details using both the tables. (iii) List all the employee detail that who are all located in Chennai.
		(iv) Display the emp_name getting highest salary
		(v) Write PL/SQL queries to create triggers.

```sql
-- Create emp_details table
CREATE TABLE emp_details (
    emp_no INT,
    emp_name VARCHAR(255),
    DOB DATE,
    address VARCHAR(255),
    doj DATE,
    mobile_no VARCHAR(15),
    dept_no INT,
    salary DECIMAL(10, 2)
);

-- Create dept_details table
CREATE TABLE dept_details (
    dept_no INT,
    dept_name VARCHAR(255),
    location VARCHAR(255)
);

-- Select dept_no from dept_details not in emp_details
SELECT dept_no FROM dept_details WHERE dept_no NOT IN (SELECT dept_no FROM emp_details);

-- List all employees located in Chennai
SELECT * FROM emp_details WHERE address LIKE '%Chennai%';

-- Display emp_name with the highest salary
SELECT emp_name FROM emp_details ORDER BY salary DESC LIMIT 1;

-- PL/SQL trigger example (you need to define your own logic here)
CREATE OR REPLACE TRIGGER emp_salary_trigger
BEFORE INSERT ON emp_details
FOR EACH ROW
BEGIN
    -- Your trigger logic here
    -- You can access the new values using :NEW.column_name
    -- For example: DBMS_OUTPUT.PUT_LINE('New salary: ' || :NEW.salary);
END;
/
```

### 6. Create the following table with the mapping given below.
	emp_details(emp_no, emp_name, DOB, address, doj, mobile_no, dept_no, salary).
		(i) List all employees which starts with either B or C.
		(ii) Display the names and dob of all employees who were born in Feburary.
		(iii) List the employees who are all in Cochin.
		(iv) List out the employee names whose salary is greater than 15000.
		(v) Write a pl/sql program to find the sum of 1-100 numbers.

```sql
-- Create emp_details table
CREATE TABLE emp_details (
    emp_no INT,
    emp_name VARCHAR(255),
    DOB DATE,
    address VARCHAR(255),
    doj DATE,
    mobile_no VARCHAR(15),
    dept_no INT,
    salary DECIMAL(10, 2)
);

-- Insert sample data (for demonstration purposes)
INSERT INTO emp_details VALUES
(1, 'John Doe', '1990-02-15', 'New York', '2022-01-01', '1234567890', 1, 20000),
(2, 'Alice Smith', '1985-05-10', 'Cochin', '2022-02-01', '9876543210', 2, 18000),
(3, 'Bob Johnson', '1992-06-20', 'Berlin', '2022-03-15', '5678901234', 1, 16000),
(4, 'Charlie Brown', '1998-02-05', 'Cochin', '2022-04-20', '3456789012', 2, 22000),
-- Add more sample data as needed
;

-- List all employees starting with B or C
SELECT * FROM emp_details WHERE emp_name LIKE 'B%' OR emp_name LIKE 'C%';

-- Display names and DOB of employees born in February
SELECT emp_name, DOB FROM emp_details WHERE EXTRACT(MONTH FROM DOB) = 2;

-- List employees in Cochin
SELECT * FROM emp_details WHERE address = 'Cochin';

-- List employee names with salary greater than 15000
SELECT emp_name FROM emp_details WHERE salary > 15000;

-- PL/SQL program to find the sum of numbers from 1 to 100
DECLARE
    total_sum INT := 0;
BEGIN
    FOR i IN 1..100 LOOP
        total_sum := total_sum + i;
    END LOOP;
    
    DBMS_OUTPUT.PUT_LINE('Sum of numbers from 1 to 100: ' || total_sum);
END;
/
```

### 7. Create the following tables with the mapping given below.
	d. stud_details(reg_no, stu_name, DOB, address, city)
	e. mark_details(reg_no, mark1, mark2,mark3,total)
		(i) Alter the table mark_details to add a column average with data type as number.
		(ii) Display the months between the DOB and till date.
		(iii) Using alter command drop the column address from the table stud_details. 
		(iv) Display the student name along with marks using join.
		(v) Write a pl/sql program to find the sum & avg marks of all the student tusing procedures.

```sql
-- Create stud_details table
CREATE TABLE stud_details (
    reg_no INT PRIMARY KEY,
    stu_name VARCHAR(255),
    DOB DATE,
    address VARCHAR(255),
    city VARCHAR(255)
);

-- Create mark_details table
CREATE TABLE mark_details (
    reg_no INT PRIMARY KEY,
    mark1 INT,
    mark2 INT,
    mark3 INT,
    total INT,
    average NUMBER
);

-- Alter table mark_details to add a column 'average'
ALTER TABLE mark_details ADD average NUMBER;

-- Display months between DOB and current date
-- Note: The actual SQL to calculate months between dates can vary based on the database system being used.
-- Below is an example for Oracle. Modify accordingly for your database.
SELECT MONTHS_BETWEEN(SYSDATE, DOB) AS months_between FROM stud_details;

-- Using alter command drop the column 'address' from stud_details
ALTER TABLE stud_details DROP COLUMN address;

-- Display student name along with marks using JOIN
SELECT s.stu_name, m.mark1, m.mark2, m.mark3
FROM stud_details s
JOIN mark_details m ON s.reg_no = m.reg_no;

-- PL/SQL program to find the sum & avg marks of all students using procedures
CREATE OR REPLACE PROCEDURE calculate_marks_statistics IS
    total_marks NUMBER;
    avg_marks NUMBER;
BEGIN
    -- Calculate total marks
    SELECT SUM(total) INTO total_marks FROM mark_details;

    -- Calculate average marks
    SELECT AVG(total) INTO avg_marks FROM mark_details;

    -- Display the results
    DBMS_OUTPUT.PUT_LINE('Total Marks of all students: ' || total_marks);
    DBMS_OUTPUT.PUT_LINE('Average Marks of all students: ' || avg_marks);
END;
/

-- Execute the procedure
EXECUTE calculate_marks_statistics;
```

### 8. Create the following tables with the mapping given below.
	a. stud_details (reg_no, stu_name, DOB, address, city)
	b. mark_details (reg_no, mark1, mark2, mark3, total)
		(i) Find out the name of all students.
		(ii) List all the student detail that who are all located in Chennai.
		(iii) Drop the table mark_details.
		(iv) Enlist the students who are all scored above 80 marks.
		(v) Write a pl/sql program to find the address of a particular student using functions.

```sql
-- Create stud_details table
CREATE TABLE stud_details (
    reg_no INT PRIMARY KEY,
    stu_name VARCHAR(255),
    DOB DATE,
    address VARCHAR(255),
    city VARCHAR(255)
);

-- Create mark_details table
CREATE TABLE mark_details (
    reg_no INT PRIMARY KEY,
    mark1 INT,
    mark2 INT,
    mark3 INT,
    total INT
);

-- Find out the name of all students
SELECT stu_name FROM stud_details;

-- List all the student details located in Chennai
SELECT * FROM stud_details WHERE city = 'Chennai';

-- Drop the table mark_details
DROP TABLE mark_details;

-- Enlist the students who scored above 80 marks
-- Assuming you want to include the total marks here
SELECT s.stu_name, m.total
FROM stud_details s
JOIN mark_details m ON s.reg_no = m.reg_no
WHERE m.total > 80;

-- PL/SQL program to find the address of a particular student using functions
CREATE OR REPLACE FUNCTION get_student_address(reg_no_in IN INT) RETURN VARCHAR2 IS
    student_address VARCHAR2(255);
BEGIN
    -- Assuming you want to find the address based on reg_no
    SELECT address INTO student_address
    FROM stud_details
    WHERE reg_no = reg_no_in;

    RETURN student_address;
END;
/

-- Example of using the function
DECLARE
    address VARCHAR2(255);
BEGIN
    address := get_student_address(1); -- Replace 1 with the desired reg_no
    DBMS_OUTPUT.PUT_LINE('Student Address: ' || address);
END;
/
```

### 9. Create the following table with the mapping given below.
	a. stud_details(reg_no, stu_name, DOB, address, city)
	b. mark_details(reg_no, mark1, mark2, mark3, total)
		(i) Find the name of the student whose reg_no  is’107’.
		(ii) Display the details of a particular student whose name  is ‘PETER’.
		(iii) Rename the table mark_details as ’academics’.
		(iv) Display the students name alon with their marks using Join.
		(v) Write a pl/sql program to find the sum & avg marks of all the student using procedures.

```sql
-- Create stud_details table
CREATE TABLE stud_details (
    reg_no INT PRIMARY KEY,
    stu_name VARCHAR(255),
    DOB DATE,
    address VARCHAR(255),
    city VARCHAR(255)
);

-- Create mark_details table
CREATE TABLE mark_details (
    reg_no INT PRIMARY KEY,
    mark1 INT,
    mark2 INT,
    mark3 INT,
    total INT
);

-- Insert sample data into stud_details
INSERT INTO stud_details VALUES (101, 'John', '1990-01-01', 'Address1', 'City1');
INSERT INTO stud_details VALUES (102, 'Jane', '1992-02-15', 'Address2', 'City2');
INSERT INTO stud_details VALUES (107, 'Peter', '1988-05-20', 'Address3', 'City3');

-- Insert sample data into mark_details
INSERT INTO mark_details VALUES (101, 80, 85, 90, 255);
INSERT INTO mark_details VALUES (102, 75, 88, 92, 255);
INSERT INTO mark_details VALUES (107, 90, 95, 88, 273);

-- (i) Find the name of the student whose reg_no is '107'
SELECT stu_name
FROM stud_details
WHERE reg_no = 107;

-- (ii) Display the details of a particular student whose name is 'PETER'
SELECT *
FROM stud_details
WHERE stu_name = 'PETER';

-- (iii) Rename the table mark_details as 'academics'
ALTER TABLE mark_details
RENAME TO academics;

-- (iv) Display the students' names along with their marks using Join
SELECT s.stu_name, a.mark1, a.mark2, a.mark3, a.total
FROM stud_details s
JOIN academics a ON s.reg_no = a.reg_no;

-- (v) PL/SQL program to find the sum & avg marks of all students using procedures
CREATE OR REPLACE PROCEDURE calculate_marks_stats IS
    total_marks NUMBER;
    avg_marks NUMBER;
BEGIN
    -- Assuming you want to calculate the sum and average of total marks
    SELECT SUM(total), AVG(total)
    INTO total_marks, avg_marks
    FROM academics;

    DBMS_OUTPUT.PUT_LINE('Total Marks: ' || total_marks);
    DBMS_OUTPUT.PUT_LINE('Average Marks: ' || avg_marks);
END;
/

-- Example of calling the procedure
BEGIN
    calculate_marks_stats;
END;
/
```

