(sol)=
# Solutions

## Preliminary problems

P1.
The correct statements are (ii) and (v).

In statement (iv), the quantifiers $\forall$ and $\exists$ are the wrong way round, while in (i) they are missing altogether. Statement (iii) asserts that last part, $|x_n-l|<\varepsilon$ $\forall n\geq N$, should hold for all $\varepsilon$ and for all $N$ --- so again, there is an issue with the quantifiers.

Bonus exercise: prove that (iv) holds if and only if $(x_n)$ is the constant sequence $x_n=l$ for all $n\in\mathbb{N}$.


P2. (HW1 QUESTION)

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

P3. HW1 QUESTION

The Bolzano--Weierstrass theorem states that every bounded sequence has a convergent subsequence. Its proof combines the following two results:

    - The monotone convergence theorem (Theorem 3.10 in the MAS107 notes), which states that bounded monotone sequences must converge. <br> More specifically, every monotone increasing sequence that is bounded above converges to its supremum, and every monotone decreasing sequence bounded below converges to its infimum.

    - Theorem 3.13 from MAS107: Every sequence has a monotone subsequence.

Proof of Bolzano--Weierstrass: <br>

If $(x_n)$ is a bounded sequence, then it has a monotone subsequence, $(x_{n_k})$, by Theorem 3.13. This subsequence must also be bounded since $(x_n)$ is bounded, and hence it converges by the monotone convergence theorem.


