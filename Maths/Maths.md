# Part - A
### 1:
![[Pasted image 20240315223501.png]]
![[Pasted image 20240315223523.png]]
![[Pasted image 20240315223611.png]]

### 2:
![[Pasted image 20240315223636.png]]
![[Pasted image 20240315223753.png]]
![[Pasted image 20240315223814.png]]

### 3:
![[Pasted image 20240315223836.png]]
![[Pasted image 20240315224130.png]]
![[Pasted image 20240315224151.png]]

### 4:
![[Pasted image 20240315223922.png]]
![[Pasted image 20240315224234.png]]
![[Pasted image 20240315224252.png]]



### 5:
![[Pasted image 20240315223935.png]]
![[Pasted image 20240315224314.png]]
![[Pasted image 20240315224330.png]]



### 6:
![[Pasted image 20240315223944.png]]
![[Pasted image 20240315224004.png]]
![[Pasted image 20240315224351.png]]


### 7:
![[Pasted image 20240315224028.png]]
![[Pasted image 20240315224432.png]]
![[Pasted image 20240315224442.png]]

### 8:
![[Pasted image 20240315224037.png]]
![[Pasted image 20240315224509.png]]
![[Pasted image 20240315224525.png]]

### 9:
![[Pasted image 20240315224048.png]]
#### What is Graph Theory?
1. Graph Theory is a branch of Mathematics in which we study graphs.
2. Graphs are mathematical structures which consists of a set V of vertices and set E of edges. 
3. Vertices(also called nodes)
#### Origins of Graph Theory:
1. The ‘feeble glance’ which <font color="#ffc000">Leonhard Euler</font> (1707–1783) directed towards the geometry of position consists of a single paper now considered to be the starting point of modern graph theory.
2. The paper published by Euler appeared in Commentarii Academiae Scientiarum Imperialis Petropolitanae in <font color="#ffff00">1736</font> on the <span style="background:#fdbfff">Seven Bridges of Königsberg</span> is regarded as the first paper in the history of graph theory.
3. He created first graph to simulate a real time place and situation to solve a problem which was then considered one of the toughest problems.

### 10:
![[Pasted image 20240315224058.png]]

# Part - B

#### 11:
![[Pasted image 20240315225216.png]]
i)
![[Pasted image 20240315225245.png]]
![[Pasted image 20240315225257.png]]
ii)
![[Pasted image 20240315225323.png]]

#### 12:
![[Pasted image 20240315225348.png]]

i) a→(b→c),(d→(b∧¬c)) and (a∧d) is invalid:

![[Pasted image 20240315232235.png]]

<span style="background:#ff4d4f">BEWARE of ChatGPT</span>

Optional Answer from ChatGPT:
 ![[Pasted image 20240314152101.png]]

ii) Using Truth table: P. T.:- P -> (Q -> R) => (P -> Q) -> (P -> R)
![[Pasted image 20240314152351.png]]

#### 13:
![[Pasted image 20240315225843.png]]
![[Pasted image 20240315225931.png]]
![[Pasted image 20240315225959.png]]
![[Pasted image 20240315230015.png]]


#### 14:
![[Pasted image 20240315230102.png]]
![[Pasted image 20240315230129.png]]
![[Pasted image 20240315230146.png]]
![[Pasted image 20240315230156.png]]

# Part - C (i guess this comes under part - c)
#### 15:
![[Pasted image 20240315230239.png]]

<span style="background:#affad1">Know the concept and DIY</span>
https://www.javatpoint.com/tree-traversal
### i)
1. <font color="#ffff00">Preorder</font> traversal:
	1. This technique follows the '**<span style="background:#b1ffff">root left right</span>**' policy.
	2. It means that, first root node is visited after that the left subtree is traversed recursively, and finally, right subtree is recursively traversed. 
	3. As the root node is traversed before (or pre) the left and right subtree, it is called preorder traversal.
	4. **Algorithm**:
		1. Until all nodes of the tree are not visited  
			1.  Step 1 - Visit the root node  
			2. Step 2 - Traverse the left subtree recursively.  
			3. Step 3 - Traverse the right subtree recursively.
	5. Output:<span style="background:#fff88f">A → B → D → E → C → F → G</span>
	6. ![[Pasted image 20240314150321.png]]
2. <font color="#ffff00">Postorder</font> traversal:
	1. This technique follows the '**<span style="background:#affad1">left-right root</span>**' policy. 
	2. It means that the first left subtree of the root node is traversed, after that recursively traverses the right subtree, and finally, the root node is traversed. 
	3. As the root node is traversed after (or post) the left and right subtree, it is called postorder traversal.
	4. **Algorithm**:
		1. Until all nodes of the tree are not visited  
			1. Step 1 - Traverse the left subtree recursively.  
			2. Step 2 - Traverse the right subtree recursively.  
			3. Step 3 - Visit the root node.
	5. Output: <span style="background:#fff88f">D → E → B → F → G → C → A</span>
	6. ![[Pasted image 20240314150537.png]]
3. <font color="#ffff00">Inorder</font> traversal:
	1. This technique follows the '**<span style="background:#affad1">left-right root</span>**' policy. 
	2. It means that first left subtree is visited after that root node is traversed, and finally, the right subtree is traversed. 
	3. As the root node is traversed between the left and right subtree, it is named inorder traversal.
	5. **Algorithm**:
		1. Until all nodes of the tree are not visited  
			1. Step 1 - Traverse the left subtree recursively.  
			2. Step 2 - Visit the root node.
			3. Step 3 - Traverse the right subtree recursively.
	6. Output: <span style="background:#fff88f">D → B → E → A → F → C → G</span>
	7. ![[Pasted image 20240315231500.png]]

### ii)
<span style="background:#fdbfff">PART - C: ii)</span> For the graph of Figure 1.20, give an example of each of the following or explain why no such an example exists. 
	1. **An x —y walk of length 6:**
		1. An example of an x — y walk of length 6 in the graph would be: <span style="background:#fff88f">x — u — v — w — z — t — y </span>
		2. This walk consists of 6 edges.
	2. **A v — w trail that is not a v — w path:**
		1. In the graph, a v — w trail that is not a v — w path could be: <span style="background:#fff88f">v — u — w</span>. 
		2. This trail visits the vertex u twice, which makes it a trail but not a path.



----------
# <span style="background:#d3f8b6">END :)</span>

-----------

