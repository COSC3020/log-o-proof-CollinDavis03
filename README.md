# Asymptotic Equivalences

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

I have started with the formal definition of $O$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$

## Answer

**Definition of Big O**

For a function $T(n)$, we can say $T(n) \in O(f(n))$ if: 

$\exists c > 0, n_{0} > 0$ such that $T(n) \leq c * f(n), \forall n \geq n_0$

**Step 1: Show $T(n) \in O(log_{5}n) \rightarrow T(n) \in O(log_{2}n)$**

1. Assume $T(n) \in O(log_{5}n$. By definition, there exists constants $c > 0$ and $n_{0} > 0$ 

$T(n) \leq c * log_{5} n, \forall n \geq n_{0}$ 

2. Using the base-change formula for logarithms:

   $log_{5} n = (log_{2} n) / (log_{2} 5)$

   Substituting this into the inequality:

   $T(n) \leq c * ((log_{2} n) / (log_{2} 5))$

3. Let $c' = (c) / (log_{2} 5)$ , where $c'$ is a constant because $log_{2} 5$ is constant.

   Then:
         $T(n) \leq c' * log_{2} n, \forall n \geq n_{0}$

4. By definition of Big O, $T(n) \in O(log_{2} n)$.

**Step 2: Show $T(n) \in O(log_{2}n) \rightarrow T(n) \in O(log_{5}n)$**

 1. Assume $T(n) \in O(log_{2}n$. By definition, there exists constants $c > 0$ and $n_{0} > 0$ 

$T(n) \leq c * log_{2} n, \forall n \geq n_{0}$ 

2. Using the base-change formula for logarithms:

   $log_{2} n = (log_{5} n) / (log_{5} 2)$

   Substituting this into the inequality:

   $T(n) \leq c * ((log_{5} n) / (log_{5} 2))$

3. Let $c' = (c) / (log_{5} 2)$ , where $c'$ is a constant because $log_{5} 2$ is constant.

   Then:
         $T(n) \leq c' * log_{5} n, \forall n \geq n_{0}$

4. By definition of Big O, $T(n) \in O(log_{5} n)$.

**Conclusion:** 
From steps 1 and 2, we have shown that: 

  $T(n) \in O(log_{5} n) <-> T(n) \in O(log_{2} n)$

This implies: 

  $O(log_{2} n) = O(log_{5} n)$

Thus, the logarithm base does not affect an algorithm's asymptotic complexity, as the difference is only a constant factor. 

## Sources 
I looked at AaronATM's repo to see how to get started. I borrowed nothing from him just how he started the problem. 

## Plagarism Statement
“I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.”
