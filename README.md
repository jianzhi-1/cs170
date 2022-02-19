# CS 170
### Efficient Algorithms and Intractable Problems
UC Berkeley Spring 2022, taught by Prof Prasad Raghavendra and Prof John Wright

- [x] Week 1: Asymptotic Analysis (lec1); Divide and Conquer (lec2)
- [x] Week 2: Master's Theorem (lec3); Fourier Transform (lec4)
- [x] Week 3: Graphs (lec5); DFS and variants (lec6)
- [x] Week 4: Paths and Dijkstra (lec7); Greedy (lec8)
- [x] Week 5: Minimum spanning tree (lec9); UFDS (lec10)
- [ ] Week 6: 
- [ ] Week 7:

### Asymptotic Analysis
- Let *f, g: ℤ<sup>+</sup> → ℝ<sup>+</sup>*. Say *f = O(g)* if there is a constant *c > 0* s.t. *f(n) ≤ c·g(n)*.
- *f = Ω(g)* means *g = O(f)*
- *f = Θ(g)* means *f = O(g)* and *f = Ω(g)*
- *g(n) = 1 + c + ... + c<sup>n</sup>*
  - *Θ(1)* if *c < 1*
  - *Θ(n)* if *c = 1*
  - *Θ(c<sup>n</sup>)* if *c > 1*

### Divide and Conquer
- Multiplication: *O(n<sup>log(3)</sup>)*
- Strassen's Algorithm: matrix multiplication in *O(n<sup>log(7)</sup>)*
- Master Theorem: For a recurrence function of the form *T(n) = a T(n/b) + n<sup>c</sup>* with *b > 1*, *a, c > 0*
  - *c > log<sub>b</sub>a* → *T(n) ∈ O(n<sup>c</sup>)*
  - *c = log<sub>b</sub>a* → *T(n) ∈ O(n<sup>c</sup> log n)*
  - *c < log<sub>b</sub>a* → *T(n) ∈ O(n<sup>log<sub>b</sub>a</sup>)*

### Fourier Transform

##### Discrete Fourier Transform (≈ Evaluation)
Input: *(a<sub>0</sub>, ..., a<sub>n-1</sub>)* which defines a polynomial *A(z) = Σa<sub>i</sub>z^<sup>n</sup>*
Output: Evaluates *A* at the *n*th roots of infinity (i.e. *A(1), A(-1), A(i), A(-i), ...*)

##### Inverse Fourier Transform (≈ Interpolation)
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
- *a<sub>l</sub> = (1/n<sup>1/2</sup>) ΣA(ω<sup>j</sup>) ω<sup>-lj</sup>*
- Replacing *ω* in FFT with *1/ω*

##### Applications
- Convolution of polynomials (just set number of points to *2<sup>k</sup> > n*

### Graphs

### Dynamic Programming

### Linear Programming

### Network Flow

### Duality

### Matching

### Probabilistic Algorithms

### Implementation
Rip, why the coding in CS170 is in Python 😔

```python3
import random
rc = random.choice
rs = random.shuffle

def f(a, b):
  return random.randint(a, b) # returns integer from [a, b] (inclusive)
```

### Exam Area

#### Midterm 1 Prep 😤
See my [Midterm 1 Sheet](https://github.com/jianzhi-1/cs61a/blob/main/MidTerm1Sheet.pdf)
- [ ] 21 Fall
- [ ] 21 Spring
- [ ] 20 Fall
- [x] 20 Spring
- [x] 19 Fall
- [x] 19 Spring

#### Midterm 2 Prep 😤
- [ ] YY Spring/Fall

#### Final Exam Prep 😤
- [ ] YY Spring/Fall
