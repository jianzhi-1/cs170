# CS 170
### Efficient Algorithms and Intractable Problems
UC Berkeley Spring 2022, taught by Prof Prasad Raghavendra and Prof John Wright

- [x] Week 1: Asymptotic Analysis (lec1); Divide and Conquer (lec2)
- [x] Week 2: Master's Theorem (lec3); Fourier Transform (lec4)
- [x] Week 3: Graphs (lec5); DFS and variants (lec6)
- [x] Week 4: Paths and Dijkstra (lec7); Greedy (lec8)
- [x] Week 5: Minimum Spanning Tree (lec9); UFDS (lec10)
- [x] Week 6: Minimum Set Cover (lec11); Dynamic Programming (lec12)
- [x] Week 7: All Pairs Shortest Path (lec13); Applications of Dynamic Programming (lec14)
- [x] Week 8: Linear Programming (lec15); Max Flow, Bipartite Matching (lec16)
- [x] Week 9: Duality Theorems, Zero Sum Games (lec17); Multiplicative Weights Update (lec18)
- [x] Week 10: ๐ Spring Break ๐
- [x] Week 11: Reduction (lec19); P and NP, NP Completeness (lec20)
- [x] Week 12: Midterm 2; 
- [x] Week 13: ; Streaming
- [x] Week 14: Sketching
- [x] Week 15: Primality Testing; Quantum Algorithms

### Asymptotic Analysis
- Let *f, g: โค<sup>+</sup> โ โ<sup>+</sup>*. Say *f = O(g)* if there is a constant *c > 0* s.t. *f(n) โค cยทg(n)*.
- *f = ฮฉ(g)* means *g = O(f)*
- *f = ฮ(g)* means *f = O(g)* and *f = ฮฉ(g)*
- *g(n) = 1 + c + ... + c<sup>n</sup>*
  - *ฮ(1)* if *c < 1*
  - *ฮ(n)* if *c = 1*
  - *ฮ(c<sup>n</sup>)* if *c > 1*

### Divide and Conquer
- Multiplication: *O(n<sup>log(3)</sup>)*
- Strassen's Algorithm: matrix multiplication in *O(n<sup>log(7)</sup>)*
- Master Theorem: For a recurrence function of the form *T(n) = a T(n/b) + n<sup>c</sup>* with *b > 1*, *a, c > 0*
  - *c > log<sub>b</sub>a* โ *T(n) โ O(n<sup>c</sup>)*
  - *c = log<sub>b</sub>a* โ *T(n) โ O(n<sup>c</sup> log n)*
  - *c < log<sub>b</sub>a* โ *T(n) โ O(n<sup>log<sub>b</sub>a</sup>)*

### Fourier Transform

##### Discrete Fourier Transform (โ Evaluation)
Input: *(a<sub>0</sub>, ..., a<sub>n-1</sub>)* which defines a polynomial *A(z) = ฮฃa<sub>i</sub>z^<sup>n</sup>*
Output: Evaluates *A* at the *n*th roots of infinity (i.e. *A(1), A(-1), A(i), A(-i), ...*)

##### Inverse Fourier Transform (โ Interpolation)
Input: *(A(1), A(-1), A(i), A(-i), ...)* (i.e. the evaluations of *A* at *n*th roots of unity)
Output: *(a<sub>0</sub>, ..., a<sub>n-1</sub>)* (i.e. the coefficients of the polynomial)

##### Fast Fourier Transform (FFT) Algorithm
Key ideas:
- Divide and Conquer, split problem of degree *n* polynomial into two sub-problems of degree *n/2* polynomials
- *A(z) = E(z<sup>2</sup>) + z O(z<sup>2</sup>)*, where *E* and *O* are polynomials of degree *n/2*
- Evaluating *A* at *n*th roots of unity, suffices to evaluate *E* and *O* at *n/2*th roots of unity
- More efficient that naive algorithm, because it avoids unnecessary computation of terms shared by *E* and *O*

Runtime complexity: *O(n log n)* where *n* is the degree of the polynomial

##### Inverse Fourier Transform
- *a<sub>l</sub> = (1/n<sup>1/2</sup>) ฮฃA(ฯ<sup>j</sup>) ฯ<sup>-lj</sup>*
- Replacing *ฯ* in FFT with *1/ฯ*

##### Applications
- Convolution of polynomials (just set number of points to *2<sup>k</sup> > n*

### Graphs

### Dynamic Programming

### Network Flow
##### s-t Max Flow
- Ford Fulkerson *O((|V| + |E|)f<sup>**</sup>* where *f<sup>\*</sup>* is the maximum flow.
  - Might not terminate for **irrational** capacities.
- Edmond-Karp *O(|E|<sup>2</sup>|V|)*
- Dinic's Algorithm *O(|V|<sup>2</sup>|E|)*
- Lemma 1: Any *s-t* flow decomposes into at most *m* cycles and *s-t* paths
- Lemma 2: Suppose *f* is a flow in *G* and it is not a max flow. Then *f<sup>\*</sup> - f* is a feasible flow in *G<sub>f</sub>*

### Matching

### Probabilistic Algorithms

### Implementation
Rip, why the coding in CS170 is in Python ๐

```python3
import random
rc = random.choice
rs = random.shuffle

def f(a, b):
  return random.randint(a, b) # returns integer from [a, b] (inclusive)
```

### Exam Area

#### Midterm 1 Prep ๐ค
See my [Midterm 1 Sheet](https://github.com/jianzhi-1/cs170/blob/main/CS170_Midterm1Sheet.pdf)
- [x] 20 Fall
- [x] 20 Spring
- [x] 19 Fall
- [x] 19 Spring

#### Midterm 2 Prep ๐ค
See my [Midterm 2 Sheet](https://github.com/jianzhi-1/cs170/blob/main/CS170Midterm2Sheet.pdf)
- [x] 19 Fall
- [x] 19 Spring

#### Final Exam Prep ๐ค
- [ ] YY Spring/Fall
