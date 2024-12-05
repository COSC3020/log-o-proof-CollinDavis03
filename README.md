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

**Step 1: Show $log_{2n} \in O(log_{5} n)$**
$log_{2} = (log_{5}n)/(log_{5}2$

let c = $1 / (log_{5} 2) $ Then: 

$log_{2}n \leq c * log_{5}n$ 

Since c is constant that would make %log_{5} 2$ a constant. By definition of O, there exists a constant such that $log_{2} n \leq c * log_{5} n$. Thus making: 

$log_{2}n \in O(log_{5}n)$ 

**Step 2: Show $log_{5}n \in O(log_{2}n)$**

$log_{5}n = (log_{2}n)/(log_{2}5)$

let c = $1 / (log_{2}5)$ Then: 

$log_{5} n \leq c * log_{2} n. 

With $log_{2} 5$ being a constant then by definition of O, there exists a constant c > 0 such that $log_{5} n \leq c * log_{2} n$ Thus: 

$log_{5} n \in O(log_{2} n) 

**Conclusion:**

Since both $log_{2} n \in O(log_{5} n)$ and $log_{5} n \in O(log_{2} n)$ we can conclude that 

$O(log_{2} n) = O(log_{5} n). 

## Sources 
I looked at AaronATM's repo to see how to get started. I borrowed nothing from him just how he started the problem. 

## Plagarism Statement
“I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.”
