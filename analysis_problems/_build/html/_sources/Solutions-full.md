(sol)=
# Solutions

## Preliminary problems

1. %P1
The correct statements are (ii) and (v).

In statement (iv), the quantifiers $\forall$ and $\exists$ are the wrong way round, while in (i) they are missing altogether. Statement (iii) asserts that last part, $|x_n-l|<\varepsilon$ $\forall n\geq N$, should hold for all $\varepsilon$ and for all $N$ --- so again, there is an issue with the quantifiers.

Bonus exercise: prove that (iv) holds if and only if $(x_n)$ is the constant sequence $x_n=l$ for all $n\in\N$.

\vspace{1em}
2. %P2 - HW1 QUESTION
Let $\varepsilon>0$. According to the definition, we must prove there is an $N\in\N$ for which $\left|\frac{2n}{3n-1}-\frac{2}{3}\right|<\varepsilon$ whenever $n\geq N$.

Now,
$$
\left|x_n-\frac{2}{3}\right| = \left|\frac{2n}{3n-1}-\frac{2}{3}\right| = \frac{6n-(6n-2)}{3(3n-1)} = \frac{2}{3(3n-1)}.
$$
This will be strictly less than $\varepsilon$ whenever $3n-1>\frac{2}{3\varepsilon}$., or in other words, whenever
$$
n>\frac{1}{3}\left(\frac{2}{3\varepsilon}+1\right)=\frac{2+3\varepsilon}{9\varepsilon}.
$$
Let $N$ be any integer greater than $\frac{2+3\varepsilon}{9\varepsilon}$. Then $\left|x_n-\frac{2}{3}\right|<\varepsilon$ for all $n\geq N$, and we have proven that $x_n\rightarrow\frac{2}{3}$ as $n\rightarrow\infty$ using the definition.


\vspace{1em}
3. %P3 - HW1 QUESTION
The Bolzano--Weierstrass theorem states that every bounded sequence has a convergent subsequence. Its proof combines the following two results:
    - The monotone convergence theorem (Theorem 3.10 in the MAS107 notes), which states that bounded monotone sequences must converge. <br> More specifically, every monotone increasing sequence that is bounded above converges to its supremum, and every monotone decreasing sequence bounded below converges to its infimum.
    - Theorem 3.13 from MAS107: Every sequence has a monotone subsequence.
Proof of Bolzano--Weierstrass: \\
If $(x_n)$ is a bounded sequence, then it has a monotone subsequence, $(x_{n_k})$, by Theorem 3.13. This subsequence must also be bounded since $(x_n)$ is bounded, and hence it converges by the monotone convergence theorem.


\vspace{1em}4. %P4
[label={(\roman*)}]    1. Let $a, b \geq 0$. Then,
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
    2.  Note that the inequality we have been asked to prove is symmetric in $a$ and $b$, in the sense that exchanging the roles of $a$ and $b$ does not affect the value of either side.

This means we can assume without loss of generality that $\sqrt{|a|}\geq\sqrt{|b|}$. Then,
$$
\left|\sqrt{|a|} - \sqrt{|b|}\right| = \sqrt{|a|}-\sqrt{|b|},
$$
and we need only show that
$$
\begin{equation}\label{eq:sqrta-sqrtb}
\sqrt{|a|} - \sqrt{|b|} \leq \sqrt{|a - b|}.
\end{equation}
$$
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
    3. Let $(a_n)$ be a real sequence converging to $l\in\R$. By (ii),
$$
\left|\sqrt{|a_{n}|}-\sqrt{|l|}\right| \leq \sqrt{\big|a_n-l\big|}
$$
for all $n\in\N$.

Let $\varepsilon>0$. Since $a_n\rightarrow l$, there is $N\in\N$ such that $|a_n-l|<\varepsilon^2$ whenever $n\geq N$. Hence for $n\geq N$,
$$
\big|\sqrt{|a_{n}|}-\sqrt{|l|}\big| \leq \sqrt{\varepsilon^2} = \varepsilon.
$$
Thus $\ds\lim_{n\rightarrow\infty}\sqrt{|a_n|} = \sqrt{|l|}$.
\vspace{1em}5. %P5
%Look up and carefully define the \emph{supremum} and \emph{infimum} of a set $A\subseteq\R$. What conditions must be met for each of these to exist?

When it exists, the supremum of a set $A\subseteq\R$ is defined to be the unique number $\alpha\in\R$ such that
    - $\alpha$ is an upper bound for $A$, and
    - if $M$ is any other upper bound for $A$, then $\alpha\leq M$.
We write $\sup A$ for the supremum of $A$, when it exists.

The definition of the infimum is similar: when it exists, the infimum of $A$ is the unique number $\beta\in\R$ such that[label={(\roman*)}]    1. $\beta$ is a lower bound for $A$, and
    2. if $L$ is any other lower bound for $A$, then $\alpha\geq L$.
We write $\inf A$ for the infimum of $A$, when it exists.

The axiom of completeness for the real numbers says that every non-empty bounded above subset of $\R$ has a supremum. Equivalently, it says that every non-empty bounded below subset of $\R$ has an infimum.

For more details, see page 32 of your Semester 2 MAS107 notes.


\vspace{1em}6. %P6
[label={(\roman*)}]    1. $\ds\sup\left\{\frac{m}{n}:m,n\in\N \text{ s.t } m<n\right\}=1$,

$\ds\inf\left\{\frac{m}{n}:m,n\in\N \text{ s.t } m<n\right\}=0$.
    2. $\ds\sup\left\{\frac{(-1)^m}{n}:m,n\in\N \text{ s.t } m<n\right\}=\frac{1}{3}$,

$\ds\inf\left\{\frac{(-1)^m}{n}:m,n\in\N \text{ s.t } m<n\right\}=-\frac{1}{2}$.
    3. $\ds\sup\left\{\frac{n}{3n + 1} :n\in\N\right\}=\frac{1}{3}$, $\ds\inf\left\{\frac{n}{3n + 1} :n\in\N\right\}=\frac{1}{4}$.
\vspace{1em}7. %P7
[label={(\roman*)}]    1. This is false --- for a counter-example, take any singleton set. Then $\sup A=\inf A=1$.

A correct version of the statement would be $\inf A \leq \sup A$.
    2. True. The analogous statement for $\sup$ was called the characteristic property of the supremum in your MAS107 lecture notes --- see Lemma 2.8 on page 36.
    3. True. Since $\sup B$ is an upper bound for $B$, and $A$ is a subset of $B$, $\sup B$ must be an upper bound for $A$. But $\sup A$ is a the least upper bound for $A$, hence $\sup A\leq \sup B$.

The analogous property for $\inf$ is that $\inf A\geq\inf B$ whenever $A\subseteq B$.
    4. False. For a counter-example, take $B=\left\{\frac{1}{n}:n\in\N\right\}$, for which $\inf B=0$.
    5. True. Let $s=\max\{\sup A,\sup B\}$. Then $s\geq \sup A$ and $s\geq \sup B$, so $s$ is an upper bound for both $A$ and $B$. Therefore, $s$ is an upper bound for $A\cup B$. But $\sup(A\cup B)$ is the least upper bound of $A\cup B$, and so $s\geq\sup(A\cup B)$. Also, since $A$ and $B$ are both subsets of $A\cup B$, we have by statement (iii) that $s=\max\{\sup A,\sup B)\leq\sup(A\cup B)$. Hence $\max\{\sup A,\sup B)=\sup(A\cup B)$.

## 1.1. Limits of functions

 % Formerly Ch3 of MAS221 Sem 1 problem booklet1. %1 - HW1 QUESTION
One has to identify the real numbers where the given formula does not make sense, usually because of a zero in a denominator somewhere, and exclude them.
[label={(\roman*)}]    1. $A=\R \setminus \{0, -1\}$.
    2. $f_{2}(x) = \ds\frac{(x-1)(x+4)}{(x-1)(x+2)(x+3)}$, so
$A=\R \setminus \{1, -2, -3\}$.
    3. $f_{3}(x) = \ds\frac{x+4}{(x+2)(x+3)}$, so
$A=\R \setminus \{-2, -3\}$.
    4. $A=\R \setminus \{1\}$.
    5. $A=\R \setminus \{0\}$.
\vspace{1em}2. %2 - HW1 QUESTION
[label={(\roman*)}]    1. $L=[0,1]\cup[2,3]$.
    2. $L=\emptyset$.  (All convergent sequences in $\Z$ are eventually constant.)
    3. $L=\R$.
    4. $L=[0,1]$
    5. $L=\{0\}$
\vspace{1em}3. %3
We had $A= \R \setminus \{1, -2, -3\}$, and $f_2:A\to\R$; $\ds f_{2}(x)= \frac{(x + 4)}{(x + 2)(x + 3)}$.

Let $(x_n)$ be a sequence in $A$ converging to $1$. Then, using algebra of limits for real sequences,
$$
\lim_{n\to\infty}f_2(x_n)= \lim_{n\to\infty} \frac{(x_n + 4)}{(x_n + 2)(x_n + 3)} =  \frac{(1 + 4)}{(1 + 2)(1 + 3)} = \frac{5}{12},
$$
where the last equality is using algebra of limits. So $\ds\lim_{x \rightarrow 1}f_{2}(x) = \frac{5}{12}$.

Let $x_n=-2 + \frac{1}{n}$, so that $(x_n)$ is a sequence in $A$ converging to $-2$. Then we see that $(f_2(x_n))$ diverges to $+\infty$ and so $\lim_{x \rightarrow -2}f_{2}(x)$  does not exist.

Similarly, considering $x_n=-3 + \frac{1}{n}$,  we see that $\lim_{x \rightarrow -3}f_{2}(x)$ does not exist.


