### Short Questions

#### 1. Mention the Applications of Data Science

Data science has numerous applications across various industries. Some notable ones include:

- **Healthcare**: Predicting disease outbreaks, personalizing treatment plans, and analyzing patient data for better healthcare outcomes.
- **Finance**: Fraud detection, risk management, and algorithmic trading.
- **Retail**: Customer segmentation, inventory management, and personalized marketing.
- **Transportation**: Route optimization, predictive maintenance, and autonomous vehicles.
- **Entertainment**: Recommendation systems (e.g., Netflix, Spotify), content personalization, and audience analytics.

#### 2. Define Sample

A sample is a subset of individuals or observations selected from a larger population. It is used in statistical analysis to make inferences about the population without having to study the entire population.

#### 3. How to Read Dataset in R Programming?

In R, you can read datasets using various functions depending on the data format. For example, to read a CSV file, you can use:

```R
data <- read.csv("path/to/file.csv")
```

Other functions include `read.table()` for text files, `read.xlsx()` for Excel files (with the `xlsx` package), and `readRDS()` for RDS files.

#### 4. What is EDA?

Exploratory Data Analysis (EDA) is the process of examining datasets to summarize their main characteristics, often with visual methods. It helps in understanding the data structure, detecting anomalies, and forming hypotheses for further analysis.

#### 5. State Hypothesis Testing

Hypothesis testing is a statistical method used to make decisions or inferences about population parameters based on sample data. It involves:

1. Formulating a null hypothesis (H0) and an alternative hypothesis (H1).
2. Choosing a significance level (α).
3. Calculating a test statistic from the sample data.
4. Comparing the test statistic to a critical value to decide whether to reject H0.

### Long Questions

#### 1. Explain in Detail About the Life Cycle of Data Science

The data science life cycle typically involves the following stages:

1. **Problem Definition**: Identifying the business problem or objective.
2. **Data Collection**: Gathering relevant data from various sources.
3. **Data Cleaning**: Removing or correcting errors and inconsistencies in the data.
4. **Data Exploration**: Performing EDA to understand the data characteristics and relationships.
5. **Feature Engineering**: Creating new features or selecting important ones for modeling.
6. **Modeling**: Applying statistical or machine learning algorithms to the data.
7. **Evaluation**: Assessing the model's performance using metrics like accuracy, precision, recall, etc.
8. **Deployment**: Implementing the model in a production environment.
9. **Monitoring and Maintenance**: Continuously monitoring the model's performance and updating it as needed.

#### 2. Elucidate Different Sources and 5V’s of Big Data

**Sources of Big Data**:

1. **Social Media**: Platforms like Facebook, Twitter, and LinkedIn.
2. **Sensors/IoT Devices**: Smart devices, industrial equipment, and environmental sensors.
3. **Transactions**: Financial transactions, e-commerce activities, and point-of-sale systems.
4. **Public Data**: Government records, research data, and open data platforms.
5. **Media**: Images, videos, and audio files from various digital media.

**5V's of Big Data**:

1. **Volume**: The amount of data generated.
2. **Velocity**: The speed at which data is generated and processed.
3. **Variety**: The different types of data (structured, unstructured, semi-structured).
4. **Veracity**: The reliability and accuracy of data.
5. **Value**: The potential insights and benefits derived from analyzing the data.

### Problem Solving

#### 1. Cricket Score Data Set

Given the scores: 80, 52, 40, 52, 70, 1, 6

**Mean**: Mean=80+52+40+52+70+1+67=3017=43\text{Mean} = \frac{80 + 52 + 40 + 52 + 70 + 1 + 6}{7} = \frac{301}{7} = 43Mean=780+52+40+52+70+1+6​=7301​=43

**Median**: Ordered scores: 1, 6, 40, 52, 52, 70, 80 The median is the middle value: 52

**Mode**: The mode is the most frequent value: 52

#### 2. Temperature Data

Given the temperatures: 23, 25, 28, 28, 32, 33, 35

**Range**: Range=35−23=12\text{Range} = 35 - 23 = 12Range=35−23=12

**Interquartile Range (IQR)**:

1. Order the data: 23, 25, 28, 28, 32, 33, 35
2. Find Q1 (first quartile, 25th percentile): 25
3. Find Q3 (third quartile, 75th percentile): 33 IQR=Q3−Q1=33−25=8\text{IQR} = Q3 - Q1 = 33 - 25 = 8IQR=Q3−Q1=33−25=8

### Conceptual Questions

#### 1. Brief on Types of Exploratory Data Analysis and Why is EDA Important in Data Science?

**Types of EDA**:

1. **Univariate Analysis**: Examines one variable at a time (e.g., histograms, box plots).
2. **Bivariate Analysis**: Analyzes the relationship between two variables (e.g., scatter plots, correlation).
3. **Multivariate Analysis**: Explores interactions between multiple variables (e.g., pair plots, heatmaps).

**Importance of EDA**:

- Identifies patterns, trends, and anomalies.
- Helps in feature selection and engineering.
- Provides insights that guide further analysis and modeling.
- Validates assumptions and informs hypothesis testing.

#### 2. Explain About Data Visualization Libraries in Python

Popular data visualization libraries in Python include:

1. **Matplotlib**: The most widely used library for creating static, animated, and interactive visualizations.
2. **Seaborn**: Built on top of Matplotlib, provides a high-level interface for drawing attractive and informative statistical graphics.
3. **Plotly**: Enables the creation of interactive plots and dashboards.
4. **Bokeh**: Focuses on interactive visualizations for web applications.
5. **Altair**: A declarative statistical visualization library that simplifies the creation of complex plots.

#### 3. Describe in Detail About Parametric and Non-Parametric Tests

**Parametric Tests**:

- Assumes underlying statistical distributions (e.g., normal distribution).
- Examples: t-test, ANOVA.
- Used when the sample size is large and data follows a known distribution.

**Non-Parametric Tests**:

- Does not assume any specific distribution.
- Examples: Mann-Whitney U test, Kruskal-Wallis test.
- Used when the sample size is small or data does not follow a normal distribution.

### Practical Application

#### 1. How to Calculate Correlation Coefficient Using Python?

You can use the `numpy` or `pandas` library to calculate the correlation coefficient:

```python
import numpy as np
import pandas as pd

# Using numpy
x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]
correlation = np.corrcoef(x, y)[0, 1]

# Using pandas
data = pd.DataFrame({'x': x, 'y': y})
correlation = data['x'].corr(data['y'])

print(correlation)

```

#### 2. Steps to Predict Diabetes Using Data Science Process

1. **Problem Definition**: Define the objective (e.g., predict diabetes).
2. **Data Collection**: Gather relevant data (e.g., patient health records).
3. **Data Cleaning**: Handle missing values, outliers, and inconsistencies.
4. **Exploratory Data Analysis**: Understand data patterns and relationships.
5. **Feature Engineering**: Create new features or select important ones.
6. **Modeling**: Apply machine learning algorithms (e.g., logistic regression, decision trees).
7. **Evaluation**: Assess the model’s performance using metrics (e.g., accuracy, AUC-ROC).
8. **Deployment**: Implement the model in a production environment.
9. **Monitoring**: Continuously monitor and update the model.

#### 3. Real-Life Application of Correlation and Regression

**Correlation**:

- Used in finance to understand the relationship between different stocks or market indices.
- In healthcare, it helps in identifying the correlation between lifestyle factors and disease risk.

**Regression**:

- In real estate, regression models predict property prices based on features like location, size, and amenities.
- In marketing, regression analysis determines the impact of different advertising channels on sales.