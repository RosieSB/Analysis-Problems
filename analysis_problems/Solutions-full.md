(sol)=
# Solutions

## Preliminary problems

[P1.](P1)
The correct statements are (ii) and (v). 

In statement (iv), the quantifiers $\forall$ and $\exists$ are the wrong way round, while in (i) they are missing altogether. Statement (iii) asserts that last part, $|x_n-l|<\varepsilon$ $\forall n\geq N$, should hold for all $\varepsilon$ and for all $N$ --- so again, there is an issue with the quantifiers.

Bonus exercise: prove that (iv) holds if and only if $(x_n)$ is the constant sequence $x_n=l$ for all $n\in\mathbb{N}$.

---

[P2.](P2) (Homework 1 question)

Let $\varepsilon>0$. According to the definition, we must prove there is an $N\in\mathbb{N}$ for which $\left|\frac{2n}{3n-1}-\frac{2}{3}\right|<\varepsilon$ whenever $n\geq N$.

Now,

$$
\left|x_n-\frac{2}{3}\right| = \left|\frac{2n}{3n-1}-\frac{2}{3}\right| = \frac{6n-(6n-2)}{3(3n-1)} = \frac{2}{3(3n-1)}.
$$

This will be strictly less than $\varepsilon$ whenever $3n-1>\frac{2}{3\varepsilon}$., or in other words, whenever

$$
n>\frac{1}{3}\left(\frac{2}{3\varepsilon}+1\right)=\frac{2+3\varepsilon}{9\varepsilon}.
$$

Let $N$ be any integer greater than $\frac{2+3\varepsilon}{9\varepsilon}$. Then $\left|x_n-\frac{2}{3}\right|<\varepsilon$ for all $n\geq N$, and we have proven that $x_n\rightarrow\frac{2}{3}$ as $n\rightarrow\infty$ using the definition.


---

[P3.](P3) (Homework 1 question)

The Bolzano--Weierstrass theorem states that every bounded sequence has a convergent subsequence. Its proof combines the following two results:

- The monotone convergence theorem (Theorem 3.10 in the MAS107 notes), which states that bounded monotone sequences must converge. <br> More specifically, every monotone increasing sequence that is bounded above converges to its supremum, and every monotone decreasing sequence bounded below converges to its infimum.

- Theorem 3.13 from MAS107: Every sequence has a monotone subsequence.

**Proof of Bolzano--Weierstrass:** <br>
If $(x_n)$ is a bounded sequence, then it has a monotone subsequence, $(x_{n_k})$, by Theorem 3.13. This subsequence must also be bounded since $(x_n)$ is bounded, and hence it converges by the monotone convergence theorem.


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

## Limits of functions

[1.](1) One has to identify the real numbers where the given formula does not make sense, usually because of a zero in a denominator somewhere, and exclude them.

(i) $A=\mathbb{R} \setminus \{0, -1\}$.

(ii) $g_{2}(x) = \displaystyle\frac{(x-1)(x+4)}{(x-1)(x+2)(x+3)}$, so $A=\mathbb{R} \setminus \{1, -2, -3\}$.

(iii) $g_{3}(x) = \displaystyle\frac{x+4}{(x+2)(x+3)}$, so $A=\mathbb{R} \setminus \{-2, -3\}$.

(iv) $A=\mathbb{R} \setminus \{1\}$.

(v) $A=\mathbb{R} \setminus \{0\}$.

---

[2.](2) (Homework 1 question)
   
(i) $L=[0,1]\cup[2,3]$.
   
(ii) $L=\emptyset$.  (All convergent sequences in $\mathbb{Z}$ are eventually constant.)
   
(iii) $L=\mathbb{R}$.
   
(iv) $L=[0,1]$
   
(v) $L=\{0\}$

---

[3.](3) (i) We are given $f:\mathbb{R}\to\mathbb{R}$; $f(x)=4x+7$. Intuition tells us that 

$$
\lim_{x\rightarrow 2}f(x) = 4\cdot 2+7 = 15.
$$

To prove this, let $\varepsilon>0$. We seek $\delta>0$ such that $0<|x-2|<\delta$ implies $|f(x)-15|<\varepsilon$.

Note that

$$
|f(x)-15| = |4x+7-15| = |4x-8| = 4|x-2|.
$$

Therefore, putting $\delta=\frac{\varepsilon}{4}$, we get that whenever $0<|x-2|<\delta$, 

$$
|f(x)-17| = 4|x-2| < 4\cdot\frac{\varepsilon}{4} = \varepsilon.
$$

For the limit as $x\rightarrow 0$, we claim that $\lim_{x\rightarrow 0}f(x)=7$. To prove this, note that $|f(x)-7|=4|x|$. This means that given $\varepsilon>0$, if $0<|x|<\frac{\varepsilon}{4}$ then 

$$
|f(x)-7|<4\cdot\frac{\varepsilon}{4} = \varepsilon.
$$

It follows that $\lim_{x\rightarrow 0}f(x)$ exists and is equal to $7$.

(ii) We have $f:\{0\}\cup[1,3]\to\mathbb{R}$; $f(x)=3x^2-1$, so using intuition only, $\lim_{x\rightarrow 2} f(x)=3\cdot 4-1=11$.

Let $\varepsilon>0$. We seek $\delta>0$ such that for all $x\in\{0\}\cup[1,3]$, 

$$
0<|x-2|<\delta \; \Rightarrow \; |f(x)-11|<\varepsilon.
$$

Now, for $x\in\{0\}\cup[1,3]$,

$$
|f(x)-11| = |3x^2-12| = 3|x^2-4| = 3|x-2||x+2| \leq 15|x-2|.
$$    

(Here, we have used the fact that $|x+2| = x+2 \leq 5$, for $x\in\{0\}\cup[1,3]$.) 

Hence we can let $\delta:=\frac{1}{15}$ and conclude that if $x\in\{0\}\cup[1,3]$ and $0<|x-2|<\frac{1}{15}$, then 

$$
|f(x)-11|<15\cdot\frac{\varepsilon}{15} =\varepsilon.
$$

For this $f$, $\lim_{x\rightarrow 0}f(x)$ is not defined, since $0$ is not a limit point of the domain of $f$.



(iii) Finally, let $f:(0,\infty)\to\mathbb{R}$; $f(x)=x+\frac{1}{x}$. The limit of $f(x)$ as $x\rightarrow 2$ ought to be $2+\frac{1}{2}=\frac{5}{2}$.

Let $\varepsilon>0$, and consider

$$
\left|f(x)-\frac{5}{2}\right| = \left|x+\frac{1}{x}-\frac{5}{2}\right| = \left|\frac{2x^2+2-5x}{2x}\right| = \left|\frac{(x-2)(2x-1)}{2x}\right| = |x-2|\left|1-\frac{1}{2x}\right|.
$$

Now, for $x\in(0,\infty)$, we have $0<1-\frac{1}{2x}<1$, and so 

$$
\left|f(x)-\frac{5}{2}\right| = |x-2|\left|1-\frac{1}{2x}\right| < |x-2|.
$$

Therefore, we can take $\delta:=\varepsilon$ in this case to get that

$$
0<|x-2|<\delta \; \Rightarrow \; \left|f(x)-\frac{5}{2}\right|<\varepsilon.
$$

So $\lim_{x\rightarrow 2}f(x)=\frac{5}{2}$ in this case.

For the last part, note that $f(x)=x+\frac{1}{x}$ does not converge to a finite limit as $x\rightarrow 0$. In fact, $\lim_{x\rightarrow 0}f(x)=\infty$. One way to prove this is to show that $f(x)$ surpasses any possible bound as $x\rightarrow 0$. Note that

$$
f(x) = x+\frac{1}{x} > \frac{1}{x}.
$$

Therefore, given an arbitrary number $K>0$, we can take $0<x<\frac{1}{K}$ to ensure that 

$$
f(x) = x+\frac{1}{x} > \frac{1}{x} > K.
$$

This proves that $\lim_{x\rightarrow 0} f(x) = \infty$, for this choice of $f$.

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

[7.](7) (Homework 2 question?)
<br>
When $x > 0, \displaystyle\frac{|x|}{x} = \displaystyle\frac{x}{|x|} = \displaystyle\frac{x}{x} = 1 = \text{sgn}(x)$,
<br>
when $x < 0, \displaystyle\frac{|x|}{x} = \displaystyle\frac{x}{|x|} = -\displaystyle\frac{x}{x} = -1 = \text{sgn}(x)$.
<br>
The left limit is $\displaystyle\lim_{x \rightarrow 0^-} \text{sgn}(x) = -1$, since for any sequence $(x_n)$ approaching $0$ from the left, we have $\text{sgn}(x_n) = -1$ for all $n$.
<br>
Similarly, the right limit is $\displaystyle\lim_{x \rightarrow 0^+} \text{sgn}(x) = 1$,  since for any sequence $(x_n)$ approaching $0$ from the right, we have $\text{sgn}(x_n) = 1$ for all $n$.
<br>
Since the left and right limits are different, $\displaystyle\lim_{x \rightarrow 0}\text{sgn}(x)$ does not exist.

---

[8.](8) (Homework 2 question?)
   
(i) For $a\neq 1$, the left and right limits exist and are both equal to $f(a)$, using the algebra of limits. The only point at which left and right limits disagree is $a = 1$, with

$$
\lim_{x \rightarrow 1-}f(x) = 0, \; \text{ and } \; \lim_{x \rightarrow 1+}f(x) = 1.
$$

(ii) In this case, left and right limits disagree at every $n \in \mathbb{Z}$, with $\lim_{x \rightarrow a-}[x] = n-1, \lim_{x \rightarrow n+}[x] = n$. At every other real number, the left and right limits exist and are both equal to the value of the function there.

(iii) Here, left and right limits disagree at $x = 0, 1$ and $2$. We have

$$
\lim_{x \rightarrow 0^-}h(x) = 3, \hspace{1em} \lim_{x \rightarrow 1-}h(x) = -2, \hspace{1em}  \lim_{x \rightarrow 2-}h(x) = 10,
$$

$$
\lim_{x \rightarrow 0^+}h(x) = -2, \hspace{1em} \lim_{x \rightarrow 1+}h(x) = 10, \hspace{1em}  \lim_{x \rightarrow 2+}h(x) = 3.
$$

---

[9.](9) The largest subset of $\mathbb{R}$ for which the formula $f(x)=\sin\left(\frac{1}{x}\right)$ makes sense is $A = \mathbb{R} \setminus \{0\}$.
<br>
Observe that for any real number $\theta\in\mathbb{R}$,

$$
f\left(\frac{1}{\theta+2\pi n}\right) = \sin(\theta+2\pi n) = \sin(\theta).
$$

To prove $f$ has no limit at $0$, we need only choose two values of $\theta$ for which sine takes distinct values. We choose $\theta=\frac{\pi}{2}$ and $\theta=\frac{3\pi}{2}$.
<br>
By choosing the right values for $\theta$, we can use this to construct two distinct sequences $(x_n)$ and $(y_n)$ that both converge to $0$, but for which $\sin(x_n)$ and $\sin(y_n)$ have different limits.
<br>
We use $\theta=\frac{\pi}{2}$ and $\theta=\frac{3\pi}{2}$ (other choices possible).
<br>
For each $n\in\mathbb{N}$, let $x_n=\frac{1}{\frac{\pi}{2} + 2\pi n}$ and $y_n=\frac{1}{3\frac{\pi}{2} + 2\pi n}$. Then

$$
\lim_{n\rightarrow\infty} x_{n} =\lim_{n\rightarrow\infty} y_n= 0,
$$

while for all $n\in\mathbb{N}$,

$$
f(x_n) = \sin\left(\frac{\pi}{2}\right) =1 \hspace{2em} \text{ and } \hspace{2em} f(y_n)=\sin\left(\frac{3\pi}{2}\right)=-1.
$$

So $\lim_{n\rightarrow\infty} f(x_{n}) = 1$, but $\lim_{n\rightarrow\infty} f(y_n) = -1$. Since these limits are not equal, $\lim_{x\to 0} f(x)$ does not exist.
<br>
Of course, we could have chosen any values of $\theta$ we liked, and constructed a sequence $(x_n)$ with limit $0$ for which $\lim_{n\rightarrow\infty}f(x_n)$ is equal to any real number we liked in the interval $[-1,1]$. The graph of this function ({numref}`s1x`) may give some intuition as to how this is possible.

```{figure} ../analysis_problems/figs/sin(1,x).png
---
width: 700px
name: s1x
---
Graph of the function $f:\mathbb{R}\to\mathbb{R}$; $f(x)=\sin\left(\frac{1}{x}\right)$ (Problem 9).
```


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

(i) Let $X\subset\mathbb{R}$ and $f:X\to\mathbb{R}$. We say that $\lim_{x \rightarrow \infty}f(x) = l$ if whenever $(x_{n})$ is a sequence that diverges to infinity, with $x_{n}\in X$ for all $n\in\mathbb{N}$, then $\lim_{x \rightarrow \infty}f(x_{n}) = l$.

