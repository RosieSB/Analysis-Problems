(sol)=
# Solutions
Complete up to Q16, excluding homework questions. 

Homework solutions will be released alongside the return of each piece of work.

(ch1sol)=
## Preliminary problems

[P1.](P1)
The correct statements are (ii) and (v). 

In statement (iv), the quantifiers $\forall$ and $\exists$ are the wrong way round, while in (i) they are missing altogether. Statement (iii) asserts that last part, $|x_n-l|<\varepsilon$ $\forall n\geq N$, should hold for all $\varepsilon$ and for all $N$ --- so again, there is an issue with the quantifiers.

Bonus exercise: prove that (iv) holds if and only if $(x_n)$ is the constant sequence $x_n=l$ for all $n\in\mathbb{N}$.

---
(P2sol)=
[P2.](P2) To appear (Homework 1 question)


---
(P3sol)=
[P3.](P3) To appear (Homework 1 question)

---

[P4.](P4)(i) Let $a, b \geq 0$. Then,

$$
\left(\sqrt{a+b}\right)^2 = a+b,
$$

while,

$$
\left(\sqrt{a}+\sqrt{b}\right)^2 = a + 2\sqrt{a}\sqrt{b} + b \geq a+b.
$$

Therefore

$$
\left(\sqrt{a}+\sqrt{b}\right)^2 \geq \left(\sqrt{a+b}\right)^2.
$$	

Since $\sqrt{a}$, $\sqrt{b}$ and $\sqrt{a+b}$ are all non-negative and the square root function is increasing, we can square root both sides to get

$$
\sqrt{a}+\sqrt{b}\geq\sqrt{a+b}.
$$

(ii)  Note that the inequality we have been asked to prove is symmetric in $a$ and $b$, in the sense that exchanging the roles of $a$ and $b$ does not affect the value of either side.

This means we can assume without loss of generality that $\sqrt{|a|}\geq\sqrt{|b|}$. Then,

$$
\left|\sqrt{|a|} - \sqrt{|b|}\right| = \sqrt{|a|}-\sqrt{|b|},
$$

and we need only show that
```{math}
:label: eq:sqrta-sqrtb
\sqrt{|a|} - \sqrt{|b|} \leq \sqrt{|a - b|}.
```
We use a trick similar to the proof of Corollary 1.1, and write

$$
\sqrt{|a|} = \sqrt{\big|(a-b) + b\big|}.
$$

By the triangle inequality, we have that $|a| = \big|(a-b) + b\big| \leq |a-b|+|b|$.

Since the square root function is increasing, we can square root both sides to get

$$
\sqrt{|a|} \leq \sqrt{|a-b|+|b|}.
$$

Applying the result from (i) to the right-hand side, it follows that

$$
\sqrt{|a|} \leq \sqrt{|a-b|+|b|} \leq \sqrt{|a-b|}+\sqrt{|b|}.
$$

