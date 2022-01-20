# CS 170
### Efficient Algorithms and Intractable Problems
UC Berkeley Spring 2022, taught by Prof Prasad Raghavendra

- [x] Week 0: Asymptotic Analysis (lec1); Divide and Conquer (lec2)
- [ ] Week 1: 
- [ ] Week 2:
- [ ] Week 3:
- [ ] Week 4:
- [ ] Week 5:

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
- Master Theorem: For a recurrence function of the form *T(n) = a T(n/b) + f(n)*:
  - temp
  - temp

