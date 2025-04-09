# Little-o

In addition to the big-O, big-$\Omega$, and big-$\Theta$ notation that
we covered at the beginning of this class, a few other notations are sometimes
used in asymptotic analysis.  For example, "little-$o$" notation.

Prove (i.e.\ give a formal mathematical proof) that $f(n)\in o(g(n))$ implies
that $f(n)\in O(g(n))$.

Hint: The proof will be *very* short and *very* easy. You can start by
identifying the differences between the definitions of O and o.

I have started with the formal definition of $o$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$f(n)\in o(g(n)) \iff \forall c>0, \exists n_0, \forall n\ge n_0: f(n) < c g(n)$

## Solution

First let's compare little-o and big-O:

Little-o:

$$f(n)\in o(g(n)) \iff \forall c>0, \exists n_0, \forall n\ge n_0: f(n) < c g(n)$$

This says that for every positive constant $c$ there is a threshold $n_0$ that for all $n$ greater than or equal to $n_0$, the function $f(n)$ is less than $c g(n)$

Big-O:

$$T(n) \in O(f(n)) \iff \exists c, n_0,  \forall n \geq n_0: T(n) \leq c f(n)$$

This says that for every positive (implied) constant $c$ there is a threshold that for all $n$ greater than or equal to $n_0$, the function $T(n)$ is less than _or equal to_ $c f(n)$. We can convert this to similar function notation:

$$f(n) \in O(g(n)) \iff \exists c, n_0,  \forall n \geq n_0: f(n) \leq c g(n)$$

That means to show " $f(n)\in o(g(n))$ implies that $f(n)\in O(g(n))$ " we need to find a positive constant $c$ and $n_0$ that for all $n \geq n_0$, $f(n) \le c g(n)$. For the sake of simplicity we can let $c = 1$. Following the definition of little-o, there must exist some $n_0$ such that $f(n) < g(n)$. Because this is a strict inequality, it must imply the weaker inequality ($\le$):

$f(n) \le g(n)$

We have now found a constant $c$ and an $n_0$ such that for all $n \ge n_0, f(n) \le c g(n)$.

$$\therefore  f(n)\in o(g(n)) \implies f(n)\in O(g(n))$$

## Disclaimer

I used [this](https://math.stackexchange.com/questions/2543452/what-are-the-strong-and-weak-in-mathematics) to make sure the equality strength argument wasn't bogus.

I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.
