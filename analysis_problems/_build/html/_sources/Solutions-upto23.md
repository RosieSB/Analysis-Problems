(sol)=
# Solutions
Complete up to Q23, excluding some homework questions. 

Homework solutions will be released alongside the return of each piece of work.

(ch1sol)=
## Preliminary problems

[P1.](P1)
The correct statements are (ii) and (v). 

In statement (iv), the quantifiers $\forall$ and $\exists$ are the wrong way round, while in (i) they are missing altogether. Statement (iii) asserts that last part, $|x_n-l|<\varepsilon$ $\forall n\geq N$, should hold for all $\varepsilon$ and for all $N$ --- so again, there is an issue with the quantifiers.

Bonus exercise: prove that (iv) holds if and only if $(x_n)$ is the constant sequence $x_n=l$ for all $n\in\mathbb{N}$.

---

(P2sol)=
[P2.](P2) *(Homework 1 question).*

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

(P3sol)=
[P3.](P3) *(Homework 1 question).*

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
[2.](2) *(Homework 1 question).*<br>
````{note}
This question was ambiguous about whether or not proofs are required. Strictly speaking, "being able to prove rigorously which real numbers are the limit points of a given set" is not a key learning outcome for this module, so the proofs included below are largely for interest. What is important is that you know the definition of a limit point, and understand it well enough that you can identify which real numbers are limit points of a given set, and which are not.
````
(i) $X=(0,1)\cup[2,3)\cup\{4,5\}$. Set of limit points: $L=[0,1]\cup[2,3]$.

````{dropdown} Proof (dropdown)
Let $L$ be the set of all limit points of $X$. We prove that $L=[0,1]\cup[2,3]$ by proving $L\subseteq[0,1]\cup[2,3]$ and $L\supseteq[0,1]\cup[2,3]$. 

$(\supseteq)$ Let $a\in[0,1]\cup[2,3]$. We prove $a$ is a limit point of $X=(0,1)\cup[2,3)\cup\{4,5\}$ by explicitly writing down a sequence $(x_n)$ in $X\setminus\{a\}$ with limit $a$. In fact, $x_n=a+\frac{1}{n+3}$ works for any choice $a\in[0,1)\cup[2,3)$. If $a=0$ or $a=3$, then use $x_n=a-\frac{1}{n}$ instead. Either way, we have shown that $a\in L$.

$(\subseteq)$ If $a\in L$, then there is a sequence $(x_n)$ in $X\setminus\{a\}$, with $a=\lim_{n\rightarrow\infty}x_n$. Since $x_n\in X$ for all $n\in\mathbb{N}$, we must have $0<x_n\leq 5$ for all $n\in\mathbb{N}$, and so $0\leq a\leq 5$. 

If $a\in(1,2)$, then the definition of convergence says that for any $\varepsilon>0$, we can find $N\in\mathbb{N}$ such that $x_n\in(a-\varepsilon,a+\varepsilon)$ for all $n\geq N$. We know this holds for any $\varepsilon>0$, so in particular we can choose $\varepsilon>0$ such that $(a-\varepsilon,a+\varepsilon)\subseteq(1,2)$. For this choice of $\varepsilon$ and resulting $N$, we have that $x_n\in(1,2)$ for all $n\geq N$. But this contradicts $(x_n)$ being a sequence in $X$. So $a\notin (1,2)$.

Finally, suppose $a>3$. By a similar argument, we can choose $\varepsilon>0$ small enough so that $(a-\varepsilon,a+\varepsilon)\subseteq(3,\infty)$. Since $x_n\rightarrow a$, we know there exists $N\in\mathbb{N}$ such that $|x_n-a|<\varepsilon$ for all $n\geq N$. Therefore, for all $n\geq N$, we have $x_n\in(a-\varepsilon,a+\varepsilon)\subseteq (3,\infty)$. In other words, $x_n>3$ for all $n\geq N$. The only elements of $X$ that are strictly larger than $3$ are $4$ and $5$. This means that $x_n\in\{4,5\}$ for all $n\geq N$. But then, since $(x_n)$ converges to $a$, it must be eventually constant and equal to $a$, contradicting $x_n\neq a$ for all $n\in\mathbb{N}$. So $a\leq 3$.

