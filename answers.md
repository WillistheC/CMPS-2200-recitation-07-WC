# CMPS 2200 Recitation 07
## Answers

**Name:**_________________________
**Name:**_________________________


Place all written answers from `recitation-07.md` here for easier grading.



- **2) (2 pts)** Write a recurrence for the **work** of this algorithm and solve it. Assume the input is $n$ to compute $F_n$.

  Since fib_recursive calls the recursion on $n-1$ and $n-2$, we get $W(n) = 1 + W(n-1) + W(n-2)$

  After $k$ expansions, it reaches $W(n) ≈ (2^{k}-1) + 2^{k}W(n-k) = 2^{n+1} + 2^{n}W(0) = O(2^{n})

- **3) (2 pts)** Write a recurrence for the **span** of this algorithm and solve it.

  Following that logic, to find the longest chain of dependence: $S(n) = 1 + max{S(n-1), S(n-2)}$

  Clearly, that gets to $S(n) = 1 + S(n-1)$ after expansion, $S(n) = (n - 1) + S(1) = O(n)$

- **4) (1 pt)** Inspecting the `counts` list, what interesting pattern emerges?

  We get the fib sequence backward

- **6) (2 pts)** When computing $F_n$, what is the maximum number of times that `fib_top_down(i)` will be called for any value $i$? Based on this, what is the **work** and **span** of this algorithm?

It is called at most twice, so $W(n) = O(2n) = O(n)$

- **8) (2 pts)** When computing $F_n$, what is the maximum number of times that
  $F_i$ will be read from the list for any value $i$? Based on this, what is the **work** and **span** of `fib_bottom_up`?

It is called at most twice, so $W(n) = O(2n) = O(n)$
