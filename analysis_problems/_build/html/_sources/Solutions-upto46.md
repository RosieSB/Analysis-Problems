(sol)=
# Solutions
Complete up to Q26, excluding some homework questions. 

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

[5.](5) The first part follows by using the sequential criterion for a limit of a function, and then applying the result of [P4 (iii)](#P4)..
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

(8sol)=
[8.](8) *(Homework 2 question).* 
   
(i) We are given $f:\mathbb{R}\to\mathbb{R}$; $f(x) = \begin{cases} 1 -x & \text{if }x < 1\\ x^{2}& \text{if }x \geq 1. \end{cases}$

For $a\neq 1$, the left and right limits exist and are both equal to $f(a)$, using the algebra of limits. The only point at which left and right limits disagree is $a = 1$, with

$$
\lim_{x \rightarrow 1^-}f(x) = 0, \; \text{ and } \; \lim_{x \rightarrow 1^+}f(x) = 1.
$$

To prove the left limit, let $\varepsilon>0$. For $x<1$, $f(x)=1-x$. Therefore, if $-\varepsilon<x-1<0$, we have $0<1-x<\varepsilon$, and hence $|f(x)|=|1-x|<\varepsilon$.

For the right limit: We know that if $x>1$, $f(x)=x^2$. Given $\varepsilon>0$, we seek $\delta>0$ such that if $0<x<\delta$, then $|f(x)-1|<\varepsilon$. Now,

$$
|f(x)-1|=|x^2-1|=|x+1|\cdot|x+1|.
$$

We can bound the $|x+1|$ factor above by $3$ provided we choose a $\delta$ that is at most $1$. Indeed: if $0<x-1<1$, then $2<x+1<3$, so $|x+1|<3$.  

We choose $\delta=\min\left\{1,\frac{\varepsilon}{3}\right\}$. Then, for $0<x-1<\delta$, we have $0<x-1<1$ and $0<|x-1|<\frac{\varepsilon}{3}$. So,

$$
|f(x)-1|=|x+1|\cdot|x-1| < 3\cdot\frac{\varepsilon}{3}=\varepsilon.
$$

````{note}
We could have also used algebra of limits to prove/evaluate the left- and right-limits here. For example, to show $\lim_{x\rightarrow 1^-}f(x)=1$, apply algebra of limits to the function $x^2$ (domain $\mathbb{R}$). This tells us that $\lim_{x\rightarrow 1}x^2=1$. Therefore, by Proposition 2.1, $\lim_{x\rightarrow 1^-}x^2=1$. But then, since $f(x)=x^2$ for all $x<1$, we must have that $\lim_{x\rightarrow 1^-}f(x)=\lim_{x\rightarrow 1^-}x^2=1$.
````

(ii) Consider $g:\mathbb{R}\to\mathbb{R}$, $g(x) = [x] = \left\{\begin{array}{cl} \lfloor x\rfloor & \text{ if } x\geq 0 \\ \lceil x \rceil & \text{ if } x<0 \end{array}\right.$. 

A quick think about how $[x]$ behaves for positive and negative $x$ gives the graph {numref}`intx`.

```{figure} ../analysis_problems/figs/[x].png
---
width: 400px
name: intx
---
Graph of the function $g:\mathbb{R}\to\mathbb{R}$; $g(x)=[x]$ (Problem 8).
```

In this case, left and right limits disagree at every $n \in \mathbb{Z}\setminus\{0\}$. In fact, if $n\in\mathbb{N}$, then {numref}`intx` suggests that 

$$
\lim_{x\rightarrow n^+}[x]=n, \;\lim_{x\rightarrow n^-}[x]=n-1, \; \lim_{x\rightarrow -n^+}[x]= -n+1, \text{ and } \lim_{x\rightarrow -n^-}[x]=-n.
$$ 

At every other real number, the left and right limits exist and are both equal to the value of the function there.

Here some proofs: 

- To prove $\lim_{x \rightarrow n^+}[x] = n$: Note that if $0<x-n<\frac{1}{2}$, we have $[x]=n$, and so $|[x]-n|=0$. In particular, if $\varepsilon>0$, then $0<x-n<\frac{1}{2}$ implies $|[x]-n|<\varepsilon$.

- To prove $\lim_{x\rightarrow n^-}[x]=n-1$: By the same principle, if $-\frac{1}{2}<x-n<0$, then $[x]=n-1$, and so $|[x]-(n-1)|=0$. In particular, for all $\varepsilon>0$, we have that $-\frac{1}{2}<x-n<0$ implies $|[x]-(n-1)|<\varepsilon$.

- The proofs of $\lim_{x\rightarrow -n^+}[x]= -n+1$ and $\lim_{x\rightarrow -n^-}[x]=-n$ are very similar --- or you could just note that $[-x]=-[x]$ and apply algebra of limits.

(iii) We are given $h:\mathbb{R}\to\mathbb{R}$, $h(x) =3 - 5\mathbb{1}_{(0, 1]}(x) + 7\mathbb{1}_{(1, 2]}(x)$. Again, it helps to draw a graph first --- see {numref}`8iii`.


```{figure} ../analysis_problems/figs/8iii.png
---
width: 500px
name: 8iii
---
Graph of the function $h=3 - 5\mathbb{1}_{(0, 1]} + 7\mathbb{1}_{(1, 2]}$ (Problem 8).
```

Here, left and right limits disagree at $x = 0, 1$ and $2$. We have

$$
\lim_{x \rightarrow 0^-}h(x) = 3, \hspace{1em} \lim_{x \rightarrow 1^-}h(x) = -2, \hspace{1em}  \lim_{x \rightarrow 2^-}h(x) = 10,
$$

$$
\lim_{x \rightarrow 0^+}h(x) = -2, \hspace{1em} \lim_{x \rightarrow 1^+}h(x) = 10, \hspace{1em}  \lim_{x \rightarrow 2^+}h(x) = 3.
$$

To prove $\lim_{x \rightarrow 0^-}h(x) = 3$ using [Definition 2.4](https://rosiesb.github.io/Analysis-Notes/2LoF.html#marg), note that for any $x<0$, $h(x)=3$ and so $|h(x)-3|=0$. So for any $\varepsilon>0$ and any choice of $\delta>0$, we have that $-\delta<x<0$ implies $|h(x)-3|=0<\varepsilon$. 

The proof of $\lim_{x \rightarrow 1^-}h(x) = -2$ is very similar: let $\varepsilon>0$, and note that if $-\frac{1}{2}<x-1<0$, then $\frac{1}{2}<x<1$, and so $h(x)=-2$. But then, $|h(x)-(-2)|=0<\varepsilon$.

The proof of $\lim_{x \rightarrow 2^-}h(x) = 10$ is exactly the same, just take $-\frac{1}{2}<x-2<0$ and note $h(x)=10$, instead.

The right limit proofs are similar. 

---

(9sol)=
[9.](9) *(Homework 2 question).* The largest subset of $\mathbb{R}$ for which the formula $f(x)=\sin\left(\frac{1}{x}\right)$ makes sense is $A = \mathbb{R} \setminus \{0\}$.
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

for all $n\in\mathbb{N}$. Since $\displaystyle\lim_{n\to \infty} x_n=0$, we have $ \displaystyle\lim_{n\to \infty} |x_n| =0$. Therefore, by the squeeze theorem, $\displaystyle\lim_{n\rightarrow 0}x_n\sin\left(\frac{1}{x_n}\right) = 0$.
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

[14.](14) If $(x_{n})$ is any sequence that converges to $a$, we know that $f(x_n)$ converges to $f(a)$ as $f$ is continuous at $a$, and we need to show that $(|f|(x_n))$ converges to $|f|(a)$.
<br>
By Corollary 1.1, if $(x_{n})$ is any sequence that converges to $a$,
\begin{align*}
0 \leq ||f|(a)| -|f|(x_{n})| &= ||f(a) - |f(x_{n})|| \\
&\leq |f(a) - f(x_{n})| \rightarrow 0~\mbox{as}~n \rightarrow \infty, 
\end{align*}
as $f$ is continuous. So by the squeeze theorem, $\lim_{n\rightarrow\infty} |f|(x_{n}) = |f|(a)$, and so $f$ is continuous at $a$.

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

(18sol)=
[18.](18) *(Homework 3 question).*
   
(i) We are given $f:\mathbb{R} \setminus \{0\} \rightarrow \mathbb{R}$; $f(x) = \frac{(1 + x)^{2} - 1}{x}$, a continuous function (since it is a rational function).

For $x \neq 0, f(x) = x+2$, and so $\lim_{x \rightarrow 0}f(x) = 2$, by algebra of limits. Therefore the required continuous extension of $f$ is 

$$
\tilde{f}:\mathbb{R}\to\mathbb{R}; \; \tilde{f}(x) = \left\{\begin{array}{c c} \displaystyle\frac{(1 + x)^{2} - 1}{x} & ~\mbox{if}~x \neq 0\\ 
& \\
2 & ~\mbox{if}~x = 0. \end{array} \right.
$$

Or, put more simply: $\tilde{f}(x)=x+2$ for all $x\in\mathbb{R}$. 

(ii) Let now $f(x) = \frac{(x-2)(x^{2} + 2x + 4)}{(x-2)(x+2)}$. The largest possible domain for $f$ is $A=\mathbb{R} \setminus \{-2, 2\}$ (the set where the denominator is non-zero). For $x \neq 2, -2$,

$$
f(x) = \frac{(x-2)(x^{2} + 2x + 4)}{(x-2)(x+2)}=\frac{x^{2} + 2x + 4}{x + 2}=x+\frac{4}{x+2}.
$$

This is a rational function, and hence continuous everywhere the denominator is non-zero by [Theorem 3.2(iv)](https://rosiesb.github.io/Analysis-Notes/3Cty.html#AOL3).

We claim that $\lim_{x \rightarrow -2}f(x)$ does not exist. To see this, consider the sequence $(x_{n})$ given by $x_n=-2 + \frac{1}{n}$. Then,

$$
f(x_{n}) = -2 + \frac{1}{n}+4n \rightarrow -\infty \; \text{ as } \; n \rightarrow \infty.
$$

Thus $f$ has no continuous extension to the point $x =-2$.

[**Note:** Here, we have proven that $f(x)$ does not converge as $x\rightarrow-2$. We have *not* proven that $\lim_{x\rightarrow -2} f(x)=-\infty$. To show this, we would have had to choose an arbitrary sequence $(x_n)$ in $A$ with limit $-2$ and proven that for this **general** sequence, $\lim_{n\rightarrow\infty}f(x_n)=-\infty$ (or constructed an $K-\delta$ argument using [Definition 2.3](https://rosiesb.github.io/Analysis-Notes/2LoF.html#div+-infty)). ]


On the other hand, $f$ does have a continuous extension to $\mathbb{R}\setminus\{-2\}$. Indeed, by algebra of limits we have

$$
\lim_{x \rightarrow 2}f(x) = \lim_{x\rightarrow 2}\left(x+\frac{4}{x+2}\right) = 3,
$$

and so $f$ has a continuous extension

$$
\tilde{f}:\mathbb{R} \setminus \{-2\}\to\mathbb{R}; \hspace{1em} \tilde{f}(x) = x+\frac{4}{x+2}.
$$

We can see this behaviour in the graph of the function ({numref}`q18`)

```{figure} ../analysis_problems/figs/(x2+2x+4),(x+2).png
---
width: 500px
name: q18
---
Graph of the function $\tilde{f}:\mathbb{R}\setminus\{-2\}\to\mathbb{R}$; $f(x)=x+\frac{4}{x+2}$ (Problem 18).
```


---

(19sol)=
[19.](19) *(Homework 2 question).* Assume $g$ is continuous and $g(a) > 0$. Then for all $\varepsilon>0$ there exists $\delta>0$ such that for all $x\in\mathbb{R}$, $|x-a|<\delta$ implies $|g(x)-g(a)|<\varepsilon$. Let $\varepsilon=\frac{g(a)}{2}$. Then for some $\delta>0$, we have $|g(x)-g(a)|<\frac{g(a)}{2}$. But then $\frac{g(a)}{2}<g(x)<\frac{3g(a)}{2}$, and in particular, $g(x)>\frac{g(a)}{2}>0$.

**Alternate solution using sequences:**<br>
Suppose, for a contradiction, that  there is no  $\delta > 0$ such that $g(x) > 0$  for all $ x \in (a - \delta, a + \delta)$. Then, in particular, for all $n\in\mathbb{N}$ there exists $x_{n} \in \left(a - \frac{1}{n}, a + \frac{1}{n}\right)$ such that $g(x_{n}) \leq 0$. By the squeeze theorem, we have $\lim_{n\rightarrow\infty} x_{n} = a$. So, by continuity of $g$ at $a$, we have $\lim_{n\rightarrow\infty} g(x_{n})$ exists and equals $g(a)$. But $g(x_n)\leq 0$ for all $n\in\mathbb{N}$, and so

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

(22sol)=
[22.](22) *(Homework 2 question).* 
Recall from [Example 3.10](https://rosiesb.github.io/Analysis-Notes/3Cty.html#eg:dirichlet2) in the notes that Dirichlet's "other" function (AKA Thomae's function) is defined  $g:[0, 1)\rightarrow \mathbb{R}$ defined by

$$
g(x) =\begin{cases}
	1 &\text{if $x = 0$},\\
	\displaystyle\frac{1}{n}& \text{if $x = m/n \in \mathbb{Q}\cap[0,1)$, and $\text{gcd}(m,n)=1$.}\\
	0&\text{if $x \in [0,1)\setminus \mathbb{Q}$}.
\end{cases}
$$

Suppose that $a \in \mathbb{Q}\cap[0,1)$. Then $g(a)=\frac{1}{k}$, for some fixed $k\in\mathbb{N}$. Every real number is the limit of a sequence of irrational numbers[^note]. Therefore, there is a sequence $(x_{n})$ of irrational numbers that converges to $a$. Since $a\in[0,1)$, we may assume (removing some initial terms if necessary) that $x_n\in[0,1)\setminus\mathbb{Q}$ for all $n\in\mathbb{N}$. 

[^note]:This, and other related properties of (ir)rational numbers, was a focus of study in MAS107/117 Semester 2. 

If $g$ was continuous at $a$, we would have $\lim_{n\rightarrow\infty}g(x_n)=g(a)$. But in fact, $g(x_n)=0$ for all $n\in\mathbb{N}$, so $\lim_{n\rightarrow\infty}g(x_n)=0\neq \frac{1}{k}=g(a)$.

It follows that $g$ is discontinuous at every rational point of its domain.



---

[23.](23) The function $\mathbb{1}_{(a, b)}$ is left continuous at $a$ (but not right continuous), and right continuous at $b$ (but not left continuous).

To prove the left continuity at $a$, let $(x_{n})$ be any sequence in $\mathbb{R}$ which converges to $a$ with $x_{n} < a$ for all $n\in\mathbb{N}$. Then $\lim_{n\rightarrow\infty} \mathbb{1}_{(a, b)}(x_{n}) = 0 = \mathbb{1}_{(a, b)}(a).$ On the other hand to see that it is not right continuous at $a$, let $(y_{n})$ be any sequence in $\mathbb{R}$ which converges to $a$ with $a < y_{n} < b$ for all $n\in\mathbb{N}$. Then
$ \lim_{n\rightarrow\infty} \mathbb{1}_{(a, b)}(y_{n}) = 1 \neq \mathbb{1}_{(a, b)}(a). $ The other assertion is proved similarly.
<br>
[Contrast this with $\mathbb{1}_{[a, b]}$, which was discussed in the notes.]

---

[24.](24) Since $f$ is continuous on $[a, b]$, so is $g$. We have $g(a) = f(a) - \gamma < 0$ and $g(b) = f(b) - \gamma > 0$. Hence by [Proposition 3.1](https://rosiesb.github.io/Analysis-Notes/3Cty.html#ivt-sc), there exists $c \in (a, b)$ with $g(c) = 0$, i.e. $f(c) = \gamma$, as was required.

---

(25sol)=
[25.](25) 
*(Homework 3 question).*
Let $a,b\in\mathbb{R}$, $a<b$, and suppose $f:[a,b] \rightarrow (a,b)$ is a continuous function.

The question suggests we consider a function of the form $g(x) = f(x) - $ (*something*), and apply the intermediate value theorem. Since we seek a point $c\in(a,b)$ for which $f(c)=c$, we try $g(x)=f(x)-x$. This is a continuous function on $[a,b]$, since $f$ is. Moreover, any zero of $g$ will be a fixed point of $f$.

Since the range of $f$ is contained in $(a, b)$, we have $a<f(x)<b$ for all $x\in[a,b]$. In particular, $f(a) > a$ and $f(b) < b$, and so $g(a) = f(a) - a > 0$ and $g(b) = f(b) - b < 0$. In other words, $0\in(g(a),g(b))$. By the intermediate value theorem (or by [Proposition 3.1](https://rosiesb.github.io/Analysis-Notes/3Cty.html#ivt-sc), the special case where $\gamma=0$), there exists $c \in (a, b)$ such that $g(c) = 0$, i.e., such that $f(c) = c$.

For the counter--example, consider $f:(0,1)\to(0,1)$, $f(x) = x^2$. It is continuous on $(0, 1)$ but there is no $c \in (0, 1)$ for which $c^2 = c$.

---

[26.](26) Define $\gamma = \inf_{x \in [a, b]}f(x)$ and assume that it is not attained, so $\gamma < f(x)$ for all $x \in [a,b]$. Then consider the function 

$$
h:[a,b]\to \mathbb{R}; \; h(x) = \displaystyle\frac{1}{f(x) - \gamma}.
$$

This is continuous, and hence bounded on $[a, b]$. So there exists $K \geq 0$ such that $|h(x)| \leq K$ for all $x \in [a, b]$. Since $\gamma=\inf_{x\in[a,b]}f(x)$, given any $\varepsilon > 0$, there exists $x \in [a, b]$ such that $f(x) < \gamma + \varepsilon$. Now take $\varepsilon = \frac{1}{K}$ to deduce that $h(x) > K$, which yields the required contradiction.

[**Alternatively:** We proved in lectures that continuous functions on $[a,b]$ are bounded and attain a maximum value. Since $f$ is continuous on $[a,b]$, so is $-f$, and hence $-f$ attains a maximum: say $k\in[a,b]$ is such that $-f(k)=\sup_{x\in[a,b]}(-f(x))$. Then, using a standard property[^infsup] of sup's and inf's,

$$
f(k)=-\sup_{x\in[a,b]}(-f(x)) = \inf_{x\in[a,b]}f(x).
$$

In other words, $f$ attains its minimum.]

[^infsup]: More generally, for any bounded set $A\subseteq\mathbb{R}$, $\sup(A)=-\inf(-A)$ and $\inf(A)=-\sup(-A)$, where we write $-A:=\{-x:x\in A\}$ (standard notation). For a proof, see Theorem 2.7 on page 33 of the [MAS107 Sem 2 notes](https://drive.google.com/file/d/1r9b3XqA1u-dzkbnGjPPBxIyj6YF1TE_C/view?usp=sharing).

---

[27.](27) (i) Let $f:\mathbb{R}\to\mathbb{Z}$ be continuous, and suppose $f$ is not a constant function.

Then there must be $a,b\in\mathbb{R}$ such that $a\neq b$ and $f(a)\neq f(b)$. Without loss of generality, assume $a<b$. 

Then $f$ is continuous on $[a,b]$, and since $f(a)\neq f(b)$, $f$ is also non-constant on $[a,b]$. By [Corollary 3.3](https://rosiesb.github.io/Analysis-Notes/3Cty.html#interval), $f([a,b]])=[m,M]$. This contradicts $f$ having codeomain $\mathbb{Z}$.

It follows that $f$ must be a constant function.

(ii) Argue as in (i), using the fact that between any two rational numbers, we can find an irrational number.

---

[28.](28) By algebra of limits, $\frac{1}{f}$ is continuous on $[0, 1]$ and so is bounded by Theorem 3.5.

---

[29.](29) 
<br>
If $f$ is continuous on $[0, 1]$, then it is bounded by Theorem 3.5, and so there exists $L \geq 0$ such that $|f(x)| \leq L$ for all $x \in [0, 1]$. Hence the range of $f$ is a subset of  $[-L, L]$ and cannot be all of $\mathbb{R}$.

---

[30.](30) Since $(x_{n})$ is bounded, by the Bolzano--Weierstrass theorem it has a convergent subsequence $(x_{n_{k}})$. Let $c=\lim_{k \rightarrow \infty}x_{n_{k}}$ and note that $c \in [0, 1]$, since $x_{n_k}\in[0,1]$ for all $k$.
<br>
A straight-forward induction argument shows that $f(x_{n_{k}}) \leq r^{n_{k}-1}f(x_{n_{1}})$ for all $k\in\mathbb{N}$. But then, since the range of $f$ is contained in $[0,1]$, we have

$$
0 \leq f(x_{n_{k}}) \leq r^{n_{k}-1}
$$

for all $k\in\mathbb{N}$. Since $r < 1$, $\lim_{k\to\infty} r^{n_k-1} =0$. By the squeeze theorem, $ \lim_{k \rightarrow \infty}f(x_{n_{k}}) = 0$ and by continuity of $f$ at $c$, $f(c) = \lim_{k \rightarrow \infty}f(x_{n_{k}})$, so $f(c)=0$.

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

(ch4sol)=
## Differentiation

[37.](37) This is Definition 2.2 in the notes:
<br>
The function $f$ has limit $l$ at the point $a$ if for every $\varepsilon>0$ there exists $\delta>0$ such that for all $x\in X$, 

$$
0<|x-a|<\delta \; \text{ implies } \; |f(x)-l|<\varepsilon.
$$

We write $\lim_{x\to a}f(x)=l$.

---

[38.](38)

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

[41.](41) To appear (Homework 5 question)  

---

[42.](42) Let  $f:\mathbb{R}\to \mathbb{R}$ given by 

$$
f(x) = \begin{cases} x^2\sin\left(\frac{1}{x}\right) & \text{if }x \neq 0,\\ 0 & \text{if }x = 0.\end{cases}
$$

Using the product and chain rules and standard derivatives, for $x \neq 0$, $f$ is differentiable at $x$ with $f'(x) = 2x\sin\left(\frac{1}{x}\right) - \cos\left(\frac{1}{x}\right)$. At $x = 0,$

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