It follows that $a\in[0,1]\cup[2,3]$.<span style="float:right;">$\square$</span>
````
   
(ii)  $X=\mathbb{Z}$. Set of limit points: $L=\emptyset$.  

````{dropdown} Proof (dropdown)
If $a$ is a limit point of $\mathbb{Z}$, then there is a sequence $(x_n)$ in $\mathbb{Z}$, with $x_n\neq a$ for all $n\in\mathbb{N}$, and $\lim_{n\rightarrow\infty}x_n=a$. But all convergent sequences in $\mathbb{Z}$ are eventually constant, so this is impossible.  <span style="float:right;">$\square$</span>
````

(iii)$X=\mathbb{R}\setminus\mathbb{Z}$. Set of limit points:  $L=\mathbb{R}$.

````{dropdown} Proof (dropdown)
If $a\in\mathbb{Z}$, then $x_n:=a+\frac{1}{2n}$ defines a sequence in $X$ with limit $a$, and clearly $x_n\neq a$ for all $n\in\mathbb{N}$. This shows $\mathbb{Z}\subseteq L$. If $a\in\mathbb{R}\setminus\mathbb{Z}$, then $a$ must lie in some open interval $(k,k+1)$, where $k\in\mathbb{Z}$ (in fact $k=\lfloor x\rfloor$). 

```{figure} ../analysis_problems/figs/2iii.png
---
width: 500px
name: 2iii
---
Sketch to decide/justify choice $\delta:=\min\{x-a,k+1-a\}$ (Problem 2(iii))
```

Let $\delta=\min\{x-a,k+1-a\}$ (this choice is strongly motivated by a sketch --- see {numref}`2iii`.). Then $x_n:=a+\frac{\delta}{n}$ defines a sequence in $(k,k+1)$, with limit $a$, and such that $x_n\neq a$ for all $n\in\mathbb{N}$.<span style="float:right;">$\square$</span>
````

(iv) $X=\{x\in\mathbb{Q}:0<x<1\}$. Set of limit points: $L=[0,1]$

````{dropdown} Proof (dropdown)
If $(x_n)$ is a convergent sequence in $X$, then $0<x_n<1$ for all $n\in\mathbb{N}$, and so $0\leq\lim_{n\rightarrow\infty}x_n\leq 1$. This shows that $L\subseteq [0,1]$. On the other hand, if $a\in[0,1]$, then by density of the rationals, for all $n\in\mathbb{N}$ there is a rational number $x_n$ satisfying $a<x_n<a+\frac{1}{n}$. Then, $x_n\neq a$ for all $n\in\mathbb{N}$, and by the squeeze theorem, $x_n\rightarrow a$ as $n\rightarrow\infty$. Also, since $a\in[0,1]$, with the exception of the case $a=1$ (treated separately below), we will eventually have $0<x_n<1$ for all $n\in\mathbb{N}$ sufficiently large. In other words, removing a finite number of initial terms if necessary, we have found a sequence in $X\setminus\{a\}$ with limit $a$.

For the case $a=1$, use the same argument, but with sequence $(x_n)$ of rational numbers chosen so that  $1-\frac{1}{n}<x_n<1$, for each $n\in\mathbb{N}$.<span style="float:right;">$\square$</span>
````

(v) $X=\displaystyle\left\{\frac{1}{n}:n\in\mathbb{N}\right\}$.  $L=\{0\}$

````{dropdown} Proof (dropdown)
That $0\in L$ follows by taking the sequence $x_n=\frac{1}{n}$. On the other hand, if $a\in L$, then there is a sequence $(x_n)$ in $X\setminus\{a\}$ with limit $a$. All elements of $X$ are strictly positive, so $x_n>0$ for all $n\in\mathbb{N}$, and hence $a\geq 0$. Suppose that $a>0$. Then by definition of convergence, there is $N\in\mathbb{N}$ such that $|x_n-a|<\frac{a}{2}$ for all $n\geq N$. But then $x_n\in\left(\frac{a}{2},\frac{3a}{2}\right)$ for all $n\geq N$. There are only finitely many elements of $X$ that lie in this interval, and we know $(x_n)$ converges to $a$. So, the only option is that $(x_n)$ is eventually constant and equal to $a$. This is a contradiction, since $(x_n)$ is a sequence in $X\setminus\{a\}$. It follows that $a=0$.<span style="float:right;">$\square$</span>
````
---

