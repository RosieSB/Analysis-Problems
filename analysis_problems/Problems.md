---
jupytext:
  cell_metadata_filter: -all
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.11.5
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

(prob)=
# Problems
## Preliminary problems

1. Which of the following statements is the correct definition of convergence of a real sequence $(x_n)$ to a limit $l\in\R$? How would you correct the incorrect statements?
<br>
[Note: There is more than one correct answer.]
    1. $\varepsilon>0$ $N\in\N$ then $|x_n-l|<\varepsilon$.
    2. $\forall\varepsilon>0$ $\exists N\in\N$ s.t.  $|x_n-l|<\varepsilon$ $\forall n\geq N$.
    3. For all $\varepsilon>0$ and $N\in\N$, we have $|x_n-l|<\varepsilon$ whenever $n\geq N$.
    4. $\exists\varepsilon>0$ s.t. $\forall N\in\N$, $|x_n-l|<\varepsilon$ $\forall n\geq N$.
    5. Given any $\varepsilon>0$, there is $N\in\N$ such that $|x_n-l|<\varepsilon$ whenever $n\geq N$.
2.  %P2
Prove using the $(\varepsilon-N)$-definition of convergence that the sequence $(x_n)$ given by $x_n = \frac{2n}{3n-1}$ converges to $\frac{2}{3}$ as $n\rightarrow\infty$.
3.  %P3
Using your MAS107 notes or another resource, look up and carefully state the Bolzano--Weierstrass theorem.

Its proof combines two other important results about sequences from MAS107. What do these results say?

[Note: We will use all three of these theorems at various points this semester. Check you are clear on what each of them is saying, and remember your lecturers and tutors are here to help.]
4.  %P4
    1. If $a, b \geq 0$, show that

$$
\sqrt{a + b} \leq \sqrt{a} + \sqrt{b}.
$$

[Hint: Consider the square of both sides. You may use that the square root function is increasing.]

    2.  If $a,b \in \R$, deduce that

$$
\left|\sqrt{|a|} - \sqrt{|b|}\right| \leq \sqrt{|a - b|}.
$$