(ii) The analogue of the $(\varepsilon- \delta)$ criterion is $(\varepsilon-K)$: given any $\varepsilon > 0$, there exists $K > 0$ such that if $x > K$ then $|f(x) -l| < \varepsilon$.
<br>
For the proof, suppose the $(\varepsilon- K)$ criterion holds and $\lim_{n\rightarrow\infty} x_{n} = \infty$. Then given any $L > 0$, there exists $N\in\mathbb{N}$ such that if $n\geq N$, we have $x_{n} > L$. Now take $L$ to be $K$ from the criterion and we get that for all $n\geq N, |f(x_{n}) - l| < \varepsilon$. Hence $\lim_{x \rightarrow \infty}f(x_{n}) = l$, as required.
<br>
For the converse, we again imitate the proof of Theorem 2.1. So suppose the $(\varepsilon-K)$ criterion does not hold. This time choose successively $K = 1, 2, \ldots$ and construct $x_{n}$ in the domain $X$ of $f$ such that $x_{n} > n$, and $|f(x_{n}) - l| \geq \varepsilon$ for each $n\in\mathbb{N}$. So $f$ does not converge to $l$ as $x\to\infty$.

(iii) Given any $\varepsilon > 0$, choose $K = \frac{1}{\varepsilon}$. Then $x > K \Rightarrow \frac{1}{x} < \varepsilon$, and so $\lim_{x\to\infty} \frac{1}{x}=0$. The case where $x\to-\infty$ is similar.

---

[12.](12)
(i) Let $f:X\to\mathbb{R}$ be a function, where $X\subseteq\mathbb{R}$. We say that $\lim_{x \rightarrow \infty} f(x) = \infty$ if for any sequence $(x_{n})$ in $X$ which diverges to infinity, we also have that $(f(x_{n}))$ diverges to infinity.
<br>
The analogue of $(\varepsilon - \delta)$ is:
>Given any $M > 0$, there exists $K > 0$ such that $x > K$ implies $f(x) > M$.
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

---

[17.](17)
(i) Continuous on $\mathbb{R} \setminus \{1\}$. Jump discontinuity at $1$ with $J_{f}(1) = 1$.
(ii) Continuous on $\mathbb{R} \setminus \mathbb{Z}$. Jump discontinuity at $n$ with $J_{g}(n) = 1$ for all $n\in\mathbb{Z}_+$.
(iii) Continuous at $\mathbb{R} \setminus \{0,1,2\}$. Each of $0, 1, 2$ is a jump discontinuity and we have $J_{h}(0) =-5, J_{h}(1) = 12, J_{h}(2) = -7.$

---

[18.](18) (Homework 2 question?)
   
(i) For $x \neq 0, f(x) = x+2$. Since $\lim_{x \rightarrow 0}f(x) = 2$, the required continuous extension is $\tilde{f}$ where