(3sol)=
[3.](3) *(Homework 1 question).*

(i) We are given $f:\mathbb{R}\to\mathbb{R}$; $f(x)=4x+7$. Intuition tells us that 

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

Hence we can let $\delta:=\frac{\varepsilon}{15}$ and conclude that if $x\in\{0\}\cup[1,3]$ and $0<|x-2|<\frac{1}{15}$, then 

$$
|f(x)-11|<15\cdot\frac{\varepsilon}{15} =\varepsilon.
$$

For this $f$, $\lim_{x\rightarrow 0}f(x)$ is not defined, since $0$ is not a limit point of the domain of $f$.


(3iiisol)=
(iii) Finally, let $f:(0,\infty)\to\mathbb{R}$; $f(x)=x+\frac{1}{x}$. The limit of $f(x)$ as $x\rightarrow 2$ ought to be $2+\frac{1}{2}=\frac{5}{2}$.

Let $\varepsilon>0$, and consider

$$
\left|f(x)-\frac{5}{2}\right| = \left|x+\frac{1}{x}-\frac{5}{2}\right| = \left|\frac{2x^2+2-5x}{2x}\right| = \left|\frac{(x-2)(2x-1)}{2x}\right| = |x-2|\left|1-\frac{1}{2x}\right|.
$$

Observe that if $x\in(0,\infty)$ and $|x-2|<1$, then $0<1-\frac{1}{2x}<1$, and so 

$$
\left|f(x)-\frac{5}{2}\right| = |x-2|\left|1-\frac{1}{2x}\right| < |x-2|.
$$

To make sure the above inequality holds **and** is bounded above by $\varepsilon$, let $\delta:=\min\{\varepsilon,1\}$. 

Suppose that $x\in(0,\infty)$ with $0<|x-2|<\delta$. Then by our choice of $\delta$, $0<|x-2|<1$ and $0<|x-2|<\varepsilon$ both hold simultaneously. It follows that 

$$
\left|f(x)-\frac{5}{2}\right|<|x-2|<\varepsilon,
$$

and hence $\lim_{x\rightarrow 2}f(x)=\frac{5}{2}$ is proved.

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

---