[Hint: Imitate the proof of Corollary~\iflatexml 0.2.6 \else[cor:tri](#cor:tri) \fi in the lecture notes.]
    3.  Hence prove that if the sequence $(a_{n})$ converges to $l$, then $\left(\sqrt{|a_{n}|}\right)$ converges to $\sqrt{|l|}$. % [Hint: Use the result of (ii).]
5.  %P5
Look up and carefully define the \emph{supremum} and \emph{infimum} of a set $A\subseteq\R$. What conditions must be met for each of these to exist?
6.  %P6
Compute, without proof, the suprema and infima (if they exist) of the following sets:
    1. $\left\{\frac{m}{n}:m,n\in\N \text{ s.t } m<n\right\}$.
    2. $\left\{\frac{(-1)^m}{n}:m,n\in\N \text{ s.t } m<n\right\}$.
    3. $\left\{\frac{n}{3n + 1} :n\in\N\right\}$.
7.  %P7
Let $A$ and $B$ be bounded and non-empty subsets of $\R$. Which of the following statements are true, and which are false?
    1. $\inf A < \sup A$.
    2. For all $\varepsilon>0$, there is $x\in A$ such that $x-\inf A < \varepsilon$.
    3. $A\subseteq B$ implies $\sup A \leq \sup B$.
    4. If $x>0$ for all $x\in B$, then $\inf B >0$.
    5. $\sup(A\cup B) = \max\{\sup A,\sup B\}$.

## 1.1. Limits of functions

 % Formerly Ch3 of MAS221 Sem 1 problem booklet1.  %1
For each of the following formulas, what is the largest subset $X$ of $\R$  which may be taken as the domain of a function with that formula?
    1. $f_{1}(x) = \ds\frac{x^{2} + 2x + 7}{x(x+1)}$,
    2. $f_{2}(x) = \ds\frac{(x-1)(x+4)}{x^{3} + 4x^{2} + x - 6}$,
    3. $f_{3}(x) = \ds\frac{x+4}{x^{2}+5x + 6}$,
    4. $f_{4}(x) = \exp{\left(-\ds\frac{1}{x-1}\right)}$,
    5. $f_{5}(x) = \cos\left(\ds\frac{1}{\pi x}\right)$.
1. %2
For each of the sets $X\subseteq\R$ below, calculate the associated set $L$ of its limit points. Where possible, please provide a sketch with your answers.

$$
\begin{array}{rlcrl}
\LI & X=(0,1)\cup[2,3)\cup\{4,5\}, &\qquad& \LI & X=\Z, \\
\LI & X=\R\setminus\Z, &\qquad& \LI & X=\{x\in\Q:0<x<1\}, \\
\LI & X=\ds\left\{\frac{1}{n}:n\in\N\right\}.
\end{array}
$$



2.  %3
For $f_2:A\to \R$ as in part (ii) of the question [q:44](#q:44), investigate each of
$$
\lim_{x \rightarrow 1}f_{2}(x), \hspace{3em} \lim_{x \rightarrow -2}f_{2}(x) \hspace{2em} \text{ and } \hspace{2em} \lim_{x \rightarrow -3}f_{2}(x).
$$
Calculate the value of each limit, if it exists.



3.  %4
If $f: \R \rightarrow [0, \infty)$ satisfies $\ds\lim_{x \rightarrow a} f(x) = l$, where $l > 0$, show that $\ds\lim_{x \rightarrow a} \sqrt{f(x)} = \sqrt{l}$.

Hence calculate $\ds\lim_{x \rightarrow 1}\sqrt{\ds\frac{x+1}{x^{2}}}$.

[Hint: For the first part, use the result of \iflatexml [iii](#iii) \else [q:25](#q:25)[iii](#iii) \fi from the preliminary exercises.]



4.  %5
Why are limits of functions unique?% (compare with Theorem 2.1.4)?



5.  %6 - HW2 question
Verify that $\sign(x) = \ds\frac{|x|}{x} = \ds\frac{x}{|x|}$, for $x \neq 0$ (see Example \iflatexml 1.1.3 \else [eg:sgn](#eg:sgn) \fi in the notes for the definition).

Show that $\ds\lim_{x \rightarrow 0}\sign(x)$ does not exist. Show that both the left and right limits exist at $x=0$, and find their values.


6.  %7 - HW2 question
For the following functions, each of which is defined on the whole of $\R$, find every point at which both the left and right limits exist, but are different from each other, and find the values of these limits.
    1. $f(x) = \begin{cases}
1 -x & \text{if }x < 1\\
x^{2}& \text{if }x \geq 1.
\end{cases}$
    2. $g(x) = [x]$, where
$$
\begin{equation}\label{eq:[x]}
[x] = \left\{\begin{array}{cl} \lfloor x\rfloor & \text{ if } x\geq 0 \\ \lceil x \rceil & \text{ if } x<0 \end{array}\right.
\end{equation}
$$
denotes the integer part of $x$.
    3. $h(x) =3 - 5{\bf 1}_{(0, 1]}(x) + 7{\bf 1}_{(1, 2]}(x)$. [Here we have used the notation for indicator functions --- see Example \iflatexml 1.1.4 \else [eg:indicator](#eg:indicator) \fi in the notes.]
7.  %8
What is the largest subset $A$ of $\R$ for which we can specify a function by $f(x) = \sin\left(\frac{1}{x}\right)$? Does $f:A\to\R$ have a limit at $x = 0$? [Hint: Consider sequences whose $n$th term is $\frac{1}{\theta + 2n\pi}$, and think about good choices for $\theta$.]



8.  %9
What is the largest subset $A$ of $\R$ for which we
can specify a function by $f(x) = x\sin\left(\frac{1}{x}\right)$? Does $f:A\to\R$  have a limit at $x = 0$?


%

%
9. %Let $f:X\to\R$ and let $a\in\R$ be a limit point of $X$. Prove that
%

%    1. $\lim_{x\rightarrow a^-}f(x) = l$ if and only if for any sequence $(x_n)$ in $X$ for which $x_n<a$ for all $n\in\N$ and $\lim_{n\rightarrow\infty}=a$, we %have $\lim_{n\rightarrow\infty}f(x_n)=l$, for some $l\in\R$.
%
    2. $\lim_{x\rightarrow a^+}f(x) = l$ if and only if for any sequence $(x_n)$ in $X$ for which $x_n>a$ for all $n\in\N$ and $\lim_{n\rightarrow\infty}=a$, we %have $\lim_{n\rightarrow\infty}f(x_n)=l$, for some $l\in\R$.
%
10.  %10
In the notes, we gave meaning to $\ds\lim_{x \rightarrow a} f(x)$ where $f:\R \rightarrow \R$ is a function and $a \in \R$.  In this question, you can investigate what happens when $x$ tends to $\infty$ or $-\infty$.
    1. Formulate a rigorous definition, in terms of sequences, of what it means for $\ds\lim_{x \rightarrow \infty}f(x)$ and $\ds\lim_{x \rightarrow -\infty}f(x)$ to exist. [Hint: First decide whether you want to use {\it convergent}  or {\it divergent} sequences.]
    2. Find an analogue of the $(\varepsilon-\delta)$ criterion for this case, and prove the analogous result to Theorem \iflatexml 1.2.6 \else [ed](#ed) \fi. [Hint: For the analogue of $(\varepsilon-\delta)$, think very carefully about how you are going to control the behaviour of $x$. Remember that you cannot treat $\infty$ as if it were a number!]
    3. Check that you can prove that $\ds\lim_{x \rightarrow \infty}\frac{1}{x} = \lim_{x \rightarrow -\infty}\frac{1}{x} = 0$, using your criterion.
11.  %11
    1. Formulate a rigorous definition for $\ds\lim_{x \rightarrow \infty}f(x) = \infty$ in terms of sequences  and write down an analogue of the $(\varepsilon-\delta)$ criterion. [The cases  $\ds\lim_{x \rightarrow \infty}f(x) = -\infty$ and $\ds\lim_{x \rightarrow -\infty}f(x) = \pm \infty$ can be treated similarly.]
    2. Let $f:\R \rightarrow [0, \infty)$ and $g:\R \rightarrow [0, \infty)$, and suppose that $\ds\lim_{x \rightarrow \infty}f(x) = \infty$ and $\ds\lim_{x \rightarrow \infty}g(x) = l$, where $l > 0$. Define $h(x) = f(x)g(x)$ for all $x \in \R$. Show that $\ds\lim_{x \rightarrow \infty}h(x) = \infty$.
    3. Let $p: \R \rightarrow \R$ be an even polynomial of degree $m$, where the leading coefficient (i.e.~the coefficient of $x^{m}$) is positive. Show that $\ds\lim_{x \rightarrow \infty}p(x) = \lim_{x \rightarrow -\infty}p(x) = \infty$. What happens when $m$ is odd?

## 1.2. Continuity

 % Formerly Ch4 of MAS221 Sem 1 problem booklet\iflatexml  \else \setcounterref{enumi}{q:54} \fi

12.  %12
Return to Problem [q:44](#q:44). Consider each function there, defined on the largest subset $A$ of $\R$
which can be taken as its domain, as found in that problem. For each function,
what is the maximum subset of $A$ on which it is continuous?



121.  %13

Let $f: \R \rightarrow \R$ be continuous at a point $a$.
Prove that $|f|$ is continuous at $a$, where $|f|(x) = |f(x)|$, for all $x \in \R$.

[Hint: Use the formulation of continuity with sequences (Theorem \iflatexml 2.1.2(ii) \else [cont1](#cont1)(ii) \fi) and Corollary~\iflatexml 0.2.6 \else[cor:tri](#cor:tri)\fi from the notes.]



1211.  %14
Prove Theorem \iflatexml 2.1.6 \else [fof](#fof) \fi in the notes (i.e.~that composition of continuous functions is continuous). [Hint: Use sequences.]



12111.  %15
Define $f:\R \setminus \{0\}\to \R$ and $g: \R \rightarrow \R\setminus \{0\}$ by $f(x) = \frac{1}{x}$, and $g(x) = 1 + x^{2}$. Write down the functions $f \circ g$, and $g \circ f$, giving their domains explicitly. What can you say about continuity of these functions?



121111.  %16
For each of the functions in Problem [q:49](#q:49):
    1. Find the maximum subset of $\R$ on which it is continuous.
    2. Identify those discontinuities which are jumps, and calculate the size of each jump.
1211111.  %17- HW2 question
    1. Define $f:  \R \setminus \{0\} \rightarrow \R$ by
$$
f(x) = \ds\frac{(1 + x)^{2} - 1}{x}.
$$

Find an extension of $f$ to the whole of $\R$ that is continuous there.
    2. Write down the largest subset of $\R$ which can be taken as the domain $A$ of the function $f$ given by
$$
f(x) = \ds\frac{x^{3}-8}{x^{2} - 4}
$$
and explain why $f$ is continuous at every point of $A$. The complement $A^{c}$ of $A$ in $\R$ comprises two points. Show that $f$ may be extended to be continuous at only one of these points, and write down this continuous extension.
12111111.  %18
Suppose that the function $g: \R \rightarrow \R$ is continuous at $a$ with $g(a) > 0$. Show that there exists $\delta > 0$ such that $g(x) > 0$  for all \$ x \in (a - \delta, a + \delta)\$. [Hint: Assume $g(a) > 0$ and try a proof by contradiction.]



121111111.  %19
    1. For any $x, y \in \R$ show that
$$
\max\{x, y\} = \frac{1}{2}(x + y) + \frac{1}{2}|x - y|.
$$
Hence show that if both $f:A\to \R$ and $g: B \rightarrow \R$ are continuous at $a$, then so is $\max\{f, g\}$, where for all $x \in A\cap B$,
$$
\max\{f, g\}(x)  = \max\{f(x), g(x)\}.
$$
    2. Find a similar expression for $\min\{x, y\}$, and hence prove continuity of $\min\{f, g\}$ at $a$.
1211111111.  %20
The aim of this question is to prove the following: the only functions $f: \R \rightarrow \R$ which are continuous at zero and satisfy $f(x+y) = f(x) + f(y)$ for all $x,y \in \R$ are the linear mappings $f(x) = kx$ for all $x \in \R$, where $k \in \R$ is fixed.

Begin by considering $f: \R \rightarrow \R$, such that $f(x+y) = f(x) + f(y)$ for all $x,y \in \R$.
    1. Prove that $f(0) = 0$.
    2. Show that $f(-x) = -f(x)$ for all $x \in \R$.
    3. If $f$ is continuous at zero, prove that it is continuous at every $x \in \R$.
    4. If $f(1) = k$, prove that $f(n) = kn$ for all $n\in \mathbb{Z}$.
    5. If $f(1) = k$, prove that $f\left(\frac{p}{q}\right) = k\frac{p}{q}$ for all $\frac{p}{q} \in \mathbb{Q}$.
    6. If $f(1) = k$ and $f$ is continuous at zero, prove that $f(x) =kx$ for all $x \in \R$.
undefined.  %21
Show that Dirichlet's ``other'' function, as discussed in Example \iflatexml 2.2.5 \else [eg:dirichlet2](#eg:dirichlet2) \fi in the notes, is discontinuous at every rational point in its domain.


12111111111.  %22 - HW2 question
What can you say about left/right continuity of the function  ${\bf 1}_{(a, b)}:\R\to\R$ at the points $a$ and $b$?



121111111111.  %23
Prove Corollary~\iflatexml 2.3.2 \else [ivp2](#ivp2)\fi. [Hint: Apply the intermediate value theorem to the function $g(x) = f(x) - \gamma$, for $x \in [a, b]$.]



1211111111111.  %24
Use Corollary~\iflatexml 2.3.2 \else [ivp2](#ivp2) \fi to show the following.
    1. Every continuous function from $\R$ to $\mathbb{Z}$ is constant.
    2. Every continuous function from $\R$ to $\Q$ is constant.
12111111111111.  %25
Prove the following {\it fixed point theorem}: if $f:[a,b] \rightarrow (a,b)$ is continuous, then there exists $c \in (a, b)$ such that $f(c) = c$.

[Hint: This is a similar proof to that of Problem [q:66](#q:66). This time you need to consider a function of the form \$g(x) = f(x) - \$ {\it something}. What is {\it something}?] Give a counter--example to demonstrate that the claim is false if the domain of $f$ is restricted to $(0, 1)$.



.  %26
Complete the proof of the extreme value theorem (Theorem \iflatexml 2.3.6 \else [thm:evt](#thm:evt) \fi), i.e.~prove that a continuous function $f:[a,b]\to\R$ attains its infimum.



.  %27
Show that if $f:[0,1] \rightarrow \R$ is continuous and $0$ is not in the range of  $f$, then the function $\frac{1}{f}:[0,1]\to \R$ is bounded, where for each $x \in [0,1], \left(\frac{1}{f}\right)(x) = \frac{1}{f(x)}$.



.  %28
Explain why there are no continuous functions having domain $[0, 1]$ and range $\R$. [Hint: Use Theorem \iflatexml 2.3.6 \else [thm:evt](#thm:evt) \fi.]



1.  %29
Suppose that the function $f:[0,1] \rightarrow [0,1]$ is continuous, and fix $0 < r < 1$. Suppose that we are given a sequence $(x_{n})$ in $[0,1]$ such that $f(x_{n+1}) \leq rf(x_{n})$ for all $n\in\N$. Show that there exists $c \in [0, 1]$ for which $f(c) = 0$. [Hint: Use the Bolzano-Weierstrass theorem.]



11.  %30
Show that for each $n\in\N$, the function $f: [0, \infty)\to\R$ given by $f(x) =x^{n}$ is strictly monotonic increasing.



111.  %31
Show that the function $f(x) = \sin(x)$ has a continuous inverse when restricted to the interval $\left[-\frac{\pi}{2}, \frac{\pi}{2}\right]$. What goes wrong outside this interval? [Hint: Use an appropriate trigonometric identity.]



1111.  %32
Find $\ds\lim_{x \rightarrow 1}\frac{1 - x}{1 - x^{\frac{m}{n}}}$, where $m, n \in \N$.



11111.  %33
If $f:[a, b] \rightarrow \R$ is continuous and bijective, and $f(a) < f(b)$, show that $f$ is strictly monotonic increasing.



111111. $^*$ %34
Show that if $f, g: \R \rightarrow \R$  are monotonic increasing, with $f+g$ continuous, then both $f$ and $g$ are continuous.



1111111. $^*$ %35
%\vspace{-0.8cm}
    1. Let $(x_{n})$ be a sequence in $\R$ for which $x_{1} = a > 0$ and $x_{n+1} = \sqrt{x_{n}}$, for all $n\in\N$. Show that $\ds\lim_{n \rightarrow \infty} x_{n} = 1$.
    2. Let $f: \R \rightarrow \R$ be a continuous function for which $f(x) = f(x^{2})$ for all $x \in \R$. Use the result of (i) to show that $f$ is constant.

## 1.3. Differentiation

%*{Chapter 5 problems} % Differentiation\iflatexml  \else \setcounterref{enumi}{q:78} \fi36.  %36
Let $f:A\to\R$ and let $a\in\R$ be such that there is some sequence $(x_n)$ in $A$ with
$x_n\neq a$ for all $n$ and $\ds\lim_{n\to\infty} x_n=a$. What does it mean to say that
the function $f$ has limit $l$ at the point $a$? What notation do we use to write this?

[ This question is asking you to recall (or revise if you can't recall) Definition \iflatexml 1.2.3 \else [def:functionlimit](#def:functionlimit) \fi from the lecture notes. %3.2.1 from semester 1.
That's a key definition and we build on it when we define what it means to be differentiable - see the next question. ]




361.  %37
    1. Give the definition of what it means for a function $f:A\to\R$ to be differentiable at $a \in A$.
    2. State carefully what this means in terms of limits of sequences.
    3. State carefully what this means in terms of the $\varepsilon-\delta$ criterion.
[ The first part is just asking you to give Definition \iflatexml 3.2.1 \else [def:functionlimit](#def:functionlimit) \fi and the other parts are checking that you know what this
means.
The key points from Chapter \iflatexml 1 \else [chap:functionlimits](#chap:functionlimits) \fi are Definition \iflatexml 1.2.3 \else [def:functionlimit](#def:functionlimit) \fi of a limit of a function and Theorem \iflatexml 1.2.6 \else [ed](#ed) \fi giving the ($\varepsilon-\delta$) criterion. But you need to see how to apply these, not just copy them out. Here they have to be applied to the relevant function for the definition of differentiability, not $f$ itself. ]


3611.  Give a rigorous proof that the function $f:\R\setminus\{0\}\to \R$ given by
$f(x) = \frac{1}{x}$ is differentiable for all $x \in \R \setminus \{0\}$ from the definition of the derivative
and find $f'(x)$ explicitly. Can we extend the function so that it is differentiable on the whole of $\R$ by defining its value at zero to be zero?



36111.  Let $k\in \R\setminus\{0\}$. Give a rigorous proof from the definition of the derivative  that  $f:\R\to \R$ given by  $f(x) = e^{kx}$ is differentiable for all $x \in \R$, and find $f'(x)$ explicitly.

[ Hint: For fixed $k\in \R$, let $g:\R\to\R$ be given by \$g(h)=e^{kh} - 1 - kh \$.
You may use the fact that  $\ds\lim_{h \rightarrow 0}\frac{g(h)}{h} = 0$. (This follows from the series expansion
of the exponential function, which you already know, and we will study more later.) ]



361111.  Consider the function  $f:\R\to \R$ given by
$$
f(x) = \begin{cases}
x\sin\left(\frac{1}{x}\right) & \text{if $x \neq 0$,}\\
0 & \text{if $x = 0$}.
\end{cases}
$$
    1. Show that $f$
is differentiable at every $x \neq 0$. (You can use standard derivatives and facts about derivatives, such as the product and chain rules.)
    2. Show that $f$ is not differentiable at $x = 0$. (Use the definition of
the derivative as a limit. You may assume that $\sin\left(\frac{1}{x}\right)$ has no limit as $x$ tends to $0$. This was Problem [q:50](#q:50).)
3611111.   Show that the function  $f:\R\to \R$ given by
$$
f(x) = \begin{cases}
x^2\sin\left(\frac{1}{x}\right) & \text{if $x \neq 0$,}\\
0 & \text{if $x = 0$}.
\end{cases}
$$
is differentiable at every $x \in \R$. What can you say about its second derivative?

[ Hint: You will need to consider the case $x=0$ separately from $x\in\R\setminus\{0\}$. You may assume that the limit
as $x$ tends to $0$ of $x\sin\left(\frac{1}{x}\right)$ exists and equals $0$. This was studied in Problem [q:51](#q:51). ]



36111111. 
    1. Sketch the graph of any continuous function $f:[0,1]\to \R$ which is not differentiable at $x=\frac{1}{2}$, but is differentiable at all other points. [You do \emph{not} need to give a formula.]
    2. Sketch the graph of any continuous function $f:[0,1]\to \R$ which is not differentiable at $x=\frac{1}{3}$ and is not differentiable at $x=\frac{2}{3}$, but is differentiable at all other points. [You do \emph{not} need to give a formula.]
361111111.  Let $f:\R\to \R$ be given by $f(x) = x - [x]$ for all $x \in \R$, where $[x]$ denotes the integer part of $f$ (see ([eq:[x]](#eq:[x]))).

Explain carefully at which points $f$  is differentiable, and find the value of its derivative there. [It will probably help to sketch the graph!]



3611111111.  Show that if $f:\R \rightarrow \R$ is differentiable at $a$ then
$$
\lim_{h \downarrow 0} \ds\frac{f(a + h) - f(a - h)}{2h} = f'(a).
$$
By considering $f:\R\to\R$ given by
$f(x) = |x|$, show that the limit on the left-hand side may exist, even when $f$ is not differentiable at $a$.


%

%
36111111111. %45
%Prove Theorem \iflatexml 3.2.7 \else [lrd](#lrd) \fi, i.e.~show that $f:\R \rightarrow \R$ is differentiable at $a$ if and only if it is both right and left differentiable there, and these two derivatives both agree there, in which case $f'(a)$ is their common value.



361111111111.  A function $f:\R \rightarrow \R$ is defined by
$$
f(x) = \begin{cases} -x^{2} & \text{if $x < 0$,}\\ x^{2} & \text{if $x \geq 0$.} \end{cases}
$$
Determine whether each of the following is true or false. Justify your answers.
    1. $f$ is continuous at $0$.
    2. $f'(0)$ exists.
    3. $f':\R\to\R$ is continuous at $0$.
    4. $f^{\prime \prime}(0)$ exists.
3611111111111. 
    1. Must any differentiable function $f:[a, b] \rightarrow \R$ have a maximum and minimum value? Why?
    2. If $f:[a, b] \rightarrow \R$ is differentiable  and $f(a) = f(b)$, must $f$ have a maximum and minimum value in $(a, b)$?
36111111111111.  Let $a_{0}, a_{1}, \ldots, a_{n}$ be real numbers
such that
$$
a_{0} + \frac{a_{1}}{2} + \frac{a_{2}}{3} + \cdots + \frac{a_{n}}{n+1} = 0.
$$
Consider $f:\R\to\R$ given by
$f(x) = a_{0}+ a_{1}x + a_{2}x^{2} + \cdots + a_{n}x^{n}$.
Show that there is some $c\in (0,1)$ such that $f(c)=0$.
[Hint: Integrate the function $f$ term--by--term, and think about how to use Rolle's theorem.]



361111111111111. 
    1. Use the mean value theorem to show the following. If $f:\R \rightarrow \R$ is continuous on $[a, b]$ and differentiable on $(a, b)$ with $f'(c)= 0$ for all $c \in (a, b)$, then $f$ is constant on $[a, b]$.
    2. Use part (i) to show that if
$g, h:\R\to\R$ are both continuous on $[a, b]$ and differentiable on $(a, b)$ with $h'(x) = g'(x)$ for all $x \in (a, b)$, then there exists $k \in \R$ such that $h(x) = g(x) + k$, for all $x \in [a, b]$.
3611111111111111.  If $f:\R \rightarrow \R$ is continuous on $[a, b]$ and differentiable on $(a, b)$ and there exist $m, M \in \R$ such that $m \leq f'(c) \leq M$, for all $c \in (a, b)$, show that
$$
f(a) + m(b - a) \leq f(b) \leq f(a) + M(b-a).
$$


%

%
36111111111111111.  "inverses revisited"
%Show that the restriction of $f(x) = \cos(x)$ to $[0, \pi]$ has an inverse defined on $[-1, 1]$, which is differentiable on $(-1, 1)$.



361111111111111111.  %50
If $r > 0$ and $q \in \R$ show that the polynomial $p(x) = x^{3} + rx + q$ has exactly one real zero.
[ You may assume the result of Corollary~\iflatexml 2.3.3 \else [pol](#pol)\fi: $p$ has at least one real root. So you need to show that there can't be more than one. ]



3611111111111111111.  %51
Let $r>1$ and fix $y\in (0,1)$. By applying the mean value theorem to the function $f(x)=x^r$ on $[y,1]$, show that
$$
1 - y^r < r(1 - y).
$$



36111111111111111111.  %52
Let $f:\R \rightarrow \R$ be twice differentiable at $a$ with $f'(a) = 0$. If $f^{\prime \prime}(a) < 0$, show that $f$ has a local maximum at $a$, while if $f^{\prime \prime}(a) > 0$, show that $f$ has a local minimum at $a$.


%

%
361111111111111111111. %Prove Cauchy's mean value theorem (Theorem [cmvt](#cmvt) in the notes.)
%[Hint: Define $h(x) = f(x) - \rho g(x)$, where $\rho = \frac{f(b) - f(a)}{g(b) - g(a)}$ and show how to obtain the result by applying Rolle's Theorem to $h$.]


%

%
3611111111111111111111. %Use L'H\^{o}pital's rule and the result of Problem [q:87](#q:87) to show that if $f$ is twice differentiable at $a$, then
%	$$
f^{\prime \prime}(a) = \ds\lim_{h \downarrow 0}\frac{f(a+ h) - 2f(a) + f(a-h)}{h^{2}}.
$$


%

%
36111111111111111111111. $^{*}$
%The purpose of this question is to prove the $\infty/\infty$ version of L'H\^{o}pital's rule, which is stated as Theorem [thm:L'Hop-infty](#thm:L'Hop-infty) in the notes.

%Let $f$ and $g$ be differentiable on $(a, b)$ with $g'(x) \neq 0$ for all $x \in (a, b)$.

%Suppose that $\ds\lim_{x \downarrow a}f(x) = \lim_{x \downarrow a}g(x) = \infty$ and $\ds\lim_{x \downarrow a}\frac{f'(x)}{g'(x)}=L$.
%

%    1. Let $\varepsilon>0$. Show there exists $\delta>0$ such that  $f(x) \neq 0$, $g(x) \neq 0$, and
%	$$
L-\varepsilon<\frac{f'(x)}{g'(x)} < L+\varepsilon
$$
%for all $x \in (a, a+\delta)$.
%
%
    2. Show that for all $a<x<y<a+\delta$, there is $c_{x,y} \in (a, a+\delta)$ such that
%	$$
\frac{f'(c_{x,y})}{g'(c_{x,y})} = \frac{f(x) - f(y)}{g(x) - g(y)}.
$$
%[Hint: use Cauchy's mean value theorem (Theorem [cmvt](#cmvt)).]

%
    3. Deduce that
%	$$
(L-\varepsilon)\left(1-\frac{g(y)}{g(x)}\right)<\frac{f(x)}{g(x)}-\frac{f(y)}{g(x)}<(L+\varepsilon)\left(1-\frac{g(y)}{g(x)}\right).
$$


%
    4. By letting $x\rightarrow a^+$ while holding $y$ fixed, show that
%	$$
L-\varepsilon< \ds\lim_{x \downarrow a}\frac{f(x)}{g(x)} \leq L+\varepsilon,
$$
%and hence deduce the result.

%
%

%361111111111111111111111. %Use Taylor's (or Maclaurin's) theorem (c.f.~Theorem [thm:Taylor-0](#thm:Taylor-0)) to find the indicated remainder terms appearing in the following expansions (where $x \in \R$):
%

%    1. $e^{x} = 1 + x + \cdots + \frac{x^{n-1}}{(n-1)!} + R_n(x)$.
%
    2. $\sin(x) = x - \frac{x^{3}}{3!} + \cdots + (-1)^{n+1}\frac{x^{2n-1}}{(2n-1)!} + R_{2n}(x)$.
%
    3. $\cos(x) = 1 - \frac{x^{2}}{2!} + \cdots + (-1)^{n}\frac{x^{2n}}{(2n)!} + R_{2n+1}(x).$
%
%

%3611111111111111111111111. %Prove that for all $x \in \R$:
%	$$
1- \frac{x^{2}}{2} \leq \cos(x) \leq 1 - \frac{x^{2}}{2} + \frac{x^{4}}{24}.
$$

%{q:103}--{q:111} labels missing as these were Chapter 6 (now part of MAS107)

## 1.4. Sequences and series of functions

%{Chapter 8 problems} % Sequences and series of functions\iflatexml  \else \setcounterref{enumi}{q:97} \fi
%53. %

%    1. State the definition of a sequence of functions $f_n \colon \R \rightarrow \R$ converging uniformly to a function $f\colon \R\rightarrow \R$.
%
    2. Prove that if a sequence $(f_n)$ of continuous functions $f_n \colon \R \rightarrow \R$ converges uniformly to a function $f\colon \R \rightarrow \R$, then the function $f$ is continuous.
%
%531. Consider the sequence of functions  $(f_n)$, where $f_n:[0,\pi ]\to \R$ is defined by $f_n(x) = \sin^n (x)$ for each $n\in\N$. Show that the sequence $(f_n)$ converges pointwise. Does the sequence $(f_n)$  converge uniformly? Justify your answer.



5311. For each of the following sequences of functions $(f_n)$ determine the pointwise limit (if it exists), and decide whether $(f_n)$ converges uniformly to this limit.
    1. $f_n:[0,1]\to\R$, $f_n (x) = x^{\frac{1}{n}}$.
    2. $f_n:\R\to\R$, where $\ds f_n (x)  = \left\{ \begin{array}{ll} 0 & x\leq n, \\ x-n & x\geq n \\ \end{array} \right.$.
    3. $f_n:(1,\infty)\to\R$, $f_n(x) = \frac{e^x}{x^n}$.
    4. $f_n:[-1,1]\to\R$, $f_n(x) = e^{-nx^2}$.
    5. $f_n:\R\to\R$, $f_n(x) = e^{-x^2}{n}$.
53111. For each of the following sequences of functions $(g_n)$ find the pointwise limit, and determine whether the sequence converges uniformly on $[0,1]$, and on $[0,\infty)$.
    1. $\ds g_n(x) = \frac{x}{n}$.
    2. $\ds g_n(x) = \frac{x^n}{1+x^n}$.
    3. $\ds g_n (x) = \frac{x^n}{n+x^n}$.
531111. For each of the following sequences of functions $(h_n)$, where $h_n\colon [0,1]\rightarrow \R$, find the pointwise limit, if it exists, and in that case determine whether the sequence converges uniformly.
    1. $h_n(x) = \left(1-\frac{x}{n}\right)^2$.
    2. $h_n(x) = x-x^n$.
    3. $h_n (x) = \sum_{k=0}^n x^k$.
5311111. 
Define $f_n\colon \R\rightarrow \R$ by
$$
f_n (x) = \frac{n+\cos x}{2n+\sin^2 x}.
$$
    1. Find the pointwise limit of the sequence of functions $(f_n)$.
    2. Show that the sequence $(f_n)$ converges uniformly.
    3. Calculate $f_n'$ and show that $f'(x) = \lim_{n\rightarrow \infty} f_n'(x)$. Does $(f_n)$ satisfy the conditions of Theorem \iflatexml 4.2.3 \else [udiff](#udiff)\fi?
53111111. 
    1. Let $n\in \N$. Show that we can define a continuous function $f_n\colon [0,1]\rightarrow \R$ by
$$
f_n(x) = \left\{ \begin{array}{ll}
\ds 0 & x=0, \\
\ds\frac{x^{\frac{1}{n}}-1}{\ln x} & 0<x<1, \\
\ds\frac{1}{n} & x=1. \\
\end{array} \right.
$$

(Note: you only need check continuity at $x=0$ and $x=1$.)
    2. Does the sequence $(f_n)$ converge  uniformly to a limit? Justify your answer. If you wish, you may assume without proof that each function $f_n$ is monotone increasing.

%
    3. Prove that
%	$$
\lim_{n\rightarrow \infty }\int_0^1 f_n(x)dx =0.
$$
%

%531111111.   Compute the limits
%	$$
\lim_{n\rightarrow \infty} \int_0^1 \frac{e^{t^4}}{n}dt, \qquad \lim_{n\rightarrow \infty} \int_1^2 t^{2- \frac{\sin nt}{n}}dt,
$$
%justifying any procedures you use.


%
5311111111. %
%

%
%    1. Find a sequence of differentiable functions $(f_n)$, where  $f_n \colon [0,1] \rightarrow \R$, that converges pointwise to a function $f\colon [0,1]\rightarrow \R$, but such that the sequence of derivatives $(f'_n)$ does not converge to $f'$.
%
    2. Is it possible to have a sequence of differentiable  functions $(f_n)$, where
%$f_n \colon [0,1] \rightarrow \R$, that converges {\em uniformly} to a function $f\colon [0,1]\rightarrow \R$, but such that the sequence of derivatives $(f'_n)$ does not converge to $f'$~? Justify your answer.
%
%

%53111111111.  Which of the following functions are uniformly continuous? Justify your answers.


%


%    1. The function $f\colon (0,2] \rightarrow \R$ defined by  $f(x) = \frac{1}{x}$.

%
    2. The function $g\colon [1,2]\rightarrow \R$ defined by  $g(x) = \frac{1}{x}$.

%
    3. The function $h\colon [1,\infty ) \rightarrow \R$ defined by $h(x) = \frac{1}{x}$.

%
531111111111. Let $f_n:[a,b]\to\R$. Suppose that $\sum_{n=1}^\infty f_n$ converges uniformly to $f$. Show that the sequence $(f_n)$ converges uniformly to the zero function.



5311111111111. The functions $\cos,\sin:\R\to\R$ are defined by the infinite series
$$
s(x) = \sum_{n=0}^\infty\frac{(-1)^nx^{2n+1}}{(2n+1)!}, \hspace{2em} \text{ and } \hspace{2em} c(x) = \sum_{n=0}^\infty\frac{(-1)^kx^{2n}}{(2n)!}.
$$
    1. Prove that these functions are well-defined as pointwise limits, and that their series converge absolutely.
    2. Show that when restricted to a closed bounded interval $[-R,R]$, where $R>0$, both series' converge uniformly.
    3. Prove that $s$ and $c$ are differentiable everywhere, with $s'(x)=c(x)$ and $c'(x)=-s(x)$.
[Hint: Mimic the approach of Example \iflatexml 4.3.5 \else [eg:exp](#eg:exp)\fi in the notes.]
    4. Prove that $c^2+s^2=1$.

[Hint: Differentiate the function $f:\R\to\R$ given by $f(x)=c(x)^2+s(x)^2$ for each $x$.]
    5. ~* Show that $\exp(ix)=c(x)+is(x)$ for all $x\in\R$, where $\exp$ is the function from Example \iflatexml 4.3.5 \else [eg:exp](#eg:exp)\fi. You should justify any rearrangements of terms in infinite series (MAS107 Theorem 4.18 may help).
53111111111111.  By using the Weierstrass $M$-test or otherwise, for each of the following series, determine whether it  converges uniformly on $\R$ and  whether it  converges uniformly on $[0,1]$.
    1. $$
\sum_{n=1}^\infty \frac{1}{n^2 +x^2}
$$
    2. $$
\sum_{n=0}^\infty \frac{(-1)^nx^{2n+1}}{(2n+1)!}
$$
    3. $$
\sum_{n=1}^\infty \sin (nx)
$$
    4. (*)
$$
\sum_{n=1}^\infty \frac{\sin (nx)}{n}
$$
531111111111111. 
    1. Show the series $\sum_{n=1}^\infty x^n$ converges uniformly for $x\in [0,a]$ whenever $0<a<1$.
    2. Does the series converge uniformly on $[0,1)$~? Explain.
5311111111111111. Prove that there is a function $f\colon [0,2\pi] \rightarrow \R$ defined by
$$
f(x) = \sum_{n=1}^\infty \frac{\sin n x }{n^2}
$$
and that this function is continuous.

## 1.5. Integration

%{Chapter 7 problems} % Integration \iflatexml  \else \setcounterref{enumi}{q:133} \fi64.  Let $f:[1,4]\to\R$; $\ds f(x)=\frac{1}{x}$.

Let $P$ be the partition consisting of points $\left\{1,\frac{3}{2},2,4\right\}$.
    1. Compute $L(f,P)$, $U(f,P)$ and $U(f,P)-L(f,P)$.
    2. What happens to the value of $U(f,P)-L(f,P)$ when we add the point $3$ to the partition?
    3. Find a partition $P'$ of $[1,4]$ for which $U(f,P')-L(f,P')<\frac{2}{5}$.
641. Let $g:[0,1]\to\R$; $\ds g(x)=\left\{\begin{array}{cc} 1 & \text{for } 0\leq x<1 \\ 2 &\text{for } x=1 \end{array}\right.$.
[label=(\roman*)]    1. Show that $L(g,P)=1$ for every partition $P$ of $[0,1]$.
    2. Construct a partition $P$ for which $U(g,P)<1+\frac{1}{10}$
    3. Given $\varepsilon>0$, construct a partition $P_\varepsilon$ such that $U(g,P_\varepsilon)<1+\varepsilon$.
%
    4. Calculate $\int_0^1g(x)dx$.
6411.  (Exam question)
    1. Define step functions $r,s\colon \R \rightarrow \R$ by
$$
r = {\bf{1}}_{[0,1)} + e {\bf{1}}_{[1,2)} + e^4 {\bf{1}}_{[2,3]}, \qquad  s = e {\bf{1}}_{[0,1]} + e^4 {\bf{1}}_{(1,2]} + e^9 {\bf{1}}_{(2,3]}.
$$

Evaluate the integrals
$$
\int_0^3 r(x)dx, \qquad \int_0^3 s(x)dx.
$$
    2. Why is the function $f\colon [0,3]\rightarrow \R$ defined by $f(x)=e^{x^2}$ Riemann integrable?
    3. Prove that
$$
1+e+e^4 \leq \int_0^3 e^{x^2}\ dx \leq e+e^4+e^9.
$$

[Hint: there's no need to calculate the integral in the middle; use the previous parts to prove the inequalities.]
64111. Let $f,g:[a,b]\to\R$ be integrable functions.
    1. Show that if $P$ is a partition of $[a,b]$, then
$$
U(f+g,P) \leq U(f,P)+U(g,P)
$$
and
$$
L(f+g,P) \geq L(f,P)+L(g,P).
$$
Can you think of a particular example where these inequalities are strict?
    2. Let $P_1$ and $P_2$ be partitions of $[a,b]$. Show that
$$
U(f+g,P_1\cup P_2) \leq U(f,P_1) + U(g,P_2)
$$
and
$$
L(f+g,P_1\cup P_2) \geq L(f,P_1) + L(g,P_2)
$$
[Hint: Lemma [lem:ref](#lem:ref) may be helpful.]
    3. Deduce that
$$
L(f+g) \geq \int_a^bf(x)dx + \int_a^bg(x)dx
$$
and
$$
U(f+g) \leq \int_a^bf(x)dx + \int_a^bg(x)dx.
$$
Explain why this means $f+g$ must be integrable, with
$$
\int_a^b(f(x)+g(x))dx = \int_a^bf(x)dx + \int_a^bg(x)dx.
$$
641111. Show that if $k\in\R$ and $f:[a,b]\to\R$ is integrable, then so is $kf:[a,b]\to\R$; $x\mapsto kf(x)$, and
$$
\int_a^b kf(x)dx = k\int_a^bf(x).
$$
[Hint: It may help to treat the cases $k\geq 0$ and $k<0$ separately.]


6411111. Let $f$ be bounded on a set $A\subseteq\R$, and let
$$
M=\sup\{f(x):x\in A\}, \; m=\inf\{f(x):x\in A\},
$$
$$
M'=\sup\{|f(x)|:x\in A\}, \; \text{ and } \; m'=\inf\{|f(x)|:x\in A\}.
$$
    1. Show that $M-m\geq M'-m'$.
    2. Show that if $f$ is integrable $[a,b]$, then
$$
U(|f|,P)-L(|f|,P) \leq U(f,P) - L(f,P)
$$
for any partition $P$ of $[a,b]$.
    3. Complete the proof of Proposition \iflatexml 5.3.1(iii) \else [propsint](#propsint)([linear](#linear)) \fi; that is, show that $|f|$ is integrable whenever $f$ is.
64111111.  Let $f\colon \R \rightarrow \R$ be a continuous function, and let $a,b\colon \R \rightarrow \R$ be differentiable functions. Prove that
$$
\frac{d}{dx} \int_{a(x)}^{b(x)} f(t)dt = b'(x)f(b(x))-a'(x)f(a(x)).
$$



641111111.   Define a function $l:(0,\infty ) \rightarrow \R$ by
$$
l(x) = \int_1^x \frac{1}{t}dt.
$$

Show the following directly from the definition of $l$ via an integral (that is, \emph{without} using any properties of the function $\ln$). %You may assume the fundamental theorem of calculus and integration by substitution.
    1. $l$ is differentiable, and $l'(x) = \frac{1}{x}$.
    2. $l(xy) = l(x)+l(y)$ for all $x,y >0$.

%
    3. $l\left(\frac{x}{y}\right) = l(x)-l(y)$ for all $x,y >0$.
%

%6411111111.  (*)  Let $f\colon (0,\infty ) \rightarrow \R$ be a continuous function satisfying the formula $f(xy) =f(x)+f(y)$ for all $x,y>0$.

%


%    1. Prove that $f(x^a ) =af(x)$ for all $x>0$ and $a\in \R$.

%[Hint: Prove this first for $a\in\N$, then $a\in\Z$, then $a\in\Q$, and finally extend to $\R$ by continuity.]

%
    2. Prove that $f(x) = f(e)\ln (x)$ for all $x>0$.

%
    3. For the above function $L$, prove that $L(x) =\ln x$.

%
64111111111.  (*) Let $f\colon [a,b]\rightarrow \R$ be Riemann integrable. Prove that there is a number $x\in [a,b]$ such that
$$
\int_a^x f(t)dt = \int_x^b f(t)dt.
$$

[Hint: apply the intermediate value theorem to the function $F$ given by
$$
F(x) = \int_a^x f(t)dt - \int_x^b f(t)dt .\qquad ]
$$



641111111111. 
    1. Let $f\colon [a,b]\rightarrow \R$ be Riemann integrable. Suppose there are $m,M\in \R$ such that $m\leq f(x)\leq M$ for all $x\in [a,b]$. Prove that there is a number $\mu \in [m,M]$ such that
$$
\int_a^b f(x)\ dx = (b-a)\mu .
$$
    2. Let $f\colon [a,b]\rightarrow \R$ be continuous. Prove that there is some $c \in [a,b]$ such that
$$
\int_a^b f(x)\ dx = (b-a)f(c) .
$$
[Hint: The intermediate value theorem is useful.]
6411111111111. Let $f\colon [a,b]\rightarrow \R$ be continuous, and let $g\colon [a,b]\rightarrow [0,\infty )$ be integrable. Prove that there is some $c \in [a,b]$ such that
$$
\int_a^b f(x)g(x)\ dx = f(c) \int_a^b g(x)\ dx .
$$

Do we need the assumption $g(x)\geq 0$? Justify your answer.