Equation [](#eq:sqrta-sqrtb) now follows by subtracting $\sqrt{|b|}$ from both sides.

(iii) Let $(a_n)$ be a real sequence converging to $l\in\mathbb{R}$. By (ii),

$$
\left|\sqrt{|a_{n}|}-\sqrt{|l|}\right| \leq \sqrt{\big|a_n-l\big|}
$$

for all $n\in\mathbb{N}$.

Let $\varepsilon>0$. Since $a_n\rightarrow l$, there is $N\in\mathbb{N}$ such that $|a_n-l|<\varepsilon^2$ whenever $n\geq N$. Hence for $n\geq N$,

$$
\big|\sqrt{|a_{n}|}-\sqrt{|l|}\big| \leq \sqrt{\varepsilon^2} = \varepsilon.
$$

Thus $\displaystyle\lim_{n\rightarrow\infty}\sqrt{|a_n|} = \sqrt{|l|}$.


---

[P5.](P5) When it exists, the supremum of a set $A\subseteq\mathbb{R}$ is defined to be the unique number $\alpha\in\mathbb{R}$ such that

- $\alpha$ is an upper bound for $A$, and

- if $M$ is any other upper bound for $A$, then $\alpha\leq M$.

We write $\sup A$ for the supremum of $A$, when it exists.

The definition of the infimum is similar: when it exists, the infimum of $A$ is the unique number $\beta\in\mathbb{R}$ such that

(i) $\beta$ is a lower bound for $A$, and

(ii) if $L$ is any other lower bound for $A$, then $\alpha\geq L$.

We write $\inf A$ for the infimum of $A$, when it exists.

The axiom of completeness for the real numbers says that every non-empty bounded above subset of $\mathbb{R}$ has a supremum. Equivalently, it says that every non-empty bounded below subset of $\mathbb{R}$ has an infimum.

For more details, see page 32 of your Semester 2 MAS107 notes.

---

[P6.](P6)(i) $\displaystyle\sup\left\{\frac{m}{n}:m,n\in\mathbb{N} \text{ s.t } m<n\right\}=1$, $\displaystyle\inf\left\{\frac{m}{n}:m,n\in\mathbb{N} \text{ s.t } m<n\right\}=0$.

(ii) $\displaystyle\sup\left\{\frac{(-1)^m}{n}:m,n\in\mathbb{N} \text{ s.t } m<n\right\}=\frac{1}{3}$, $\displaystyle\inf\left\{\frac{(-1)^m}{n}:m,n\in\mathbb{N} \text{ s.t } m<n\right\}=-\frac{1}{2}$.

(iii) $\displaystyle\sup\left\{\frac{n}{3n + 1} :n\in\mathbb{N}\right\}=\frac{1}{3}$, $\displaystyle\inf\left\{\frac{n}{3n + 1} :n\in\mathbb{N}\right\}=\frac{1}{4}$.

---

[P7.](P7)(i) This is false --- for a counter-example, take any singleton set. Then $\sup A=\inf A=1$.

A correct version of the statement would be $\inf A \leq \sup A$.

(ii) True. The analogous statement for $\sup$ was called the characteristic property of the supremum in your MAS107 lecture notes --- see Lemma 2.8 on page 36.

(iii) True. Since $\sup B$ is an upper bound for $B$, and $A$ is a subset of $B$, $\sup B$ must be an upper bound for $A$. But $\sup A$ is a the least upper bound for $A$, hence $\sup A\leq \sup B$. The analogous property for $\inf$ is that $\inf A\geq\inf B$ whenever $A\subseteq B$.

(iv) False. For a counter-example, take $B=\left\{\frac{1}{n}:n\in\mathbb{N}\right\}$, for which $\inf B=0$.

(v) True. Let $s=\max\{\sup A,\sup B\}$. Then $s\geq \sup A$ and $s\geq \sup B$, so $s$ is an upper bound for both $A$ and $B$. Therefore, $s$ is an upper bound for $A\cup B$. But $\sup(A\cup B)$ is the least upper bound of $A\cup B$, and so $s\geq\sup(A\cup B)$. Also, since $A$ and $B$ are both subsets of $A\cup B$, we have by statement (iii) that $s=\max\{\sup A,\sup B)\leq\sup(A\cup B)$. Hence $\max\{\sup A,\sup B)=\sup(A\cup B)$.

(ch2sol)=
## Limits of functions

[1.](1) One has to identify the real numbers where the given formula does not make sense, usually because of a zero in a denominator somewhere, and exclude them.

(i) $A=\mathbb{R} \setminus \{0, -1\}$.

(ii) $g_{2}(x) = \displaystyle\frac{(x-1)(x+4)}{(x-1)(x+2)(x+3)}$, so $A=\mathbb{R} \setminus \{1, -2, -3\}$.

(iii) $g_{3}(x) = \displaystyle\frac{x+4}{(x+2)(x+3)}$, so $A=\mathbb{R} \setminus \{-2, -3\}$.

(iv) $A=\mathbb{R} \setminus \{1\}$.

(v) $A=\mathbb{R} \setminus \{0\}$.

---

(2sol)=
[2.](2) To appear (Homework 1 question)
   
---

(3sol)=
[3.](3) To appear (Homework 1 question)

---

[4.](4) We had $A= \mathbb{R} \setminus \{1, -2, -3\}$, and $f_2:A\to\mathbb{R}$; $\displaystyle g_{2}(x)= \frac{(x + 4)}{(x + 2)(x + 3)}$.

It is considerably easier to use the sequential criterion for functional limits (Theorem 2.1) than it is to proceed directly using the Definition 2.1. We include both methods, for completeness.


**Method 1: Sequences:** <br>
Let $(x_n)$ be a sequence in $A$ converging to $1$. Then, using algebra of limits for real sequences,

$$
\lim_{n\to\infty}f_2(x_n)= \lim_{n\to\infty} \frac{(x_n + 4)}{(x_n + 2)(x_n + 3)} =  \frac{(1 + 4)}{(1 + 2)(1 + 3)} = \frac{5}{12},
$$

where the last equality is using algebra of limits. So $\displaystyle\lim_{x \rightarrow 1}g_{2}(x) = \frac{5}{12}$.

Let $x_n=-2 + \frac{1}{n}$, so that $(x_n)$ is a sequence in $A$ converging to $-2$. Then we see that $(f_2(x_n))$ diverges to $+\infty$ and so $\lim_{x \rightarrow -2}g_{2}(x)$  does not exist.

Similarly, considering $x_n=-3 + \frac{1}{n}$,  we see that $\lim_{x \rightarrow -3}g_{2}(x)$ does not exist.

**Method 2: $(\varepsilon-\delta)$ criterion**: <br>
Intuitively speaking, the limit as $x\rightarrow 1$ "should" be $\frac{(1 + 4)}{(1 + 2)(1 + 3)}=\frac{5}{12}$. 

We prove $\lim_{x\rightarrow 1}f_2(x) = \frac{5}{12}$.

Let $\varepsilon>0$. We wish to find $\delta>0$ so that if $x\in A$ and $0<|x-1|<\delta$, then $\left|f_2(x)-\frac{5}{12}\right| <\varepsilon$.

Now,
\begin{align*}
\left|f_2(x)-\frac{5}{12}\right| &= \left|\frac{(x + 4)}{(x + 2)(x + 3)}-\frac{5}{12}\right| \\
&= \left|\frac{12(x+4)-5(x+2)(x+3)}{(x+2)(x+3)}\right| \\
&= \left|\frac{18-5x^2-13x}{(x+2)(x+3)}\right| \\
&= \left|\frac{(1-x)(5x+18)}{(x+2)(x+3)}\right|  = |x-1|\cdot\frac{|5x+18|}{|x+2||x+3|}.
\end{align*}

We are going to constrain $x$ to be very close to $1$. In particular, we can assume $0<x<2$, so

$$
\left|f_2(x)-\frac{5}{12}\right| =|x-1|\cdot\frac{|5x+18|}{|x+2||x+3|} < |x-1| \frac{5(2)+18}{(2)(3)} = \frac{14}{3}|x-1|.
$$

Finally, we choose $\delta:= \frac{3}{14}\varepsilon$. Then, for $0<|x-1|< \delta$,

$$
\left|f_2(x)-\frac{5}{12}\right| <  \frac{14}{3}|x-1| <  \frac{14}{3}\cdot \frac{3}{14}\varepsilon = \varepsilon.
$$

---

[5.](5) The first part follows by using the definition of the limit of a function in terms of limits of sequences, and then applying the result of [P4 (iii)](#P4)..
<br>
To be precise let $(x_{n})$ be any sequence in $\mathbb{R} \setminus \{a\}$ that converges to $a$. Then since we are given that $\lim_{x \rightarrow a} f(x) = l$, we must have that $\lim_{n\rightarrow\infty} f(x_{n}) = l$. But then by [P4 (iii)](#P4)., we have $\lim_{n\rightarrow\infty} \sqrt{f(x_{n}}) = \sqrt{l}$. So by definition of the limit of a function, $\lim_{x \rightarrow a} \sqrt{f(x)} = \sqrt{l}$.
<br>
Using algebra of limits,  $\lim_{x \rightarrow 1}\displaystyle\frac{x+1}{x^{2}}=\frac{1+1}{1^2}=2$ and
then by the first part $\lim_{x \rightarrow 1}\sqrt{\displaystyle\frac{x+1}{x^{2}}} = \sqrt{2}$.

---

[6.](6) Let $f:A\to \mathbb{R}$ and suppose that $\lim_{x \rightarrow a} f(x) = l$ and $\lim_{x \rightarrow a} f(x) = l'$. Then given any sequence $(x_{n})$ in $A \setminus \{a\}$ that converges to $a$, we have $\lim_{n\rightarrow\infty} f(x_{n}) = l$ and also $\lim_{n\rightarrow\infty} f(x_{n}) = l'$. But then $l = l'$, by uniqueness of limits.

---

[7.](7) 
When $x > 0, \displaystyle\frac{|x|}{x} = \displaystyle\frac{x}{|x|} = \displaystyle\frac{x}{x} = 1 = \text{sgn}(x)$, and when $x < 0, \displaystyle\frac{|x|}{x} = \displaystyle\frac{x}{|x|} = -\displaystyle\frac{x}{x} = -1 = \text{sgn}(x)$. So $\text{sgn}(x) = \displaystyle\frac{|x|}{x} = \displaystyle\frac{x}{|x|}$, when $x\neq 0$.
<br>
Consider the sequences $x_n=\frac{1}{n}$ and $y_n=-\frac{1}{n}$. If $\lim_{x\rightarrow 0}\text{sgn}(x)$ existed, then we would have

$$
\lim_{n\rightarrow\infty}\text{sgn}(x_n)=\lim_{n\rightarrow\infty}\text{sgn}(y_n)=\lim_{x\rightarrow 0}\text{sgn}(x).
$$

But in fact, $\text{sgn}(x_n)=1$ and $\text{sgn}(y_n)=-1$ for all $n\in\mathbb{N}$, so

$$
\lim_{n\rightarrow\infty}\text{sgn}(x_n)=1\neq-1=\lim_{n\rightarrow\infty}\text{sgn}(y_n).
$$

So $\text{sgn}$ does not converge as $x\rightarrow 0$.

For the left and right limits at $0$:

- The left limit is $\displaystyle\lim_{x \rightarrow 0^-} \text{sgn}(x) = -1$, since for any sequence $(x_n)$ approaching $0$ from the left, we have $\text{sgn}(x_n) = -1$ for all $n$.

- The right limit is $\displaystyle\lim_{x \rightarrow 0^+} \text{sgn}(x) = 1$,  since for any sequence $(x_n)$ approaching $0$ from the right, we have $\text{sgn}(x_n) = 1$ for all $n$.

---

[8.](8) To appear (Homework 2 question)

---

[9.](9) To appear (Homework 2 question)


---

[10.](10) The largest subset of $\mathbb{R}$ for which the formula $f(x)=x\sin\left(\frac{1}{x}\right)$ makes sense is $A = \mathbb{R} \setminus \{0\}$.
<br>
We claim that $\displaystyle\lim_{x \rightarrow 0} x \sin\left(\frac{1}{x}\right) = 0$.
<br>
To see this, let $(x_{n})$ be an arbitrary sequence in $A$ that converges to $0$. The sine function takes values only in the interval $[-1,1]$, and so

$$
\left|x_n\sin\left(\frac{1}{x_n}\right)\right| \leq |x_n|
$$

for each $n\in\mathbb{N}$. Put another way,

$$
-|x_{n}| \leq x_{n}\sin\left(\frac{1}{x_n}\right) \leq |x_{n}|
$$

for all $n\in\mathbb{N}$. Since $\displaystyle\lim_{n\to \infty} x_n=0$, we have $ \displaystyle\lim_{n\to \infty} |x_n| =0$. Therefore, but the sandwich rule, $\displaystyle\lim_{n\rightarrow 0}x_n\sin\left(\frac{1}{x_n}\right) = 0$.
<br>
Since $(x_n)$ was arbitrary, $\displaystyle\lim_{x \rightarrow 0} x \sin\left(\frac{1}{x}\right) = 0$.
<br>
You should contrast {numref}`xs1x` with {numref}`s1x` that for the previous question.


```{figure} ../analysis_problems/figs/xsin(1,x).png
---
width: 700px
name: xs1x
---
Graph of the function $f:\mathbb{R}\to\mathbb{R}$; $f(x)=x\sin\left(\frac{1}{x}\right)$ (Problem 10).
```

---

[11.](11) We'll just do $\displaystyle\lim_{x \rightarrow \infty}f(x)$ here, as $\displaystyle\lim_{x \rightarrow -\infty}f(x)$ is so similar.

(i) Let $X\subset\mathbb{R}$ and $f:X\to\mathbb{R}$. We say that $\lim_{x \rightarrow \infty}f(x) = l$ if for all $\varepsilon>0$ there exists $K>0$ such that for all $x\in X$, $x>K$ implies $|f(x)-l|<\varepsilon$.

(ii) The analogue of the sequential criterion is: 
>$\lim_{x \rightarrow \infty}f(x) = l$ if for any sequence $(x_{n})$ in $X$ that diverges to infinity, we have $\lim_{x \rightarrow \infty}f(x_{n}) = l$.

For the proof,  imitate the proof of [Theorem 2.1](https://rosiesb.github.io/Analysis-Notes/2LoF.html#ed). Suppose the $(\varepsilon- K)$ criterion stated in part (i) holds. Let $\varepsilon>0$, and choose $K>0$ such that for all $x\in X$, $x>K$ implies $|f(x)-l|<\varepsilon$.  Let $(x_n)$ be any sequence in $X$ that diverges to infinity. Then using the same $K>0$, there exists $N\in\mathbb{N}$ such that if $n\geq N$, then $x_{n} > K$.  But then, for all $n\geq N$, $x_n>K$, which in turn implies $|f(x_{n}) - l| < \varepsilon$. Hence $\lim_{x \rightarrow \infty}f(x_{n}) = l$, as required.

For the converse, we prove by contrapositive. Suppose the $(\varepsilon-K)$ criterion does not hold. Then there exists $\varepsilon>0$ such that for all $K>0$, there is $x\in X$ for which $x>K$ and $|f(x)-l|\geq \varepsilon$. Apply this successively to $K = 1, 2, 3, \ldots$. For $K=n$, we get $x_n\in X$ with $x_{n} > n$, and $|f(x_{n}) - l| \geq \varepsilon$ for each $n\in\mathbb{N}$. But then, $(x_n)$ is a sequence in $X$ diverging to infinity, and such that $f(x_n)\nrightarrow l$. This shows that the sequential criterion fails. 

(iii) Using the definition: Given any $\varepsilon > 0$, choose $K = \frac{1}{\varepsilon}$. Then $x > K \Rightarrow \frac{1}{x} < \varepsilon$, and so $\lim_{x\to\infty} \frac{1}{x}=0$.

Using sequences: Let $(x_n)$ be any sequence in $\mathbb{R}\setminus\{0\}$ diverging to infinity as $n\rightarrow\infty$. Then, by algebra of limits, $\frac{1}{x_n}\rightarrow 0$. Since the sequence was chosen arbitrarily, it follows that $\lim_{x\rightarrow\infty}\frac{1}{x}=0$.

The case where $x\to-\infty$ is similar.

---

[12.](12)
(i) Let $f:X\to\mathbb{R}$ be a function, where $X\subseteq\mathbb{R}$. We say that $\lim_{x \rightarrow \infty} f(x) = \infty$ if: 
>Given any $M > 0$, there exists $K > 0$ such that $x > K$ implies $f(x) > M$.

The analogue of the sequential criterion is:
>For any sequence $(x_{n})$ in $X$ which diverges to infinity, we also have that $(f(x_{n}))$ diverges to infinity.

The other cases are similar.

(ii) Let $f:\mathbb{R}\to[0,\infty)$, $g:\mathbb{R}\to[0,\infty)$, and suppose $\displaystyle\lim_{x\rightarrow\infty}f(x)=\infty$ and $\displaystyle\lim_{x\rightarrow\infty}g(x)=l$, where $l>0$.
<br>
Let $M > 0$. Since $\lim_{x\rightarrow\infty}f(x)=\infty$, there exists $K_1 > 0$ such that

$$
f(x)>\frac{2M}{l} \hspace{2em} \forall x > K_1.
$$

Since $\lim_{x\rightarrow\infty}g(x)=l$, for all $\varepsilon>0$ we can find $K_2>0$ such that $x>K_2$ implies $|g(x)-l|<\varepsilon$. In other words,

$$
l-\varepsilon < g(x) < l+\varepsilon, \hspace{2em} \forall x>K_2.
$$

This is true for all $\varepsilon$. We apply it specifically to $\varepsilon = \frac{l}{2}$. Then, there is $K_2>0$ such that

$$
\frac{l}{2} < g(x) < \frac{3l}{2}, \hspace{2em} \forall x>K_2.
$$

Let $K=\max\{K_1,K_2\}$. If $x>K$, then $x>K_1$ and $x>K_2$, so $f(x)>\frac{2M}{l}$ and $\frac{l}{2} < g(x) < \frac{3l}{2}$.
<br>
Hence for $x>K$,

$$
f(x)g(x) > \frac{2M}{l}\frac{l}{2} = M.
$$

That is, $\lim_{x\rightarrow\infty}f(x)g(x) = \infty$.

(iii) Let $p:\mathbb{R}\to\mathbb{R}$ be a polynomial of even degree $m$, with positive leading coefficient. Write $m = 2n$ and let
\begin{align*}
p(x) &= a_{2n}x^{2n} + a_{2n-1}x^{2n-1} + \cdots + a_{1}x + a_{0}\\
&= x^{2n}\left(a_{2n} + \frac{a_{2n-1}}{x} + \cdots + \frac{a_{1}}{x^{2n-1}} + \frac{a_{0}}{x^{2n}}\right). 
\end{align*}
We use part (ii). Take $f(x) = x^{2n}$ and $\displaystyle g(x) = a_{2n} + \frac{a_{2n-1}}{x} + \cdots + \frac{a_{1}}{x^{2n-1}} + \frac{a_{0}}{x^{2n}}$.
<br>
Observe that $\displaystyle\lim_{x \rightarrow \infty}f(x) = \infty$ and $\displaystyle\lim_{x \rightarrow \infty}g(x) = a_{2n}$. Hence by part (ii),

$$
\lim_{x \rightarrow \infty}p(x) = \lim_{x \rightarrow \infty}f(x)g(x) = \infty.
$$

If $n$ is odd, $\lim_{x \rightarrow \infty}p(x) = \infty$, but $\lim_{x \rightarrow -\infty}p(x) = -\infty$.


(ch3sol)=
## Continuity


[13.](13) For each of (i) to (v), the function is continuous at each point of its domain. For (i), (ii) and (iii), we have rational functions, which are continuous on all points of $A$ (which is the subset of $\mathbb{R}$ where the denominator is non-zero). For (iv) and (v), we have compositions of rational functions with the exponential and cosine functions, which are continuous on the whole of $\mathbb{R}$. Again, the functions are continuous on all points of $A$ (which is the subset of $\mathbb{R}$ where the denominator of the rational function is non-zero).

---

[14.](14) If $(x_{n})$ is any sequence that converges to $a$, we know that $f(x_n)$ converges to $f(a)$ as $f$ is continuous at $a$, and
we need to show that $(|f|(x_n))$ converges to $|f|(a)$.
<br>
By Corollary 1.1, if $(x_{n})$ is any sequence that converges to $a$,
\begin{align*}
0 \leq ||f|(a)| -|f|(x_{n})| &= ||f(a) - |f(x_{n})|| \\
&\leq |f(a) - f(x_{n})| \rightarrow 0~\mbox{as}~n \rightarrow \infty, 
\end{align*}
as $f$ is continuous. So by the sandwich rule, $\lim_{n\rightarrow\infty} |f|(x_{n}) = |f|(a)$, and so $f$ is continuous at $a$.

---

[15.](15) Let $(x_{n})$ be a sequence in $A$ that converges to $a$. Since $f$ is continuous at $a$ we have $\lim_{n\rightarrow\infty} f(x_{n}) = f(a)$. And then, since $g$ is continuous at $f(a)$, we have $\lim_{n\rightarrow\infty} g(f(x_{n})) = g(f(a))$, and the result follows.

---

[16.](16) $f \circ g:\mathbb{R}\to \mathbb{R}$ given by $(f \circ g)(x) = \frac{1}{1  + x^{2}}$. It is continuous on $\mathbb{R}$ by Theorem 3.2(iv).
<br>
$g \circ f:\mathbb{R} \setminus \{0\} \to \mathbb{R} \setminus \{0\}$ given by $(g \circ f)(x) = {1  + \frac{1}{x^2}}$. It is continuous on $\mathbb{R} \setminus \{0\}$ by Theorem 3.2(iv).