[17.](17)
The proofs for each of these answers are immediate by [Problem 8](#8).

(i) $f:\mathbb{R}\to\mathbb{R}$; $f(x) = \begin{cases} 1 -x & \text{if }x < 1\\ x^{2}& \text{if }x \geq 1. \end{cases}$ 

This function is continuous on $\mathbb{R} \setminus \{1\}$, with a jump discontinuity at $x=1$ of size $1$.

(ii) $g:\mathbb{R}\to\mathbb{R}$; $g(x) = [x] = \left\{\begin{array}{cl} \lfloor x\rfloor & \text{ if } x\geq 0 \\ \lceil x \rceil & \text{ if } x<0 \end{array}\right.$ 

This function is continuous on $\mathbb{R}\setminus\{\pm k: k\in\mathbb{N}\}$. Jump discontinuity at $n$ with size $1$ for all $n\in\mathbb{Z}_+$.

(iii) $h:\mathbb{R}\to\mathbb{R}$; $h(x) =3 - 5\mathbb{1}_{(0, 1]}(x) + 7\mathbb{1}_{(1, 2]}(x)$ 

This is continuous at $\mathbb{R} \setminus \{0,1,2\}$, with jump discontinuities at $0$, $1$, and $2$. The jump sizes are, respectively, $0$, $-5$, and $-7$.  

---

[18.](18) To appear (Homework 3 question)  

---

[19.](19) To appear (Homework 2 question).

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

(ii) You can check that for all $a, b \in \mathbb{R}$,

$$
\min\{a, b\} = \frac{1}{2}(a + b) - \frac{1}{2}|a - b|,
$$

and then argue as in (i).

Alternatively, one could derive (ii) from (i) by using $\min\{f,g\} = - \max\{-f, -g\}$.

---

[21.](21) Let $f: \mathbb{R} \rightarrow \mathbb{R}$ be such that 
```{math}
:label: linear
f(x+y) = f(x) + f(y) \; \forall x,y \in \mathbb{R}.
```
Then:

(i) $f(0) = f(0 + 0) = f(0) + f(0) = 2f(0)$, hence $f(0) = 0$.

(ii) For all $x\in\mathbb{R}$, we have by (i), $0 = f(0) = f(x + -x) = f(x) + f(-x)$. So $f(-x)=-f(x)$.

(iii) Suppose $f$ is continuous at zero. Then, if $x \neq 0$ then any sequence $(x_{n})$ which converges to $x$ can be written as $x_{n} = x + y_{n}$ where $(y_{n})$ converges to zero. Since $f$ is assumed to be continuous at $0$, we have that $ \lim_{n\rightarrow\infty} f(y_{n})$ exists and equals $f(0)$. By (i), $f(0)=0$, hence 

$$
\lim_{n\rightarrow\infty} f(x_{n}) = \lim_{n\rightarrow\infty} f(a + y_{n}) = f(a) + \lim_{n\rightarrow\infty} f(y_{n}) = f(a) + f(0) = f(a)+0 = f(a).
$$

(iv) Let $k=f(1)$. We use induction on $n\in\mathbb{N}$. If $n=1$, then $f(n)=f(1)=k=k\cdot 1$, so the statement holds. Assume it holds for some $n\in\mathbb{N}$. Then by [](#linear),

$$
f(n+1) = f(n) + f(1) = nk + k = (n+1)k.
$$

Hence by induction, $f(n)=nk$, for all $n\in\mathbb{N}$. Combine this with part (ii) to extend to all $n\in \mathbb{Z}$.

(v) Still writing $k=f(1)$, consider $\frac{p}{q}\in\mathbb{Q}$, where $p\in \mathbb{Z}$ and $q\in \mathbb{N}$. By (iv),

$$
pk = f(p) = f\left(q\cdot \frac{p}{q}\right) = qf\left(\frac{p}{q}\right),
$$

and the result follows.

(vi) Finally, let $k=f(1)$, and assume $f$ is continuous at $0$, and let $x\in\mathbb{R}$. If $x\in\mathbb{Q}$, then we have already shown $f(x)=kx$ in part (v). So assume $x$ is irrational. By denseness of the rationals, there is a sequence $(r_n)$ of rational numbers converging to $x$. By (v), $f(r_n)=kr_n$ for all $n\in\mathbb{N}$. By (iii), $f$ is continuous at $x$, so using algebra of limits, we have

$$
f(x) = \lim_{n\rightarrow\infty} f(r_n) =   \lim_{n\rightarrow\infty} kr_n=k \lim_{n\rightarrow\infty} r_n = kx.
$$

---

[22.](22) To appear (Homework 2 question).

---

[23.](23) The function $\mathbb{1}_{(a, b)}$ is left continuous at $a$ (but not right continuous), and right continuous at $b$ (but not left continuous).

To prove the left continuity at $a$, let $(x_{n})$ be any sequence in $\mathbb{R}$ which converges to $a$ with $x_{n} < a$ for all $n\in\mathbb{N}$. Then $\lim_{n\rightarrow\infty} \mathbb{1}_{(a, b)}(x_{n}) = 0 = \mathbb{1}_{(a, b)}(a).$ On the other hand to see that it is not right continuous at $a$, let $(y_{n})$ be any sequence in $\mathbb{R}$ which converges to $a$ with $a < y_{n} < b$ for all $n\in\mathbb{N}$. Then
$ \lim_{n\rightarrow\infty} \mathbb{1}_{(a, b)}(y_{n}) = 1 \neq \mathbb{1}_{(a, b)}(a). $ The other assertion is proved similarly.
<br>
[Contrast this with $\mathbb{1}_{[a, b]}$, which was discussed in the notes.]