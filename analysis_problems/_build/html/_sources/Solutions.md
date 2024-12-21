(sol)=
# Solutions

## Preliminary problems

1.
The correct statements are (ii) and (v).

In statement (iv), the quantifiers $\forall$ and $\exists$ are the wrong way round, while in (i) they are missing altogether. Statement (iii) asserts that last part, $|x_n-l|<\varepsilon$ $\forall n\geq N$, should hold for all $\varepsilon$ and for all $N$ --- so again, there is an issue with the quantifiers.

Bonus exercise: prove that (iv) holds if and only if $(x_n)$ is the constant sequence $x_n=l$ for all $n\in\N$.


2. (HW1 QUESTION)
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



3. (HW1 QUESTION)
The Bolzano--Weierstrass theorem states that every bounded sequence has a convergent subsequence. Its proof combines the following two results:
    - The monotone convergence theorem (Theorem 3.10 in the MAS107 notes), which states that bounded monotone sequences must converge. <br> More specifically, every monotone increasing sequence that is bounded above converges to its supremum, and every monotone decreasing sequence bounded below converges to its infimum.
    - Theorem 3.13 from MAS107: Every sequence has a monotone subsequence.
Proof of Bolzano--Weierstrass: \\
If $(x_n)$ is a bounded sequence, then it has a monotone subsequence, $(x_{n_k})$, by Theorem 3.13. This subsequence must also be bounded since $(x_n)$ is bounded, and hence it converges by the monotone convergence theorem.


4.
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

(ii) Note that the inequality we have been asked to prove is symmetric in $a$ and $b$, in the sense that exchanging the roles of $a$ and $b$ does not affect the value of either side.

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

(iii) Let $(a_n)$ be a real sequence converging to $l\in\mathbb{R}$. By (ii),

$$
\left|\sqrt{|a_{n}|}-\sqrt{|l|}\right| \leq \sqrt{\big|a_n-l\big|}
$$

for all $n\in\N$.

Let $\varepsilon>0$. Since $a_n\rightarrow l$, there is $N\in\N$ such that $|a_n-l|<\varepsilon^2$ whenever $n\geq N$. Hence for $n\geq N$,

$$
\big|\sqrt{|a_{n}|}-\sqrt{|l|}\big| \leq \sqrt{\varepsilon^2} = \varepsilon.
$$

Thus $\displaystyle\lim_{n\rightarrow\infty}\sqrt{|a_n|} = \sqrt{|l|}$.


5. When it exists, the supremum of a set $A\subseteq\mathbb{R}$ is defined to be the unique number $\alpha\in\mathbb{R}$ such that
    - $\alpha$ is an upper bound for $A$, and
    - if $M$ is any other upper bound for $A$, then $\alpha\leq M$.
We write $\sup A$ for the supremum of $A$, when it exists.

The definition of the infimum is similar: when it exists, the infimum of $A$ is the unique number $\beta\in\mathbb{R}$ such that

(i) $\beta$ is a lower bound for $A$, and
  
(ii) if $L$ is any other lower bound for $A$, then $\alpha\geq L$.
We write $\inf A$ for the infimum of $A$, when it exists.

The axiom of completeness for the real numbers says that every non-empty bounded above subset of $\mathbb{R}$ has a supremum. Equivalently, it says that every non-empty bounded below subset of $\mathbb{R}$ has an infimum.

For more details, see page 32 of your Semester 2 MAS107 notes.


6. (i) $\displaystyle\sup\left\{\frac{m}{n}:m,n\in\N \text{ s.t } m<n\right\}=1$,

$\displaystyle\inf\left\{\frac{m}{n}:m,n\in\N \text{ s.t } m<n\right\}=0$.

(ii) $\displaystyle\sup\left\{\frac{(-1)^m}{n}:m,n\in\N \text{ s.t } m<n\right\}=\frac{1}{3}$,

$\displaystyle\inf\left\{\frac{(-1)^m}{n}:m,n\in\N \text{ s.t } m<n\right\}=-\frac{1}{2}$.

(iii) $\displaystyle\sup\left\{\frac{n}{3n + 1} :n\in\N\right\}=\frac{1}{3}$, $\displaystyle\inf\left\{\frac{n}{3n + 1} :n\in\N\right\}=\frac{1}{4}$.

7. (i) This is false --- for a counter-example, take any singleton set. Then $\sup A=\inf A=1$.

A correct version of the statement would be $\inf A \leq \sup A$.

(ii) True. The analogous statement for $\sup$ was called the characteristic property of the supremum in your MAS107 lecture notes --- see Lemma 2.8 on page 36.

(iii) True. Since $\sup B$ is an upper bound for $B$, and $A$ is a subset of $B$, $\sup B$ must be an upper bound for $A$. But $\sup A$ is a the least upper bound for $A$, hence $\sup A\leq \sup B$.

The analogous property for $\inf$ is that $\inf A\geq\inf B$ whenever $A\subseteq B$.

(iv) False. For a counter-example, take $B=\left\{\frac{1}{n}:n\in\N\right\}$, for which $\inf B=0$.

(v) True. Let $s=\max\{\sup A,\sup B\}$. Then $s\geq \sup A$ and $s\geq \sup B$, so $s$ is an upper bound for both $A$ and $B$. Therefore, $s$ is an upper bound for $A\cup B$. But $\sup(A\cup B)$ is the least upper bound of $A\cup B$, and so $s\geq\sup(A\cup B)$. Also, since $A$ and $B$ are both subsets of $A\cup B$, we have by statement (iii) that $s=\max\{\sup A,\sup B)\leq\sup(A\cup B)$. Hence $\max\{\sup A,\sup B)=\sup(A\cup B)$.

