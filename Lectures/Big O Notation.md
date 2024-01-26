
**What is the key idea of of Big O?**
	We care about how the number of operations **scales** with the size of the input. (algo's rate of growth)

- When taking into consideration the big O of an algorithm, we must ignore constant factors and lower-order terms. 

We have three types of cases for analysis of an algorithm:
1. Worst-case
2. Best-case
3. Average-case


#### What do we mean when we say "$T(n)$ is O($f(n)$)"?

 $T(n)$ denotes the worst-case runtime for an algorithm. 


##### In Language

$T(n) = O(f(n))$ iff $T(n)$ is **eventually upper bounded** by a constant multiple of $f(n)$. 


##### In Graph Example:

![[Pasted image 20240125141806.png]]

##### Math Definition:

$T(n) = O(f(n))$ $iff$ there exists positive **constants**, $c$ and $n_0$ such that for all $n \ge n_0$ 

$$ \begin{aligned} 
T(n) &= O(f(n)) \\ 
& \iff \\ 
\exists \; c, n_0 \; &s.t. \; \forall \; n \ge n_0 \\ 
\\
T(n) &\le c \cdot f(n) \\ 
\end{aligned} $$

When we say "$T(n)$ is $O(f(n))$" we only need cases when $n$ is **sufficiently** large, i.e., $\forall \;\; n\ge n_0$ 

![[Pasted image 20240125143309.png]]


### Proofs:

- To prove $T(n) = O(f(n))$ , you need to annouce $c$ and $n_0$ right away:  
	"Let $c=$ `__` and $n_0 =$ `__`. We will show that $T(n) \le c \cdot f(n)$  for all $n \ge n_0$ "


Example:

Let $c=4$ and $n_0 = 5$. We will now show that $3n^2 + 5n \le c \cdot n^2$ for all $n\ge n_0$.
We know that for any $n \ge n_0$, we have:

$$\begin{aligned} 5 &\le n \\ 
5n &\le n^2 \\ 
5n + 3n^2 &\le n^2 + 3n^2 \\ 
2n^2 + 5n &\le 4n^2 \\ 
\end{aligned}$$

Using our choice of $c$ and $n_0$, we have successfully shown that $3n^2 + 5n \le c\cdot n^2$ for all $n \le n_0$.
From the definition of Big-O, this proves that $3n^2 + 5n = O(n^2)$

>[!Note] Note: If you are asked to formally disprove that T(n) is O(f(n)), **use proof by contradiction**