P4.
   
    (i) Let $a, b \geq 0$. Then,

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
    We use a trick similar to the proof of Corollary~\iflatexml 0.2.6, \else[cor:tri](#cor:tri), \fi and write
    
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
    
    Equation ([eq:sqrta-sqrtb](#eq:sqrta-sqrtb)) now follows by subtracting $\sqrt{|b|}$ from both sides.
    
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

P5. When it exists, the supremum of a set $A\subseteq\mathbb{R}$ is defined to be the unique number $\alpha\in\mathbb{R}$ such that
    
    - $\alpha$ is an upper bound for $A$, and
    
    - if $M$ is any other upper bound for $A$, then $\alpha\leq M$.

We write $\sup A$ for the supremum of $A$, when it exists.

The definition of the infimum is similar: when it exists, the infimum of $A$ is the unique number $\beta\in\mathbb{R}$ such that    

    (i) $\beta$ is a lower bound for $A$, and

    (ii) if $L$ is any other lower bound for $A$, then $\alpha\geq L$.
    <br>
    We write $\inf A$ for the infimum of $A$, when it exists.
    <br>
    The axiom of completeness for the real numbers says that every non-empty bounded above subset of $\mathbb{R}$ has a supremum. Equivalently, it says that every non-empty bounded below subset of $\mathbb{R}$ has an infimum.

    For more details, see page 32 of your Semester 2 MAS107 notes.


P6.
    (i) $\displaystyle\sup\left\{\frac{m}{n}:m,n\in\mathbb{N} \text{ s.t } m<n\right\}=1$, $\displaystyle\inf\left\{\frac{m}{n}:m,n\in\mathbb{N} \text{ s.t } m<n\right\}=0$.
    
    (ii) $\displaystyle\sup\left\{\frac{(-1)^m}{n}:m,n\in\mathbb{N} \text{ s.t } m<n\right\}=\frac{1}{3}$, $\displaystyle\inf\left\{\frac{(-1)^m}{n}:m,n\in\mathbb{N} \text{ s.t } m<n\right\}=-\frac{1}{2}$.

    (iii) $\displaystyle\sup\left\{\frac{n}{3n + 1} :n\in\mathbb{N}\right\}=\frac{1}{3}$, $\displaystyle\inf\left\{\frac{n}{3n + 1} :n\in\mathbb{N}\right\}=\frac{1}{4}$.

P7.
    (i) This is false --- for a counter-example, take any singleton set. Then $\sup A=\inf A=1$.

    A correct version of the statement would be $\inf A \leq \sup A$.
    
    (ii) True. The analogous statement for $\sup$ was called the characteristic property of the supremum in your MAS107 lecture notes --- see Lemma 2.8 on page 36.
    
    (iii) True. Since $\sup B$ is an upper bound for $B$, and $A$ is a subset of $B$, $\sup B$ must be an upper bound for $A$. But $\sup A$ is a the least upper bound for $A$, hence $\sup A\leq \sup B$.
    <br>The analogous property for $\inf$ is that $\inf A\geq\inf B$ whenever $A\subseteq B$.
    
    (iv) False. For a counter-example, take $B=\left\{\frac{1}{n}:n\in\mathbb{N}\right\}$, for which $\inf B=0$.
    
    (v) True. Let $s=\max\{\sup A,\sup B\}$. Then $s\geq \sup A$ and $s\geq \sup B$, so $s$ is an upper bound for both $A$ and $B$. Therefore, $s$ is an upper bound for $A\cup B$. But $\sup(A\cup B)$ is the least upper bound of $A\cup B$, and so $s\geq\sup(A\cup B)$. Also, since $A$ and $B$ are both subsets of $A\cup B$, we have by statement (iii) that $s=\max\{\sup A,\sup B)\leq\sup(A\cup B)$. Hence $\max\{\sup A,\sup B)=\sup(A\cup B)$.

## 1.1. Limits of functions

One has to identify the real numbers where the given formula does not make sense, usually because of a zero in a denominator somewhere, and exclude them.

    (i) $A=\mathbb{R} \setminus \{0, -1\}$.

    (ii) $f_{2}(x) = \displaystyle\frac{(x-1)(x+4)}{(x-1)(x+2)(x+3)}$, so $A=\mathbb{R} \setminus \{1, -2, -3\}$.
    
    (iii) $f_{3}(x) = \displaystyle\frac{x+4}{(x+2)(x+3)}$, so $A=\mathbb{R} \setminus \{-2, -3\}$.
    
    (iv) $A=\mathbb{R} \setminus \{1\}$.
    
    (v) $A=\mathbb{R} \setminus \{0\}$.
2. HW1 QUESTION
   
    (i) $L=[0,1]\cup[2,3]$.
   
    (ii) $L=\emptyset$.  (All convergent sequences in $\mathbb{Z}$ are eventually constant.)
   
    (iii) $L=\mathbb{R}$.
   
    (iv) $L=[0,1]$
   
    (v) $L=\{0\}$

3. We had $A= \mathbb{R} \setminus \{1, -2, -3\}$, and $f_2:A\to\mathbb{R}$; $\displaystyle f_{2}(x)= \frac{(x + 4)}{(x + 2)(x + 3)}$.

Let $(x_n)$ be a sequence in $A$ converging to $1$. Then, using algebra of limits for real sequences,

$$
\lim_{n\to\infty}f_2(x_n)= \lim_{n\to\infty} \frac{(x_n + 4)}{(x_n + 2)(x_n + 3)} =  \frac{(1 + 4)}{(1 + 2)(1 + 3)} = \frac{5}{12},
$$

where the last equality is using algebra of limits. So $\displaystyle\lim_{x \rightarrow 1}f_{2}(x) = \frac{5}{12}$.

Let $x_n=-2 + \frac{1}{n}$, so that $(x_n)$ is a sequence in $A$ converging to $-2$. Then we see that $(f_2(x_n))$ diverges to $+\infty$ and so $\lim_{x \rightarrow -2}f_{2}(x)$  does not exist.

Similarly, considering $x_n=-3 + \frac{1}{n}$,  we see that $\lim_{x \rightarrow -3}f_{2}(x)$ does not exist.

4. The first part follows by using the definition of the limit of a function in terms of limits of sequences, and then applying the result of Problem~[q:25](#q:25) (iii).
<br>
To be precise let $(x_{n})$ be any sequence in $\mathbb{R} \setminus \{a\}$ that converges to $a$. Then since we are given that $\lim_{x \rightarrow a} f(x) = l$, we must have that $\lim_{n\rightarrow\infty} f(x_{n}) = l$. But then by Problem~[q:25](#q:25) (iii), we have $\lim_{n\rightarrow\infty} \sqrt{f(x_{n}}) = \sqrt{l}$. So by definition of the limit of a function, $\lim_{x \rightarrow a} \sqrt{f(x)} = \sqrt{l}$.
<br>
Using algebra of limits,  $\lim_{x \rightarrow 1}\displaystyle\frac{x+1}{x^{2}}=\frac{1+1}{1^2}=2$ and
then by the first part $\lim_{x \rightarrow 1}\sqrt{\displaystyle\frac{x+1}{x^{2}}} = \sqrt{2}$.

5. Let $f:A\to \mathbb{R}$ and suppose that $\lim_{x \rightarrow a} f(x) = l$ and $\lim_{x \rightarrow a} f(x) = l'$. Then given any sequence $(x_{n})$ in $A \setminus \{a\}$ that converges to $a$, we have $\lim_{n\rightarrow\infty} f(x_{n}) = l$ and also $\lim_{n\rightarrow\infty} f(x_{n}) = l'$. But then $l = l'$, by uniqueness of limits.

6. HW2 QUESTION
<br>
When $x > 0, \displaystyle\frac{|x|}{x} = \displaystyle\frac{x}{|x|} = \displaystyle\frac{x}{x} = 1 = \sign(x)$,
<br>
when $x < 0, \displaystyle\frac{|x|}{x} = \displaystyle\frac{x}{|x|} = -\displaystyle\frac{x}{x} = -1 = \sign(x)$.
<br>
The left limit is $\displaystyle\lim_{x \rightarrow 0^-} \sign(x) = -1$, since for any sequence $(x_n)$ approaching $0$ from the left, we have $\sign(x) = -1$ for all $n$.
<br>
Similarly, the right limit is $\displaystyle\lim_{x \rightarrow 0^+} \sign(x) = 1$,  since for any sequence $(x_n)$ approaching $0$ from the right, we have $\sign(x) = 1$ for all $n$.
<br>
Since the left and right limits are different, $\displaystyle\lim_{x \rightarrow 0}\sign(x)$ does not exist.

7. HW2 QUESTION
   
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

8. The largest subset of $\mathbb{R}$ for which the formula $f(x)=\sin\left(\frac{1}{x}\right)$ makes sense is $A = \mathbb{R} \setminus \{0\}$.
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
Of course, we could have chosen any values of $\theta$ we liked, and constructed a sequence $(x_n)$ with limit $0$ for which $\lim_{n\rightarrow\infty}f(x_n)$ is equal to any real number we liked in the interval $[-1,1]$. The graph of this function below may give some intuition as to how this is possible.

![](figs/sin(1,x))
Graph of the function $f:\mathbb{R}\to\mathbb{R}$; $f(x)=\sin\left(\frac{1}{x}\right)$.

9. The largest subset of $\mathbb{R}$ for which the formula $f(x)=x\sin\left(\frac{1}{x}\right)$ makes sense is $A = \mathbb{R} \setminus \{0\}$.
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
You should contrast the picture below with that for the previous question.

![](figs/xsin(1,x))
Graph of the function $f:\mathbb{R}\to\mathbb{R}$; $f(x)=x\sin\left(\frac{1}{x}\right)$.


10. We'll just do $\displaystyle\lim_{x \rightarrow \infty}f(x)$ here, as $\displaystyle\lim_{x \rightarrow -\infty}f(x)$ is so similar.
    
    (i) Let $X\subset\mathbb{R}$ and $f:X\to\mathbb{R}$. We say that $\lim_{x \rightarrow \infty}f(x) = l$ if whenever $(x_{n})$ is a sequence that diverges to infinity, with $x_{n}\in X$ for all $n\in\mathbb{N}$, then $\lim_{x \rightarrow \infty}f(x_{n}) = l$.
    
    (ii) The analogue of the $(\varepsilon- \delta)$ criterion is $(\varepsilon-K)$: given any $\varepsilon > 0$, there exists $K > 0$ such that if $x > K$ then $|f(x) -l| < \varepsilon$.
    <br>
    For the proof, suppose the $(\varepsilon- K)$ criterion holds and $\lim_{n\rightarrow\infty} x_{n} = \infty$. Then given any $L > 0$, there exists $N\in\mathbb{N}$ such that if $n\geq N$, we have $x_{n} > L$. Now take $L$ to be $K$ from the criterion and we get that for all $n\geq N, |f(x_{n}) - l| < \varepsilon$. Hence $\lim_{x \rightarrow \infty}f(x_{n}) = l$, as required.
    <br>
    For the converse, we again imitate the proof of Theorem \iflatexml 1.2.6 \else [ed](#ed) \fi. So suppose the $(\varepsilon-K)$ criterion does not hold.
    This time choose successively $K = 1, 2, \ldots$ and construct $x_{n}$ in the domain $X$ of $f$ such that $x_{n} > n$, and $|f(x_{n}) - l| \geq \varepsilon$ for each $n\in\mathbb{N}$. So $f$ does not converge to $l$ as $x\to\infty$.
    
    (iii) Given any $\varepsilon > 0$, choose $K = \frac{1}{\varepsilon}$. Then $x > K \Rightarrow \frac{1}{x} < \varepsilon$, and so $\lim_{x\to\infty} \frac{1}{x}=0$. The case where $x\to-\infty$ is similar.

11.
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

## 1.2. Continuity
12. For each of (i) to (v), the function is continuous at each point of its domain. For (i), (ii) and (iii), we have rational functions, which are continuous on all points of $A$ (which is the subset of $\mathbb{R}$ where the denominator is non-zero). For (iv) and (v), we have compositions of rational functions with the exponential and cosine functions, which are continuous on the whole of $\mathbb{R}$. Again, the functions are continuous on all points of $A$ (which is the subset of $\mathbb{R}$ where the denominator of the rational function is non-zero).

13. If $(x_{n})$ is any sequence that converges to $a$, we know that $f(x_n)$ converges to $f(a)$ as $f$ is continuous at $a$, and
we need to show that $(|f|(x_n))$ converges to $|f|(a)$.
<br>
By Corollary 0.2.6, if $(x_{n})$ is any sequence that converges to $a$,
\begin{align*}
0 \leq ||f|(a)| -|f|(x_{n})| &= ||f(a) - |f(x_{n})|| \\
&\leq |f(a) - f(x_{n})| \rightarrow 0~\mbox{as}~n \rightarrow \infty, 
\end{align*}
as $f$ is continuous. So by the sandwich rule, $\lim_{n\rightarrow\infty} |f|(x_{n}) = |f|(a)$, and so $f$ is continuous at $a$.

14. Let $(x_{n})$ be a sequence in $A$ that converges to $a$. Since $f$ is continuous at $a$ we have $\lim_{n\rightarrow\infty} f(x_{n}) = f(a)$. And then, since $g$ is continuous at $f(a)$, we have $\lim_{n\rightarrow\infty} g(f(x_{n})) = g(f(a))$, and the result follows.

15. $f \circ g:\mathbb{R}\to \mathbb{R}$ given by $(f \circ g)(x) = \frac{1}{1  + x^{2}}$. It is continuous on $\mathbb{R}$ by Theorem 2.1.5(iv).
<br>
$g \circ f:\mathbb{R} \setminus \{0\} \to \mathbb{R} \setminus \{0\}$ given by $(g \circ f)(x) = {1  + \frac{1}{x^2}}$. It is continuous on $\mathbb{R} \setminus \{0\}$ by Theorem 2.1.5(iv).

16.
    (i) Continuous on $\mathbb{R} \setminus \{1\}$. Jump discontinuity at $1$ with $J_{f}(1) = 1$.
    (ii) Continuous on $\mathbb{R} \setminus \mathbb{Z}$. Jump discontinuity at $n$ with $J_{g}(n) = 1$ for all $n\in\mathbb{Z}_+$.
    (iii) Continuous at $\mathbb{R} \setminus \{0,1,2\}$. Each of $0, 1, 2$ is a jump discontinuity and we have $J_{h}(0) =-5, J_{h}(1) = 12, J_{h}(2) = -7.$

17. HW2 question
   
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

    This is a rational function, and hence continuous everywhere the denominator is non-zero by Theorem 2.1.5(iv).
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

    We can see this behaviour in the graph of the function:

    ![](figs/(x%5E2+2x+4),(x+2))
    Graph of the function $\tilde{f}:\mathbb{R}\setminus\{-2\}\to\mathbb{R}$; $f(x)=\frac{x^2+2x+4}{x+2}$.

18. Assume $g$ is continuous and $g(a) > 0$. Suppose, for a contradiction, that  there is no  $\delta > 0$ such that $g(x) > 0$  for all $ x \in (a - \delta, a + \delta)$. Then, in particular, for all $n\in\mathbb{N}$ there exists $x_{n} \in \left(a - \frac{1}{n}, a + \frac{1}{n}\right)$ such that $g(x_{n}) \leq 0$. By the sandwich rule, we have $\lim_{n\rightarrow\infty} x_{n} = a$. So, by continuity of $g$ at $a$, we have $\lim_{n\rightarrow\infty} g(x_{n})$ exists and equals $g(a)$. But $g(x_n)\leq 0$ for all $n\in\mathbb{N}$, and so

$$
g(a)=\lim_{n\rightarrow\infty} g(x_{n}) \leq 0,
$$

which is a contradiction.

19.
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
    and continuity follows by Theorem  2.1.5(i) and (iii) and Problem~[q:56](#q:56).

    (ii) Check that for all $a, b \in \mathbb{R}$,
    
    $$
    \min\{a, b\} = \frac{1}{2}(a + b) - \frac{1}{2}|a - b|,
    $$
    
    and then argue as in (i).

    Alternatively, one could derive (ii) from (i) by using $\min\{f,g\} = - \max\{-f, -g\}$.

20.
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
    $$ and the result follows.
    
    (vi) We have already proved this for rational $x$, so suppose that $x$ is irrational. Then we can find a sequence $\left(\frac{p_{n}}{q_{n}}\right)$ of rational numbers that converges to $x$ (as we did in the solution to Example 4.2.4). Then using (iii), (v) and algebra of limits, we have
    
    $$
    f(x) = \lim_{n\rightarrow\infty} f\left(\frac{p_n}{q_n}\right) =   \lim_{n\rightarrow\infty} k \frac{p_n}{q_n}=k \lim_{n\rightarrow\infty} \frac{p_n}{q_n} = kx.
    $$

21. Suppose that $x \in \mathbb{Q}$. Then as in the solution to Example 4.2.4 we can find a sequence $(x_{n})$ of irrationals that converges to $x$ and then

$$
\lim_{n\rightarrow\infty} g(x_{n}) = 0 \neq g(x),
$$

and so $g$ is not continuous at $x$.

22. HW2 question
<br>
The function ${\bf 1}_{(a, b)}$ is left continuous at $a$ (but not right continuous), and right continuous at $b$ (but not left continuous).
To prove the left continuity at $a$, let $(x_{n})$ be any sequence in $\mathbb{R}$ which converges to $a$ with $x_{n} < a$ for all $n\in\mathbb{N}$. Then $\lim_{n\rightarrow\infty} {\bf 1}_{(a, b)}(x_{n}) = 0 = {\bf 1}_{(a, b)}(a).$ On the other hand to see that it is not right continuous at $a$, let $(y_{n})$ be any sequence in $\mathbb{R}$ which converges to $a$ with $a < y_{n} < b$ for all $n\in\mathbb{N}$. Then
$ \lim_{n\rightarrow\infty} {\bf 1}_{(a, b)}(y_{n}) = 1 \neq {\bf 1}_{(a, b)}(a). $ The other assertion is proved similarly.
<br>
[Contrast this with ${\bf 1}_{[a, b]}$, which was discussed in the notes.]

23. Since $f$ is continuous on $[a, b]$, so is $g$. We have $g(a) = f(a) - \gamma < 0$ and $g(b) = f(b) - \gamma > 0$. Hence by the intermediate value theorem (Theorem \iflatexml  2.3.1 \else [ivp](#ivp) \fi), there exists $c \in (a, b)$ with $g(c) = 0$, i.e. $f(c) = \gamma$, as was required.

24.
    (i) If $f$ is continuous on $\mathbb{R}$ it is continuous on $[a, b]$ for each $a < b$. If $f$ is not a constant, we must be able to find $a, b$ such that $f(a) \neq f(b)$. Now either $f(a) < f(b)$ or $f(a) > f(b)$. Assume the former (without loss of generality). Then there exists $m, n \in \mathbb{Z}$ with $m < n$ such that $f(a) = m$ and $f(b) = n$. Hence by Corollary~\iflatexml 2.3.2 \else [ivp2](#ivp2)\fi, there exists $c \in (a, b)$ so that $f(c) = m + \frac{1}{2} \notin\mathbb{Z}$, and that is the desired contradiction.
    (ii) Argue as in (i), using the fact that between any two rational numbers, we can find an irrational number.

25. HW3 question
<br>
*Something* is $x$. That is, define $g:[a,b]\to\mathbb{R}$ given by $g(x) = f(x) - x$. Then $g$ is continuous (because $f$ is and the function $h(x)=x$ is, and using algebra of limits). Since the range of $f$ is contained in $(a, b)$, we have $f(a) > a$ and $f(b) < b$, and so $g(a) = f(a) - a > 0$ and $g(b) = f(b) - b < 0$. So we can apply the intermediate value theorem to the function $g$ on $[a,b]$. This says that there exists $c \in (a, b)$ such that $g(c) = 0$, i.e. $f(c) = c$.
<br>
For the counter--example, consider $f(x) = x^2$. It is continuous on $(0, 1)$ but there is no $c \in (0, 1)$ for which $c^2 = c$.

26. Define $\gamma = \inf_{x \in [a, b]}f(x)$ and assume that it is not attained, so $\gamma < f(x)$ for all $x \in [a,b]$. Then consider the function $h:[a,b]\to \mathbb{R}$ given by $h(x) = \displaystyle\frac{1}{f(x) - \gamma}$. This is continuous, and hence bounded on $[a, b]$. So there exists $K \geq 0$ such that $|h(x)| \leq K$ for all $x \in [a, b]$. By Problem
15(ii), given any $\varepsilon > 0$, there exists $x \in [a, b]$ such that $f(x) < \gamma + \varepsilon$. Now take $\varepsilon = \frac{1}{K}$ to deduce that $h(x) > K$, which yields the required contradiction.

27. By algebra of limits, $\frac{1}{f}$ is continuous on $[0, 1]$ and so is bounded by Theorem \iflatexml 2.3.6 \else [thm:evt](#thm:evt) \fi .

28. HW3 question
<br>
If $f$ is continuous on $[0, 1]$, then it is bounded by Theorem \iflatexml 2.3.6 \else [thm:evt](#thm:evt) \fi , and so there exists $L \geq 0$ such that $|f(x)| \leq L$ for all $x \in [0, 1]$. Hence the range of $f$ is a subset of  $[-L, L]$ and cannot be all of $\mathbb{R}$.

29. Since $(x_{n})$ is bounded, by the Bolzano--Weierstrass theorem it has a convergent subsequence $(x_{n_{k}})$. Let $c=\lim_{k \rightarrow \infty}x_{n_{k}}$ and note that $c \in [0, 1]$, since $x_{n_k}\in[0,1]$ for all $k$.
<br>
A straight-forward induction argument shows that $f(x_{n_{k}}) \leq r^{n_{k}-1}f(x_{n_{1}})$ for all $k\in\mathbb{N}$. But then, since the range of $f$ is contained in $[0,1]$, we have

$$
0 \leq f(x_{n_{k}}) \leq r^{n_{k}-1}
$$

for all $k\in\mathbb{N}$. Since $r < 1$, $\lim_{k\to\infty} r^{n_k-1} =0$. By the sandwich rule, $ \lim_{k \rightarrow \infty}f(x_{n_{k}}) = 0$ and by continuity of $f$ at $c$, $f(c) = \lim_{k \rightarrow \infty}f(x_{n_{k}})$, so $f(c)=0$.

30. For all $x > y$,

$$
x^{n} - y^{n} = (x - y)(x^{n-1} + x^{n-2}y + \cdots + xy^{n-1} + y^{n-1}) > 0.
$$

31. For all $-\frac{\pi}{2} \leq x < y \leq \frac{\pi}{2}$,

$$
\sin(y) - \sin(x) = 2\sin\left(\frac{y - x}{2}\right)\cos\left(\frac{y + x}{2}\right) > 0,
$$

so the function is strictly monotonic increasing on this interval. It is also continuous (stated in notes), and so by Theorem 2.3.10, it is has a continuous inverse $f^{-1}(x) = \arcsin(x)$ (or $\sin^{-1}(x)$) defined on $[-1, 1]$. Outside the interval $\left[-\frac{\pi}{2}, \frac{\pi}{2}\right]$, the function $f$ might fail to be strictly increasing. In fact it is strictly decreasing on each interval of the form $\left((4n+1)\frac{\pi}{2}, (4n + 3)\frac{\pi}{2}\right)$, and strictly increasing on each interval of the form $\left((4n-1)\frac{\pi}{2}, (4n + 1)\frac{\pi}{2}\right)$, where $n\in\mathbb{Z}_+$.

32. We seek a continuous extension of the mapping $x\mapsto \frac{1-x}{1-x^{\frac{m}{n}}}$ to a domain that includes $1$. Then, we can use continuity to evaluate the limit as $x\rightarrow 1$.
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

Both $f$ and $g$ are continuous at every point in their domain (for $f$, this was proven in Example \iflatexml \else [nthroot](#nthroot)\fi). Hence by the composition theorem for continuous functions (Theorem \iflatexml 2.1.6 \else [fof](#fof) \fi), the map

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

33. We claim that if $a < x < b$, we have $f(a) < f(x) < f(b)$. To see this, note that if $f(a) \geq f(x)$ then either $f(a) = f(x)$, or $f(a) > f(x)$.
<br>
If $f(a)=f(x)$, then $f$ cannot be bijective, which is a contradiction. 
<br>
Suppose that $f(a)>f(x)$. Applying Corollary~\iflatexml 2.3.7 \else [interval](#interval)\fi to $f|_{[x,b]}$, the image of $[x,b]$ under $f$ must an interval, $[m,M]$, say. Note that $f(a)\in(m,M)$: indeed, $f(a)>f(x)>M$, and $f(a)<f(b)<m$. Therefore, by the intermediate value theorem (or Corollary 2.3.2 more specifically), there exists $c \in (x, b)$ such that $f(c) = f(a)$, and this again violates the injectivity of the mapping $f$. A similar argument can be used to show that we cannot have $f(b) \leq f(x)$.
<br>
Finally, applying our initial result to $f|_{[a, y]}$, we see that if $a<x<y<b$, then $f(a) < f(x) < f(y)$. Hence $f$ is strictly monotonic increasing.

34. First observe that $f+g$ is monotonic increasing since both $f$ and $g$ are. Choose $a \in \mathbb{R}$. Given $\varepsilon > 0$, there exists $\delta > 0$ so that if $x > a + \delta$ then

$$
|f(x) + g(x) - f(a) - g(a)|  =  f(x) + g(x) - f(a) - g(a) < \varepsilon,
$$

and so

$$
|f(x) - f(a)| = f(x) - f(a) < \varepsilon +g(a) - g(x) < \varepsilon,
$$

as $g$ is increasing. This proves that $g$ is right--continuous at $a$. A similar argument (interchanging the roles of $a$ and $x$) proves that it is left--continuous, and hence continuous at $a$. Then $g = (f + g) - f$ is the difference of two continuous functions, and hence is itself continuous.

35. 
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

## 1.3. Differentiation

36. This is Definition \iflatexml 1.2.3 \else [def:functionlimit](#def:functionlimit) \fi in the notes:
<br>
The function $f$ has limit $l$ at the point $a$ if for every sequence  $(x_n)$ in $A$ with $x_n\neq a$ for all $n$ and $\lim_{n\to\infty} x_n=a$, we have $\lim_{n\to\infty}f(x_n)=l$. We write $\lim_{x\to a}f(x)=l$.

37. HW4 question
    (i) This is Definition \iflatexml 3.2.1 \else [def:functionlimit](#def:functionlimit) \fi in the notes: we say that $f$ is {\it differentiable} at $a \in A$ if $ \lim_{x \rightarrow a}\frac{f(x) - f(a)}{x - a}$ exists. Or, equivalently, $ \lim_{h \rightarrow 0}\frac{f(a +h) - f(a)}{h}$ exists.
    <br>
    That is, we fix $a\in A$ and we consider the function $g$ given by $g(h)=\frac{f(a +h) - f(a)}{h}$. Then $f$ is differentiable at $a$ if the limit of $g$ as $h$ goes to zero exists.
    
    (ii) This is Definition \iflatexml 1.2.3 \else [def:functionlimit](#def:functionlimit) \fi from the notes, the definition of limit of a function in terms of sequences. It's very important to understand that it's not applied directly to $f$ here; it's applied to the function $g$ above:
    <br>
    $f$ is differentiable at $a$ if there exists some number $f'(a) \in \mathbb{R}$ for which, given any sequence $(h_{n})$ that converges to $0$, with $h_n\neq 0$ for all $n$, we have

    $$
    \frac{f(a + h_{n}) - f(a)}{h_{n}} \rightarrow f'(a) \hspace{1em} \text{ as } \hspace{1em} n\rightarrow\infty.
    $$
    
    (iii) This is asking for the equivalent description of limit of a function given by the $(\varepsilon - \delta)$ criterion (Theorem 1.2.6). Again it needs to be applied to $g$ as above not $f$ itself:
    <br>
    We say $f$ is differentiable at $a$ if there exists a number $f'(a)$ for which, given $\varepsilon>0$, there exists $\delta > 0$ such that if $0<|h| < \delta$, then 	
    $$
    \left|\displaystyle\frac{f(a+h) - f(a)}{h} - f'(a)\right| < \varepsilon.
    $$