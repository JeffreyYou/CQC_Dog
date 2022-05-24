# Dynamic Programming

### 1. Video Game Problem &2. Coin Problem

<div align=center><img width="800"  src="./Pictures/1.PNG"/></div>

### 2. 0-1 Knapsack & Subset Sum

Request 1 ... n each takes time Wi to process.

Can schedule jobs at any time between 0 to W

Object: To schedule jobs such that we maximize the machine's Utilization.



OPT(i, W) = value of the optimal solution using a subset of the items {1...i} with max allowed weight w

```
If n ∉ O, OPT(n, w) = OPT(n-1, W)

If n ∈O, OPT(n, w) = Wn + OPT(n-1,W-Wn)
```

<div align=center><img width="800"  src="./Pictures/2.PNG"/></div>

Subset-sum (n, w):

```
for i = 1 to n
	for w = 0 to W
		use recurrence formula above to compute M[i,w]
	endfor
endfor
return M[n, W]
```

O(nW)

Pseudo-Polynomial time

### 3. Similarity

<div align=center><img width="800"  src="./Pictures/3.PNG"/></div>

### 4. Matrix Multiplication

<div align=center><img width="800"  src="./Pictures/4.PNG"/></div>

### 5. Shortest Path

<div align=center><img width="800"  src="./Pictures/5.PNG"/></div>

# Network Flow

### 1. Residual Graph

<div align=center><img width="800"  src="./Pictures/6.PNG"/></div>

<div align=center><img width="800"  src="./Pictures/7.PNG"/></div>



### 2. Ford- Fullcerson

<div align=center><img width="800"  src="./Pictures/8.PNG"/></div>

<div align=center><img width="800"  src="./Pictures/9.PNG"/></div>

<div align=center><img width="800"  src="./Pictures/11.PNG"/></div>

### 3. Time Complexity

<div align=center><img width="800"  src="./Pictures/10.PNG"/></div>





### 4. Bipartite graph Matching

<div align=center><img width="800"  src="./Pictures/12.PNG"/></div>

### 5. Edge Disjoint Path

<div align=center><img width="800"  src="./Pictures/13.PNG"/></div>

<div align=center><img width="800"  src="./Pictures/14.PNG"/></div>

### 6. Node Disjoint Path

<div align=center><img width="800"  src="./Pictures/15.PNG"/></div>

### 7. Circulation Network

Max flow of G

D = Sigma dv(in or out)

X<D no feasible circle

X>D not possible

X=D feasible circle

<div align=center><img width="800"  src="./Pictures/17.PNG"/></div>

<div align=center><img width="800"  src="./Pictures/16.PNG"/></div>

To remove nodes:

Add S,T. assign demand value to S and T

### 8. Circulation with Demands & Lower bounds

f0 = lower bounds

Lv at each node is fin-fout

Node value D' = D - Lv

<div align=center><img width="800"  src="./Pictures/17.PNG"/></div>

<div align=center><img width="800"  src="./Pictures/18.PNG"/></div>

<div align=center><img width="800"  src="./Pictures/19.PNG"/></div>

<div align=center><img width="800"  src="./Pictures/20.PNG"/></div>

<div align=center><img width="800"  src="./Pictures/21.PNG"/></div>

### 9. Survey Design

<div align=center><img width="800"  src="./Pictures/22.PNG"/></div>

<div align=center><img width="800"  src="./Pictures/23.PNG"/></div>

<div align=center><img width="800"  src="./Pictures/24.PNG"/></div>

<div align=center><img width="800"  src="./Pictures/25.PNG"/></div>
