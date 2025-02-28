(sol)=
# Solutions

(ch1sol)=
## Preliminary problems

[P1.](P1)
The correct statements are (ii) and (v). 

In statement (iv), the quantifiers $\forall$ and $\exists$ are the wrong way round, while in (i) they are missing altogether. Statement (iii) asserts that last part, $|x_n-l|<\varepsilon$ $\forall n\geq N$, should hold for all $\varepsilon$ and for all $N$ --- so again, there is an issue with the quantifiers.

Bonus exercise: prove that (iv) holds if and only if $(x_n)$ is the constant sequence $x_n=l$ for all $n\in\mathbb{N}$.

---

[P2.](P2) To appear (Homework 1 question)


---

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

[2.](2) To appear (Homework 1 question)
   
---

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