$$
\tilde{f}(x) = \left\{\begin{array}{c c} \displaystyle\frac{(1 + x)^{2} - 1}{x} & ~\mbox{if}~x \neq 0\\ 
& \\
2 & ~\mbox{if}~x = 0. \end{array} \right.
$$

(ii) The largest domain is $A=\mathbb{R} \setminus \{-2, 2\}$ (the set where the denominator is non-zero). For $x \neq 2, -2$,

$$
f(x) = \frac{(x-2)(x^{2} + 2x + 4)}{(x-2)(x+2)}=\frac{x^{2} + 2x + 4}{x + 2}.
$$

This is a rational function, and hence continuous everywhere the denominator is non-zero by Theorem 3.2(iv).
<br>
We claim that $\lim_{x \rightarrow -2}f(x)$ does not exist. To see this, consider the sequence $(x_{n})$, whose $n$\textsuperscript{th} term is $-2 + \frac{1}{n}$, and check that

$$
f(x_{n}) = n\left(-4 -\frac{2}{n} + \frac{1}{n^2}\right) \rightarrow -\infty~\mbox{when}~n \rightarrow \infty.
$$

Thus $f$ has no continuous extension to the point $x =-2$.
<br>
But on the other hand,

$$
\lim_{x \rightarrow 2}f(x) = \lim_{x\rightarrow 2}  \frac{x^{2} + 2x + 4}{x + 2} = \frac{12}{4} = 3,
$$

and so $f$ has a continuous extension

$$
\tilde{f}:\mathbb{R} \setminus \{-2\}\to\mathbb{R}; \hspace{1em} \tilde{f}(x) = \frac{x^2+2x+4}{x+2}.
$$

We can see this behaviour in the graph of the function ({numref}`q18`)

```{figure} ../analysis_problems/figs/(x2+2x+4),(x+2).png
---
width: 500px
name: q18
---
Graph of the function $\tilde{f}:\mathbb{R}\setminus\{-2\}\to\mathbb{R}$; $f(x)=\frac{x^2+2x+4}{x+2}$ (Problem 18).
```

---

[19.](19) Assume $g$ is continuous and $g(a) > 0$. Suppose, for a contradiction, that  there is no  $\delta > 0$ such that $g(x) > 0$  for all $ x \in (a - \delta, a + \delta)$. Then, in particular, for all $n\in\mathbb{N}$ there exists $x_{n} \in \left(a - \frac{1}{n}, a + \frac{1}{n}\right)$ such that $g(x_{n}) \leq 0$. By the sandwich rule, we have $\lim_{n\rightarrow\infty} x_{n} = a$. So, by continuity of $g$ at $a$, we have $\lim_{n\rightarrow\infty} g(x_{n})$ exists and equals $g(a)$. But $g(x_n)\leq 0$ for all $n\in\mathbb{N}$, and so

$$
g(a)=\lim_{n\rightarrow\infty} g(x_{n}) \leq 0,
$$

which is a contradiction.

---

[20.](20)
(i) 

$$
\max\{a, b\} = \left\{\begin{array}{c c} a & ~\mbox{if}~a \geq b\\
b & ~\mbox{if}~a < b.\\ \end{array} \right.
$$

On the other hand,

$$
\frac{1}{2}( a+b) + \frac{1}{2}|a-b| = \left\{\begin{array}{c c c} \frac{1}{2}(a+b) + \frac{1}{2}(a- b) & = a & ~\mbox{if}~a \geq b\\[.5em]
\frac{1}{2}(a+b) + \frac{1}{2}(b- a) &=  b & ~\mbox{if}~a < b,\\ \end{array} \right.
$$

and the result follows.

Then for all $x \in A\cap B,$

$$
\max\{f, g\}(x) = \frac{1}{2}(f(x) + g(x)) + \frac{1}{2}|f(x) - g(x)|,
$$

and continuity follows by Theorem  3.2(i) and (iii) and [Problem 14](14).

(ii) Check that for all $a, b \in \mathbb{R}$,

$$
\min\{a, b\} = \frac{1}{2}(a + b) - \frac{1}{2}|a - b|,
$$

and then argue as in (i).

Alternatively, one could derive (ii) from (i) by using $\min\{f,g\} = - \max\{-f, -g\}$.

---

[21.](21)
(i) $f(0) = f(0 + 0) = f(0) + f(0) = 2f(0)$, hence $f(0) = 0$.

(ii) By (i), $0 = f(0) = f(x + -x) = f(x) + f(-x)$. So $f(-x)=-f(x)$.

(iii) If $a \neq 0$ then any sequence $(x_{n})$ which converges to $a$ can be written as $x_{n} = a + y_{n}$ where $(y_{n})$ converges to zero. If $f$ is continuous at $0$, then $ \lim_{n\rightarrow\infty} f(y_{n})$ exists and equals $f(0)$, which is $0$ by part (i). So

$$
\lim_{n\rightarrow\infty} f(x_{n}) = \lim_{n\rightarrow\infty} f(a + y_{n}) = f(a) + \lim_{n\rightarrow\infty} f(y_{n}) = f(a) + f(0) = f(a).
$$

(iv) Firstly, assume $n\in\mathbb{N}$ and use induction. It is true for $n = 1$. Assume it holds for some $n\in\mathbb{N}$, then

$$
f(n+1) = f(n) + f(1) = nk + k = (n+1)k.
$$

So by induction, the result holds for all $n\in\mathbb{N}$.
Combine this with part (ii), to extend to all $n\in \mathbb{Z}$.

(v) Consider $\frac{p}{q}\in\mathbb{Q}$, where $p\in \mathbb{Z}$ and $q\in \mathbb{N}$. By (iv),

$$
pk = f(p) = f\left(q\cdot \frac{p}{q}\right) = qf\left(\frac{p}{q}\right),
$$

and the result follows.

(vi) We have already proved this for rational $x$, so suppose that $x$ is irrational. Then we can find a sequence $\left(\frac{p_{n}}{q_{n}}\right)$ of rational numbers that converges to $x$ (as we did in the solution to Example 3.7). Then using (iii), (v) and algebra of limits, we have

$$
f(x) = \lim_{n\rightarrow\infty} f\left(\frac{p_n}{q_n}\right) =   \lim_{n\rightarrow\infty} k \frac{p_n}{q_n}=k \lim_{n\rightarrow\infty} \frac{p_n}{q_n} = kx.
$$

---

[22.](22) Suppose that $x \in \mathbb{Q}$. Then as in the solution to Example 3.7 we can find a sequence $(x_{n})$ of irrationals that converges to $x$ and then

$$
\lim_{n\rightarrow\infty} g(x_{n}) = 0 \neq g(x),
$$

and so $g$ is not continuous at $x$.

---

[23.](23) (Homework 2 question?)
<br>
The function $\mathbb{1}_{(a, b)}$ is left continuous at $a$ (but not right continuous), and right continuous at $b$ (but not left continuous).
To prove the left continuity at $a$, let $(x_{n})$ be any sequence in $\mathbb{R}$ which converges to $a$ with $x_{n} < a$ for all $n\in\mathbb{N}$. Then $\lim_{n\rightarrow\infty} \mathbb{1}_{(a, b)}(x_{n}) = 0 = \mathbb{1}_{(a, b)}(a).$ On the other hand to see that it is not right continuous at $a$, let $(y_{n})$ be any sequence in $\mathbb{R}$ which converges to $a$ with $a < y_{n} < b$ for all $n\in\mathbb{N}$. Then
$ \lim_{n\rightarrow\infty} \mathbb{1}_{(a, b)}(y_{n}) = 1 \neq \mathbb{1}_{(a, b)}(a). $ The other assertion is proved similarly.
<br>
[Contrast this with $\mathbb{1}_{[a, b]}$, which was discussed in the notes.]

---

[24.](24) Since $f$ is continuous on $[a, b]$, so is $g$. We have $g(a) = f(a) - \gamma < 0$ and $g(b) = f(b) - \gamma > 0$. Hence by the intermediate value theorem ([Theorem 3.4](https://rosiesb.github.io/Analysis-Notes/3Cty.html#ivt)), there exists $c \in (a, b)$ with $g(c) = 0$, i.e. $f(c) = \gamma$, as was required.

---

[25.](25)
(i) Let $f:\mathbb{R}\to\mathbb{Z}$ be continuous, and suppose $f$ is not a constant function.

Then there must be $a,b\in\mathbb{R}$ such that $a\neq b$ and $f(a)\neq f(b)$. Without loss of generality, assume $a<b$. 

Then $f$ is continuous on $[a,b]$, and since $f(a)\neq f(b)$, $f$ is also non-constant on $[a,b]$. By [Corollary 3.3](https://rosiesb.github.io/Analysis-Notes/3Cty.html#interval), $f([a,b]])=[m,M]$. This contradicts $f$ having codeomain $\mathbb{Z}$.

It follows that $f$ must be a constant function.

(ii) Argue as in (i), using the fact that between any two rational numbers, we can find an irrational number.

---

[26.](26) (Homework 3 question?)
<br>
*Something* is $x$. That is, define $g:[a,b]\to\mathbb{R}$ given by $g(x) = f(x) - x$. Then $g$ is continuous (because $f$ is and the function $h(x)=x$ is, and using algebra of limits). Since the range of $f$ is contained in $(a, b)$, we have $f(a) > a$ and $f(b) < b$, and so $g(a) = f(a) - a > 0$ and $g(b) = f(b) - b < 0$. So we can apply the intermediate value theorem to the function $g$ on $[a,b]$. This says that there exists $c \in (a, b)$ such that $g(c) = 0$, i.e. $f(c) = c$.
<br>
For the counter--example, consider $f(x) = x^2$. It is continuous on $(0, 1)$ but there is no $c \in (0, 1)$ for which $c^2 = c$.

---

[27.](27) Define $\gamma = \inf_{x \in [a, b]}f(x)$ and assume that it is not attained, so $\gamma < f(x)$ for all $x \in [a,b]$. Then consider the function $h:[a,b]\to \mathbb{R}$ given by $h(x) = \displaystyle\frac{1}{f(x) - \gamma}$. This is continuous, and hence bounded on $[a, b]$. So there exists $K \geq 0$ such that $|h(x)| \leq K$ for all $x \in [a, b]$. By Problem 16(ii), given any $\varepsilon > 0$, there exists $x \in [a, b]$ such that $f(x) < \gamma + \varepsilon$. Now take $\varepsilon = \frac{1}{K}$ to deduce that $h(x) > K$, which yields the required contradiction.

---

[28.](28) By algebra of limits, $\frac{1}{f}$ is continuous on $[0, 1]$ and so is bounded by Theorem 3.5.

---

[29.](29) (Homework 3 question?)
<br>
If $f$ is continuous on $[0, 1]$, then it is bounded by Theorem 3.5, and so there exists $L \geq 0$ such that $|f(x)| \leq L$ for all $x \in [0, 1]$. Hence the range of $f$ is a subset of  $[-L, L]$ and cannot be all of $\mathbb{R}$.

---

[30.](30) Since $(x_{n})$ is bounded, by the Bolzano--Weierstrass theorem it has a convergent subsequence $(x_{n_{k}})$. Let $c=\lim_{k \rightarrow \infty}x_{n_{k}}$ and note that $c \in [0, 1]$, since $x_{n_k}\in[0,1]$ for all $k$.
<br>
A straight-forward induction argument shows that $f(x_{n_{k}}) \leq r^{n_{k}-1}f(x_{n_{1}})$ for all $k\in\mathbb{N}$. But then, since the range of $f$ is contained in $[0,1]$, we have

$$
0 \leq f(x_{n_{k}}) \leq r^{n_{k}-1}
$$

for all $k\in\mathbb{N}$. Since $r < 1$, $\lim_{k\to\infty} r^{n_k-1} =0$. By the sandwich rule, $ \lim_{k \rightarrow \infty}f(x_{n_{k}}) = 0$ and by continuity of $f$ at $c$, $f(c) = \lim_{k \rightarrow \infty}f(x_{n_{k}})$, so $f(c)=0$.

---

[31.](31) For all $x > y$,

$$
x^{n} - y^{n} = (x - y)(x^{n-1} + x^{n-2}y + \cdots + xy^{n-1} + y^{n-1}) > 0.
$$

---

[32.](32) For all $-\frac{\pi}{2} \leq x < y \leq \frac{\pi}{2}$,

$$
\sin(y) - \sin(x) = 2\sin\left(\frac{y - x}{2}\right)\cos\left(\frac{y + x}{2}\right) > 0,
$$

so the function is strictly monotonic increasing on this interval. It is also continuous (stated in notes), and so by Theorem 3.6, it is has a continuous inverse $f^{-1}(x) = \arcsin(x)$ (or $\sin^{-1}(x)$) defined on $[-1, 1]$. Outside the interval $\left[-\frac{\pi}{2}, \frac{\pi}{2}\right]$, the function $f$ might fail to be strictly increasing. In fact it is strictly decreasing on each interval of the form $\left((4n+1)\frac{\pi}{2}, (4n + 3)\frac{\pi}{2}\right)$, and strictly increasing on each interval of the form $\left((4n-1)\frac{\pi}{2}, (4n + 1)\frac{\pi}{2}\right)$, where $n\in\mathbb{Z}_+$.

---

[33.](33) We seek a continuous extension of the mapping $x\mapsto \frac{1-x}{1-x^{\frac{m}{n}}}$ to a domain that includes $1$. Then, we can use continuity to evaluate the limit as $x\rightarrow 1$.
<br>
Observe that, if we write $y = x^{\frac{1}{n}}$, then

$$
\frac{1 - x}{1 - x^{\frac{m}{n}}} = \frac{1 - y^{n}}{1 - y^{m}} = \frac{\;\frac{1}{1-y^m}\;}{\;\frac{1}{1-y^n}\;} = \frac{1+y+y^2+\ldots+y^{m-1}}{1+y+y^2+\ldots+y^{n-1}},
$$

by the geometric sum formula. Note that the left hand side is not defined at $x=1$, but the right hand side is.
<br>
Let $f:[0,\infty)\to[0,\infty)$; $f(x)=x^{\frac{1}{n}}$, and let

$$
g:\mathbb{R}\to\mathbb{R};\hspace{1em} g(y)=\frac{1+y+y^2+\ldots+y^m}{1+y+y^2+\ldots+y^m}.
$$

Both $f$ and $g$ are continuous at every point in their domain (for $f$, this was proven in Example 3.9). Hence by the composition theorem for continuous functions (Theorem 3.3), the map

$$
g\circ f:[0,\infty)\to\mathbb{R}; \hspace{1em} g\circ f(x) = \frac{1+x^{\frac{1}{n}}+x^{\frac{2}{n}}+\ldots+x^{\frac{m-1}{n}}}{1+x^{\frac{1}{n}}+x^{\frac{2}{n}}+\ldots+x^{\frac{n-1}{n}}}
$$

is continuous. Also, by our initial calculation,

$$
g\circ f(x) = \frac{1 - x}{1 - x^{\frac{m}{n}}}
$$

whenever $x\geq 0$ and $x^{\frac{m}{n}}\neq 1$. Therefore,

$$
\lim_{x\rightarrow 1}\frac{1 - x}{1 - x^{\frac{m}{n}}} = \lim_{x\rightarrow 1}g\circ f(x) = g\circ f(1) = \frac{1+1+\ldots+1}{1+1+\ldots+1} = \frac{m}{n},
$$

by continuity of $g\circ f$.

---

[34.](34) We claim that if $a < x < b$, we have $f(a) < f(x) < f(b)$. To see this, note that if $f(a) \geq f(x)$ then either $f(a) = f(x)$, or $f(a) > f(x)$.
<br>
If $f(a)=f(x)$, then $f$ cannot be bijective, which is a contradiction. 
<br>
Suppose that $f(a)>f(x)$. Applying [Corollary 3.3](https://rosiesb.github.io/Analysis-Notes/3Cty.html#interval) to $f|_{[x,b]}$, the image of $[x,b]$ under $f$ must an interval, $[m,M]$, say. Note that $f(a)\in(m,M)$: indeed, $f(a)>f(x)>M$, and $f(a)<f(b)<m$. Therefore, by the intermediate value theorem (or [Corollary 3.1](https://rosiesb.github.io/Analysis-Notes/3Cty.html#ivt2) more specifically), there exists $c \in (x, b)$ such that $f(c) = f(a)$, and this again violates the injectivity of the mapping $f$. A similar argument can be used to show that we cannot have $f(b) \leq f(x)$.
<br>
Finally, applying our initial result to $f|_{[a, y]}$, we see that if $a<x<y<b$, then $f(a) < f(x) < f(y)$. Hence $f$ is strictly monotonic increasing.

---

[35.*](35) First observe that $f+g$ is monotonic increasing since both $f$ and $g$ are. Choose $a \in \mathbb{R}$. Given $\varepsilon > 0$, there exists $\delta > 0$ so that if $x > a + \delta$ then

$$
|f(x) + g(x) - f(a) - g(a)|  =  f(x) + g(x) - f(a) - g(a) < \varepsilon,
$$

and so

$$
|f(x) - f(a)| = f(x) - f(a) < \varepsilon +g(a) - g(x) < \varepsilon,
$$

as $g$ is increasing. This proves that $g$ is right--continuous at $a$. A similar argument (interchanging the roles of $a$ and $x$) proves that it is left--continuous, and hence continuous at $a$. Then $g = (f + g) - f$ is the difference of two continuous functions, and hence is itself continuous.

---

[36.*](36) 
(i) If $0<a<1$, then $0<a<\sqrt{a}<1$. So $(x_n)$ is monotonic increasing and bounded above by $1$, and hence converges to some limit $0\leq l\leq 1$. By continuity of the square root function, $\sqrt{l}=\lim_{n\rightarrow\infty}\sqrt{x_n}$. But $\sqrt{x_n}=x_{n+1}\rightarrow l$ as $n\rightarrow\infty$. By uniqueness of limits, $\sqrt{l}=l$, and so $l=1$.
<br>
If instead $a>1$, then $a>\sqrt{a}>1$, and so $(x_n)$ is monotonic decreasing and bounded below by $1$. So the sequences converges to a limit, and by an identical argument to above, this limit has to be $1$.

(ii) For all $a>0, n\in\mathbb{N}, f(a) = f\left(a^{\frac{1}{2}}\right) = \cdots = f\left(a^{\frac{1}{2^{n-1}}}\right)$. That is, $f(a)=f(x_n)$ for all $n\in\mathbb{N}$. By continuity,

$$
f(a) = \lim_{n\rightarrow\infty} f(x_n) = f\left(\lim_{n\rightarrow\infty} x_n\right) = f(1).
$$

If $a<0$, then $a^2>0$ and so $f(a)=f\left(a^2\right)=f(1)$. Finally, by continuity,

$$
f(0)=\lim_{x\rightarrow 0}f(x) = \lim_{x\rightarrow 0}f(1) = f(1),
$$

and we have shown that $f(x)=f(1)$ for all $x\in\mathbb{R}$.

## Differentiation

[37.](37) This is Definition 2.2 in the notes:
<br>
The function $f$ has limit $l$ at the point $a$ if for every $\varepsilon>0$ there exists $\delta>0$ such that for all $x\in X$, 

$$
0<|x-a|<\delta \; \text{ implies } \; |f(x)-l|<\varepsilon.
$$

We write $\lim_{x\to a}f(x)=l$.

---

[38.](38) (Homework 4 question?)

(i) This is Definition 4.1 in the notes: we say that $f$ is *differentiable* at $a \in A$ if $ \lim_{x \rightarrow a}\frac{f(x) - f(a)}{x - a}$ exists. Or, equivalently, $ \lim_{h \rightarrow 0}\frac{f(a +h) - f(a)}{h}$ exists.
<br>
That is, we fix $a\in A$ and we consider the function $g$ given by $g(h)=\frac{f(a +h) - f(a)}{h}$. Then $f$ is differentiable at $a$ if the limit of $g$ as $h$ goes to zero exists.

(ii) Using the sequential criterion (Theorem 2.1 in the notes):
<br>
$f$ is differentiable at $a$ if there exists some number $f'(a) \in \mathbb{R}$ for which, given any sequence $(h_{n})$ that converges to $0$, with $h_n\neq 0$ for all $n$, we have

$$
\frac{f(a + h_{n}) - f(a)}{h_{n}} \rightarrow f'(a) \hspace{1em} \text{ as } \hspace{1em} n\rightarrow\infty.
$$

(iii) This is asking for the equivalent description of limit of a function given by the $(\varepsilon - \delta)$ criterion (Theorem 2.1). Again it needs to be applied to $g$ as above not $f$ itself:
<br>
We say $f$ is differentiable at $a$ if there exists a number $f'(a)$ for which, given $\varepsilon>0$, there exists $\delta > 0$ such that if $0<|h| < \delta$, then

$$
\left|\displaystyle\frac{f(a+h) - f(a)}{h} - f'(a)\right| < \varepsilon.
$$

---

[39.](39) Let $x\in\mathbb{R}\setminus\{0\}$. Then
\begin{align*}
\frac{f(x + h) -f(x)}{h} &= \frac{1}{h}\left(\frac{1}{x+ h} -\frac{1}{x}\right)\\
&= -\frac{1}{x(x+h)} \rightarrow -\frac{1}{x^{2}},~\mbox{as}~h \rightarrow 0. 
\end{align*}
Thus $f$ is differentiable at all $x\in\mathbb{R}\setminus\{0\}$ and $f'(x)=-\frac{1}{x^2}$ for all $x\in\mathbb{R}\setminus\{0\}$.
<br>
The extended function (where we define its value at $x=0$ to be zero) is not continuous at $x=0$, since $\lim_{x \rightarrow 0^+}\frac{1}{x} =\infty$. Therefore it is not differentiable at $x=0$, by Theorem 4.1.

---

[40.](40) As in the hint, let $g(h) = e^{kh} - 1 - kh $. Then

\begin{align*}
\frac{f(x + h) -f(x)}{h} &= \frac{1}{h}(e^{k(x +h)} - e^{kx})\\
&= e^{kx}\frac{1}{h}(e^{kh} - 1) = e^{kx}\left(k + \frac{g(h)}{h}\right) \rightarrow ke^{kx},~\mbox{as}~h \rightarrow 0,
\end{align*}

using the given fact that  $\lim_{h \rightarrow 0}\frac{g(h)}{h} = 0$. Thus $f$ is differentiable at each $x\in\mathbb{R}$ and $f'(x)=ke^{kx}$.

---

[41.](41) 
(i) Using the product and chain rules for differentiation, and that $\sin$ is differentiable with derivative $\cos$,
if $x \neq 0$, $f$ is differentiable at $x$ with $f'(x) = \sin\left(\frac{1}{x}\right) - \frac{1}{x}\cos\left(\frac{1}{x}\right)$.
(ii) But
$\frac{f(x) - f(0)}{x} = \sin\left(\frac{1}{x}\right)$ has no limit as $x \rightarrow 0$ (see [Problem 9](9)), so $f$ is not differentiable at $0$.

---

[42.](42) Again using the product and chain rules and standard derivatives,
for $x \neq 0$, $f$ is differentiable at $x$ with $f'(x) = 2x\sin\left(\frac{1}{x}\right) - \cos\left(\frac{1}{x}\right)$. At $x = 0,$

$$
\lim_{x \rightarrow 0}\frac{f(x) - f(0)}{x} = \lim_{x \rightarrow 0}x\sin\left(\frac{1}{x}\right) = 0,
$$

by [Problem 10](10). So $f$ is differentiable at $0$ with $f'(0) = 0$. For the second derivative, with $x \neq 0$, we have

$$
f^{\prime \prime}(x) = 2\sin\left(\frac{1}{x}\right) - \frac{2}{x}\cos\left(\frac{1}{x}\right) - \frac{1}{x^{2}}\sin\left(\frac{1}{x}\right).
$$

But $f^{\prime \prime}$ doesn't exist at $x = 0$, as in [Problem 41](41).

---

[43.](43) We give sketches of simple examples of functions as described. There should be some kind of "corner" or "cusp" at the relevant points, so that there is clearly no well-defined gradient there. But the functions are required to be continuous, so there should be no jump or other discontinuity.

(i) {numref}`q43i`

```{figure} ../analysis_problems/figs/nondiff1,2.png
---
width: 500px
name: q43i
---
Graph of a function $f:[0,1]\to\mathbb{R}$ that is not differentiable at $\frac{1}{2}$, but is everywhere else (Problem 43(i)).
```

(ii) {numref}`q43ii`

```{figure} ../analysis_problems/figs/nondiff1,3_2,3.png
---
width: 500px
name: q43ii
---
Graph of a function $f:[0,1]\to\mathbb{R}$ that is differentiable at all points in its domain apart from $\frac{1}{3}$ and $\frac{2}{3}$ (Problem 43(ii)).
```

---

[44.](44) It helps to sketch the graph. On the interval $[0,1]$, we have $[x]=0$ and so the graph resembles $y=x$. This pattern then repeats, and we have the following graph for $f(x)=x-[x]$ --- see {numref}`q44`

```{figure} ../analysis_problems/figs/x-[x].png
---
width: 500px
name: q44
---
Graph of the function $f:\mathbb{R}\to\mathbb{R}$; $f(x)=x-[x]$ (Problem 44).
``` 

The function $f$ is differentiable for all $x \in \mathbb{R} \setminus \mathbb{Z}$. For such points, taking $h>0$ sufficiently small, we have
$[x+h]=[x]$ and so

$$
\frac{f(x+h)-f(x)}{h} = \frac{(x + h)- [x + h] - x + [x]}{h} = \frac{h}{h}=1.
$$

Thus $f'(x) = 1$  for all $x \in \mathbb{R} \setminus \mathbb{Z}$. If $x \in \mathbb{Z}$, then $f$ is not continuous at $x$  (it has a jump discontinuity of $-1$ there) and so cannot be differentiable there (by Theorem  4.1).


---

[45.](45) First observe that if $f$ is differentiable at $a$, then

$$
f'(a) = \lim_{h \rightarrow 0}\frac{f(a + h) - f(a)}{h} = \lim_{h \rightarrow 0}\frac{f(a - h) - f(a)}{-h} = \lim_{h \rightarrow 0}\frac{f(a) - f(a-h)}{h}.
$$

So
\begin{align*}
\frac{f(a+ h) - f(a - h)}{2h} &=  \frac{1}{2}\left(\frac{f(a + h) - f(a)}{h} +  \frac{f(a) - f(a-h)}{h}\right) \\
&\hspace{7em}\rightarrow  \frac{1}{2}2f'(a) = f'(a),~\mbox{as}~h \rightarrow 0. 
\end{align*}

On the other hand, by Example 5.2.5, $f:\mathbb{R}\to\mathbb{R}$ given by
$f(x)=|x|$ is not differentiable at $x=0$. But

$$
\lim_{h \rightarrow 0^+} \displaystyle\frac{|h|-|{}-h|}{2h} =0.
$$

---

[46.](46)
(i) True: $f$ is continuous at zero as $f(0) = 0= \lim_{x \rightarrow 0^-}f(x) = \lim_{x \rightarrow 0^+}f(x)$.
   
(ii) True: $f'(0)$ exists and is zero. To see this compute

$$
f'_{+}(0) = \lim_{h \rightarrow 0^+}\frac{h^{2}}{h} = \lim_{h \rightarrow 0^+} h= 0.
$$

and

$$
f'_{-}(0)= \lim_{h \rightarrow 0^-}\frac{-h^{2}}{h} = \lim_{h \rightarrow 0^-} -h =0.
$$

(iii) True: $f'$ is continuous at zero since $f':\mathbb{R}\to\mathbb{R}$ is given by

$$
f'(x) = \left\{\begin{array}{c c} -2x & ~\mbox{if}~x < 0\\ 0& ~\mbox{if}~x =0 \\ 2x & ~\mbox{if}~x > 0 \end{array} \right.,
$$

so $f'(0) = \lim_{x \rightarrow 0^-} f'(x) = \lim_{x \rightarrow 0^+}f'(x) = 0$.

(iv) False:  $f^{\prime \prime}_{+}(0) = \lim_{h \rightarrow 0^+}\frac{2h - 0}{h} = 2, f^{\prime \prime}_{-}(0) = \lim_{h \rightarrow 0^-}\frac{-2h - 0}{h} = -2$, and so $f^{\prime \prime}(0)$ does not exist.

---

[47.](47)
(i) Yes: $f$ is differentiable on $[a, b]$ and hence continuous on $[a, b]$ by Theorem  4.1, so it attains its sup and inf on $[a, b]$ by the extreme value theorem, Theorem 3.5, and these are the maximum and minimum (respectively).

(ii) No: the maximum or minimum could be $f(a)=f(b)$.
If $f(a)$ is not the maximum value, then this must occur in $(a, b)$. Similarly for the minimum. If $f(a) = f(b)$ is both the maximum and minimum value, then $f$ is constant, and the value occurs in $(a, b)$.

---

[48.](48) Following the hint, define $g:\mathbb{R}\rightarrow \mathbb{R}$ by

$$
g(x) = a_{0}x + \frac{a_{1}}{2}x^{2} + \frac{a_{2}}{3}x^{3}  + \cdots + \frac{a_{n}}{n+1}x^{n}.
$$

Then $g$ is a polynomial, so it is differentiable on $[0, 1]$ and using standard derivatives, $g'(x)=f(x)$. Also $g(0) = g(1) = 0$. So by Rolle's theorem, there exists $c \in (0, 1)$ such that $g'(c) = 0$, i.e.$f(c) = 0$.

---

[49.](49)
(i) Let $x, y$ be such that $a \leq x < y \leq b$. We want to show that $f(x)=f(y)$.

Apply the mean value theorem to the restriction of $f$ to the interval $[x, y]$, to find there exists $d \in (x, y)$ for which

$$
f(y) - f(x) = f'(d)(y-x).
$$

By assumption, $f'(c)=0$ for all $c\in(a,b)$, so $f'(d)=0$.

Thus $f(x)=f(y)$. Since this holds for all $x,y\in [a,b]$, $f$ is constant on $[a,b]$.

(ii) Define $f:\mathbb{R}\to\mathbb{R}$ by $f = h-g$. Then the function $f$ is continuous on $[a,b]$ and differentiable on $(a,b)$, because $g$ and $h$ are, and $f'(x)=h'(x)-g'(x)=0$ for all $x\in (a,b)$. Thus $f$ satisfies all the conditions of (i). By part (i), $f$ is constant on $[a,b]$. That is, there exists some $k\in \mathbb{R}$, such that $f(x)=k$ for all $x\in [a,b]$. Thus $h(x)=g(x)+k$ for all $x\in [a,b]$.

---

[50.](50) By the mean value theorem, $f(b) = f(a) + f'(c)(b - a)$ for some $c\in (a,b)$. So, since $m \leq f'(c) \leq M$, for all $c \in (a, b)$,

$$
f(a) + m(b - a) \leq f(b) \leq f(a) + M(b - a).
$$


---

[51.](51) The polynomial $p$ is of odd degree so it has at least one real root by [Corollary 3.2](https://rosiesb.github.io/Analysis-Notes/3Cty.html#pol). Also $p$ is differentiable with $p'(x) = 3x^{2} + r > 0$, for all $x \in \mathbb{R}$, so $p$ is strictly monotonic increasing on any closed interval $[a, b]$, and hence on the whole of $\mathbb{R}$, by Corollary 4.1. Then by the inverse function theorem (Theorem 3.6), $p$ is invertible and hence injective, and so there is exactly one zero.

---

[52.](52) Let $r>1$ and fix $y\in (0,1)$. Apply the mean value theorem to the function $f:[y,1]\to\mathbb{R}$ given by $f(x) = x^r$. Then there exists $c \in (y, 1)$ such that

$$
\frac{f(1)-f(y)}{1-y}=f'(c)=rc^{r-1}.
$$

Now, $0<c<1$, and $r>1$, so $c^{r-1}<1$. Thus

$$
1 - y^r = rc^{r-1}( 1- y) < r(1 - y).
$$

---

[53.](53) Consider the first case. Here we have

$$
f''(a) = \lim_{h \rightarrow 0}\frac{f'(a + h) - f'(a)}{h} =  \lim_{h \rightarrow 0}\frac{f'(a + h)}{h} < 0.
$$

In particular, $f^{\prime \prime}_{+}(a) = \lim_{h \rightarrow 0^+}\frac{f'(a + h)}{h} < 0$, and so $f'(a + h) < 0$ for sufficiently small positive $h$, (say $0 < h < \delta$), in which case, by Corollary 4.1, $f$ is strictly decreasing on $[a,  a + \delta]$. We also have $f^{\prime \prime}_{-}(a) = \lim_{h \rightarrow 0^-}\frac{f'(a + h)}{h} < 0$, and so $f'(a + h) > 0$ for sufficiently small negative $h$, (say $-\delta_{1} < h < 0$), in which case, by Corollary 4.1, $f$ is strictly increasing on $[a- \delta_{1}, a]$. Then it follows that $f$ has a local minimum at $a$. The other case is similar.



## Sequences and series of functions

[54.](54) For $x\in [0,\pi ]$ we have $0\leq \sin x<1$ except when $x=\frac{\pi}{2}$, where $\sin x=1$. Thus $f_n(x)$ converges pointwise to the function $f\colon [0, \pi ]\rightarrow \mathbb{R}$ defined by

$$
f(x) = \left\{ \begin{array}{ll}
0 & x\neq \frac{\pi}{2}, \\
1 & x=\frac{\pi}{2}. \\
\end{array} \right.
$$

Each function $f_n$ is continuous. The function $f$ is not continuous. So the sequence $(f_n)$ does not converge uniformly (otherwise we would have a contradiction to Theorem 5.1 --- the uniform limit theorem).


---

[55.](55) 
(i) Observe that $(f_n)$ converges pointwise to the function

$$
f(x) = \left\{ \begin{array}{ll}
0 & x=0, \\
1 & x>0. \\
\end{array} \right.
$$

Each function $(f_n)$ is continuous, but the function $f$ is not continuous at $0$, so the convergence cannot be uniform.

(ii) Let $x\in \mathbb{R}$. Then for any $n\geq x$, we have $f_n (x) =0$, so the sequence $(f_n)$ converges pointwise to the zero function.
<br>
On the other hand

$$
M_n = \sup \{ |f_n(t) -0| : t\in \mathbb{R} \} = \infty,
$$

so certainly $(M_n)$ does not converge to zero, and the sequence $(f_n)$ therefore does not converge uniformly to the zero function.

(iii) For $x>1$, $\frac{1}{x^n} \rightarrow 0$ as $n\rightarrow \infty$. Hence for each $x\in (1,\infty )$, $\frac{e^x}{x^n}\rightarrow 0$ as $n\rightarrow \infty$, and the sequence $(f_n)$ converges pointwise to the zero function.
<br>
But $\frac{e^x}{x^n}\rightarrow \infty$ as $x\rightarrow \infty$, so

$$
M_n = \sup \{ |f_n(t) -0| : t\in (1,\infty ) \} = \infty.
$$

So certainly $(M_n)$ does not converge to zero, and the sequence $(f_n)$ therefore does not converge uniformly to the zero function.

(iv) We know that $e^{-k}\rightarrow 0$ as $k\rightarrow \infty$, so $f_n(x)\rightarrow 0$ as $n\rightarrow \infty$ if $x\neq 0$. If $x=0$, then $f_n(x)=1$ for all $n$. So $(f_n)$ converges pointwise to the function

$$
f(x) = \left\{ \begin{array}{ll}
1 & x=0, \\
0 & x\neq 0. \\
\end{array} \right.
$$

Each function $(f_n)$ is continuous, but the function $f$ is not continuous at $0$, so the convergence cannot be uniform.

(v) The sequence $(f_n)$ clearly does not converge pointwise.

---

[56.](56) We consider $g_n:D\to\mathbb{R}$, and consider the cases $D=[0,1]$ and $D=[0,\infty)$, with $g_n(x)$ given by different expressions in each part below.
<br>
By Proposion 5.2, $(g_n)$ will converge uniformly to a function $g$ if and only if

$$
M_n := \sup \{ |g_n(t) -g(t)| : t\in D \} \rightarrow 0 \text{ as } n\rightarrow \infty.
$$

(i) If $\displaystyle g_n(x)=\frac{x}{n}$, then for each $x$, $g_n(x)\rightarrow 0$ as $n\rightarrow \infty$, so the sequence $(g_n)$ converges pointwise to the zero function.
<br>
On the interval $[0,1]$,

$$
M_n = \sup \{ |g_n(t) -0 | : t\in [0,1] \}  = \frac{1}{n}
$$

Note that $M_n\rightarrow 0$ as $n\rightarrow \infty$, so on the interval $[0,1]$, the sequence $(g_n)$ converges uniformly to the zero function.
<br>
On the other hand,  on $[0,\infty )$,

$$
M_n = \sup \{ |g_n(t) -0 | : t\in [0,\infty ) \}  = \infty,
$$

so the sequence $(g_n)$ does not converge uniformly on $[0,\infty )$.

(ii) Now consider $\displaystyle g_n(x) := \frac{x^n}{1+x^n}$. Observe that

$$
g_n (x) = \frac{1}{1+\frac{1}{x^n}} \rightarrow \left\{ \begin{array}{ll}
0 & x<1, \\
\frac{1}{2} & x=1, \\
1 & x>1. \\
\end{array} \right.
$$

Thus the pointwise limit function is not continuous on $[0,1]$ or on $[0,\infty )$, so convergence is not uniform on either interval.

(iii) Let $\displaystyle g_n(x) =  \frac{x^n}{n+x^n}$.

If $0\leq x\leq 1$, then $\frac{n}{x^n} \rightarrow \infty$ as $n\rightarrow \infty$, so $g_n(x)\rightarrow 0$ as $n\rightarrow \infty$. If $x>1$, then $\frac{n}{x^n} \rightarrow 0$ as $n\rightarrow \infty$, so $g_n(x)\rightarrow 1$ as $n\rightarrow \infty$. So $(g_n)$ converges pointwise to

$$
g (x) =  \left\{ \begin{array}{ll}
0 & x\leq 1, \\
1 & x>1. \\
\end{array} \right.
$$

On the interval $[0,1]$,

$$
M_n = \sup \{ |g_n(t) -0 | : t\in [0,1] \}  = \frac{1}{1+n} \rightarrow 0
$$

as $n\rightarrow \infty$. So the sequence $(g_n)$ converges uniformly to the zero function on $[0,1]$.
<br>
On the other hand the above pointwise limit $g$ is not continuous on $[0,\infty )$, whereas each function $g_n$ is continuous on $[0,\infty )$, so convergence is not uniform on $[0,\infty )$.

---

[57.](57) 
(i) Observe that, for all $x\in[0,1]$, $h_n(x)\rightarrow 1$ as $n\rightarrow \infty$.
So $(h_n)$ converges pointwise to the constant function $h:[0,1]\to\mathbb{R}$, $h(x)=1$ for all $x$.

Let

$$
M_n = \sup \{ |h_n(x)-1| : x\in [0,1] \} = 1 - \left(1-\frac{1}{n}\right)^2 =\frac{1}{n^2}-\frac{2}{n}.
$$

So $M_n\rightarrow 0$ as $n\rightarrow \infty$. So $(h_n)$ converges uniformly to the constant function $h$.

(ii) We know that $x^n \rightarrow 0$ as $n\rightarrow \infty$ if $0\leq x<1$, and $x^n\rightarrow 1$ as $n\rightarrow \infty$ if $x=1$. Hence $(h_n)$ converges pointwise to the function $h$, where

$$
h (x) =\left\{ \begin{array}{ll}
x & 0\leq x<1, \\
0 & x=1. \\
\end{array} \right.
$$

Each function $h_n$ is continuous, and this limit is not continuous, so convergence is not uniform.

(iii) The sequence $(h_n(x))$ has pointwise limit $\frac{1}{1-x}$ if $0\leq x<1$ (geometric series), but it does not converge if $x=1$. Because it does not converge when $x=1$, the sequence of functions $(h_n)$ does not converge pointwise  on $[0,1]$ (and so it certainly does not converge uniformly on $[0,1]$).

---

[58.](58)
(i) For each $t$, we have

$$
f_n(t) = \frac{n+\cos x}{2n+\sin^2 x} = \frac{1+\frac{\cos x}{n}}{2+\frac{\sin^2 x}{n}} \rightarrow \frac{1}{2}
$$

as $n\rightarrow \infty$. So the sequence $(f_n)$ converges pointwise to the constant function $f:\mathbb{R}\to\mathbb{R}$, with $f(x)=\frac{1}{2}$ for all $x\in\mathbb{R}$.

(ii) Note that, for all $x\in\mathbb{R}$,
\begin{align*}
\left|f_n(x) - \frac{1}{2}\right| =  \left| \frac{2n+2\cos x -2n -\sin^2 x}{2(2n+\sin^2 x)} \right| 
&= \left| \frac{2\cos x -\sin^2 x}{2(2n+\sin^2 x)} \right| \\
&\leq \frac{2+1}{2(2n)}=\frac{3}{4n} \rightarrow 0 
\end{align*}
as $n\rightarrow \infty$.
<br>
It follows that $(f_n)$ converges to $f$ uniformly.

(iii) Using the quotient rule,
\begin{align*}
f_n'(x) &= \frac{-\sin(x)(2n+\sin^2(x))-(n+\cos(x))\cdot 2\sin(x)\cos(x)}{\left(2n+\sin^2(x)\right)^2} \\
&= \frac{-\sin(x)\left(2n+\sin^2(x)+2n\cos(x)+2\cos^2(x)\right)}{\left(2n+\sin^2(x)\right)^2} \\
&= \frac{-\sin(x)\left(2n+1+2n\cos(x)+\cos^2(x)\right)}{\left(2n+\sin^2(x)\right)^2}.
\end{align*}
Since $f$ is a constant function, $f'(x)=0$ for all $x\in\mathbb{R}$. We show that $f_n'(x)\rightarrow 0$ as $n\rightarrow\infty$, for each $x\in\mathbb{R}$.
<br>
We have:
\begin{align*}
|f_n'(x)| &= \frac{|\sin(x)|\left|2n+1+2n\cos(x)+\cos^2(x)\right|}{\left(2n+\sin^2(x)\right)^2} \\
&\leq \frac{2n+1+2n|\cos(x)|+|\cos(x)|^2}{\left(2n\right)^2},
\end{align*}
(using the triangle inequality and the fact that $\sin^2(x)\geq 0$), so
\begin{align*}
|f_n'(x)| &\leq \frac{4n+2}{4n^2} = \frac{2n+1}{2n^2} \rightarrow 0 \text{ as } n\rightarrow \infty.
\end{align*}
Therefore $f_n'(x)\rightarrow 0$ as $n\rightarrow \infty$, for all $x\in\mathbb{R}$.
<br>
The conditions of Theorem 5.2 will be satisfied if we can prove that $f_n'\rightarrow 0$ uniformly.
<br>
We have already shown that $|f_n'(x)|\leq \frac{2n+1}{2n^2}$ for all $x\in\mathbb{R}$ and $n\in\mathbb{N}$, so most of the work is already done here. We have

$$
M_n := \sup\{|f_n(x)|:x\in\mathbb{R}\} \leq \frac{2n+1}{2n^2}\rightarrow 0 \text{ as } n\rightarrow\infty,
$$

so by Proposition 5.2, $f_n'\rightarrow 0$ uniformly. So $(f_n)$ satisfies the conditions of Theorem 5.2.

---

[59.](59) 
(i) As indicated in the question, we need to check continuity at $x=0$ and $x=1$.
<br>
Let $0<x<1$, so

$$
f_n(x) = \frac{x^{\frac{1}{n}}-1}{\ln x}.
$$

We have $x^{\frac{1}{n}} -1 \rightarrow -1 \neq 0$ as $x\rightarrow 0$, and $\ln x\rightarrow -\infty$ as $x\rightarrow 0$. So clearly

$$
\frac{x^{\frac{1}{n}}-1}{\ln x} \rightarrow 0 =f_n(0)
$$

as $x\rightarrow 0$, and $f_n$ is continuous at $0$.
<br>
On the other hand,

$$
x^{\frac{1}{n}} -1 \rightarrow 1-1=0 \qquad \text{and}\qquad \ln x\rightarrow 0
$$

as $x\rightarrow 1$, so by L'H\^opital's rule,

$$
\lim_{x\rightarrow 1} \frac{x^{\frac{1}{n}} -1}{\ln x} = \lim_{x\rightarrow 1} \frac{\left(\frac{1}{n}\right)x^{\frac{1}{n}-1}}{\frac{1}{x}} = \frac{1}{n} = f_n(1),
$$

so  $f_n$ is continuous at $1$.

(ii) Since we can assume the function $f_n$ is increasing, we have

$$
|f_n(x) |\leq \frac{1}{n}
$$

for all $x\in [0,1]$. But $\frac{1}{n}\rightarrow 0$ as $n\rightarrow \infty$, so it follows that $(f_n)$ converges uniformly to the zero function.


---

[60.](60) Let $s_n(x)=\sum_{i=1}^n f_i(x)$. Then $(s_n)$ converges uniformly to $f$, and by Proposition 5.2, this is equivalent to $\sup\{|s_n(x)-f(x)|\}\to 0$ as $n\to\infty$. So
\begin{align*}
\sup\{|f_n(x)|\}&=\sup\{|s_n(x)-s_{n-1}(x)|\}\\
&\leq \sup \{|s_n(x)-f(x)|+|f(x)-s_{n-1}(x)|\}\\
&\leq \sup \{|s_n(x)-f(x)|\}+\sup\{|f(x)-s_{n-1}(x)|\}\\
&\qquad\to 0, \quad\text{as $n\to\infty$.}
\end{align*}
So by Proposition 5.2, $(f_n)$ converges uniformly to $0$.

---

[61.](61) For each $n\in\mathbb{N}$, define $f_n,g_n:\mathbb{R}\to\mathbb{R}$ by $f_n(x)=\frac{(-1)^nx^{2n+1}}{(2n+1)!}$ and $g_n(x)=\frac{(-1)^nx^{2n}}{(2n)!}$.

(i) To establish absolute pointwise summability of $(f_n)$, observe that for each **fixed** $x\in\mathbb{R}$,

$$
\frac{|f_{n+1}(x)|}{|f_n(x)|} = \frac{x^{2n+3}(2n+1)!}{(2n+3)!x^{2n+1}} = \frac{x^2}{(2n+3)(2n+1)} \rightarrow 0,
$$

as $n\rightarrow\infty$. Therefore by the ratio test, $s(x) = \sum_{n=0}^\infty f_n(x)$ is absolutely convergent for each $x\in\mathbb{R}$.

A similar argument applied instead to the seqence $(g_n)$ will show absolute pointwise convergence of the series associate with $c$ (make sure you can write out the details yourself, though!).

(ii) Let $R>0$, and restrict each $f_n$ defined above to the interval $[-R,R]$. Let $M_n=\frac{R^{2n+1}}{(2n+1)!}$ for each $n\in\mathbb{N}$. Then

$$
|f_n(x)| = \frac{x^{2n+1}}{(2n+1)!} \leq M_n
$$

for all $x\in[-R,R]$ and $n\in\mathbb{N}$. By the same ratio test argument as above, $(M_n)$ is a summable sequence of real numbers, and so by the Weierstrass $M$-test the series $s:=\sum_{n=0}^\infty f_n$ converges uniformly on $[-R,R]$.
<br>
Applying the same argument to $(g_n)$ establishes the result for $c$.

(iii) Observe that $f_n$ and $g_n$ are differentiable everywhere for all $n\in\mathbb{N}$, and for each $x\in\mathbb{R}$,

$$
f_n'(x) = \frac{(-1)^n(2n+1)x^{2n}}{(2n+1)!}=\frac{(-1)^nx^{2n}}{(2n)!}=g_n(x) \hspace{2em} \text{ for } n=0,1,2,\ldots
$$

and

$$
g_n'(x) = \frac{(-1)^n(2n)x^{2n-1}}{(2n)!} = \frac{(-1)^nx^{2n-1}}{(2n-1)!} = -f_{n-1}(x) \hspace{2em} \text{ for } n=1,2,\ldots.
$$

Also, $g_0(x)=1$, so $g_0'(x)=0$ for all $x$.
<br>
We can now apply Theorem 5.4 to the sequences $(f_n)$ and $(g_n)$ to obtained the desired results for $s$ and $c$. The uniform summability of $(f_n')$ and $(g_n')$ follows from that of $(g_n)$ and $(f_n)$, respectively. Clearly each term $f_n'$ and $g_n'$ are also continuous, and so by Theorem 5.4, $s=\sum_{n=0}^\infty f_n$ and $c=\sum_{n=0}^\infty g_n$ are both differentiable on $(-R,R)$, and can be differentiated term by term. But $R$ was arbitrary, and so in fact we have shown that $s$ and $c$ are differentiable everywhere, with derivatives given by

$$
s'(x) = \sum_{n=0}^\infty g_n(x) = c(x)
$$

and

$$
c'(x) = \sum_{n=1}^\infty (-f_{n-1}(x)) = -s(x),
$$

for all $x\in\mathbb{R}$.

(iv) The real crux of this part of this question is that the series' for $\exp$, $s(x)$ and $c(x)$ are absolutely convergent for each $x\in R$. This allows us to rearrange their terms without disturbing any convergence properties --- this was the content of Theorem 4.18 in MAS107.

Using rearrangement, we have for each $x\in\mathbb{R}$,
\begin{align*}
\exp(ix) = \sum_{n=0}^\infty\frac{(ix)^n}{n!} &= \sum_{n \text{ even}}^\infty\frac{(ix)^n}{n!}  + \sum_{n \text{ odd}}^\infty\frac{(ix)^n}{n!} \\
&= \sum_{k=0}^\infty\frac{(ix)^{2k}}{(2k)!} + \sum_{k=0}^\infty\frac{(ix)^{2k+1}}{(2k+1)!} \\
&= \sum_{k=0}^\infty\frac{(-1)^kx^{2k}}{(2k)!} + \sum_{k=0}^\infty\frac{i(-1)^kx^{2k+1}}{(2k+1)!} \\
&= c(x) + is(x).
\end{align*}

---

[62.](62)
(i) Let $M_n =\frac{1}{n}^2$. Note that

$$
\frac{1}{n^2+x^2} \leq \frac{1}{n^2}
$$

for all $x\in \mathbb{R}$, and the series $\sum_{n=1}^\infty M_n$ converges. So by the Weierstrass $M$-test, the series $ \sum_{n=1}^\infty \frac{1}{n^2 +x^2}$ converges uniformly on $\mathbb{R}$.

It also converges uniformly on $[0,1]$ by the same argument.

(ii) Observe that, for each $n\in \mathbb{N}$,

$$
\sup \left\{ \left| \frac{(-1)^nx^{2n+1}}{(2n+1)!} \right| : x\in \mathbb{R} \right\} = \infty
$$

so the series cannot converge uniformly on $\mathbb{R}$. (The series converging uniformly means the sequence
of partial sums $s_n$ converging uniformly. But then you would have $s_{n+1}-s_n$ converging uniformly
to the zero function, which is not the case.)

But let

$$
M_n = \sup \left\{ \left| \frac{(-1)^nx^{2n+1}}{(2n+1)!} \right|  : x\in [0,1] \right\} = \frac{1}{(2n+1)!}.
$$

Then the terms of the series are bounded above by $M_n$, and $\sum_{n=0}^\infty M_n$ converges. So the series converges uniformly on $[0,1]$.

(iii) $\sin (nx)$ does not converge to $0$ as $n\rightarrow \infty$ at certain values of $x$, (for example $x=\frac{\pi}{4}\in [0,1]$),  so the series does not converge, let alone uniformly, either on $[0,1]$ or $\mathbb{R}$.

(iv)* The series $\sum_{n=1}^\infty  \frac{\sin (nx)}{n}$ does not converge uniformly on $[0,1]$. So it does not converge uniformly on $\mathbb{R}$ either. To see this, suppose it does converge uniformly. Then the limit $f(x)$ would be a continuous function on $[0,1]$. Since $f$ is continuous at $0$, we have 

$$
0=f(0)=\lim_{N\to\infty} f(\frac{\pi}{N})=\lim_{N\to\infty} \sum_{n=1}^N \frac{\sin\left(\frac{n\pi}{N}\right)}{n}.
$$

On the other hand,
\begin{align*}
\sum_{n=1}^N \frac{\sin\left(\frac{n\pi}{N}\right)}{n}&\geq \frac{1}{N}\left( \sum_{n=1}^N \sin\left(\frac{n\pi}{N}\right)\right)\\
&\quad =\frac{1}{N}\left( \frac{\sin(\frac{N}{2}\frac{\pi}{N})\sin(\frac{N+1}{2}\frac{\pi}{N})}{\sin(\frac{\pi}{2N})}\right).
\end{align*}

As $ N\to \infty$, this has limit

$$
\lim_{N\to\infty} \frac{1}{N}\left(\frac{\sin(\frac{\left(1+\frac{1}{N}\right)\pi}{2})}{\sin(\frac{\pi}{2N})}\right)
=\lim_{x\to 0}\frac{2}{\pi}\frac{x}{\sin(x)}=\frac{2}{\pi},
$$

giving a contradiction.

---

[63.](63) 
(i) Let $M_n =a^n$. Then for $x\in [0,a]$, we have $|x^n|\leq M_n$, and since $|a|<1$, the series $\sum_{n=1}^\infty M_n$ converges.

Hence, by the Weierstrass $M$-test, the series converges uniformly for $x\in [0,a]$.

(ii) Let

$$
S_n(x) = 1+x+x^2+\cdots + x^n.
$$

Let

$$
A_n = \sup \{ S_n (x) : x\in [0,1 ) \} = S_n(1) =1+1 + \cdots + 1 = n.
$$

The sequence  $(A_n)$ does not converge. It follows that the sequence of partial sums $(S_n(x))$ does not converge uniformly on $[0,1)$. Hence the series does not converge uniformly on $[0,1)$.

---

[64.](64) 
Let $f_n:[0,2\pi]\to\mathbb{R}$ be given by

$$
f_n (x) = \frac{\sin (nx )}{n^2}.
$$

Then $f_n$ is continuous. Note that

$$
|f_n (x )| \leq  \frac{1}{n^2}
$$

for all $x \in [0,2\pi]$, and

$$
\sum_{n=1}^\infty \frac{1}{n^2}
$$

converges.

Hence, by the Weierstrass $M$-test, the series $\sum_{n=1}^\infty f_n (x )$ converges uniformly for $x \in [0,2\pi]$. The uniform limit of a series of continuous functions is continuous, so $f$ is therefore continuous.

(65sol)=
[65.*](65) Note this question is starred, meaning it is intended more for interest and deviates more from the standard benchmark of question for this module

(i) Entering the series partial sums $\frac{4}{\pi}\sum_{k=0}^N\frac{(-1)^k}{2k+1}\cos\left(\frac{(2k+1)\pi x}{2}\right)$ into [Desmos](https://www.desmos.com/calculator/bd3xikfhb0) for a large value of $N$ yields the following (see {numref}`fourier1`).

```{figure} ../analysis_problems/figs/fourier1.png
---
width: 400px
name: fourier1
---
Desmos graph for $\frac{4}{\pi}\sum_{k=0}^100\frac{(-1)^k}{2k+1}\cos\left(\frac{(2k+1)\pi x}{2}\right)$ (Problem 65).
```

This graph was created with $N=100$, but any $N>50$ looks similar.

The graph suggests that the infinite series $\frac{4}{\pi}\sum_{k=0}^\infty\frac{(-1)^k}{2k+1}\cos\left(\frac{(2k+1)\pi x}{2}\right)$ is the Fourier series of the following square wave (see {numref}`fourier2`).

```{figure} ../analysis_problems/figs/fourier2.png
---
width: 600px
name: fourier2
---
Square wave $f(x)=\frac{4}{\pi}\sum_{k=0}^\infty\frac{(-1)^k}{2k+1}\cos\left(\frac{(2k+1)\pi x}{2}\right)$ (Problem 65).
```

In {numref}`fourier2`, we have been deliberately vague about the value of $f(x)$ when $x$ is an odd integer. In fact, direct calculation using the series shows that $f(x)=0$ for all odd integer values of $x$. 

```{figure} ../analysis_problems/figs/fourier3.png
---
width: 600px
name: fourier3
---
Improved graph of the square wave $f(x)=\frac{4}{\pi}\sum_{k=0}^\infty\frac{(-1)^k}{2k+1}\cos\left(\frac{(2k+1)\pi x}{2}\right)$ (Problem 65).
```

In particular, 

$$
f(x) = \left\{\begin{array}{cl} 0 & \text{ for } x \text{ an odd integer},\\
1 & \text{ for } 4k-1<x<4k+1, \; k\in\mathbb{Z}, \\
-1 & \text{ for } 4k+1<x<4k+3 \; k\in\mathbb{Z}  \end{array}\right.
$$

Of course, $f$ is a periodic function with period $2$.

(ii) We already showed directly in (i) that $f(x)=0$ whenever $x$ is an odd integer, but this might not have been obvious from the [Desmos graph](https://www.desmos.com/calculator/bd3xikfhb0) alone.


(iii) $f$ is differentiable at all points in $\mathbb{R}$ except for the odd integers. So $\text{Dom}(f') = \mathbb{R}\setminus\{2k+1:k\in\mathbb{Z}\}$. For $x\in\text{Dom}(f')$, $f'(x)=0$.

(iv) Differentiating the formal series 

$$
\frac{4}{\pi}\left[\cos\left(\frac{\pi x}{2}\right)-\frac{1}{3}\cos\left(\frac{3\pi x}{2}\right)+\frac{1}{5}\cos\left(\frac{5\pi x}{2}\right)-\frac{1}{7}\cos\left(\frac{7\pi x}{2}\right)+\ldots\right]
$$

term-by-term yields

$$
-2\left[\sin\left(\frac{\pi x}{2}\right)-\sin\left(\frac{3\pi x}{2}\right)+\sin\left(\frac{5\pi x}{2}\right)-\sin\left(\frac{7\pi x}{2}\right)+\ldots\right].
$$

When $x$ is an even integer, this series converges and equals $0$. A quick plug into [Desmos](https://www.desmos.com/calculator/req6vnpabz) suggests the series diverges for all other values of $x$.

**Extension:** Can you prove this?

````{admonition} Historical note
:class: note
In [Problem 65](#65sol), we found that at all points aside from the odd integers, the function

$$
f(x)=
\frac{4}{\pi}\left[\cos\left(\frac{\pi x}{2}\right)-\frac{1}{3}\cos\left(\frac{3\pi x}{2}\right)+\frac{1}{5}\cos\left(\frac{5\pi x}{2}\right)-\frac{1}{7}\cos\left(\frac{7\pi x}{2}\right)+\ldots\right]
$$

is differentiable with derivative equal to $0$. However, differentiating term-by-term yields a series that diverges for all values of $x$ except the even integers. 

It was apparent contradictions such as this that created such a stir among the contemporaries of Fourier, and meant his 1807 paper was never accepted for publication. As modern mathematicians, we have access to subtle ideas like uniform and absolute convergence (not to mention a functioning definition of differentiability) that allow us to make sense of the strange behaviour exhibited by this series. Mathematicians of the early 19th century could not reconcile the obvious usefulness of the method Fourier had showcased with everything they knew or believed to be true about functions, series and derivatives. 

Following these events was a huge collective effort of the whole mathematical community to properly understand and develop rigorous foundations for calculus --- or as it came to be known, real analysis.

**Disclaimer:** I am not a historian. For more on this fascinating subject, I recommend reading Chapter 1 of [A Radical Approach to Real Analysis by Bressoud](https://find.shef.ac.uk/permalink/f/1lephdb/44SFD_ALMA_DS21193257230001441).
````

## Integration

[66.](66) Let $f:[1,4]\to\mathbb{R}$; $f(x)=\frac{1}{x}$, and let $P=\{1,\frac{3}{2},2,4\}$.

(i) Below ({numref}`q64i`) is a sketch of the graph of $f$, the partition $P$, and the associated upper and lower Riemann sums.

```{figure} ../analysis_problems/figs/int1i.png
---
width: 500px
name: q64i
---
$y=\frac{1}{x}$, with upper and lower sums (Problem 66(i)). 
```

We have $U(f,P) = \sum_{k=1}^4M_k(x_k-x_{k-1})$, where $x_0=1$, $x_1=\frac{3}{2}$, $x_2=2$, $x_3=4$, and

$$
M_1=\sup\left\{\frac{1}{x}:1\leq x\leq\frac{3}{2}\right\}=1, \hspace{1em} M_2=\sup\left\{\frac{1}{x}:\frac{3}{2}\leq x\leq 2\right\}=\frac{2}{3},
$$

$$
M_3=\sup\left\{\frac{1}{x}:2\leq x\leq 4\right\}=\frac{1}{2}.
$$

Therefore,
\begin{align*}
U(f,P) &= 1\cdot\left(\frac{3}{2}-1\right) + \frac{2}{3}\cdot\left(2-\frac{3}{2}\right) + \frac{1}{2}\cdot(4-2) \\
&= \frac{1}{2} + \frac{1}{3} + 1 = \frac{11}{6}.
\end{align*}
Similarly, $L(f,P) = \sum_{k=1}^4m_k(x_k-x_{k-1})$, where

$$
m_1=\inf\left\{\frac{1}{x}:1\leq x\leq\frac{3}{2}\right\}=\frac{2}{3}, \hspace{1em} m_2=\inf\left\{\frac{1}{x}:\frac{3}{2}\leq x\leq 2\right\}=\frac{1}{2},
$$

and

$$
m_3=\inf\left\{\frac{1}{x}:2\leq x\leq 4\right\}=\frac{1}{4}.
$$

Hence
\begin{align*}
L(f,P) = \frac{2}{3}\cdot\left(\frac{3}{2}-1\right) + \frac{1}{2}\left(2-\frac{3}{2}\right) + \frac{1}{4}(4-2) \\
&= \frac{1}{3} + \frac{1}{4} + \frac{1}{2} = \frac{13}{12},
\end{align*}
and so

$$
U(f,P)-L(f,P) = \frac{11}{6}-\frac{13}{12} = \frac{9}{12} = \frac{3}{4}.
$$

(ii) Adding the point $P$ has the following effect ({numref}`q64ii`)

```{figure} ../analysis_problems/figs/int1ii.png
---
width: 500px
name: q64ii
---
Upper and lower sums with additional point $3$ (Problem 66(ii)).
``` 

We now have $x_0=1$, $x_1=\frac{3}{2}$, $x_2=2$, $x_3=3$ and $x_4=4$. $M_1$, $M_2$, $m_1$ and $m_2$ are not affected by the additional point, while

$$
M_3 = \sup\left\{\frac{1}{x}:2\leq x\leq 3\right\}=\frac{1}{2},\hspace{1em} M_4 =\sup\left\{\frac{1}{x}:3\leq x\leq 4\right\}=\frac{1}{3},
$$

$$
m_3 = \inf\left\{\frac{1}{x}:2\leq x\leq 3\right\}=\frac{1}{3}, \hspace{1em} \text{and} \hspace{1em} m_4 =\inf\left\{\frac{1}{x}:3\leq x\leq 4\right\}=\frac{1}{4}.
$$

Therefore

$$
U(f,P) = 1\left(\frac{1}{2}\right) + \frac{2}{3}\left(\frac{1}{2}\right) + \frac{1}{2}(1) + \frac{1}{3}(1) = \frac{1}{2}+\frac{1}{3}+\frac{1}{2}+\frac{1}{3} = \frac{5}{3},
$$

$$
L(f,P) = \frac{2}{3}\left(\frac{1}{2}\right) + \frac{1}{2}\left(\frac{1}{2}\right) + \frac{1}{3}(1) + \frac{1}{4}(1) = \frac{1}{3}+\frac{1}{4}+\frac{1}{3}+\frac{1}{4} = \frac{7}{6},
$$

and

$$
U(f,P) - L(f,P) = \frac{5}{3}-\frac{7}{6} = \frac{1}{2}.
$$

So the size of $U(f,P)-L(f,P)$ has decreased after adding the point $3$ to $P$.


(iii) Mimicking the proof of [Theorem 6.1](https://rosiesb.github.io/Analysis-Notes/6Int.html#thm:mono), let $x_k=1+\frac{3}{n}k$ for $k=0,\ldots,n$. Then, $P=\{x_0,\ldots,x_n\}$ partitions $[1,3]$ uniformly into $n$ intervals, each of width $\frac{3}{n}$. Since $\frac{1}{x}$ is decreasing,

$$
M_k = \sup\left\{\frac{1}{x}:x\in[x_{k-1},x_k]\right\} =\frac{1}{x_{k-1}}
$$

and

$$
m_k = \inf\left\{\frac{1}{x}:x\in[x_{k-1},x_k]\right\} =\frac{1}{x_k}
$$

for each $k$. So,
\begin{align*}
U(f,P) - L(f,P) &= \sum_{k=1}^n\left(\frac{1}{x_k} - \frac{1}{x_{k-1}}\right)\frac{3}{n} \\
&= \frac{3}{n}\left(\frac{1}{x_n}-\frac{1}{x_0}\right) = \frac{3}{n}\left(1-\frac{1}{4}\right) = \frac{9}{4n}.
\end{align*}
We have been asked to find $P$ so that $U(f,P)-L(f,P)<\frac{2}{5}$, so we choose $n$ so that $\frac{9}{4n}<\frac{2}{5}$. That is, $n>\frac{45}{8}$. In fact, $n=6$ will do.

So $x_k=1+\frac{1}{2}k$ for $k=0,\ldots,6$, and $P=\left\{1,\frac{3}{2},2,\frac{5}{2},3,\frac{7}{2},4\right\}$.

```{figure} ../analysis_problems/figs/int1iii.png
---
width: 500px
name: q64iii
---
Q66: A partition for which $U(f,P)-L(f,P)<\frac{2}{5}$ (Problem 66(iii)).
``` 

---

[67.](67) Let $g:[0,1]\to\mathbb{R}$; $\displaystyle g(x)=\left\{\begin{array}{cc} 1 & \text{for } 0\leq x<1 \\ 2 &\text{for } x=1 \end{array}\right.$.
  
(i) Let $P=\{x_0,x_1,\ldots x_n\}$ be any partition $[0,1]$, with $0=x_0<x_1<\ldots<x_n=1$. Then for $k=1,\ldots n$,

$$
m_k=\inf\{g(x) : x\in[x_{k-1},x_k\} = 1.
$$

Therefore

$$
L(g,P) = \sum_{k=1}^n(x_k-x_{k-1}) = x_n-x_0 = 1.
$$

(ii) Since $g$ is constant on $[0,1)$, we may as well take a partition consisting of 3 points --- the end points and a single point in the middle.

Let $\delta>0$ and consider the partition $P=\{0,1-\delta,1\}$ of $[0,1]$ (see {numref}`q67`).  

```{figure} ../analysis_problems/figs/q67.png
---
width: 600px
align: center
name: q67
---
Graph of $g$ with partition $P=\{0,1-\delta,1\}$ (Problem 67).
```

Making $\delta$ smaller should reduce the size of $U(g,P)$. We have

$$
M_1=\sup\{g(x) : x\in[0,1-\delta]\} = 1, \; \text{ and } \; M_2=\sup\{g(x):x\in[1-\delta,1]\}=2,
$$

so

$$
U(g,P) = 1\cdot(1-\delta) + 2\cdot\delta = 1+\delta.
$$

Taking $\delta=\frac{1}{10}$ will give $U(g,P)=1+\frac{1}{10}$. So our choice of partition should be $P=\left\{0,\frac{9}{10},1\right\}$.

(iii) By (ii), taking $P=\left\{0,1-\frac{\varepsilon}{2},1\right\}$ will give $U(g,P)=1+\frac{\varepsilon}{2} < 1+\varepsilon$.

By (i), $L(g,P)=1$, and so we've found a partition $P$ so that $U(g,P)-L(g,P)<\varepsilon$. This proves $g$ is Riemann integrable (by [Proposition 6.1](https://rosiesb.github.io/Analysis-Notes/6Int.html#intcond)).

---

[68.](68) 
For $\mathbb{1}_{[a,b]}$, this is just a special case of [Example 6.2](https://rosiesb.github.io/Analysis-Notes/6Int.html#eg:const), and there is nothing to show.

Note also that for any partition $P$ of $[a,b]$,

$$
U(\mathbb{1}_{(a,b])},P) = U(\mathbb{1}_{(a,b))},P) = U(\mathbb{1}_{(a,b])},P) = b-a
$$

This is because each of these functions have supremum $1$ on any subinterval of $[a,b]$.

For the lower integrals, let's first consider $\mathbb{1}_{(a,b]}$. Consider the partition $P=\{a,a+\delta,b\}$  (see {numref}`q68`).

```{figure} ../analysis_problems/figs/q68.png
---
width: 500px
name: q68
---
Graph  of $\mathbb{1}_{(a,b]}$, with partition $P=\{a,a+\delta,b\}$ (Problem 68).
```

Then $U(\mathbb{1}_{(a,b]},P) = b-a$ as before, while

$$
L(\mathbb{1}_{(a,b]},P) = 0\cdot(\varepsilon) + 1\cdot(b-a-\delta) = b-a-\delta.
$$

Therefore, $U(\mathbb{1}_{(a,b]},P) -L(\mathbb{1}_{(a,b]},P) = \delta$ for this partition $P$.

We can now use [Proposition 6.1](https://rosiesb.github.io/Analysis-Notes/6Int.html#intcond): given $\varepsilon>0$, the partition $P_\varepsilon:=\left\{a,a+\frac{\varepsilon}{2},b\right\}$ gives

$$
U(\mathbb{1}_{(a,b]},P_\varepsilon) -L(\mathbb{1}_{(a,b]},P_\varepsilon) = \frac{\varepsilon}{2} < \varepsilon, 
$$

and so $\mathbb{1}_{(a,b]}$ is Riemann integrable. 

To evaluate $\int_a^b\mathbb{1}_{(a,b]}(x)dx$, note that by our work above, 

$$
L(\mathbb{1}_{(a,b]},P_\varepsilon) = b-a \leq \int_a^b\mathbb{1}_{(a,b]}(x)dx < b-a+\varepsilon = U(\mathbb{1}_{(a,b]},P_\varepsilon).
$$

Since this is true for all $\varepsilon$, the only option is for $ \int_a^b\mathbb{1}_{(a,b])}(x)dx = b-a$.

The proof that $\mathbb{1}_{[a,b)}$ is integrable with $\int_a^b\mathbb{1}_{[a,b)}(x)dx = b-a$ is nearly identical --- just consider the partitions of the form $P=\{a,b-\delta,b\}$ instead.

For $\mathbb{1}_{(a,b)}$, let $\delta>0$, and consider $P=\{a,a+\delta,b-\delta,b\}$. As before, $U(\mathbb{1}_{(a,b)},P)=b-a$, and direct calculation gives

$$
L(\mathbb{1}_{(a,b)},P)= 0\cdot\delta + 1\cdot(b-\delta-a-\delta)+0\cdot\delta=b-a-2\delta.
$$

Then, given $\varepsilon>0$, take $\delta=\frac{\varepsilon}{4}$. We get

$$
U(\mathbb{1}_{(a,b)},P) -L(\mathbb{1}_{(a,b)},P) = b-a - \left(b-a-2\cdot\frac{\varepsilon}{4}\right)= \frac{\varepsilon}{2} < \varepsilon, 
$$

and so $\mathbb{1}_{(a,b)}$ is integrable, by [Proposition 6.1](https://rosiesb.github.io/Analysis-Notes/6Int.html#intcond). Moreover, 

$$
b-a \leq \int_a^b\mathbb{1}_{(a,b)}(x)dx < b-a+\varepsilon
$$

and since this is true for all $\varepsilon>0$, we must have $\int_a^b\mathbb{1}_{(a,b)}(x)dx =b-a$.

---

[69.](69) 
(i) By results from the course (specifically, [Propositions 6.2](https://rosiesb.github.io/Analysis-Notes/6Int.html#int-ind) and [Proposition 6.3](https://rosiesb.github.io/Analysis-Notes/6Int.html#propsint)(ii)), $r$ and $s$ are both linear combinations of integrable functions, and hence are integrable with

$$
\int_0^3 r(x) dx = \int_0^11dx+\int_1^2edx+\int_2^3e^4dx = 1+e+e^4,
$$

and

$$
\int_0^3 s(t)\, dt = \int_0^1edt+\int_1^2e^4dt+\int_2^3e^9dt = e+e^4+e^9.
$$

(ii) Continuous functions are integrable, by another result from the course (specifically, by [Theorem 6.2](https://rosiesb.github.io/Analysis-Notes/6Int.html#thm:ctsint)). So $f\colon [0,3]\rightarrow \mathbb{R}$ defined by $f(x)=e^{x^2}$ is integrable since it is a continuous function.

[Alternative answer: by the fact $f$ is monotonic increasing (c.f. [Theorem 6.1](https://rosiesb.github.io/Analysis-Notes/6Int.html#thm:mono)).]

(iii) Note that $r(t)\leq f(t)\leq s(t)$ for all $t$, and so by [Proposition 6.3](https://rosiesb.github.io/Analysis-Notes/6Int.html#propsint)(i),

$$
1+e+e^4  = \int_0^3 r(t)\, dt \leq \int_0^3 f(t)\, dt \leq \int_0^3 s(t)\, dt = e+e^4+e^9.
$$

---

[70.](70) Let $f,g:[a,b]\to\mathbb{R}$ be integrable functions.

(i) For any subset $A\subset[a,b]$,

$$
\sup\{f(x)+g(x):x\in A\} \leq \sup\{f(x):x\in A\} + \sup\{g(x):x\in A\},
$$

and similarly

$$
\inf\{f(x)+g(x):x\in A\} \geq \inf\{f(x):x\in A\} + \inf\{g(x):x\in A\}.
$$

It is then immediate from the definition of the upper and lower sums that

$$
U(f+g,P) \leq U(f,P)+U(g,P)
$$

and

$$
L(f+g,P) \geq L(f,P)+L(g,P).
$$

For the example where this is strict, a good strategy is to look for functions with features that "cancel out" in some sense. For example, you could take

$$
f(x) = \left\{\begin{array}{cc} 1 & \text{ if } 0\leq x\leq 1 \\  -1 & \text{ if } 1\leq x\leq 2\end{array}\right.
$$

and

$$
g(x) = \left\{\begin{array}{cc} -1 & \text{ if } 0\leq x\leq 1 \\  1 & \text{ if } 1\leq x\leq 2.\end{array}\right.
$$

Then $f+g$ is the zero function, so $L(f+g,P)=U(f+g,P)=0$. On the other hand

$$
U(f,P)+U(g,P) = 1+1 = 2,
$$

and

$$
L(f,P)+L(g,P) = -1 -1 =-2.
$$

(ii) Let $P_1$ and $P_2$ be partitions of $[a,b]$. Then
\begin{align*}
U(f+g) &\leq U(f+g,P_1\cup P_2) & \text{ (by definition of $U(f+g)$)}\\
&\leq U(f,P_1\cup P_2) + U(g,P_1\cup P_2) & \text{ (by part (i))}\\
&\leq U(f,P_1) + U(g,P_2),
\end{align*}
by [Lemma 6.1](https://rosiesb.github.io/Analysis-Notes/6Int.html#lem:ref), since $P_1\cup P_2$ is a refinement of both partitions $P_1$ and $P_2$.

The proof of the lower sum statement is similar:
\begin{align*}
L(f+g) &\leq L(f+g,P_1\cup P_2) & \text{ (definition of $L(f+g)$)}\\
&\geq L(f,P_1\cup P_2) + L(g,P_1\cup P_2) & \text{ (part (i))}\\
&\leq L(f,P_1) + L(g,P_2) & \text{(Lemma 6.1).}
\end{align*}


(iii) We just proved

$$
U(f+g,P_1\cup P_2) \leq U(f,P_1) + U(g,P_2),
$$

for all partitions $P_1$ and $P_2$ of $[a,b]$.

Taking $\inf$ over $P_1$,

$$
U(f+g) \leq U(f) + U(g,P_2),
$$

and then taking $\inf$ over $P_2$,

$$
U(f+g) \leq U(f)+U(g).
$$

Since $f$ and $g$ are integrable, $\int_a^bf(x)dx=U(f)$ and $\int_a^bg(x)dx=U(g)$. This shows that

$$
U(f+g) \leq \int_a^bf(x)dx + \int_a^bg(x)dx.
$$

A similar argument shows that

$$
L(f+g) \geq \int_a^bf(x)dx + \int_a^bg(x)dx.
$$

Hence

$$
\int_a^bf(x)dx + \int_a^bg(x)dx \leq L(f+g) \leq U(f+g) \leq \int_a^bf(x)dx + \int_a^bg(x)dx.
$$

The only option is

$$
L(f+g)=U(f+g)=\int_a^bf(x)dx + \int_a^bg(x)dx.
$$

That is, $f+g$ is integrable and

$$
\int_a^b(f(t)+g(t))dt = \int_a^bf(x)dx + \int_a^bg(x)dx.
$$

---

[71.](71) Let $P$ be the partition $a=x_0<x_1<\ldots<x_n=b$. If $k\geq 0$, then

$$
\sup_{x\in[x_{k-1},x_k]}kf(x) = k\sup_{x\in[x_{k-1},x_k]}f(x)
$$

and

$$
\inf_{x\in[x_{k-1},x_k]}kf(x) = k\inf_{x\in[x_{k-1},x_k]}f(x).
$$

Therefore $U(kf,P)=kU(f,P)$ and $L(kf,P)=kL(f,P)$, and taking infima/suprema, $U(kf)=kU(f)$ and $L(kf)=kL(f)$.

Since $f$ is integrable, $U(f)=L(f)=\int_a^bf(x)dx$, and hence

$$
U(kf)=kU(f)=kL(f)=L(kf)=k\int_a^bf(x)dx.
$$

It follows that $kf$ is integrable, with $\displaystyle\int_a^bkf(x)dx=k\int_a^bf(x)dx$.

To extend this result to include negative $k$, it is sufficient to prove the $k=-1$ case. Note that

$$
\sup_{x\in[x_{k-1},x_k]}\big(-f(x)\big) = -\inf_{x\in[x_{k-1},x_k]}f(x),
$$

and

$$
\inf_{x\in[x_{k-1},x_k]}\big(-f(x)\big) = -\sup_{x\in[x_{k-1},x_k]}f(x).
$$

Therefore, $U(-f,P)=-L(f,P)$ and $L(-f,P)=-U(f,P)$, and so
\begin{align*}
U(-f) &= \inf\{U(-f,P):\text{ partitions } P \text{ of } [a,b]\} \\
&= \inf\{-L(f,P):\text{ partitions } P \text{ of } [a,b]\} \\
&= -\sup\{L(f,P):\text{ partitions } P \text{ of } [a,b]\} = -L(f).
\end{align*}
Similarly,
\begin{align*}
L(-f) &= \sup\{L(-f,P):\text{ partitions } P \text{ of } [a,b]\} \\
&= \sup\{-U(f,P):\text{ partitions } P \text{ of } [a,b]\} \\
&= -\inf\{U(f,P):\text{ partitions } P \text{ of } [a,b]\} = -U(f).
\end{align*}
Therefore $U(-f) = -L(f) = -U(f) = L(-f)$, so $-f$ is integrable, and

$$
\int_a^b(-f(x))dx = -\int_a^b f(x)dx.
$$

---

[72.](72) We have: $M=\sup\{f(x):x\in A\}, \; m=\inf\{f(x):x\in A\}$, and $M'=\sup\{|f(x)|:x\in A\}, \; \text{ and } \; m'=\inf\{|f(x)|:x\in A\}$.

(i) Case 1: $m\geq 0$. Then $f$ is a non-negative function, so $M=M'$, $m=m'$, and $M-m=M'-m'$.

Case 2: $m\leq M\leq 0$. Then $M'=-m$, $m'=-M$, and so again $M'-m'=M-m$.

Case 3: $m<0<M$. Then $M'=\max\{M,-m\}\leq M+(-m)$, since both $M$ and $-m$ are positive numbers. Then,

$$
M'-m' \leq M' \leq M-m,
$$

since $m'\geq 0$.

(ii) Let $f:[a,b]\to\mathbb{R}$ be integrable, and let $P$ be the partition $a=x_0<x_1<\ldots<x_n=b$. For $k=1,\ldots,n$. let

$$
M_k=\sup_{x\in[x_{k-1},x_k]}f(x), \; m_k=\inf{x\in[x_{k-1},x_k]}f(x),
$$

$$
M_k'=\sup_{x\in[x_{k-1},x_k]}|f(x)|, \; \text{ and } \; m_k'=\inf{x\in[x_{k-1},x_k]}|f(x)|.
$$

Then by part (i), $M_k-m_k\geq M_k'-m_k'$ for each $k$. Therefore,
\begin{align*}
U(|f|,P) - L(|f|,P) &= \sum_{k=1}^n(M_k'-m_k')(x_k-x_{k-1}) \\
&\leq \sum_{k=1}^n(M_k-m_k)(x_k-x_{k-1}) = U(f,P)-L(f,P).
\end{align*}

(iii) Since $f$ is integrable, for all $\varepsilon>0$, we can choose the a partition $P$ so that $U(f,P)-L(f,P)<\varepsilon$. Using the result of part (ii). it follows that $U(|f|,P)-L(|f|,P)<\varepsilon$ for this partition, and so $|f|$ is integrable.

Since $-|f(x)|\leq f(x)\leq |f(x)|$ for all $x\in[a,b]$, [Proposition 6.3](https://rosiesb.github.io/Analysis-Notes/6Int.html#propsint)(iii) implies that

$$
-\int_a^b|f(x)|dx \leq \int_a^b f(x)dx \leq \int_a^b|f(x)|dx.
$$

That is,

$$
\left|\int_a^b f(x)dx\right| \leq \int_a^b|f(x)|dx.
$$

---

[73.](73) We have

$$
\int_{a(x)}^{b(x)} f(t)dt =  \int_0^{b(x)} f(t)dt - \int_0^{a(x)} f(t)\ dt.
$$

Write $F:\mathbb{R}\to\mathbb{R}$; $F(x)=\int_0^x f(t)dt.$ Then by the fundamental theorem of calculus ([Theorem 6.3](https://rosiesb.github.io/Analysis-Notes/6Int.html#ftc)), $F$ is differentiable, and $ F'(x)=f(x)$ for all $x\in\mathbb{R}$. Also, 

$$
(F\circ b)(x) = F(b(x)) = \int_0^{b(x)} f(t)dt=F(b(x)),
$$

and $b$ is differentiable. Therefore, by the chain rule ([Theorem 4.4](https://rosiesb.github.io/Analysis-Notes/4Diff.html#chain)), $F\circ b$ is also differentiable, with

$$
(F\circ b)'(x) = \frac{d}{dx}\int_0^{b(x)} f(t)dt =F'(b(x))b'(x)=f(b(x))b'(x),
$$

for all $x\in\mathbb{R}$. Similarly,

$$
\frac{d}{dx}\int_0^{a(x)} f(y)dt =f(a(x))a'(x).
$$

Subtracting these

$$
\frac{d}{dx}\int_{a(x)}^{b(x)} f(t)dt =f(b(x))b'(x) - f(a(x))a'(x),
$$

as required.

---

[74.](74) 
(i) It follows immediately from the fundamental theorem of calculus that $l$ is differentiable, with $l'(x)=\frac{1}{x}$.
 
(ii) By [Proposition 6.3](https://rosiesb.github.io/Analysis-Notes/6Int.html#propsint) in the lecture notes,

$$
l(xy) =\int_1^{xy}\frac{1}{t}\, dt= \int_1^x \frac{1}{t}\, dt + \int_x^{xy} \frac{1}{t}\, dt = l(y) + \int_x^{xy}\frac{1}{t}dt.
$$

In the second integral, set $a(x)=xy$, $b(x)=x$ and use [Problem 72](72). We have $a'(x)=y$ and $b'(x)=1$, so

$$
\frac{d}{dx}\int_x^{xy} \frac{1}{t}dt = \frac{1}{b(x)}b'(x) - \frac{1}{a(x)}a'(x) = \frac{1}{x} - \frac{y}{xy} =0.
$$

Therefore $\int_x^{xy}\frac{1}{t}dt$ is constant as a function of $x$. In particular, it coincides with its value when $x=1$:

$$
\int_x^{xy}\frac{1}{t}dt = \int_1^{y}\frac{1}{t}dt = l(y),
$$

and $l(xy)=l(x)+l(y)$ follows.


---

[75.*](75) Define $G\colon [a,b]\rightarrow \mathbb{R}$ by

$$
G(x) = \int_a^x f(t)\, dt
$$

Then $G$ is a continuous function. This was mentioned in the lectures. To see why, let $h>0$. Since the function $f$ is Riemann integrable, it is bounded, so we have $M\in \mathbb{R}$ such that $|f(t)|\leq M$ for all $t\in [a,b]$. Then

$$
|G(x+h) - G(x) | =\left| \int_x^{x+h} f(t)\, dt \right| \leq \int_x^{x+h} |f(t)|\, dt \leq Mh.
$$

Similarly $|G(x-h) - G(x) | \leq Mh$.

So $G(x+h)\rightarrow G(x)$ as $h\rightarrow 0$, and $G$ is continuous.

Thus we can define a continuous function $F\colon [a,b]\rightarrow \mathbb{R}$ by

$$
F(x) = \int_a^x f(t)\, dt - \int_x^b f(t)\, dt.
$$

Observe that

$$
F(a) = -\int_a^b f(t)\, dt,  \qquad F(b) = \int_a^b f(t)\, dt=-F(a).
$$

If $\int_a^b f(t)\, dt =0$, then we can take $x=a$ and we have the required result. Otherwise, either $F(a)<0$ and $F(b)>0$ or $F(a)>0$ and $F(b)<0$.

Either way, by the intermediate value theorem, we have $x\in [a,b]$ such that $F(x)=0$, that is to say

$$
\int_a^x f(t)\, dt = \int_x^b f(t)\, dt.
$$

---

[76.](76) 
(i) Let $\mu = \frac{1}{b-a} \int_a^b f(x)\, dx$. Then $\int_a^b f(x)\, dx=(b-a)\mu$, and we need only show that $\mu\in[m,M]$.

Consider the step functions $m\mathbf{1}_{[a,b]}$ and $M\mathbf{1}_{[a,b]}$ with $m\mathbf{1}_{[a,b]}(x)\leq f(x)\leq M\mathbf{1}_{[a,b]}(x)$ for all $x\in[a,b]$. Thus we have

$$
m(b-a)=\int_a^b m\mathbf{1}_{[a,b]}(x)\, dx \leq \int_a^b f(x)\, dx \leq \int_a^b M\mathbf{1}_{[a,b]}(x)\, dx= M(b-a).
$$

But $\int_a^b f(x)\, dx=(b-a)\mu$, and so $\mu \in [m,M]$.

(ii) We are now given that $f:[a,b]\to\mathbb{R}$ is continuous. By [Corollary 3.3](https://rosiesb.github.io/Analysis-Notes/3Cty.html#interval), $f([a,b])=[m,M]$, where 

$$
m = \inf \{ f(x) : x\in [a,b] \} \; \text{ and } \; M = \sup \{ f(x) : x\in [a,b] \}.
$$

In particular, $m<f(x)<M$ for all $x\in[a,b]$, and so by part (i),

$$
\int_a^b f(x)\, dx =(b-a)\mu,
$$

for some $\mu \in [m,M]$. As $\mu\in [m,M]=f([a,b])$ and $f$ is continuous, there is some $\xi \in [a,b]$ such that $f(\xi ) = \mu$. Hence

$$
\int_a^b f(x)\, dx =(b-a)f(\xi ).
$$

---

[77.](77) Let $f:[a,b]\to\mathbb{R}$ be continuous, and  $m = \inf \{ f(x) : x\in [a,b] \}$ and $M = \sup \{ f(x) : x\in [a,b] \}$ as before. Then $m\leq f(x)\leq M$ for all $x\in [a,b]$. As $g(x)\geq 0$, we have

$$
mg(x)\leq f(x)g(x)\leq Mg(x)
$$

for all $x\in [a,b]$. By [Proposition 6.3](https://rosiesb.github.io/Analysis-Notes/6Int.html#propsint)(i),

$$
m \int_a^b g(x)\, dx \leq \int_a^b f(x)g(x)\, dx \leq M\int_a^b g(x)\, dx.
$$

Let

$$
I= \int_a^b g(x)\, dx.
$$

Either $I=0$ or $I>0$. If $I=0$, then the above tells us that

$$
\int_a^b f(x)g(x)\, dx =0
$$

and any $\xi \in [a,b]$ satisfies

$$
\int_a^b f(x)g(x)\, dx = f(\xi ) \int_a^b g(x)\, dx .
$$

If $I>0$, then

$$
m \leq \frac{1}{I} \int_a^b f(x)g(x)\, dx \leq M.
$$

By [Corollary 3.3](https://rosiesb.github.io/Analysis-Notes/3Cty.html#interval), $f([a,b])=[m,M]$, and so there is $\xi \in [m,M]$ such that

$$
f(\xi ) = \frac{1}{I}  \int_a^b f(x)g(x)\, dx
$$

or in other words

$$
\int_a^b f(x)g(x)\, dx = f(\xi ) \int_a^b g(x)\, dx .
$$

**We do need the assumption $g(x)\geq 0$.** To see this, consider the function $g(x) = x$ for $x\in [-1,1]$. Then

$$
\int_{-1}^1 g(x)\, dx =0,
$$

so the result would say that for any continuous function $f\colon [-1,1]\rightarrow \mathbb{R}$ we have

$$
\int_{-1}^1 xf(x)\, dx =0.
$$

But this is clearly not the case, taking for example $f(x)=x$.