\vspace{1em}
4. %4
The first part follows by using the definition of the limit of a function in terms of limits of sequences, and then applying the result of Problem~[q:25](#q:25) (iii).

To be precise let $(x_{n})$ be any sequence in $\R \setminus \{a\}$ that converges to $a$. Then since we are given that $\lim_{x \rightarrow a} f(x) = l$, we must have that $\lim_{n\rightarrow\infty} f(x_{n}) = l$. But then by Problem~[q:25](#q:25) (iii), we have $\lim_{n\rightarrow\infty} \sqrt{f(x_{n}}) = \sqrt{l}$. So by definition of the limit of a function, $\lim_{x \rightarrow a} \sqrt{f(x)} = \sqrt{l}$.

\medskip
Using algebra of limits,  $\lim_{x \rightarrow 1}\ds\frac{x+1}{x^{2}}=\frac{1+1}{1^2}=2$ and
then by the first part $\lim_{x \rightarrow 1}\sqrt{\ds\frac{x+1}{x^{2}}} = \sqrt{2}$.


\vspace{1em}
5. %5
Let $f:A\to \R$ and suppose that $\lim_{x \rightarrow a} f(x) = l$ and $\lim_{x \rightarrow a} f(x) = l'$. Then given any sequence $(x_{n})$ in $A \setminus \{a\}$ that converges to $a$, we have $\lim_{n\rightarrow\infty} f(x_{n}) = l$ and also $\lim_{n\rightarrow\infty} f(x_{n}) = l'$. But then $l = l'$, by uniqueness of limits.


\vspace{1em}
6. %6 - HW2 QUESTION
When $x > 0, \ds\frac{|x|}{x} = \ds\frac{x}{|x|} = \ds\frac{x}{x} = 1 = \sign(x)$,

when $x < 0, \ds\frac{|x|}{x} = \ds\frac{x}{|x|} = -\ds\frac{x}{x} = -1 = \sign(x)$.

The left limit is $\ds\lim_{x \rightarrow 0^-} \sign(x) = -1$, since for any sequence $(x_n)$ approaching $0$ from the left, we have $\sign(x) = -1$ for all $n$.

Similarly, the right limit is $\ds\lim_{x \rightarrow 0^+} \sign(x) = 1$,  since for any sequence $(x_n)$ approaching $0$ from the right,
we have $\sign(x) = 1$ for all $n$.

Since the left and right limits are different, $\ds\lim_{x \rightarrow 0}\sign(x)$ does not exist.


\vspace{1em}
7. %7 - HW2 QUESTION
[label={(\roman*)}]    1. For $a\neq 1$, the left and right limits exist and are both equal to $f(a)$, using the algebra of limits. The only point at which left and right limits disagree is $a = 1$, with
$$
\lim_{x \rightarrow 1-}f(x) = 0, \; \text{ and } \; \lim_{x \rightarrow 1+}f(x) = 1.
$$
    2. In this case, left and right limits disagree at every $n \in \mathbb{Z}$, with $\lim_{x \rightarrow a-}[x] = n-1, \lim_{x \rightarrow n+}[x] = n$. At every other real number, the left and right limits exist and are both equal to the value of the function there.
    3. Here, left and right limits disagree at $x = 0, 1$ and $2$. We have
$$
\lim_{x \rightarrow 0^-}h(x) = 3, \hspace{1em} \lim_{x \rightarrow 1-}h(x) = -2, \hspace{1em}  \lim_{x \rightarrow 2-}h(x) = 10,
$$
$$
\lim_{x \rightarrow 0^+}h(x) = -2, \hspace{1em} \lim_{x \rightarrow 1+}h(x) = 10, \hspace{1em}  \lim_{x \rightarrow 2+}h(x) = 3.
$$
\vspace{1em}undefined. %8
The largest subset of $\R$ for which the formula $f(x)=\sin\left(\frac{1}{x}\right)$ makes sense is $A = \R \setminus \{0\}$.

Observe that for any real number $\theta\in\R$,

$$
f\left(\frac{1}{\theta+2\pi n}\right) = \sin(\theta+2\pi n) = \sin(\theta).
$$

To prove $f$ has no limit at $0$, we need only choose two values of $\theta$ for which sine takes distinct values. We choose $\theta=\frac{\pi}{2}$ and $\theta=\frac{3\pi}{2}$.

By choosing the right values for $\theta$, we can use this to construct two distinct sequences $(x_n)$ and $(y_n)$ that both converge to $0$, but for which $\sin(x_n)$ and $\sin(y_n)$ have different limits.

We use $\theta=\frac{\pi}{2}$ and $\theta=\frac{3\pi}{2}$ (other choices possible).

For each $n\in\N$, let $x_n=\frac{1}{\frac{\pi}{2} + 2\pi n}$ and $y_n=\frac{1}{3\frac{\pi}{2} + 2\pi n}$. Then

$$
\lim_{n\rightarrow\infty} x_{n} =\lim_{n\rightarrow\infty} y_n= 0,
$$

while for all $n\in\N$,

$$
f(x_n) = \sin\left(\frac{\pi}{2}\right) =1 \hspace{2em} \text{ and } \hspace{2em} f(y_n)=\sin\left(\frac{3\pi}{2}\right)=-1.
$$

So $\lim_{n\rightarrow\infty} f(x_{n}) = 1$, but $\lim_{n\rightarrow\infty} f(y_n) = -1$. Since these limits are not equal, $\lim_{x\to 0} f(x)$ does not exist.

Of course, we could have chosen any values of $\theta$ we liked, and constructed a sequence $(x_n)$ with limit $0$ for which $\lim_{n\rightarrow\infty}f(x_n)$ is equal to any real number we liked in the interval $[-1,1]$. The graph of this function below may give some intuition as to how this is possible.
%Here is how Maple draws the graph close to zero:

\iflatexml
![](figs/sin(1,x))
\else
$$
\begin{tikzpicture}
\begin{axis}[width=.9\linewidth, xlabel=$x$, ylabel=$y$, unit vector ratio*=1 1 1, xmin=-4, xmax=4, ymin=-1.5, ymax=1.5, axis lines=middle, tick align=outside, xtick={-0.6366,0.6366}, ytick={-1,1}, xticklabels={$-\frac{2}{\pi}$,$\frac{2}{\pi}$}, yticklabels={$-1$,$1$}, samples=10000]
\addplot[domain=-4:-.0001,no marks,thick] {sin(deg(1/x))};
\addplot[domain=.0001:4,no marks,thick] {sin(deg(1/x))};
\end{axis}
\end{tikzpicture}
$$
\fi
Graph of the function $f:\mathbb{R}\to\mathbb{R}$; $f(x)=\sin\left(\frac{1}{x}\right)$.

\vspace{1em}
NaN. %9
The largest subset of $\R$ for which the formula $f(x)=x\sin\left(\frac{1}{x}\right)$ makes sense is $A = \R \setminus \{0\}$.

We claim that $\ds\lim_{x \rightarrow 0} x \sin\left(\frac{1}{x}\right) = 0$.

To see this, let $(x_{n})$ be an arbitrary sequence in $A$ that converges to $0$. The sine function takes values only in the interval $[-1,1]$, and so

%	$$
\left|x_n\sin\left(\frac{1}{x_n}\right)\right| \leq |x_n|
$$

%for each $n\in\N$. Put another way,

$$
-|x_{n}| \leq x_{n}\sin\left(\frac{1}{x_n}\right) \leq |x_{n}|
$$

for all $n\in\N$. Since $\ds\lim_{n\to \infty} x_n=0$, we have \$ \ds\lim_{n\to \infty} |x_n| =0\$. Therefore, but the sandwich rule, $\ds\lim_{n\rightarrow 0}x_n\sin\left(\frac{1}{x_n}\right) = 0$.

Since $(x_n)$ was arbitrary, $\ds\lim_{x \rightarrow 0} x \sin\left(\frac{1}{x}\right) = 0$.

You should contrast the picture below with that for the previous question.

\iflatexml
![](figs/xsin(1,x))
\else
$$
\begin{tikzpicture}
\begin{axis}[width=.9\linewidth, xlabel=$x$, ylabel=$y$, unit vector ratio*=1 1 1, xmin=-4, xmax=4, ymin=-1.5, ymax=1.5, axis lines=middle, tick align=outside, xtick={-0.3183,0.3183}, ytick={-1,1}, xticklabels={$-\frac{1}{\pi}\hspace{.7em}$,$\frac{1}{\pi}$}, yticklabels={$-1$,$1$}, samples=1000]
\addplot[domain=-4:-.01,no marks,thick] {x*sin(deg(1/x))};
\addplot[domain=.01:4,no marks,thick] {x*sin(deg(1/x))};
%\addplot[domain=-4:4,no marks,blue!80] {x};
%\addplot[domain=-4:4,no marks,blue!80] {-x};
\end{axis}
\end{tikzpicture}
$$
\fi
Graph of the function $f:\mathbb{R}\to\mathbb{R}$; $f(x)=x\sin\left(\frac{1}{x}\right)$.

%\vspace{1em}

%
8. %We'll just deal with the left limit here, as the right limit argument is very similar. Assume the $(\varepsilon, \delta)$--criterion for left limits holds, and consider an arbitrary sequence $(x_{n})$ with $x_{n} < a$ for all $n\in\mathbb{N}$ that converges to $a$. Then given any $\eta > 0$, there exists $N\in\mathbb{N}$ so that if $n\geq N$, then $0 < a - x_{n} < \eta$. Now choose $\eta$ to be $\delta$ from the criterion, and argue as in the proof of Theorem \iflatexml 1.2.6 \else [ed](#ed) \fi.

%The converse works in the same way as in that proof, except that this time the sequence $(x_{n})$ is constructed by choosing $x_{n}$ in the domain of $f$ such that $0 < a - x_{n} < \frac{1}{n}$, and $|f(x_{n}) - l| \geq \varepsilon$ for each $n\in\mathbb{N}$.


\vspace{1em}
9. %10
We'll just do $\ds\lim_{x \rightarrow \infty}f(x)$ here, as $\ds\lim_{x \rightarrow -\infty}f(x)$ is so similar.
[label={(\roman*)}]    1. Let $X\subset\R$ and $f:X\to\R$. We say that $\lim_{x \rightarrow \infty}f(x) = l$ if whenever $(x_{n})$ is a sequence that diverges to infinity, with $x_{n}\in X$ for all $n\in\mathbb{N}$, then $\lim_{x \rightarrow \infty}f(x_{n}) = l$.
    2. The analogue of the $(\varepsilon- \delta)$ criterion is $(\varepsilon-K)$: given any $\varepsilon > 0$, there exists $K > 0$ such that if $x > K$ then $|f(x) -l| < \varepsilon$.

For the proof, suppose the $(\varepsilon- K)$ criterion holds and $\lim_{n\rightarrow\infty} x_{n} = \infty$. Then given any $L > 0$, there exists $N\in\mathbb{N}$ such that if $n\geq N$, we have $x_{n} > L$. Now take $L$ to be $K$ from the criterion and we get that for all $n\geq N, |f(x_{n}) - l| < \varepsilon$. Hence $\lim_{x \rightarrow \infty}f(x_{n}) = l$, as required.

For the converse, we again imitate the proof of Theorem \iflatexml 1.2.6 \else [ed](#ed) \fi. So suppose the $(\varepsilon-K)$ criterion does not hold.
This time choose successively $K = 1, 2, \ldots$ and construct $x_{n}$ in the domain $X$ of $f$ such that $x_{n} > n$, and $|f(x_{n}) - l| \geq \varepsilon$ for each $n\in\mathbb{N}$. So $f$ does not converge to $l$ as $x\to\infty$.
    3. Given any $\varepsilon > 0$, choose $K = \frac{1}{\varepsilon}$. Then $x > K \Rightarrow \frac{1}{x} < \varepsilon$, and so
$\lim_{x\to\infty} \frac{1}{x}=0$. The case where $x\to-\infty$ is similar.
\vspace{1em}10. %11
[label={(\roman*)}]    1. Let $f:X\to\R$ be a function, where $X\subseteq\R$. We say that $\lim_{x \rightarrow \infty} f(x) = \infty$ if for any sequence $(x_{n})$ in $X$ which diverges to infinity, we also have that $(f(x_{n}))$ diverges to infinity.

The analogue of $(\varepsilon - \delta)$ is:
$$
\begin{quote}Given any $M > 0$, there exists $K > 0$ such that $x > K$ implies $f(x) > M$.\end{quote}
$$
The other cases are similar.
    2. Let $f:\R\to[0,\infty)$, $g:\R\to[0,\infty)$, and suppose $\ds\lim_{x\rightarrow\infty}f(x)=\infty$ and $\ds\lim_{x\rightarrow\infty}g(x)=l$, where $l>0$.

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

Hence for $x>K$,
$$
f(x)g(x) > \frac{2M}{l}\frac{l}{2} = M.
$$
That is, $\lim_{x\rightarrow\infty}f(x)g(x) = \infty$.

%In the other case, we have $\lim_{x \rightarrow -\infty}h(x) = -\infty$; for in that case, given $K >0$,  there exists $L_{1} > 0$ such that $x < -L_{1} \Rightarrow f(x) < -K$, and for $x < \min\{-L_{1}, -L_{2}\}$ we have $f(x)g(x) < -K(l + \varepsilon)$.
    3. Let $p:\R\to\R$ be a polynomial of even degree $m$, with positive leading coefficient. Write $m = 2n$ and let
$$
\begin{align*}
p(x) &= a_{2n}x^{2n} + a_{2n-1}x^{2n-1} + \cdots + a_{1}x + a_{0}\\
&= x^{2n}\left(a_{2n} + \frac{a_{2n-1}}{x} + \cdots + \frac{a_{1}}{x^{2n-1}} + \frac{a_{0}}{x^{2n}}\right). 
\end{align*}
$$

We use part (ii). Take $f(x) = x^{2n}$ and $\ds g(x) = a_{2n} + \frac{a_{2n-1}}{x} + \cdots + \frac{a_{1}}{x^{2n-1}} + \frac{a_{0}}{x^{2n}}$.

Observe that $\ds\lim_{x \rightarrow \infty}f(x) = \infty$ and $\ds\lim_{x \rightarrow \infty}g(x) = a_{2n}$. Hence by part (ii),
$$
\lim_{x \rightarrow \infty}p(x) = \lim_{x \rightarrow \infty}f(x)g(x) = \infty.
$$


If $n$ is odd, $\lim_{x \rightarrow \infty}p(x) = \infty$, but $\lim_{x \rightarrow -\infty}p(x) = -\infty$.

## 1.2. Continuity

 % Formerly Ch4 of MAS221 Sem 1 problem booklet1. %12
For each of (i) to (v), the function is continuous at each point of its domain. For (i), (ii) and (iii), we have rational functions, which are continuous on all points of $A$ (which is the subset of $\R$ where the denominator is non-zero). For (iv) and (v), we have compositions of rational functions with the exponential and cosine functions, which are continuous on the whole of $\R$. Again, the functions are continuous on all points of $A$ (which is the subset of $\R$ where the denominator of the rational function is non-zero).


\vspace{1em}
2. %13
If $(x_{n})$ is any sequence that converges to $a$, we know that $f(x_n)$ converges to $f(a)$ as $f$ is continuous at $a$, and
we need to show that $(|f|(x_n))$ converges to $|f|(a)$.

By Corollary~\iflatexml 0.2.6 \else [cor:tri](#cor:tri)\fi, if $(x_{n})$ is any sequence that converges to $a$,
$$
\begin{align*}
0 \leq ||f|(a)| -|f|(x_{n})| &= ||f(a) - |f(x_{n})|| \\
&\leq |f(a) - f(x_{n})| \rightarrow 0~\mbox{as}~n \rightarrow \infty, 
\end{align*}
$$
as $f$ is continuous.
So by the sandwich rule, $\lim_{n\rightarrow\infty} |f|(x_{n}) = |f|(a)$, and so $f$ is continuous at $a$.


\vspace{1em}
3. %14
Let $(x_{n})$ be a sequence in $A$ that converges to $a$. Since $f$ is continuous at $a$ we have $\lim_{n\rightarrow\infty} f(x_{n}) = f(a)$. And then, since $g$ is continuous at $f(a)$, we have $\lim_{n\rightarrow\infty} g(f(x_{n})) = g(f(a))$, and the result follows.


\vspace{1em}
4. %15
$f \circ g:\R\to \R$ given by $(f \circ g)(x) = \frac{1}{1  + x^{2}}$. It is continuous on $\R$ by Theorem \iflatexml  2.1.5(iv) \else [AOL3](#AOL3)(iv) \fi.

$g \circ f:\R \setminus \{0\} \to \R \setminus \{0\}$ given by $(g \circ f)(x) = {1  + \frac{1}{x^2}}$. It is continuous on $\R \setminus \{0\}$ by Theorem \iflatexml  2.1.5(iv) \else [AOL3](#AOL3)(iv) \fi.
5. %16
[label={(\roman*)}]    1. Continuous on $\R \setminus \{1\}$. Jump discontinuity at $1$ with $J_{f}(1) = 1$.
    2. Continuous on $\R \setminus \Z$. Jump discontinuity at $n$ with $J_{g}(n) = 1$ for all $n\in\mathbb{Z}_+$.
    3. Continuous at $\R \setminus \{0,1,2\}$. Each of $0, 1, 2$ is a jump discontinuity and we have $J_{h}(0) =-5, J_{h}(1) = 12, J_{h}(2) = -7.$
\vspace{1em}6. %17 - HW2 question
[label={(\roman*)}]    1. For $x \neq 0, f(x) = x+2$. Since $\lim_{x \rightarrow 0}f(x) = 2$, the required continuous extension is $\tilde{f}$ where
$$
\tilde{f}(x) = \left\{\begin{array}{c c} \ds\frac{(1 + x)^{2} - 1}{x} & ~\mbox{if}~x \neq 0\\
& \\
2 & ~\mbox{if}~x = 0. \end{array} \right.
$$
7. The largest domain is $A=\R \setminus \{-2, 2\}$ (the set where the denominator is non-zero). For $x \neq 2, -2$,

$$
f(x) = \frac{(x-2)(x^{2} + 2x + 4)}{(x-2)(x+2)}=\frac{x^{2} + 2x + 4}{x + 2}.
$$ This is a rational function, and hence continuous everywhere the denominator is non-zero by Theorem \iflatexml  2.1.5(iv) \else [AOL3](#AOL3)(iv) \fi.

We claim that $\lim_{x \rightarrow -2}f(x)$ does not exist. To see this, consider the sequence $(x_{n})$, whose $n$\textsuperscript{th} term is $-2 + \frac{1}{n}$, and check that

$$
f(x_{n}) = n\left(-4 -\frac{2}{n} + \frac{1}{n^2}\right) \rightarrow -\infty~\mbox{when}~n \rightarrow \infty.
$$

Thus $f$ has no continuous extension to the point $x =-2$.

But on the other hand,

$$
\lim_{x \rightarrow 2}f(x) = \lim_{x\rightarrow 2}  \frac{x^{2} + 2x + 4}{x + 2} = \frac{12}{4} = 3,
$$

and so $f$ has a continuous extension

$$
\tilde{f}:\R \setminus \{-2\}\to\R; \hspace{1em} \tilde{f}(x) = \frac{x^2+2x+4}{x+2}.
$$

We can see this behaviour in the graph of the function:

\iflatexml
![](figs/(x%5E2+2x+4),(x+2))
\else
$$
\begin{tikzpicture}
\begin{axis}[width=.85\linewidth, xlabel=$x$, ylabel=$y$, unit vector ratio*=1 1 1, xmin=-13, xmax=13, ymin=-13, ymax=13, axis lines=middle, tick align=outside, xtick={-2}, ytick={2}, xticklabels={$-2$}, yticklabels={$2$}, samples=1000]
\addplot[domain=-13:-2.1,no marks,thick] {(x^2+2*x+4)/(x+2)};
\addplot[domain=-1.9:13,no marks,thick] {(x^2+2*x+4)/(x+2)};
\draw[dashed] (axis cs:-2,-13)--(axis cs:-2,13);
\end{axis}
\end{tikzpicture}
$$
\fi
Graph of the function $\tilde{f}:\mathbb{R}\setminus\{-2\}\to\mathbb{R}$; $f(x)=\frac{x^2+2x+4}{x+2}$.
%\vspace{-5cm}


\vspace{1em}8. %18
Assume $g$ is continuous and $g(a) > 0$.
Suppose, for a contradiction, that  there is no  $\delta > 0$ such that $g(x) > 0$  for all \$ x \in (a - \delta, a + \delta)\$. Then, in particular, for all $n\in\mathbb{N}$ there exists $x_{n} \in \left(a - \frac{1}{n}, a + \frac{1}{n}\right)$ such that $g(x_{n}) \leq 0$. By the sandwich rule, we have $\lim_{n\rightarrow\infty} x_{n} = a$. So, by continuity of $g$ at $a$, we have $\lim_{n\rightarrow\infty} g(x_{n})$ exists and equals $g(a)$. But $g(x_n)\leq 0$ for all $n\in\mathbb{N}$, and so
$$
g(a)=\lim_{n\rightarrow\infty} g(x_{n}) \leq 0,
$$
which is a contradiction.



\vspace{1em}
9. %19
[label={(\roman*)}]    1. $$
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
and continuity follows by Theorem \iflatexml  2.1.5(i) \else [AOL3](#AOL3)(i) \fi and (iii) and Problem~[q:56](#q:56).
    2. Check that for all $a, b \in \R$,
$$
\min\{a, b\} = \frac{1}{2}(a + b) - \frac{1}{2}|a - b|,
$$
and then argue as in (i).

Alternatively, one could derive (ii) from (i) by using $\min\{f,g\} = - \max\{-f, -g\}$.
\vspace{1em}10. %20
[label={(\roman*)}]    1. $f(0) = f(0 + 0) = f(0) + f(0) = 2f(0)$, hence $f(0) = 0$.
    2. By (i), $0 = f(0) = f(x + -x) = f(x) + f(-x)$. So $f(-x)=-f(x)$.
    3. If $a \neq 0$ then any sequence $(x_{n})$ which converges to $a$ can be written as $x_{n} = a + y_{n}$ where $(y_{n})$ converges to zero. If $f$ is continuous at $0$, then \$ \lim_{n\rightarrow\infty} f(y_{n})\$ exists and equals $f(0)$, which is
$0$ by part (i). So
$$
\lim_{n\rightarrow\infty} f(x_{n}) = \lim_{n\rightarrow\infty} f(a + y_{n}) = f(a) + \lim_{n\rightarrow\infty} f(y_{n}) = f(a) + f(0) = f(a).
$$
    4. Firstly, assume $n\in\mathbb{N}$ and use induction. It is true for $n = 1$. Assume it holds for some $n\in\mathbb{N}$, then
$$
f(n+1) = f(n) + f(1) = nk + k = (n+1)k.
$$
So by induction, the result holds for all $n\in\mathbb{N}$.
Combine this with part (ii), to extend to all $n\in \mathbb{Z}$.
    5. Consider $\frac{p}{q}\in\Q$, where $p\in \mathbb{Z}$ and $q\in \N$. By (iv),
$$
pk = f(p) = f\left(q\cdot \frac{p}{q}\right) = qf\left(\frac{p}{q}\right),
$$ and the result follows.
    6. We have already proved this for rational $x$, so suppose that $x$ is irrational. Then we can find a sequence $\left(\frac{p_{n}}{q_{n}}\right)$ of rational numbers that converges to $x$ (as we did in the solution to Example 4.2.4). Then using (iii), (v) and algebra of limits, we have
$$
f(x) = \lim_{n\rightarrow\infty} f\left(\frac{p_n}{q_n}\right) =   \lim_{n\rightarrow\infty} k \frac{p_n}{q_n}=k \lim_{n\rightarrow\infty} \frac{p_n}{q_n} = kx.
$$
\vspace{1em}11. %21
Suppose that $x \in \Q$. Then as in the solution to Example 4.2.4 we can find a sequence $(x_{n})$ of irrationals that converges to $x$ and then
$$
\lim_{n\rightarrow\infty} g(x_{n}) = 0 \neq g(x),
$$
and so $g$ is not continuous at $x$.


\vspace{1em}
12. %22 - HW2 question
The function ${\bf 1}_{(a, b)}$ is left continuous at $a$ (but not right continuous), and right continuous at $b$ (but not left continuous).
To prove the left continuity at $a$, let $(x_{n})$ be any sequence in $\R$ which converges to $a$ with $x_{n} < a$ for all $n\in\mathbb{N}$. Then
\$ \lim_{n\rightarrow\infty} {\bf 1}_{(a, b)}(x_{n}) = 0 = {\bf 1}_{(a, b)}(a). \$ On the other hand to see that it is not right continuous at $a$, let $(y_{n})$ be any sequence in $\R$ which converges to $a$ with $a < y_{n} < b$ for all $n\in\mathbb{N}$. Then
\$ \lim_{n\rightarrow\infty} {\bf 1}_{(a, b)}(y_{n}) = 1 \neq {\bf 1}_{(a, b)}(a). \$ The other assertion is proved similarly.

[Contrast this with ${\bf 1}_{[a, b]}$, which was discussed in the notes.]


\vspace{1em}
13. %23
Since $f$ is continuous on $[a, b]$, so is $g$. We have $g(a) = f(a) - \gamma < 0$ and $g(b) = f(b) - \gamma > 0$. Hence by the intermediate value theorem (Theorem \iflatexml  2.3.1 \else [ivp](#ivp) \fi), there exists $c \in (a, b)$ with $g(c) = 0$, i.e. $f(c) = \gamma$, as was required.


\vspace{1em}
14. %24
[label={(\roman*)}]    1. If $f$ is continuous on $\R$ it is continuous on $[a, b]$ for each $a < b$. If $f$ is not a constant, we must be able to find $a, b$ such that $f(a) \neq f(b)$. Now either $f(a) < f(b)$ or $f(a) > f(b)$. Assume the former (without loss of generality). Then there exists $m, n \in \Z$ with $m < n$ such that $f(a) = m$ and $f(b) = n$. Hence by Corollary~\iflatexml 2.3.2 \else [ivp2](#ivp2)\fi, there exists $c \in (a, b)$ so that $f(c) = m + \frac{1}{2} \notin\mathbb{Z}$, and that is the desired contradiction.
    2. Argue as in (i), using the fact that between any two rational numbers, we can find an irrational number.
\vspace{1em}15. %25 - HW3 question
{\it Something} is $x$. That is, define $g:[a,b]\to\R$ given by
$g(x) = f(x) - x$. Then $g$ is continuous (because $f$ is and the function $h(x)=x$ is, and using algebra of limits).
Since the range of $f$ is contained in $(a, b)$, we have $f(a) > a$ and $f(b) < b$, and so $g(a) = f(a) - a > 0$ and $g(b) = f(b) - b < 0$.
So we can apply the intermediate value theorem to
the function $g$ on $[a,b]$. This says that there exists $c \in (a, b)$ such that $g(c) = 0$, i.e. $f(c) = c$.

For the counter--example, consider $f(x) = x^2$. It is continuous on $(0, 1)$ but there is no $c \in (0, 1)$ for which $c^2 = c$.


\vspace{1em}
16. %26
Define $\gamma = \inf_{x \in [a, b]}f(x)$ and assume that it is not attained, so $\gamma < f(x)$ for all $x \in [a,b]$. Then consider the function $h:[a,b]\to \R$ given by $h(x) = \ds\frac{1}{f(x) - \gamma}$. This is continuous, and hence bounded on $[a, b]$. So there exists $K \geq 0$ such that $|h(x)| \leq K$ for all $x \in [a, b]$. By Problem
15(ii), given any $\varepsilon > 0$, there exists $x \in [a, b]$ such that $f(x) < \gamma + \varepsilon$. Now take $\varepsilon = \frac{1}{K}$ to deduce that $h(x) > K$, which yields the required contradiction.


\vspace{1em}
17. %27
By algebra of limits, $\frac{1}{f}$ is continuous on $[0, 1]$ and so is bounded by Theorem \iflatexml 2.3.6 \else [thm:evt](#thm:evt) \fi .


\vspace{1em}
18. %28 - HW3 question
If $f$ is continuous on $[0, 1]$, then it is bounded by Theorem \iflatexml 2.3.6 \else [thm:evt](#thm:evt) \fi , and so there exists $L \geq 0$ such that $|f(x)| \leq L$ for all $x \in [0, 1]$. Hence the range of $f$ is a subset of  $[-L, L]$ and cannot be all of $\R$.


\vspace{1em}
19. %29
Since $(x_{n})$ is bounded, by the Bolzano--Weierstrass theorem it has a convergent subsequence $(x_{n_{k}})$. Let $c=\lim_{k \rightarrow \infty}x_{n_{k}}$ and note that $c \in [0, 1]$, since $x_{n_k}\in[0,1]$ for all $k$.

A straight-forward induction argument shows that $f(x_{n_{k}}) \leq r^{n_{k}-1}f(x_{n_{1}})$ for all $k\in\N$. But then, since the range of $f$ is contained in $[0,1]$, we have
$$
0 \leq f(x_{n_{k}}) \leq r^{n_{k}-1}
$$
for all $k\in\N$. Since $r < 1$, $\lim_{k\to\infty} r^{n_k-1} =0$. By the sandwich rule, \$ \lim_{k \rightarrow \infty}f(x_{n_{k}}) = 0\$ and by continuity of $f$ at $c$, $f(c) = \lim_{k \rightarrow \infty}f(x_{n_{k}})$, so $f(c)=0$.


\vspace{1em}
20. %30
For all $x > y$,
$$
x^{n} - y^{n} = (x - y)(x^{n-1} + x^{n-2}y + \cdots + xy^{n-1} + y^{n-1}) > 0.
$$


\vspace{1em}
21. %31
For all $-\frac{\pi}{2} \leq x < y \leq \frac{\pi}{2}$,
$$
\sin(y) - \sin(x) = 2\sin\left(\frac{y - x}{2}\right)\cos\left(\frac{y + x}{2}\right) > 0,
$$
so the function is strictly monotonic increasing on this interval. It is also continuous (stated in notes), and so by Theorem \iflatexml 2.3.10 \else [thm:IFT](#thm:IFT) \fi , it is has a continuous inverse $f^{-1}(x) = \arcsin(x)$ (or $\sin^{-1}(x)$) defined on $[-1, 1]$. Outside the interval $\left[-\frac{\pi}{2}, \frac{\pi}{2}\right]$, the function $f$ might fail to be strictly increasing. In fact it is strictly decreasing on each interval of the form $\left((4n+1)\frac{\pi}{2}, (4n + 3)\frac{\pi}{2}\right)$, and strictly increasing on each interval of the form $\left((4n-1)\frac{\pi}{2}, (4n + 1)\frac{\pi}{2}\right)$, where $n\in\mathbb{Z}_+$.


\vspace{1em}
22. %32
We seek a continuous extension of the mapping $x\mapsto \frac{1-x}{1-x^{\frac{m}{n}}}$ to a domain that includes $1$. Then, we can use continuity to evaluate the limit as $x\rightarrow 1$.

Observe that, if we write $y = x^{\frac{1}{n}}$, then
$$
\frac{1 - x}{1 - x^{\frac{m}{n}}} = \frac{1 - y^{n}}{1 - y^{m}} = \frac{\;\frac{1}{1-y^m}\;}{\;\frac{1}{1-y^n}\;} = \frac{1+y+y^2+\ldots+y^{m-1}}{1+y+y^2+\ldots+y^{n-1}},
$$
by the geometric sum formula. Note that the left hand side is not defined at $x=1$, but the right hand side is.

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


\vspace{1em}
23. %33
We claim that if $a < x < b$, we have $f(a) < f(x) < f(b)$. To see this, note that if $f(a) \geq f(x)$ then either $f(a) = f(x)$, or $f(a) > f(x)$.

If $f(a)=f(x)$, then $f$ cannot be bijective, which is a contradiction. T

Suppose that $f(a)>f(x)$. Applying Corollary~\iflatexml 2.3.7 \else [interval](#interval)\fi to $f|_{[x,b]}$, the image of $[x,b]$ under $f$ must an interval, $[m,M]$, say. Note that $f(a)\in(m,M)$: indeed, $f(a)>f(x)>M$, and $f(a)<f(b)<m$. Therefore, by the intermediate value theorem (or Corollary~\iflatexml 2.3.2 \else [ivp2](#ivp2)\fi more specifically), there exists $c \in (x, b)$ such that $f(c) = f(a)$, and this again violates the injectivity of the mapping $f$. A similar argument can be used to show that we cannot have $f(b) \leq f(x)$.

Finally, applying our initial result to $f|_{[a, y]}$, we see that if $a<x<y<b$, then $f(a) < f(x) < f(y)$. Hence $f$ is strictly monotonic increasing.


\vspace{1em}
24. %34
First observe that $f+g$ is monotonic increasing since both $f$ and $g$ are. Choose $a \in \R$. Given $\varepsilon > 0$, there exists $\delta > 0$ so that if $x > a + \delta$ then
$$
|f(x) + g(x) - f(a) - g(a)|  =  f(x) + g(x) - f(a) - g(a) < \varepsilon,
$$
and so
$$
|f(x) - f(a)| = f(x) - f(a) < \varepsilon +g(a) - g(x) < \varepsilon,
$$
as $g$ is increasing. This proves that $g$ is right--continuous at $a$. A similar argument (interchanging the roles of $a$ and $x$) proves that it is left--continuous, and hence continuous at $a$.
Then $g = (f + g) - f$ is the difference of two continuous functions, and hence is itself continuous.


\vspace{1em}
25. %35
[label={(\roman*)}]    1. If $0<a<1$, then $0<a<\sqrt{a}<1$. So $(x_n)$ is monotonic increasing and bounded above by $1$, and hence converges to some limit $0\leq l\leq 1$. By continuity of the square root function, $\sqrt{l}=\lim_{n\rightarrow\infty}\sqrt{x_n}$. But $\sqrt{x_n}=x_{n+1}\rightarrow l$ as $n\rightarrow\infty$. By uniqueness of limits, $\sqrt{l}=l$, and so $l=1$.

If instead $a>1$, then $a>\sqrt{a}>1$, and so $(x_n)$ is monotonic decreasing and bounded below by $1$. So the sequences converges to a limit, and by an identical argument to above, this limit has to be $1$.
    2. For all $a>0, n\in\mathbb{N}, f(a) = f\left(a^{\frac{1}{2}}\right) = \cdots = f\left(a^{\frac{1}{2^{n-1}}}\right)$. That is, $f(a)=f(x_n)$ for all $n\in\N$. By continuity,
$$
f(a) = \lim_{n\rightarrow\infty} f(x_n) = f\left(\lim_{n\rightarrow\infty} x_n\right) = f(1).
$$
If $a<0$, then $a^2>0$ and so $f(a)=f\left(a^2\right)=f(1)$. Finally, by continuity,
$$
f(0)=\lim_{x\rightarrow 0}f(x) = \lim_{x\rightarrow 0}f(1) = f(1),
$$
and we have shown that $f(x)=f(1)$ for all $x\in\mathbb{R}$.

## 1.3. Differentiation

1. %36
This is Definition \iflatexml 1.2.3 \else [def:functionlimit](#def:functionlimit) \fi in the notes:

The function $f$ has limit $l$ at the point $a$ if for every sequence  $(x_n)$ in $A$ with $x_n\neq a$ for all $n$ and $\lim_{n\to\infty} x_n=a$, we have $\lim_{n\to\infty}f(x_n)=l$. We write $\lim_{x\to a}f(x)=l$.


\vspace{1em}
2. %37 - HW4 question
[label={(\roman*)}]    1. This is Definition \iflatexml 3.2.1 \else [def:functionlimit](#def:functionlimit) \fi in the notes: we say that $f$ is {\it differentiable} at $a \in A$ if \$ \lim_{x \rightarrow a}\frac{f(x) - f(a)}{x - a}\$ exists. Or, equivalently,
\$ \lim_{h \rightarrow 0}\frac{f(a +h) - f(a)}{h}\$ exists.

That is, we fix $a\in A$ and we consider the function $g$ given by $g(h)=\frac{f(a +h) - f(a)}{h}$. Then $f$ is differentiable at $a$ if the limit of $g$ as $h$ goes to zero exists.
    2. This is Definition \iflatexml 1.2.3 \else [def:functionlimit](#def:functionlimit) \fi from the notes, the definition of limit of a function in terms of sequences. It's very important to understand that it's not applied directly to $f$ here; it's applied to the function $g$ above:

$f$ is differentiable at $a$ if there exists some number $f'(a) \in \R$ for which, given any sequence $(h_{n})$ that converges to $0$, with $h_n\neq 0$ for all $n$, we have
$$
\frac{f(a + h_{n}) - f(a)}{h_{n}} \rightarrow f'(a) \hspace{1em} \text{ as } \hspace{1em} n\rightarrow\infty.
$$
    3. This is asking for the equivalent description of limit of a function given by the $(\varepsilon - \delta)$ criterion (Theorem \iflatexml 1.2.6 \else [ed](#ed) \fi).
Again it needs to be applied to $g$ as above not $f$ itself:

We say $f$ is differentiable at $a$ if there exists a number $f'(a)$ for which, given $\varepsilon>0$, there exists $\delta > 0$ such that if $0<|h| < \delta$, then 	
$$
\left|\ds\frac{f(a+h) - f(a)}{h} - f'(a)\right| < \varepsilon.
$$
\vspace{1em}3. Let $x\in\R\setminus\{0\}$. Then
$$
\begin{align*}
\frac{f(x + h) -f(x)}{h} &= \frac{1}{h}\left(\frac{1}{x+ h} -\frac{1}{x}\right)\\
&= -\frac{1}{x(x+h)} \rightarrow -\frac{1}{x^{2}},~\mbox{as}~h \rightarrow 0. 
\end{align*}
$$

Thus $f$ is differentiable at all $x\in\R\setminus\{0\}$ and
$f'(x)=-\frac{1}{x^2}$ for all $x\in\R\setminus\{0\}$.

The extended function (where we define its value at $x=0$ to be zero) is not continuous at $x=0$, since $\lim_{x \rightarrow 0^+}\frac{1}{x} =\infty$.
Therefore it is not differentiable at $x=0$, by Theorem \iflatexml  3.2.4 \else [dcont](#dcont) \fi.


\vspace{1em}
4. As in the hint, let \$g(h) = e^{kh} - 1 - kh \$. Then
$$
\begin{align*}
\frac{f(x + h) -f(x)}{h} &= \frac{1}{h}(e^{k(x +h)} - e^{kx})\\
&= e^{kx}\frac{1}{h}(e^{kh} - 1) = e^{kx}\left(k + \frac{g(h)}{h}\right) \rightarrow ke^{kx},~\mbox{as}~h \rightarrow 0,
\end{align*}
$$

using the given fact that  $\lim_{h \rightarrow 0}\frac{g(h)}{h} = 0$. Thus $f$ is differentiable at each $x\in\R$ and $f'(x)=ke^{kx}$.


\vspace{1em}
5. 
[label={(\roman*)}]    1. Using the product and chain rules for differentiation, and that $\sin$ is differentiable with derivative $\cos$,
if $x \neq 0$, $f$ is differentiable at $x$ with $f'(x) = \sin\left(\frac{1}{x}\right) - \frac{1}{x}\cos\left(\frac{1}{x}\right)$.
    2. But
$\frac{f(x) - f(0)}{x} = \sin\left(\frac{1}{x}\right)$ has no limit as $x \rightarrow 0$ (see Problem~[q:50](#q:50)), so $f$ is not differentiable at $0$.
\vspace{1em}6. Again using the product and chain rules
and standard derivatives,
for $x \neq 0$,
$f$ is differentiable at $x$ with
\$ f'(x) = 2x\sin\left(\frac{1}{x}\right) - \cos\left(\frac{1}{x}\right)\$. At $x = 0,$
$$
\lim_{x \rightarrow 0}\frac{f(x) - f(0)}{x} = \lim_{x \rightarrow 0}x\sin\left(\frac{1}{x}\right) = 0,
$$
by Problem~[q:51](#q:51). So
$f$ is differentiable at $0$ with
$f'(0) = 0$. For the second derivative, with $x \neq 0$, we have
$$
f^{\prime \prime}(x) = 2\sin\left(\frac{1}{x}\right) - \frac{2}{x}\cos\left(\frac{1}{x}\right) - \frac{1}{x^{2}}\sin\left(\frac{1}{x}\right).
$$
But $f^{\prime \prime}$ doesn't exist at $x = 0$, as in Problem~[q:83](#q:83).


\vspace{1em}


undefined. We give sketches of simple examples of functions as described. There should be some kind of ``corner'' or ``cusp''
at the relevant points, so that there is clearly no well-defined gradient there. But the functions are required to be continuous, so there should be no jump or other discontinuity.
[label={(\roman*)}]7. \hspace{1em}

\iflatexml
![](figs/nondiff1,2)
\else
$$
\begin{tikzpicture}
\begin{axis}[width=.9\linewidth, xlabel=$x$, ylabel=$y$, unit vector ratio*=1 1 1, xmin=-.3, xmax=1.3, ymin=-.25, ymax=.7, axis lines=middle, tick align=outside, xtick={.5,1}, ytick={0}, xticklabels={$\frac{1}{2}$,$1$}, yticklabels={}, samples=1000]
\addplot[domain=0:1,no marks,thick] {abs(x-.5)};
\draw[dashed] (axis cs:1,0)--(axis cs:1,5);
\end{axis}
\end{tikzpicture}
$$
\fi
Graph of a function $f:[0,1]\to\R$ that is not differentiable at $\frac{1}{2}$, but is everywhere else.
8. \hspace{1em}

\iflatexml
![](figs/nondiff1,3_2,3)
\else
$$
\begin{tikzpicture}
\begin{axis}[width=.9\linewidth, xlabel=$x$, ylabel=$y$, unit vector ratio*=1 1 1, xmin=-.3, xmax=1.3, ymin=-.25, ymax=.5, axis lines=middle, tick align=outside, xtick={.333,.666,1}, ytick={0}, xticklabels={$\frac{1}{3}$,$\frac{2}{3}$,$1$}, yticklabels={}, samples=1000]
\addplot[domain=0:.333,no marks,thick] {.333-x};
\addplot[domain=.333:.666,no marks,thick] {-(3*x-1)*(3*x-2)};
\addplot[domain=.666:1,no marks,thick] {x-.666};
\draw[dashed] (axis cs:1,0)--(axis cs:1,5);
\end{axis}
\end{tikzpicture}
$$
\fi
Graph of a function $f:[0,1]\to\R$ that is differentiable at all points in its domain apart from $\frac{1}{3}$ and $\frac{2}{3}$.
\vspace{1em}undefined. It helps to sketch the graph. On the interval $[0,1]$, we have $[x]=0$ and so the graph resembles $y=x$. This pattern then repeats, and we have the following graph for $f(x)=x-[x]$:

\iflatexml
![](figs/x-%5Bx%5D)
\else
$$
\begin{tikzpicture}
\begin{axis}[width=.9\linewidth, xlabel=$x$, ylabel=$y$, unit vector ratio*=1 1 1, xmin=-2.5, xmax=2.5, ymin=-1, ymax=1.5, axis lines=middle, tick align=outside, xtick={-2,-1,1,2}, ytick={1}, xticklabels={$-2$,$-1$,$1$,$2$}, yticklabels={$1$}, samples=1000]
\addplot[domain=-2.5:-2,no marks,thick] {x-floor(x)};
\addplot[domain=-1.999:-1,no marks,thick] {x-floor(x)};
\addplot[domain=-.999:-.001,no marks,thick] {x-floor(x)};
\addplot[domain=0.001:.999,no marks,thick] {x-floor(x)};
\addplot[domain=1.001:2,no marks,thick] {x-floor(x)};
\addplot[domain=2.001:2.5,no marks,thick] {x-floor(x)};
\node[fill=black,scale=.4,circle] at (axis cs:-2,0){};
\node[fill=black,circle,scale=.4] at (axis cs:-2,1){};
\node[fill=white,circle,scale=.3] at (axis cs:-2,1){};
\node[fill=black,scale=.4,circle] at (axis cs:-1,0){};
\node[fill=black,circle,scale=.4] at (axis cs:-1,1){};
\node[fill=white,circle,scale=.3] at (axis cs:-1,1){};
\node[fill=black,scale=.4,circle] at (axis cs:0,0){};
\node[fill=black,circle,scale=.4] at (axis cs:0,1){};
\node[fill=white,circle,scale=.3] at (axis cs:0,1){};
\node[fill=black,scale=.4,circle] at (axis cs:1,0){};
\node[fill=black,circle,scale=.4] at (axis cs:1,1){};
\node[fill=white,circle,scale=.3] at (axis cs:1,1){};
\node[fill=black,scale=.4,circle] at (axis cs:2,0){};
\node[fill=black,circle,scale=.4] at (axis cs:2,1){};
\node[fill=white,circle,scale=.3] at (axis cs:2,1){};
%\draw[dashed] (axis cs:1,0)--(axis cs:1,5);
\end{axis}
\end{tikzpicture}
$$
\fi
Graph of the function $f:\mathbb{R}\to\mathbb{R}$; $f(x)=x-[x]$.

The function $f$ is differentiable for all $x \in \R \setminus \Z$. For such points, taking $h>0$ sufficiently small, we have
$[x+h]=[x]$ and so

$$
\frac{f(x+h)-f(x)}{h} = \frac{(x + h)- [x + h] - x + [x]}{h} = \frac{h}{h}=1.
$$

Thus $f'(x) = 1$  for all $x \in \R \setminus \Z$. If $x \in \Z$, then $f$ is not continuous at $x$  (it has a jump discontinuity of $-1$ there) and so cannot be differentiable there (by Theorem \iflatexml  3.2.4 \else [dcont](#dcont) \fi).

\vspace{1em}
9. %44
First observe that if $f$ is differentiable at $a$, then
$$
f'(a) = \lim_{h \rightarrow 0}\frac{f(a + h) - f(a)}{h} = \lim_{h \rightarrow 0}\frac{f(a - h) - f(a)}{-h} = \lim_{h \rightarrow 0}\frac{f(a) - f(a-h)}{h}.
$$ So
$$
\begin{align*}
\frac{f(a+ h) - f(a - h)}{2h} &=  \frac{1}{2}\left(\frac{f(a + h) - f(a)}{h} +  \frac{f(a) - f(a-h)}{h}\right) \\
&\hspace{7em}\rightarrow  \frac{1}{2}2f'(a) = f'(a),~\mbox{as}~h \rightarrow 0. 
\end{align*}
$$


On the other hand, by Example 5.2.5, $f:\R\to\R$ given by
$f(x)=|x|$ is not differentiable at $x=0$. But
$$
\lim_{h \rightarrow 0^+} \ds\frac{|h|-|{}-h|}{2h} =0.
$$


%\vspace{1em}

%
10. %45
%Let $f:A\to\R$ be a function and $a\in A$. Assume there is some interval $(a-\varepsilon,a+\varepsilon)\subseteq A$ containing $a$ (this is necessary for $f$ to be differentiable at $a$, and to have left and right derivatives). Consider the mapping
%	$$
g_{a}: (-\varepsilon,\varepsilon)\setminus \{0\} \rightarrow \R;\hspace{1em} g_{a}(h) = \frac{f(a+h) - f(a)}{h}.
$$
%By Theorem \iflatexml 1.3.2 \else [thm:lrlims](#thm:lrlims) \fi, $g_a(h)$ will tend to a limit as $h\rightarrow 0$ if and only if the left and right limits of $g_a$ exist and agree at $0$.

%In other words, $f'(a)$ exists if and only if $f'_{-}(a)$ and $f'_+(a)$ both exist and are equal, in which case
%	$$
f'_-(a)=f'_+(a) = f'(a).
$$
%This is precisely the statement of Theorem \iflatexml 3.2.7 \else [lrd](#lrd) \fi.


\vspace{1em}
11. %45
[label={(\roman*)}]    1. True: $f$ is continuous at zero as $f(0) = 0= \lim_{x \rightarrow 0^-}f(x) = \lim_{x \rightarrow 0^+}f(x)$.
    2. True: $f'(0)$ exists and is zero. To see this compute
$$
f'_{+}(0) = \lim_{h \rightarrow 0^+}\frac{h^{2}}{h} = \lim_{h \rightarrow 0^+} h= 0.
$$
and
$$
f'_{-}(0)= \lim_{h \rightarrow 0^-}\frac{-h^{2}}{h} = \lim_{h \rightarrow 0^-} -h =0.
$$
    3. True: $f'$ is continuous at zero since $f':\R\to\R$ is given by
$$
f'(x) = \left\{\begin{array}{c c} -2x & ~\mbox{if}~x < 0\\ 0& ~\mbox{if}~x =0 \\ 2x & ~\mbox{if}~x > 0 \end{array} \right.,
$$
so $f'(0) = \lim_{x \rightarrow 0^-} f'(x) = \lim_{x \rightarrow 0^+}f'(x) = 0$.
    4. False:  $f^{\prime \prime}_{+}(0) = \lim_{h \rightarrow 0^+}\frac{2h - 0}{h} = 2, f^{\prime \prime}_{-}(0) = \lim_{h \rightarrow 0^-}\frac{-2h - 0}{h} = -2$, and so $f^{\prime \prime}(0)$ does not exist.
\vspace{1em}12. %46
[label={(\roman*)}]    1. Yes:
$f$ is differentiable on $[a, b]$ and hence continuous on $[a, b]$ by Theorem \iflatexml  3.2.4 \else [dcont](#dcont) \fi, so it attains its sup and inf on $[a, b]$ by the extreme value theorem, Theorem \iflatexml 2.3.6 \else [thm:evt](#thm:evt) \fi, and these are the maximum and minimum (respectively).
    2. No: the maximum or minimum could be $f(a)=f(b)$.
If $f(a)$ is not the maximum value, then this must occur in $(a, b)$.
Similarly for the minimum.
If $f(a) = f(b)$ is both the maximum and minimum value, then $f$ is constant, and the value occurs in $(a, b)$.
\vspace{1em}13. %47
Following the hint, define $g:\R\rightarrow \R$ by
$$
g(x) = a_{0}x + \frac{a_{1}}{2}x^{2} + \frac{a_{2}}{3}x^{3}  + \cdots + \frac{a_{n}}{n+1}x^{n}.
$$
Then $g$ is a polynomial, so it is differentiable on $[0, 1]$ and using standard derivatives, $g'(x)=f(x)$. Also $g(0) = g(1) = 0$. So by Rolle's theorem, there exists $c \in (0, 1)$ such that $g'(c) = 0$, i.e.$f(c) = 0$.


\vspace{1em}
14. %48
[label={(\roman*)}]    1. Let $x, y$ be such that $a \leq x < y \leq b$. We want to show that $f(x)=f(y)$.

Apply the mean value theorem to the restriction of $f$ to the interval $[x, y]$, to find there exists $d \in (x, y)$ for which
$$
f(y) - f(x) = f'(d)(y-x).
$$
By assumption, $f'(c)=0$ for all $c\in(a,b)$, so $f'(d)=0$.

Thus $f(x)=f(y)$. Since this holds for all $x,y\in [a,b]$, $f$ is constant on $[a,b]$.
    2. Define $f:\R\to\R$ by $f = h-g$. Then the function $f$ is continuous on $[a,b]$ and differentiable on $(a,b)$, because $g$ and $h$ are, and $f'(x)=h'(x)-g'(x)=0$ for all $x\in (a,b)$. Thus $f$ satisfies all the conditions of (i). By part (i), $f$ is constant on $[a,b]$. That is, there exists some $k\in \mathbb{R}$, such that $f(x)=k$ for all $x\in [a,b]$. Thus $h(x)=g(x)+k$ for all $x\in [a,b]$.
\vspace{1em}15. %49
By the mean value theorem, $f(b) = f(a) + f'(c)(b - a)$ for some $c\in (a,b)$. So, since $m \leq f'(c) \leq M$, for all $c \in (a, b)$,
$$
f(a) + m(b - a) \leq f(b) \leq f(a) + M(b - a).
$$


%\vspace{1em}

%
16. % "inverses revisited"
%The function $f$ is differentiable on $[0, \pi]$ with $f'(x) = -\sin(x) < 0$ on $(0, \pi)$. So by Corollary [mond](#mond) it is strictly decreasing on $[0, \pi]$. Hence by the inverse function theorem, Theorem \iflatexml 2.3.10 \else [thm:IFT](#thm:IFT) \fi , it has a strictly decreasing inverse on  $[f(\pi), f(0)]=[-1, 1]$ which is continuous on $(-1, 1)$. This is precisely the function $f^{-1}(x) = \cos^{-1}(x)$ or $\arccos(x)$. Also $x \mapsto -\sin(x)$ is  continuous on $(0, \pi)$, so by Theorem [invd](#invd), $f^{-1}$ is differentiable on $(-1, 1)$, and
%	$$
\begin{align*}
%	(f^{-1})'(y) &= \frac{1}{f'(x)}=-\frac{1}{\sin(x)}=-\frac{1}{\sqrt{1-\cos^2(x)}}\\
%	&=-\frac{1}{\sqrt{1 - y^{2}}},
%	\end{align*}
$$ for all $y \in (-1, 1)$, where $y=f(x)=\cos(x)$.


\vspace{1em}
17. %50
The polynomial $p$ is of odd degree so it has at least one real root by Corollary~\iflatexml 2.3.3 \else [pol](#pol)\fi. Also $p$ is differentiable with $p'(x) = 3x^{2} + r > 0$, for all $x \in \R$, so $p$ is strictly monotonic increasing on any closed interval $[a, b]$, and hence on the whole of $\R$, by Corollary~\iflatexml 3.5.2 \else [mond](#mond)\fi. Then by the inverse function theorem (Theorem \iflatexml 2.3.10 \else [thm:IFT](#thm:IFT) \fi), $p$ is invertible and hence injective, and so there is exactly one zero.


\vspace{1em}
18. %51
Let $r>1$ and fix $y\in (0,1)$. Apply the mean value theorem to the function $f:[y,1]\to\R$ given by $f(x) = x^r$. Then there exists $c \in (y, 1)$ such that
$$
\frac{f(1)-f(y)}{1-y}=f'(c)=rc^{r-1}.
$$
Now, $0<c<1$, and $r>1$, so $c^{r-1}<1$. Thus
$$
1 - y^r = rc^{r-1}( 1- y) < r(1 - y).
$$


\vspace{1em}
19. %52
Consider the first case. Here we have
$$
f''(a) = \lim_{h \rightarrow 0}\frac{f'(a + h) - f'(a)}{h} =  \lim_{h \rightarrow 0}\frac{f'(a + h)}{h} < 0.
$$
In particular, $f^{\prime \prime}_{+}(a) = \lim_{h \rightarrow 0^+}\frac{f'(a + h)}{h} < 0$, and so $f'(a + h) < 0$ for sufficiently small positive $h$, (say $0 < h < \delta$), in which case, by Corollary~\iflatexml 3.5.2 \else [mond](#mond)\fi, $f$ is strictly decreasing on $[a,  a + \delta]$. We also have $f^{\prime \prime}_{-}(a) = \lim_{h \rightarrow 0^-}\frac{f'(a + h)}{h} < 0$, and so $f'(a + h) > 0$ for sufficiently small negative $h$, (say $-\delta_{1} < h < 0$), in which case, by Corollary~\iflatexml 3.5.2 \else [mond](#mond)\fi, $f$ is strictly increasing on $[a- \delta_{1}, a]$. Then it follows that $f$ has a local minimum at $a$. The other case is similar.

%
20. $g$ is differentiable and hence continuous on $[a, b]$. We have $g'(b) = f'(b) - \gamma > 0$ and $g'(a) = f'(a) - \gamma < 0$, so $a$ and $b$ are not extreme points for $g$. But $g$ must attain its sup and inf in $[a, b]$ by Theorem \iflatexml 2.3.6 \else [thm:evt](#thm:evt) \fi. Since $f'$ is continuous on $[a, b]$, so is $g'$, and by Problem~[q:61](#q:61), $g' > 0$ in a neighbourhood of $b$ and $g' < 0$ in a neighbourhood of $a$. Then by Corollary [mond](#mond), $g$ is increasing in a neighbourhood of $b$ and decreasing in a neighbourhood of $a$. So it attains its minimum  in $(a, b)$, and this is an extreme point. Hence $g'(c) = 0$ and the result follows.


%\vspace{1em}


%
21. %54
%The function $h$ from the hint is continuous on $[a, b]$ and differentiable on $(a, b)$, since $f$ and $g$ are.
%After some algebraic manipulation, we obtain
%	$$
h(a) = h(b) = \frac{f(a)g(b) - f(b)g(a)}{g(b) - g(a)}.
$$
%Thus $h$ satisfies the conditions of Rolle's theorem,
%and so by Rolle's theorem, there exists $c \in (a, b)$ such that $h'(c) = 0$ and so $f'(c) = \rho g'(c)$. Thus $\frac{f'(c)}{g'(c)}=\rho$, as required.


%\vspace{1em}

%
22. %Applying l'H\^{o}pital's rule to the given limit expression yields
%	$$
\lim_{h \rightarrow 0^+}\frac{f(a+ h) - 2f(a) + f(a-h)}{h^{2}} = \lim_{h \rightarrow 0^+}\frac{f'(a+h) - f'(a-h)}{2h},
$$
%and then the result follows from the result of Problem~[q:87](#q:87).


%\vspace{1em}

%
23. %
[label={(\roman*)}]
%    1. Let $\varepsilon>0$. Since $\lim_{x\rightarrow a-}\frac{f'(x)}{g'(x)} = L$, we can choose $\delta_1>0$ such that
%	$$
\left|\frac{f'(x)}{g'(x)}-L\right| < L \hspace{2em} \text{ for all } x\in(a,a+\delta_1).
$$
%Since $\lim_{x\rightarrow a-}f(x) = \lim_{x\rightarrow 1-}g(x) = \infty$, we can choose $\delta_2 \in (a, b)$ such that $f(x) > 1$ and $g(x) > 1$ for all $x\in(a,a+\delta_2)$. In particular, $f(x)\neq 0\neq g(x)$ in this interval.

%Finally, if we take $\delta=\min\{\delta_1,\delta_2\}$, then all three conditions will be met on the interval $(a,a+\delta)$.

%
    2. Let $a<x<y<a+\delta$ Since $g'$ does not vanish on $(a,b)$, we can apply Cauchy's mean value theorem to $f$ and $g$ and for the interval $[x,y]$. Therefore, there is $c_{x,y}\in(x,y)$ such that
%	$$
\frac{f'(c_{x,y})}{g'(c_{x,y})} = \frac{f(x)-f(y)}{g(x)-g(y)}.
$$

%
    3. We know that $c\in(x,y)\subseteq(a,a+\delta)$, and so by part (i)
%	$$
L-\varepsilon < \frac{f'(c_{x,y})}{g'(c_{x,y})} < L+\varepsilon.
$$
%Therefore by (ii)
%	$$
L-\varepsilon < \frac{f(x)-f(y)}{g(x)-g(y)} < L+\varepsilon,
$$
%and a simple rearrangement (noting $g(x)\neq 0$) gives
%	$$
\begin{equation}\label{eq:57}
%	(L-\varepsilon)\left(1-\frac{g(y)}{g(x)}\right) < \frac{f(x)}{g(x)}-\frac{f(y)}{g(x)} < (L+\varepsilon)\left(1-\frac{g(y)}{g(x)}\right).
%	\end{equation}
$$

%
    4. We now let $x\rightarrow a^+$ while holding $y$ fixed (this is possible since $a<x<y$). Note that $\frac{g(y)}{g(x)},\frac{f(y)}{g(x)}\rightarrow 0$ as $x\rightarrow a^+$, and hence in the limit $x\rightarrow a^+$, ([eq:57](#eq:57)) becomes
%	$$
L-\varepsilon \leq \lim_{x\rightarrow a-}\frac{f(x)}{g(x)} \leq L+\varepsilon.
$$
%Since $\varepsilon$ was arbitrary, it follows that
%	$$
\lim_{x\rightarrow a-}\frac{f(x)}{g(x)} = L.
$$
%
%\vspace{1em}


%24. %We apply Taylor's theorem (Theorem [Tay](#Tay)) in the special case $x_0=0$. This special case is also known as Macluarin's theorem.
%
[label={(\roman*)}]
%    1. $R^n(x)=\frac{x^{n}}{n!}e^{c_x}$, for some $c_x$, where $c_x\in (0,x)$ if $x>0$ and $c_x\in (x,0)$ if $x<0$. Thus,
%$R^n(x)=\frac{x^{n}}{n!}e^{\theta x}$ for some  $0 < \theta < 1$.

%
    2. $(-1)^{n}\frac{x^{2n}}{(2n)!}\sin(\theta x)$, for some  $0 < \theta < 1$.
%
    3. $(-1)^{n+1}\frac{x^{2n+1}}{(2n+1)!}\sin(\theta x)$, for some  $0 < \theta < 1$.
%
%\vspace{1em}


%25. %Using Maclaurin's theorem, we can find $0 < \theta < 1$ and $0 < \phi < 1$, such that for all $x \in \R$, \$ \cos(x) = 1 - \frac{x^{2}}{2}\cos(\theta x) \geq 1 - \frac{x^{2}}{2}\$, since $\cos(\theta x) \leq 1$, and \$ \cos(x) = 1 - \frac{x^{2}}{2} + \frac{x^{4}}{24}\cos(\phi x) \leq 1 - \frac{x^{2}}{2} + \frac{x^{4}}{24}\$, since $\cos(\phi x) \leq 1$.

## 1.4. Sequences and series of functions

1. %53
For $x\in [0,\pi ]$ we have $0\leq \sin x<1$ except when $x=\frac{\pi}{2}$, where $\sin x=1$. Thus $f_n(x)$ converges pointwise to the function $f\colon [0, \pi ]\rightarrow \R$ defined by
$$
f(x) = \left\{ \begin{array}{ll}
0 & x\neq \frac{\pi}{2}, \\
1 & x=\frac{\pi}{2}. \\
\end{array} \right.
$$

Each function $f_n$ is continuous. The function $f$ is not continuous. So the sequence $(f_n)$ does not converge uniformly (otherwise we would have a contradiction to Theorem \iflatexml 4.2.1 \else [ucont](#ucont) \fi --- the uniform limit theorem).


\vspace{1em}
2. %54
[label={(\roman*)}]    1. Observe that $(f_n)$ converges pointwise to the function
$$
f(x) = \left\{ \begin{array}{ll}
0 & x=0, \\
1 & x>0. \\
\end{array} \right.
$$

Each function $(f_n)$ is continuous, but the function $f$ is not continuous at $0$, so the convergence cannot be uniform.
    2. Let $x\in \R$. Then for any $n\geq x$, we have $f_n (x) =0$, so the sequence $(f_n)$ converges pointwise to
the zero function.

On the other hand
$$
M_n = \sup \{ |f_n(t) -0| : t\in \R \} = \infty,
$$
so certainly $(M_n)$ does not converge to zero, and the sequence $(f_n)$ therefore does not converge uniformly to the zero function.
    3. For $x>1$, $\frac{1}{x^n} \rightarrow 0$ as $n\rightarrow \infty$. Hence for each $x\in (1,\infty )$, $\frac{e^x}{x^n}\rightarrow 0$ as $n\rightarrow \infty$, and the sequence $(f_n)$ converges pointwise to the zero function.

But $\frac{e^x}{x^n}\rightarrow \infty$ as $x\rightarrow \infty$, so
$$
M_n = \sup \{ |f_n(t) -0| : t\in (1,\infty ) \} = \infty.
$$

So certainly $(M_n)$ does not converge to zero, and the sequence $(f_n)$ therefore does not converge uniformly to the zero function.
    4. We know that $e^{-k}\rightarrow 0$ as $k\rightarrow \infty$, so $f_n(x)\rightarrow 0$ as $n\rightarrow \infty$ if $x\neq 0$. If $x=0$, then $f_n(x)=1$ for all $n$.
So
$(f_n)$ converges pointwise to the function
$$
f(x) = \left\{ \begin{array}{ll}
1 & x=0, \\
0 & x\neq 0. \\
\end{array} \right.
$$

Each function $(f_n)$ is continuous, but the function $f$ is not continuous at $0$, so the convergence cannot be uniform.
    5. The sequence $(f_n)$ clearly does not converge pointwise.
3. %55
We consider $g_n:D\to\R$, and consider the cases $D=[0,1]$ and $D=[0,\infty)$, with $g_n(x)$ given by different expressions in each part below.

By Proposion \iflatexml 4.1.7 \else [prop:uconv](#prop:uconv)\fi, $(g_n)$ will converge uniformly to a function $g$ if and only if
$$
M_n := \sup \{ |g_n(t) -g(t)| : t\in D \} \rightarrow 0 \text{ as } n\rightarrow \infty.
$$
[label={(\roman*)}]    1. If $\ds g_n(x)=\frac{x}{n}$, then for each $x$, $g_n(x)\rightarrow 0$ as $n\rightarrow \infty$, so the sequence $(g_n)$ converges pointwise to the zero function.

On the interval $[0,1]$,
$$
M_n = \sup \{ |g_n(t) -0 | : t\in [0,1] \}  = \frac{1}{n}
$$

Note that $M_n\rightarrow 0$ as $n\rightarrow \infty$, so on the interval $[0,1]$, the sequence $(g_n)$ converges uniformly to the zero function.

On the other hand,  on $[0,\infty )$,
$$
M_n = \sup \{ |g_n(t) -0 | : t\in [0,\infty ) \}  = \infty,
$$
so the sequence $(g_n)$ does not converge uniformly on $[0,\infty )$.
    2. Now consider $\ds g_n(x) := \frac{x^n}{1+x^n}$. Observe that
$$
g_n (x) = \frac{1}{1+\frac{1}{x^n}} \rightarrow \left\{ \begin{array}{ll}
0 & x<1, \\
\frac{1}{2} & x=1, \\
1 & x>1. \\
\end{array} \right.
$$

Thus the pointwise limit function is not continuous on $[0,1]$ or on $[0,\infty )$, so convergence is not uniform on either interval.
    3. Let $\ds g_n(x) =  \frac{x^n}{n+x^n}$.

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

On the other hand the above pointwise limit $g$ is not continuous on $[0,\infty )$, whereas each function $g_n$ is continuous on $[0,\infty )$, so convergence is not uniform on $[0,\infty )$.
\vspace{1em}4. %56
[label={(\roman*)}]    1. Observe that, for all $x\in[0,1]$, $h_n(x)\rightarrow 1$ as $n\rightarrow \infty$.
So $(h_n)$ converges pointwise to the constant function $h:[0,1]\to\R$, $h(x)=1$ for all $x$.

Let
$$
M_n = \sup \{ |h_n(x)-1| : x\in [0,1] \} = 1 - \left(1-\frac{1}{n}\right)^2 =\frac{1}{n^2}-\frac{2}{n}.
$$

So $M_n\rightarrow 0$ as $n\rightarrow \infty$. So $(h_n)$ converges uniformly to the constant function $h$.
    2. We know that $x^n \rightarrow 0$ as $n\rightarrow \infty$ if $0\leq x<1$, and $x^n\rightarrow 1$ as $n\rightarrow \infty$ if $x=1$. Hence $(h_n)$ converges pointwise to the function $h$, where
$$
h (x) =\left\{ \begin{array}{ll}
x & 0\leq x<1, \\
0 & x=1. \\
\end{array} \right.
$$

Each function $h_n$ is continuous, and this limit is not continuous, so convergence is not uniform.
    3. The sequence $(h_n(x))$ has pointwise limit $\frac{1}{1-x}$ if $0\leq x<1$ (geometric series), but it does not converge if $x=1$. Because it does not converge when $x=1$, the sequence of functions $(h_n)$ does not converge
pointwise  on $[0,1]$ (and so it certainly does not converge uniformly on $[0,1]$).
\vspace{1em}5. %57
[label={(\roman*)}]    1. For each $t$, we have
$$
f_n(t) = \frac{n+\cos x}{2n+\sin^2 x} = \frac{1+\frac{\cos x}{n}}{2+\frac{\sin^2 x}{n}} \rightarrow \frac{1}{2}
$$
as $n\rightarrow \infty$. So the sequence $(f_n)$ converges pointwise to the constant function $f:\R\to\R$,
with $f(x)=\frac{1}{2}$ for all $x\in\R$.
    2. Note that, for all $x\in\R$,
$$
\begin{align*}
\left|f_n(x) - \frac{1}{2}\right| =  \left| \frac{2n+2\cos x -2n -\sin^2 x}{2(2n+\sin^2 x)} \right| 
&= \left| \frac{2\cos x -\sin^2 x}{2(2n+\sin^2 x)} \right| \\
&\leq \frac{2+1}{2(2n)}=\frac{3}{4n} \rightarrow 0 
\end{align*}
$$
as $n\rightarrow \infty$.

It follows that $(f_n)$ converges to $f$ uniformly.
    3. Using the quotient rule,
$$
\begin{align*}
f_n'(x) &= \frac{-\sin(x)(2n+\sin^2(x))-(n+\cos(x))\cdot 2\sin(x)\cos(x)}{\left(2n+\sin^2(x)\right)^2} \\
&= \frac{-\sin(x)\left(2n+\sin^2(x)+2n\cos(x)+2\cos^2(x)\right)}{\left(2n+\sin^2(x)\right)^2} \\
&= \frac{-\sin(x)\left(2n+1+2n\cos(x)+\cos^2(x)\right)}{\left(2n+\sin^2(x)\right)^2}.
\end{align*}
$$

Since $f$ is a constant function, $f'(x)=0$ for all $x\in\R$. We show that $f_n'(x)\rightarrow 0$ as $n\rightarrow\infty$, for each $x\in\R$.

We have:
$$
\begin{align*}
|f_n'(x)| &= \frac{|\sin(x)|\left|2n+1+2n\cos(x)+\cos^2(x)\right|}{\left(2n+\sin^2(x)\right)^2} \\
&\leq \frac{2n+1+2n|\cos(x)|+|\cos(x)|^2}{\left(2n\right)^2},
\end{align*}
$$
(using the triangle inequality and the fact that $\sin^2(x)\geq 0$), so
$$
\begin{align*}
|f_n'(x)| &\leq \frac{4n+2}{4n^2} = \frac{2n+1}{2n^2} \rightarrow 0 \text{ as } n\rightarrow \infty.
\end{align*}
$$
Therefore $f_n'(x)\rightarrow 0$ as $n\rightarrow \infty$, for all $x\in\R$.

The conditions of Theorem \iflatexml 4.2.3 \else [udiff](#udiff)\fi will be satisfied if we can prove that $f_n'\rightarrow 0$ uniformly.

We have already shown that $|f_n'(x)|\leq \frac{2n+1}{2n^2}$ for all $x\in\R$ and $n\in\N$, so most of the work is already done here. We have
$$
M_n := \sup\{|f_n(x)|:x\in\R\} \leq \frac{2n+1}{2n^2}\rightarrow 0 \text{ as } n\rightarrow\infty,
$$
so by Proposition \iflatexml 4.1.7 \else [prop:uconv](#prop:uconv)\fi, $f_n'\rightarrow 0$ uniformly. So $(f_n)$ satisfies the conditions of Theorem \iflatexml 4.2.3 \else [udiff](#udiff)\fi.
\vspace{1em}6. %58
[label={(\roman*)}]    1. As indicated in the question, we need to check continuity at $x=0$ and $x=1$.

Let $0<x<1$, so
$$
f_n(x) = \frac{x^{\frac{1}{n}}-1}{\ln x}.
$$

We have $x^{\frac{1}{n}} -1 \rightarrow -1 \neq 0$ as $x\rightarrow 0$, and $\ln x\rightarrow -\infty$ as $x\rightarrow 0$. So clearly
$$
\frac{x^{\frac{1}{n}}-1}{\ln x} \rightarrow 0 =f_n(0)
$$
as $x\rightarrow 0$, and $f_n$ is continuous at $0$.

On the other hand,
$$
x^{\frac{1}{n}} -1 \rightarrow 1-1=0 \qquad \text{and}\qquad \ln x\rightarrow 0
$$
as $x\rightarrow 1$, so by L'H\^opital's rule,
$$
\lim_{x\rightarrow 1} \frac{x^{\frac{1}{n}} -1}{\ln x} = \lim_{x\rightarrow 1} \frac{\left(\frac{1}{n}\right)x^{\frac{1}{n}-1}}{\frac{1}{x}} = \frac{1}{n} = f_n(1),
$$
so  $f_n$ is continuous at $1$.
    2. Since we can assume the function $f_n$ is increasing, we have
$$
|f_n(x) |\leq \frac{1}{n}
$$
for all $x\in [0,1]$. But $\frac{1}{n}\rightarrow 0$ as $n\rightarrow \infty$, so it follows that $(f_n)$ converges uniformly to the
zero function.

%
    3. The result now follows immediately by the uniform convergence theorem for integrals.
%\vspace{1em}
%
%7. %For $0\leq t\leq 1$, we have
%	$$
\left| \frac{e^{t^4}}{n} \right| \leq \frac{e}{n} \rightarrow 0
$$
%as $n\rightarrow \infty$.
%
%Hence the sequence of  functions $\left(\frac{e^{t^4}}{n}\right)$ converges uniformly to the zero function on $[0,1]$. By the uniform convergence theorem for integrals, it follows that
%	$$
\lim_{n\rightarrow \infty} \int_0^1  \frac{e^{t^4}}{n}\ dt = \int_0^1 0\ dt=0 .
$$

%For $1\leq t\leq 2$, we have
%	$$
|t^{2-\frac{\sin nt}{n}} -t^2 | = |t^2| | t^{-\frac{\sin(nt)}{n}} -1 | \leq 4(t^{\frac{1}{n}}-1)\leq 4(2^{\frac{1}{n}}-1) \rightarrow 0
$$
%as $n\rightarrow \infty$.

%Hence the sequence of functions $(t^{2-\frac{\sin (nt)}{n}})$ converges uniformly
%on the interval $[1,2]$
%to the function $f:[1,2]\to\R$ given by $f(t)=t^2$. It follows that
%	$$
\lim_{n\rightarrow \infty} \int_1^2  t^{2-\frac{\sin (nt)}{n}} \ dt = \int_1^2 t^2\ dt = \left[ \frac{t^3}{3} \right]_1^2 = \frac{8}{3} - \frac{1}{3} = \frac{7}{3} .
$$


%
undefined. %See Example 3.13 in the notes, showing that the answer to both parts is ``no''.
%(What is required in Corollary 3.12 is uniform convergence of the sequence of derivatives.).

%\vspace{1em}

%
8. %
[label={(\roman*)}]

%    1. Let $0<x<y\leq \theta$. Then
%	$$
\left| \frac{1}{x} - \frac{1}{y} \right| \geq \frac{|x-y|}{\theta^2}.
$$

%So if $|x-y|= \delta$, then we can choose $\theta = \frac{1}{\sqrt{\delta}}$ so if $x,y\leq \theta$ then $|\frac{1}{x}-\frac{1}{y}|\geq 1$.

%It follows that $f$ is not uniformly continuous.

%
    2. The function $g$ is continuous, with a closed bounded domain, and is therefore uniformly continuous.

%
    3. The function $h$ is uniformly continuous. One way to see this is to use the mean value theorem. Note that, since $x\geq 1$,
%	$$
|h'(x)| = \frac{1}{x^2} \leq  1
$$
%so by the mean value theorem, for all $x,y\in [1,\infty )$ we have
%	$$
| h(y)-h(x)|\leq|y-x|.
$$

%Now let $\varepsilon >0$. Taking $\delta =\varepsilon$, we see that for $x,y\in [1,\infty )$, if $|x-y|<\delta$ then $|h(x)-h(y)|<\varepsilon$, so $h$ is uniformly continuous.

%
\vspace{1em}9. %59
Let $s_n(x)=\sum_{i=1}^n f_i(x)$.
Then $(s_n)$ converges uniformly to $f$, and by Proposition \iflatexml 4.1.7 \else [prop:uconv](#prop:uconv)\fi, this is equivalent to $\sup\{|s_n(x)-f(x)|\}\to 0$ as $n\to\infty$.
So
$$
\begin{align*}
\sup\{|f_n(x)|\}&=\sup\{|s_n(x)-s_{n-1}(x)|\}\\
&\leq \sup \{|s_n(x)-f(x)|+|f(x)-s_{n-1}(x)|\}\\
&\leq \sup \{|s_n(x)-f(x)|\}+\sup\{|f(x)-s_{n-1}(x)|\}\\
&\qquad\to 0, \quad\text{as $n\to\infty$.}
\end{align*}
$$
So by Proposition \iflatexml 4.1.7 \else [prop:uconv](#prop:uconv)\fi, $(f_n)$ converges uniformly to $0$.


\vspace{1em}
10. %60
For each $n\in\N$, define $f_n,g_n:\R\to\R$ by $f_n(x)=\frac{(-1)^nx^{2n+1}}{(2n+1)!}$ and $g_n(x)=\frac{(-1)^nx^{2n}}{(2n)!}$.
[label={(\roman*)}]    1. To establish absolute pointwise summability of $(f_n)$, observe that for each **fixed** $x\in\R$,
$$
\frac{|f_{n+1}(x)|}{|f_n(x)|} = \frac{x^{2n+3}(2n+1)!}{(2n+3)!x^{2n+1}} = \frac{x^2}{(2n+3)(2n+1)} \rightarrow 0,
$$
as $n\rightarrow\infty$. Therefore by the ratio test, $s(x) = \sum_{n=0}^\infty f_n(x)$ is absolutely convergent for each $x\in\R$.

A similar argument applied instead to the seqence $(g_n)$ will show absolute pointwise convergence of the series associate with $c$ (make sure you can write out the details yourself, though!).
    2. Let $R>0$, and restrict each $f_n$ defined above to the interval $[-R,R]$. Let $M_n=\frac{R^{2n+1}}{(2n+1)!}$ for each $n\in\N$. Then
$$
|f_n(x)| = \frac{x^{2n+1}}{(2n+1)!} \leq M_n
$$
for all $x\in[-R,R]$ and $n\in\N$. By the same ratio test argument as above, $(M_n)$ is a summable sequence of real numbers, and so by the Weierstrass $M$-test the series $s:=\sum_{n=0}^\infty f_n$ converges uniformly on $[-R,R]$.

Applying the same argument to $(g_n)$ establishes the result for $c$.
    3. Observe that $f_n$ and $g_n$ are differentiable everywhere for all $n\in\N$, and for each $x\in\R$,
$$
f_n'(x) = \frac{(-1)^n(2n+1)x^{2n}}{(2n+1)!}=\frac{(-1)^nx^{2n}}{(2n)!}=g_n(x) \hspace{2em} \text{ for } n=0,1,2,\ldots
$$
and
$$
g_n'(x) = \frac{(-1)^n(2n)x^{2n-1}}{(2n)!} = \frac{(-1)^nx^{2n-1}}{(2n-1)!} = -f_{n-1}(x) \hspace{2em} \text{ for } n=1,2,\ldots.
$$
Also, $g_0(x)=1$, so $g_0'(x)=0$ for all $x$.

We can now apply Theorem \iflatexml  4.3.3 \else [dterm](#dterm) \fi to the sequences $(f_n)$ and $(g_n)$ to obtained the desired results for $s$ and $c$. The uniform summability of $(f_n')$ and $(g_n')$ follows from that of $(g_n)$ and $(f_n)$, respectively. Clearly each term $f_n'$ and $g_n'$ are also continuous, and so by Theorem \iflatexml  4.3.3 \else [dterm](#dterm) \fi, $s=\sum_{n=0}^\infty f_n$ and $c=\sum_{n=0}^\infty g_n$ are both differentiable on $(-R,R)$, and can be differentiated term by term. But $R$ was arbitrary, and so in fact we have shown that $s$ and $c$ are differentiable everywhere, with derivatives given by
$$
s'(x) = \sum_{n=0}^\infty g_n(x) = c(x)
$$
and
$$
c'(x) = \sum_{n=1}^\infty (-f_{n-1}(x)) = -s(x),
$$
for all $x\in\R$.
    4. The real crux of this part of this question is that the series' for $\exp$, $s(x)$ and $c(x)$ are absolutely convergent for each $x\in R$. This allows us to rearrange their terms without disturbing any convergence properties --- this was the content of Theorem 4.18 in MAS107.

Using rearrangement, we have for each $x\in\R$,
$$
\begin{align*}
\exp(ix) = \sum_{n=0}^\infty\frac{(ix)^n}{n!} &= \sum_{n \text{ even}}^\infty\frac{(ix)^n}{n!}  + \sum_{n \text{ odd}}^\infty\frac{(ix)^n}{n!} \\
&= \sum_{k=0}^\infty\frac{(ix)^{2k}}{(2k)!} + \sum_{k=0}^\infty\frac{(ix)^{2k+1}}{(2k+1)!} \\
&= \sum_{k=0}^\infty\frac{(-1)^kx^{2k}}{(2k)!} + \sum_{k=0}^\infty\frac{i(-1)^kx^{2k+1}}{(2k+1)!} \\
&= c(x) + is(x).
\end{align*}
$$
\vspace{1em}11. %61
[label={(\roman*)}]    1. Let $M_n =\frac{1}{n}^2$. Note that
$$
\frac{1}{n^2+x^2} \leq \frac{1}{n^2}
$$
for all $x\in \R$, and the series $\sum_{n=1}^\infty M_n$ converges. So by the Weierstrass $M$-test, the series \$ \sum_{n=1}^\infty \frac{1}{n^2 +x^2}\$ converges uniformly on $\R$.

It also converges uniformly on $[0,1]$ by the same argument.
    2. Observe that, for each $n\in \N$,
$$
\sup \left\{ \left| \frac{(-1)^nx^{2n+1}}{(2n+1)!} \right| : x\in \R \right\} = \infty
$$
so the series cannot converge uniformly on $\R$. (The series converging uniformly means the sequence
of partial sums $s_n$ converging uniformly. But then you would have $s_{n+1}-s_n$ converging uniformly
to the zero function, which is not the case.)

But let
$$
M_n = \sup \left\{ \left| \frac{(-1)^nx^{2n+1}}{(2n+1)!} \right|  : x\in [0,1] \right\} = \frac{1}{(2n+1)!}.
$$

Then the terms of the series are bounded above by $M_n$, and $\sum_{n=0}^\infty M_n$ converges. So the series converges uniformly on $[0,1]$.
    3. $\sin (nx)$ does not converge to $0$ as $n\rightarrow \infty$ at certain values of $x$,
(for example $x=\frac{\pi}{4}\in [0,1]$),  so the series does not converge, let alone uniformly, either on $[0,1]$ or $\R$.
    4. (*) The series $\sum_{n=1}^\infty  \frac{\sin (nx)}{n}$ does not converge uniformly on $[0,1]$.
So it does not converge uniformly on $\R$ either. To see this, suppose it does converge uniformly. Then the
limit $f(x)$ would be a continuous function on $[0,1]$. Since $f$ is continuous at $0$, we have
$$
0=f(0)=\lim_{N\to\infty} f(\frac{\pi}{N})=\lim_{N\to\infty} \sum_{n=1}^N \frac{\sin\left(\frac{n\pi}{N}\right)}{n}.
$$
On the other hand,
$$
\begin{align*}
\sum_{n=1}^N \frac{\sin\left(\frac{n\pi}{N}\right)}{n}&\geq \frac{1}{N}\left( \sum_{n=1}^N \sin\left(\frac{n\pi}{N}\right)\right)\\
&\quad =\frac{1}{N}\left( \frac{\sin(\frac{N}{2}\frac{\pi}{N})\sin(\frac{N+1}{2}\frac{\pi}{N})}{\sin(\frac{\pi}{2N})}\right).\end{align*}
$$


As \$ N\to \infty\$, this has limit
$$
\lim_{N\to\infty} \frac{1}{N}\left(\frac{\sin(\frac{\left(1+\frac{1}{N}\right)\pi}{2})}{\sin(\frac{\pi}{2N})}\right)
=\lim_{x\to 0}\frac{2}{\pi}\frac{x}{\sin(x)}=\frac{2}{\pi},
$$
giving
a contradiction.
\vspace{1em}12. %62
[label={(\roman*)}]    1. Let $M_n =a^n$. Then for $x\in [0,a]$, we have $|x^n|\leq M_n$, and since $|a|<1$, the series $\sum_{n=1}^\infty M_n$ converges.

Hence, by the Weierstrass $M$-test, the series converges uniformly for $x\in [0,a]$.
    2. Let
$$
S_n(x) = 1+x+x^2+\cdots + x^n.
$$

Let
$$
A_n = \sup \{ S_n (x) : x\in [0,1 ) \} = S_n(1) =1+1 + \cdots + 1 = n.
$$

The sequence  $(A_n)$ does not converge. It follows that the sequence of partial sums $(S_n(x))$ does not converge uniformly on $[0,1)$. Hence the series does not converge uniformly on $[0,1)$.
\vspace{1em}13. %63
Let $f_n:[0,2\pi]\to\R$ be given by
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

\end{document}

## 1.5. Integration

Let $f:[1,4]\to\R$; $f(x)=\frac{1}{x}$, and let $P=\{1,\frac{3}{2},2,4\}$.[label={(\roman*)}]1. Here is a sketch of the graph of $f$, the partition $P$, and the associated upper and lower Riemann sums.

\iflatexml
![](figs/int1i.png)
\else
$$
\begin{tikzpicture}
\begin{axis}[width=.7*\textwidth, xlabel=$x$, ylabel=$y$, unit vector ratio*=.5 1 1, xmin=-.5, xmax=5, ymin=-.3, ymax=1.2, xtick={1,1.5,2,4},  xticklabels={$1$,$\frac{3}{2}$,$2$,$3$,$4$}, ytick={1,2/3,1/2,1/4}, yticklabels={$1$,$\frac{2}{3}$,$\frac{1}{2}$,$\frac{1}{4}$},
%xtick distance=1, ytick distance=1 ,
axis lines=middle, tick align=outside,samples=1000,thick]
% Upper sum
\draw[red] (axis cs:1,0)--(axis cs:1,1)--(axis cs:3/2,1)--(axis cs:3/2,0);
\draw[red] (axis cs:3/2,2/3)--(axis cs:2,2/3)--(axis cs:2,0);
\draw[red] (axis cs:2,1/2)--(axis cs:4,1/2)--(axis cs:4,0);
% Lower sum
\draw[blue] (axis cs:1,0)--(axis cs:1,2/3)--(axis cs:3/2,2/3)--(axis cs:3/2,0);
\draw[blue] (axis cs:3/2,1/2)--(axis cs:2,1/2)--(axis cs:2,0);
\draw[blue] (axis cs:2,1/4)--(axis cs:4,1/4)--(axis cs:4,0);
\addplot[domain=1:4,no marks] {1/x};
\end{axis}
\end{tikzpicture}
$$
\fi
$y=\frac{1}{x}$, with upper and lower sums.

We have $U(f,P) = \sum_{k=1}^4M_k(x_k-x_{k-1})$, where $x_0=1$, $x_1=\frac{3}{2}$, $x_2=2$, $x_3=4$, and

$$
M_1=\sup\left\{\frac{1}{x}:1\leq x\leq\frac{3}{2}\right\}=1, \hspace{1em} M_2=\sup\left\{\frac{1}{x}:\frac{3}{2}\leq x\leq 2\right\}=\frac{2}{3},
$$

$$
M_3=\sup\left\{\frac{1}{x}:2\leq x\leq 4\right\}=\frac{1}{2}.
$$

Therefore,
$$
\begin{align*}
U(f,P) &= 1\cdot\left(\frac{3}{2}-1\right) + \frac{2}{3}\cdot\left(2-\frac{3}{2}\right) + \frac{1}{2}\cdot(4-2) \\
&= \frac{1}{2} + \frac{1}{3} + 1 = \frac{11}{6}.
\end{align*}
$$
Similarly, $L(f,P) = \sum_{k=1}^4m_k(x_k-x_{k-1})$, where

$$
m_1=\inf\left\{\frac{1}{x}:1\leq x\leq\frac{3}{2}\right\}=\frac{2}{3}, \hspace{1em} m_2=\inf\left\{\frac{1}{x}:\frac{3}{2}\leq x\leq 2\right\}=\frac{1}{2},
$$

and

$$
m_3=\inf\left\{\frac{1}{x}:2\leq x\leq 4\right\}=\frac{1}{4}.
$$

Hence
$$
\begin{align*}
L(f,P) = \frac{2}{3}\cdot\left(\frac{3}{2}-1\right) + \frac{1}{2}\left(2-\frac{3}{2}\right) + \frac{1}{4}(4-2) \\
&= \frac{1}{3} + \frac{1}{4} + \frac{1}{2} = \frac{13}{12},
\end{align*}
$$
and so

$$
U(f,P)-L(f,P) = \frac{11}{6}-\frac{13}{12} = \frac{9}{12} = \frac{3}{4}.
$$
2. Adding the point $P$ has the following effect:

\iflatexml
![](figs/int1ii.png)
\else
$$
\begin{tikzpicture}
\begin{axis}[width=.7*\textwidth, xlabel=$x$, ylabel=$y$, unit vector ratio*=.5 1 1, xmin=-.5, xmax=5, ymin=-.3, ymax=1.2, xtick={1,1.5,2,3,4}, xticklabels={$1$,$\frac{3}{2}$,$2$,$3$,$4$}, ytick={1,2/3,1/2,1/3,1/4}, yticklabels={$1$,$\frac{2}{3}$,$\frac{1}{2}$,$\frac{1}{3}\hspace{1em}$,$\frac{1}{4}$},
%xtick distance=1, ytick distance=1 ,
axis lines=middle, tick align=outside,samples=1000,thick]
\draw[thin] (axis cs:0,1/3)--(axis cs:-.4,1/3);
% Upper sum
\draw[red] (axis cs:1,0)--(axis cs:1,1)--(axis cs:3/2,1)--(axis cs:3/2,0);
\draw[red] (axis cs:3/2,2/3)--(axis cs:2,2/3)--(axis cs:2,0);
\draw[red] (axis cs:2,1/2)--(axis cs:3,1/2)--(axis cs:3,0);
\draw[red] (axis cs:3,1/3)--(axis cs:4,1/3)--(axis cs:4,0);
% Lower sum
\draw[blue] (axis cs:1,0)--(axis cs:1,2/3)--(axis cs:3/2,2/3)--(axis cs:3/2,0);
\draw[blue] (axis cs:3/2,1/2)--(axis cs:2,1/2)--(axis cs:2,0);
\draw[blue] (axis cs:2,1/3)--(axis cs:3,1/3)--(axis cs:3,0);
\draw[blue] (axis cs:3,1/4)--(axis cs:4,1/4)--(axis cs:4,0);
\addplot[domain=1:4,no marks] {1/x};
\end{axis}
\end{tikzpicture}
$$
\fi
Upper and lower sums with additional point $3$.

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
3. Mimicking the proof of Theorem \iflatexml 5.2.5 \else [thm:mono](#thm:mono) \fi, let $x_k=1+\frac{3}{n}k$ for $k=0,\ldots,n$. Then, $P=\{x_0,\ldots,x_n\}$ partitions $[1,3]$ uniformly into $n$ intervals, each of width $\frac{3}{n}$. Since $\frac{1}{x}$ is decreasing,

$$
M_k = \sup\left\{\frac{1}{x}:x\in[x_{k-1},x_k]\right\} =\frac{1}{x_{k-1}}
$$

and

$$
m_k = \inf\left\{\frac{1}{x}:x\in[x_{k-1},x_k]\right\} =\frac{1}{x_k}
$$

for each $k$. So,
$$
\begin{align*}
U(f,P) - L(f,P) &= \sum_{k=1}^n\left(\frac{1}{x_k} - \frac{1}{x_{k-1}}\right)\frac{3}{n} \\
&= \frac{3}{n}\left(\frac{1}{x_n}-\frac{1}{x_0}\right) = \frac{3}{n}\left(1-\frac{1}{4}\right) = \frac{9}{4n}.
\end{align*}
$$
We have been asked to find $P$ so that $U(f,P)-L(f,P)<\frac{2}{5}$, so we choose $n$ so that $\frac{9}{4n}<\frac{2}{5}$. That is, $n>\frac{45}{8}$. In fact, $n=6$ will do.

So $x_k=1+\frac{1}{2}k$ for $k=0,\ldots,6$, and $P=\left\{1,\frac{3}{2},2,\frac{5}{2},3,\frac{7}{2},4\right\}$.

\iflatexml
![](figs/int1iii.png)
\else
$$
\begin{tikzpicture}
\begin{axis}[width=.7*\textwidth, xlabel=$x$, ylabel=$y$, unit vector ratio*=1 1 1, xmin=-.5, xmax=5, ymin=-.5, ymax=1.5, xtick={1,1.5,2,2.5,3,3.5,4}, xticklabels={$1$,$\frac{3}{2}$,$2$,$\frac{5}{2}$,$3$,$\frac{7}{2}$,$4$}, ytick={0},
%xtick distance=1, ytick distance=1 ,
axis lines=middle, tick align=outside,samples=1000,thick]
% Upper sum
\draw[red] (axis cs:1,0)--(axis cs:1,1)--(axis cs:3/2,1)--(axis cs:3/2,0);
\draw[red] (axis cs:3/2,2/3)--(axis cs:2,2/3)--(axis cs:2,0);
\draw[red] (axis cs:2,1/2)--(axis cs:5/2,1/2)--(axis cs:5/2,0);
\draw[red] (axis cs:5/2,2/5)--(axis cs:3,2/5)--(axis cs:3,0);
\draw[red] (axis cs:3,1/3)--(axis cs:7/2,1/3)--(axis cs:7/2,0);
\draw[red] (axis cs:7/2,2/7)--(axis cs:4,2/7)--(axis cs:4,0);
% Lower sum
\draw[blue] (axis cs:1,0)--(axis cs:1,2/3)--(axis cs:3/2,2/3)--(axis cs:3/2,0);
\draw[blue] (axis cs:3/2,1/2)--(axis cs:2,1/2)--(axis cs:2,0);
\draw[blue] (axis cs:2,2/5)--(axis cs:5/2,2/5)--(axis cs:5/2,0);
\draw[blue] (axis cs:5/2,1/3)--(axis cs:3,1/3)--(axis cs:3,0);
\draw[blue] (axis cs:3,2/7)--(axis cs:7/2,2/7)--(axis cs:7/2,0);
\draw[blue] (axis cs:7/2,1/4)--(axis cs:4,1/4)--(axis cs:4,0);
\addplot[domain=1:4,no marks] {1/x};
\end{axis}
\end{tikzpicture}
$$
\fi
A partition for which $U(f,P)-L(f,P)<\frac{2}{5}$.
\vspace{1em}4. Let $g:[0,1]\to\R$; $\ds g(x)=\left\{\begin{array}{cc} 1 & \text{for } 0\leq x<1 \\ 2 &\text{for } x=1 \end{array}\right.$.
[label={(\roman*)}]    1. Let $P=\{x_0,x_1,\ldots x_n\}$ be any partition $[0,1]$, with $0=x_0<x_1<\ldots<x_n=1$. Then for $k=1,\ldots n$,
$$
m_k=\inf\{g(x) : x\in[x_{k-1},x_k\} = 1.
$$
Therefore
$$
L(g,P) = \sum_{k=1}^n(x_k-x_{k-1}) = x_n-x_0 = 1.
$$
    2. For $k\neq n$, $1\notin[x_{k-1},x_k]$ and so
$$
M_k=\sup\{g(x) : x\in[x_{k-1},x_k\} = 1.
$$
On the other hand,
$$
M_n=\sup\{g(x) : x\in[x_{n-1},1\} = 2.
$$
Therefore
$$
U(g,P) = (x_1-x_0) + (x_2-x_1) + \ldots (x_{n-1},x_{n-2}) + 2(x_n-x_{n-1}) = 2x_n-x_{n-1}-x_0 = 2-x_{n-1}.
$$

Let $x_k=\frac{k}{n}$ for $k=0,\ldots,n$, where $n\in\N$ is yet to be chosen. Then
$$
U(g,P) = 2-\frac{n-1}{n} = 1+\frac{1}{n}.
$$
Taking $n=10$ will give a partition $P$ so that $U(g,P)=1+\frac{1}{10}$.
    3. Now let $\varepsilon>0$, and let $n$ be any integer strictly greater than $\frac{1}{\varepsilon}$. The partition described in (ii) then satisfies
$$
U(g,P) = 1+\frac{1}{n} < 1+\varepsilon.
$$
\vspace{1em}5. 
[label={(\roman*)}]    1. By Proposition \iflatexml 5.3.1(ii) \else[propsint](#propsint)[abc](#abc)\fi,
$$
\int_0^3 r(t)\, dt = \int_0^11dt+\int_1^2edt+\int_2^3e^4dt = 1+e+e^4,
$$
and similarly
$$
\int_0^3 s(t)\, dt = \int_0^1edt+\int_1^2e^4dt+\int_2^3e^9dt = e+e^4+e^9.
$$
    2. Note that $r(t)\leq f(t)\leq s(t)$ for all $t$, and so by  \iflatexml 5.3.1(i) \else[propsint](#propsint)[leq](#leq)\fi,
$$
1+e+e^4  = \int_0^3 r(t)\, dt \leq \int_0^3 f(t)\, dt \leq \int_0^3 s(t)\, dt = e+e^4+e^9.
$$
\vspace{1em}6. Let $f,g:[a,b]\to\R$ be integrable functions.
[label={(\roman*)}]7. For any subset $A\subset[a,b]$,

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

For the example where this is strict, a good strategy is to look for functions with features that ``cancel out'' in some sense. For example, you could take

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
    1. Let $P_1$ and $P_2$ be partitions of $[a,b]$.
Then
$$
\begin{align*}
U(f+g) &\leq U(f+g,P_1\cup P_2) \\
&\leq U(f,P_1\cup P_2) + U(g,P_1\cup P_2) \\
&\leq U(f,P_1) + U(g,P_2),
\end{align*}
$$
since $P_1\cup P_2$ is a refinement of both partitions $P_1$ and $P_2$.

The proof of the lower sum statement is similar.
    2. Taking $\inf$ over $P_1$,
$$
U(f+g) \leq U(f) + U(g,P_2),
$$
and then taking $\inf$ over $P_2$,
$$
U(f+g) \leq U(f)+U(g).
$$
Since $f$ and $g$ are integrable, this shows that
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
\vspace{1em}8. Let $P$ be the partition $a=x_0<x_1<\ldots<x_n=b$. If $k\geq 0$, then
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
It follows that $kf$ is integrable, with $\ds\int_a^bkf(x)dx=k\int_a^bf(x)dx$.

To extend this result to include negative $k$, it is sufficient to prove the $k=-1$ case. Note that
$$
\sup_{x\in[x_{k-1},x_k]}\big(-f(x)\big) = -\inf_{x\in[x_{k-1},x_k]}f(x),
$$
and
$$
\inf_{x\in[x_{k-1},x_k]}\big(-f(x)\big) = -\sup_{x\in[x_{k-1},x_k]}f(x).
$$
Therefore, $U(-f,P)=-L(f,P)$ and $L(-f,P)=-U(f,P)$, and so
$$
\begin{align*}
U(-f) &= \inf\{U(-f,P):\text{ partitions } P \text{ of } [a,b]\} \\
&= \inf\{-L(f,P):\text{ partitions } P \text{ of } [a,b]\} \\
&= -\sup\{L(f,P):\text{ partitions } P \text{ of } [a,b]\} = -L(f).
\end{align*}
$$
Similarly,
$$
\begin{align*}
L(-f) &= \sup\{L(-f,P):\text{ partitions } P \text{ of } [a,b]\} \\
&= \sup\{-U(f,P):\text{ partitions } P \text{ of } [a,b]\} \\
&= -\inf\{U(f,P):\text{ partitions } P \text{ of } [a,b]\} = -U(f).
\end{align*}
$$
Therefore $U(-f) = -L(f) = -U(f) = L(-f)$, so $-f$ is integrable, and
$$
\int_a^b(-f(x))dx = -\int_a^b f(x)dx.
$$

\vspace{1em}
9. We have 	
$$
M=\sup\{f(x):x\in A\}, \; m=\inf\{f(x):x\in A\},
$$
$$
M'=\sup\{|f(x)|:x\in A\}, \; \text{ and } \; m'=\inf\{|f(x)|:x\in A\}.
$$
[label={(\roman*)}]    1. If $m\geq 0$, then $f$ is a non-negative function, so $M=M'$, $m=m'$, and $M-m=M'-m'$.

If $m\leq M\leq 0$ then $M'=-m$, $m'=-M$, and so again $M'-m'=M-m$.

If $m<0<M$, then $M'=\max\{M,-m\}\leq M+(-m)$, since both $M$ and $-m$ are positive numbers. Then,
$$
M'-m' \leq M' \leq M-m,
$$
since $m'\geq 0$.
    2. Let $f:[a,b]\to\R$ be integrable, and let $P$ be the partition $a=x_0<x_1<\ldots<x_n=b$. for $k=1,\ldots,n$. let
$$
M_k=\sup_{x\in[x_{k-1},x_k]}f(x), \; m_k=\inf{x\in[x_{k-1},x_k]}f(x),
$$
$$
M_k'=\sup_{x\in[x_{k-1},x_k]}|f(x)|, \; \text{ and } \; m_k'=\inf{x\in[x_{k-1},x_k]}|f(x)|.
$$
Then by part (i), $M_k-m_k\geq M_k'-m_k'$ for each $k$.

Therefore,
$$
U(|f|,P) - L(|f|,P) = \sum_{k=1}^n(M_k'-m_k')(x_k-x_{k-1}) \leq \sum_{k=1}^n(M_k-m_k)(x_k-x_{k-1}) = U(f,P)-L(f,P).
$$
    3. Since $f$ is integrable, for all $\varepsilon>0$, we can choose the a partition $P$ so that $U(f,P)-L(f,P)<\varepsilon$. Using the result of part (ii). it follows that $U(|f|,P)-L(|f|,P)<\varepsilon$ for this partition, and so $|f|$ is integrable.

Since $-|f(x)|\leq f(x)\leq |f(x)|$ for all $x\in[a,b]$, Proposition [propsint](#propsint)([leq](#leq)) and ([linear](#linear) imply that
$$
-\int_a^b|f(x)|dx \leq \int_a^b f(x)dx \leq \int_a^b|f(x)|dx.
$$
That is,
$$
\left|\int_a^b f(x)dx\right| \leq \int_a^b|f(x)|dx.
$$
\vspace{1em}10. We have
$$
\int_{a(x)}^{b(x)} f(t)dt =  \int_0^{b(x)} f(t)dt - \int_0^{a(x)} f(t)\ dt.
$$
Write $F(x)=\int_0^x f(t)dt.$ Then by the fundamental theorem of calculus, \$ F'(t)=f(t)\$. Then
$$
\int_0^{b(x)} f(t)dt=F(b(x)),
$$
and using the chain rule
$$
\frac{d}{dx}\int_0^{b(x)} f(t)dt =F'(b(t))b'(t)=f(b(t))b'(t).
$$

Similarly,
$$
\frac{d}{dx}\int_0^{a(x)} f(y)dt =f(a(x))a'(x).
$$

Subtracting these
$$
\frac{d}{dx}\int_{a(x)}^{b(x)} f(t)dt =f(b(x))b'(x) - f(a(x))a'(x),
$$
as required.


\vspace{1em}
11. 
[label={(\roman*)}]    1. It follows immediately from the fundamental theorem of calculus that $l$ is differentiable, with $l'(x)=\frac{1}{x}$.
    2. By Proposition \iflatexml 5.3.1(ii) \else [propsint](#propsint)(ii) \fi in the lecture notes,
$$
l(xy) =\int_1^{xy}\frac{1}{t}\, dt= \int_1^x \frac{1}{t}\, dt + \int_x^{xy} \frac{1}{t}\, dt = l(y) + \int_x^{xy}\frac{1}{t}dt.
$$
In the second integral, set $a(x)=xy$, $b(x)=x$ and use Question [q:116](#q:116). We have $a'(x)=y$ and $b'(x)=1$, so
$$
\frac{d}{dx}\int_x^{xy} \frac{1}{t}dt = \frac{1}{b(x)}b'(x) - \frac{1}{a(x)}a'(x) = \frac{1}{x} - \frac{y}{xy} =0.
$$
Therefore $\int_x^{xy}\frac{1}{t}dt$ is constant as a function of $x$. In particular, it coincides with its value when $x=1$:
$$
\int_x^{xy}\frac{1}{t}dt = \int_1^{y}\frac{1}{t}dt = l(y),
$$
and $l(xy)=l(x)+l(y)$ follows.

%
    3. By the above $l\left(\frac{x}{y}\right) = l(x) + l\left(\frac{1}{y}\right)$. So it suffices to check that $l\left(\frac{1}{y}\right)=-l(y)$. We have
%	$$
l\left(\frac{1}{y}\right) = \int_1^{\frac{1}{y}} \frac{1}{t}\, dt.
$$

%Set $t=\frac{u}{y}$, so $dt = \frac{1}{y} du$. When $t=1$, $u=y$. When $t=\frac{1}{y}$, $u=1$, so
%	$$
L\left(\frac{1}{y}\right) = \int_y^1 \frac{y}{u}\ \frac{1}{y}\ du = - \int_1^y \frac{1}{u}\ du = - L(y),
$$
%as required.
%\vspace{1em}

%12. %
[label={(\roman*)}]
%    1. %We have $f(xy) = f(x)+f(y)$ for all $x,y>0$. We claim that $f(x^n) = nf(x)$ whenever $n\in \N$. We work by induction.

%The result certainly holds when $n=1$. Suppose the result holds when $n=k$. Then $f(x^k) = k f(x)$.
%So
%	$$
f(x^{k+1}) = f(x^k \cdot x) = f(x^k) +f(x) = kf(x)+f(x) = (k+1)f(x) .
$$

%So the result holds when $n=k+1$. Thus it holds for all $n\in \N$ by induction.

%\smallskip

%Observe $f(1) = f(1\times 1) = f(1) + f(1)$. Therefore $f(1)=0$, and $f(x^0)=0f(x)$ for any $x>0$. Now
%	$$
f\left(\frac{1}{x}\right) +f(x) = f\left(\frac{x}{x}\right) =f(1) =0
$$
%so $f\left(\frac{1}{x}\right) = -f(x)$. Hence, for $n\in \N$.
%	$$
f(x^{-n}) = f(\frac{1}{x^n} ) = -f(x^n) = -nf(x) .
$$

%It follows that $f(x^k) =kf(x)$ for all $k\in \Z$.
%\smallskip

%Let $a\in \Z$, $b\in \N$. Then $\left(x^{\frac{a}{b}}\right)^b = x^a$. By the above
%	$$
bf\left(x^{\frac{a}{b}}\right) = f\left(\left(x^{\frac{a}{b}}\right)^b\right) = f\left(x^a\right) = af(x)
$$
%so $f(x^{\frac{a}{b}}) = \frac{a}{b} f(x)$, and  $f(x^q) =qf(x)$ for all $q\in \Q$.
%\smallskip

%Let $a\in \R$. Then we have a sequence $(a_n)$ in $\Q$ converging to $a$. By continuity of $f$ and the above
%	$$
f(x^a) = \lim_{n\rightarrow \infty} f(x^{a_n}) = \lim_{n\rightarrow \infty} a_n f(x) = af(x) .
$$


%
    2. Let $x>0$. Observe
%	$$
f(x) = f(e^{\ln x})) = f(e)\ln x
$$
%by the above.

%
    3. By part (ii), it suffices to prove $L(e) =1$. We have
%	$$
L(e) = \int_1^e \frac{1}{t}\, dt.
$$

%Set $t=e^u$, so $dt = e^u\ du$. At $t=1$, we have $u=0$. At $t=e$, we have $u=1$. So
%	$$
L(e) = \int_0^1 \frac{1}{e^u} e^u\ du = \int_0^1 du = 1
$$
%as required.
%
\vspace{1em}13. Define $G\colon [a,b]\rightarrow \R$ by
$$
G(x) = \int_a^x f(t)\, dt
$$

Then $G$ is a continuous function. This was mentioned in the lectures. To see why, let $h>0$. Since the function $f$ is Riemann integrable, it is bounded, so we have $M\in \R$ such that $|f(t)|\leq M$ for all $t\in [a,b]$. Then
$$
|G(x+h) - G(x) | =\left| \int_x^{x+h} f(t)\, dt \right| \leq \int_x^{x+h} |f(t)|\, dt \leq Mh.
$$

Similarly $|G(x-h) - G(x) | \leq Mh$.

So $G(x+h)\rightarrow G(x)$ as $h\rightarrow 0$, and $G$ is continuous.

Thus we can define a continuous function $F\colon [a,b]\rightarrow \R$ by
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


\vspace{1em}
14. 
[label={(\roman*)}]    1. Consider the step functions $m\mathbf{1}_{[a,b]}$ and $M\mathbf{1}_{[a,b]}$ with
$m\mathbf{1}_{[a,b]}(x)\leq f(x)\leq M\mathbf{1}_{[a,b]}(x)$ for all $x\in[a,b]$. Thus we have

$$
m(b-a)=\int_a^b m\mathbf{1}_{[a,b]}(x)\, dx \leq \int_a^b f(x)\, dx \leq \int_a^b M\mathbf{1}_{[a,b]}(x)\, dx= M(b-a) .
$$

Let $\mu = \frac{1}{b-a} \int_a^b f(x)\, dx$.
Then $\int_a^b f(x)\, dx=(b-a)\mu$ and $m\leq \mu\leq M$, so $\mu \in [m,M]$.
    2. Let $m = \inf \{ f(x) : x\in [a,b] \}$ and $M = \sup \{ f(x) : x\in [a,b] \}$. Then by part (i) we have $\mu \in [m,M]$ where
$$
\int_a^b f(x)\, dx =(b-a)\mu.
$$

But as $f$ is a continuous function on a closed bounded interval, $m$ is the minimum value of $f$, and $M$ is the maximum value. As
$\mu\in [m,M]$ and $f$ is continuous, by the intermediate value theorem there is some $\xi \in [a,b]$ such that $f(\xi ) = \mu$. Hence
$$
\int_a^b f(x)\, dx =(b-a)f(\xi ).
$$
\vspace{1em}15. Let  $m = \inf \{ f(x) : x\in [a,b] \}$ and $M = \sup \{ f(x) : x\in [a,b] \}$. Then $m\leq f(x)\leq M$ for all $x\in [a,b]$. As $g(x)\geq 0$, we have
$$
mg(x)\leq f(x)g(x)\leq Mg(x)
$$
for all $x\in [a,b]$, and so

$$
m \int_a^b g(x)\, dx \leq \int_a^b f(x)g(x)\, dx \leq M\int_a^b g(x)\, dx.
$$

Let
$$
I= \int_a^b g(x)\, dx.
$$

If $I=0$, then the above tells us that
$$
\int_a^b f(x)g(x)\, dx =0
$$
and any $\xi \in [a,b]$ satisfies
$$
\int_a^b f(x)g(x)\, dx = f(\xi ) \int_a^b g(x)\, dx .
$$

As $g(x)\geq 0$, we need to prove the result when $I>0$. Then
$$
m \leq \frac{1}{I} \int_a^b f(x)g(x)\, dx \leq M.
$$

By the intermediate value theorem, as in the solution to Q121(ii), we have $\xi \in [m,M]$ such that
$$
f(\xi ) = \frac{1}{I}  \int_a^b f(x)g(x)\, dx
$$
or in other words
$$
\int_a^b f(x)g(x)\, dx = f(\xi ) \int_a^b g(x)\, dx .
$$

We do need the assumption $g(x)\geq 0$. To see this, consider the function $g(x) = x$ for $x\in [-1,1]$. Then
$$
\int_{-1}^1 g(x)\, dx =0,
$$
so the result would say that for any continuous function $f\colon [-1,1]\rightarrow \R$ we have
$$
\int_{-1}^1 xf(x)\, dx =0.
$$

But this is clearly not the case, taking for example $f(x)=x$.

\end{document}

## Question 162

[label={(\roman*)}]1. Let $0<t<1$, so
$$
f_x(t) = \frac{t^x-1}{\ln t}
$$

We have $t^x -1 \rightarrow -1 \neq 0$ as $t\rightarrow 0$, and $\ln t\rightarrow -\infty$ as $t\rightarrow 0$. So clearly
$$
\frac{t^x-1}{\ln t} \rightarrow 0 =f_x(0)
$$
as $t\rightarrow 0$, and $f_x$ is continuous at $0$.

On the other hand,
$$
t^x -1 \rightarrow 1-1=0 \qquad \ln t\rightarrow 0
$$
as $t\rightarrow 1$, so by L'Hopital's rule, we can differentiate the top and bottom:
$$
\lim_{t\rightarrow 1} \frac{t^x -1}{\ln t} = \lim_{t\rightarrow 1} \frac{xt^{x-1}}{\frac{1}{t}} = x = f_x(1)
$$
so  $f_x$ is continuous at $1$.
2. We say the sequence $(f_n)$ {\em converges uniformly} to a function $f\colon [0,1]\rightarrow \R$ when for all $\varepsilon >0$, we have $N\in \N$ such that $|f_n (t) -f(t)|<\varepsilon$ for all $n\geq N$ and $t\in [0,1]$.
3. Since we can assume the function $f_x$ is increasing, we have that
$$
|f_x(t)| \leq |f_x(1)| = x
$$
for all $t\in [0,1]$.

Let $(x_n)$ be a sequence of positive real numbers with limit $0$. Then $|f_{x_n}(t)| \leq x_n$ for all $t$, and $x_n\rightarrow 0$ as $n\rightarrow \infty$. Therefore $(f_{x_n})$ converges uniformly to $0$.

The result now follows by the uniform convergence theorem for integrals.
4. It suffices that $h$ and $\frac{\partial h}{\partial x}$ are continuous on the domain $(0,\infty )\times[0,1 ]$.
5. Let
$$
I = \int_0^1 \frac{t^x-1}{\ln t} \ dt = \int_0^1 \frac{e^{x\ln t}-1}{\ln t} \ dt
$$

Differentiating under the integral sign, as above
$$
\frac{dI}{dx} = \int_0^1 \frac{e^{x\ln t} \ln t}{\ln t} \ dt = \int_0^1 e^{x\ln t}\ dt = \int_0^1 t^x\ dx = \left[ \frac{1}{x+1}t^{x+1} \right]_{t=0}^{t=1} = \frac{1}{x+1}
$$

So, integrating the right hand side
$$
I = \ln (x+1) +C
$$
where $C$ is constant.

By the above, if we let $x\rightarrow 0$, the right-hand side converges to $C$, and the left-hand side converges to $0$. Therefore $C=0$, and
$$
I = \ln (x+1)
$$
as required.
