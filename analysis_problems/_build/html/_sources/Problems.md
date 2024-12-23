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
## 1. Preliminary problems

(P1)=
P1. Which of the following statements is the correct definition of convergence of a real sequence $(x_n)$ to a limit $l\in\mathbb{R}$? How would you correct the incorrect statements?
<br>
[Note: There is more than one correct answer.]

  (i) $\varepsilon>0$ $N\in\mathbb{N}$ then $|x_n-l|<\varepsilon$.

  (ii) $\forall\varepsilon>0$ $\exists N\in\mathbb{N}$ s.t.  $|x_n-l|<\varepsilon$ $\forall n\geq N$.

  (iii) For all $\varepsilon>0$ and $N\in\mathbb{N}$, we have $|x_n-l|<\varepsilon$ whenever $n\geq N$.

  (iv) $\exists\varepsilon>0$ s.t. $\forall N\in\mathbb{N}$, $|x_n-l|<\varepsilon$ $\forall n\geq N$.

  (v) Given any $\varepsilon>0$, there is $N\in\mathbb{N}$ such that $|x_n-l|<\varepsilon$ whenever $n\geq N$.

<br>

(P2)=
P2. Prove using the $(\varepsilon-N)$-definition of convergence that the sequence $(x_n)$ given by $x_n = \frac{2n}{3n-1}$ converges to $\frac{2}{3}$ as $n\rightarrow\infty$.

<br>

(P3)=
P3. Using your MAS107 notes or another resource, look up and carefully state the Bolzano--Weierstrass theorem.
<br>
Its proof combines two other important results about sequences from MAS107. What do these results say?
<br>
[Note: We will use all three of these theorems at various points this semester. Check you are clear on what each of them is saying, and remember your lecturers and tutors are here to help.]

<br>

(P4)=
P4.  
  (i) If $a, b \geq 0$, show that $\sqrt{a + b} \leq \sqrt{a} + \sqrt{b}$.
  <br>
  [Hint: Consider the square of both sides. You may use that the square root function is increasing.]

  (ii) If $a,b \in \mathbb{R}$, deduce that $\left|\sqrt{|a|} - \sqrt{|b|}\right| \leq \sqrt{|a - b|}$.
    <br>
  [Hint: Imitate the proof of Corollary 1.1 in the lecture notes.]
  
  (iii) Hence prove that if the sequence $(a_{n})$ converges to $l$, then $\left(\sqrt{|a_{n}|}\right)$ converges to $\sqrt{|l|}$. 

<br>

(P5)=
P5. Look up and carefully define the *supremum* and *infimum* of a set $A\subseteq\mathbb{R}$. What conditions must be met for each of these to exist?

<br>

(P6)=
P6. Compute, without proof, the suprema and infima (if they exist) of the following sets:
  
  (i) $\left\{\frac{m}{n}:m,n\in\mathbb{N} \text{ s.t } m<n\right\}$.
  
  (ii) $\left\{\frac{(-1)^m}{n}:m,n\in\mathbb{N} \text{ s.t } m<n\right\}$.
  
  (iii) $\left\{\frac{n}{3n + 1} :n\in\mathbb{N}\right\}$.

<br>

(P7)=
P7. Let $A$ and $B$ be bounded and non-empty subsets of $\mathbb{R}$. Which of the following statements are true, and which are false?
  
  (i) $\inf A < \sup A$.
    
  (ii) For all $\varepsilon>0$, there is $x\in A$ such that $x-\inf A < \varepsilon$.
    
  (iii) $A\subseteq B$ implies $\sup A \leq \sup B$.
    
  (iv) If $x>0$ for all $x\in B$, then $\inf B >0$.
    
  (v) $\sup(A\cup B) = \max\{\sup A,\sup B\}$.

<br>

## 2. Limits of functions
(1)=
1. For each of the following formulas, what is the largest subset $X$ of $\mathbb{R}$  which may be taken as the domain of a function with that formula?

    (i) $f_{1}(x) = \displaystyle\frac{x^{2} + 2x + 7}{x(x+1)}$,

    (ii) $f_{2}(x) = \displaystyle\frac{(x-1)(x+4)}{x^{3} + 4x^{2} + x - 6}$,

    (iii) $f_{3}(x) = \displaystyle\frac{x+4}{x^{2}+5x + 6}$,

    (iv) $f_{4}(x) = \exp{\left(-\displaystyle\frac{1}{x-1}\right)}$,

    (v) $f_{5}(x) = \cos\left(\displaystyle\frac{1}{\pi x}\right)$.

(2)=
2. For each of the sets $X\subseteq\mathbb{R}$ below, calculate the associated set $L$ of its limit points. 

    (i) $X=(0,1)\cup[2,3)\cup\{4,5\}$,
    
    (ii) $X=\mathbb{Z}$, 

    (iii) $X=\mathbb{R}\setminus\mathbb{Z}$, 
    
    (iv) $X=\{x\in\mathbb{Q}:0<x<1\}$,

    (v) $X=\displaystyle\left\{\frac{1}{n}:n\in\mathbb{N}\right\}$.

(3)=
3. Let $f:\{0\}\cup[1,3]\to\mathbb{R}$; $f(x)=3x^2-1$. 

    (i) Write down the value of $\lim_{x\rightarrow 2}f(x)$.

    (ii) Use the $(\varepsilon-\delta)$ criterion (Definition 2.1) to prove your calculation in (i) is correct.

    (iii) Does $f(x)$ converge as $x\rightarrow 0$? Justify your answer. 

(4)=
4. For $f_2:A\to \mathbb{R}$ as in part (ii) of the [Problem 1](#1), investigate each of

$$
\lim_{x \rightarrow 1}f_{2}(x), \hspace{3em} \lim_{x \rightarrow -2}f_{2}(x) \hspace{2em} \text{ and } \hspace{2em} \lim_{x \rightarrow -3}f_{2}(x).
$$

Calculate the value of each limit, if it exists.

(5)=
5. If $f: \mathbb{R} \rightarrow [0, \infty)$ satisfies $\displaystyle\lim_{x \rightarrow a} f(x) = l$, where $l > 0$, show that 

$$
\lim_{x \rightarrow a} \sqrt{f(x)} = \sqrt{l}.
$$

Hence calculate $\displaystyle\lim_{x \rightarrow 1}\sqrt{\displaystyle\frac{x+1}{x^{2}}}$.
<br><br>
[Hint: For the first part, use the result of [P4 (iii)](P4) from the preliminary exercises.]

(6)=
6. Why are limits of functions unique? 

(7)=
7. (Homework 2 question) <br> 
Verify that $\text{sgn}(x) = \displaystyle\frac{|x|}{x} = \displaystyle\frac{x}{|x|}$, for $x \neq 0$ (see Example 2.3  in the notes for the definition).
<br>
Show that $\displaystyle\lim_{x \rightarrow 0}\text{sgn}    (x)$ does not exist. Show that both the left and right limits exist at $x=0$, and find their values.

(8)=
8. (Homework 2 question) <br>
For the following functions, each of which is defined on the whole of $\mathbb{R}$, find every point at which both the left and right limits exist, but are different from each other, and find the values of these limits.

    (i) $f(x) = \begin{cases} 1 -x & \text{if }x < 1\\ x^{2}& \text{if }x \geq 1. \end{cases}$

    (ii) $g(x) = [x]$, where
    ```{math}
    :label: eq:[x]
    [x] = \left\{\begin{array}{cl} \lfloor x\rfloor & \text{ if } x\geq 0 \\ \lceil x \rceil & \text{ if } x<0 \end{array}\right.
    ```
    denotes the integer part of $x$.
    
    (iii) $h(x) =3 - 5{\bf 1}_{(0, 1]}(x) + 7{\bf 1}_{(1, 2]}(x)$. [Here we have used the notation for indicator functions --- see Example 2.4 in the notes.]

(9)=
9. What is the largest subset $A$ of $\mathbb{R}$ for which we can specify a function by $f(x) = \sin\left(\frac{1}{x}\right)$? Does $f:A\to\mathbb{R}$ have a limit at $x = 0$? [Hint: Consider sequences whose $n$th term is $\frac{1}{\theta + 2n\pi}$, and think about good choices for $\theta$.]

(10)=
10. What is the largest subset $A$ of $\mathbb{R}$ for which we can specify a function by $f(x) = x\sin\left(\frac{1}{x}\right)$? Does $f:A\to\mathbb{R}$  have a limit at $x = 0$?

(11)=
11. In the notes, we gave meaning to $\displaystyle\lim_{x \rightarrow a} f(x)$ where $f:\mathbb{R} \rightarrow \mathbb{R}$ is a function and $a \in \mathbb{R}$. In this question, you can investigate what happens when $x$ tends to $\infty$ or $-\infty$.

    (i) Formulate a rigorous definition, in terms of $\varepsilon$'s and $\delta$'s, of what it means for $\displaystyle\lim_{x \rightarrow \infty}f(x)$ and $\displaystyle\lim_{x \rightarrow -\infty}f(x)$ to exist. 
    <br>
    [Hint: For the analogue of $(\varepsilon-\delta)$, think very carefully about how you are going to control the behaviour of $x$. Remember that you cannot treat $\infty$ as if it were a number!]

    (ii) Find an analogue of the sequential criterion for this case, and prove the analogous result to Theorem 2.1. 

    (iii) Check that you can prove that $\displaystyle\lim_{x \rightarrow \infty}\frac{1}{x} = \lim_{x \rightarrow -\infty}\frac{1}{x} = 0$, using your criterion.

(12)=
12.
    (i) Formulate a rigorous definition for $\displaystyle\lim_{x \rightarrow \infty}f(x) = \infty$ in terms of sequences  and write down an analogue of the $(\varepsilon-\delta)$ criterion. [The cases  $\displaystyle\lim_{x \rightarrow \infty}f(x) = -\infty$ and $\displaystyle\lim_{x \rightarrow -\infty}f(x) = \pm \infty$ can be treated similarly.]
    
    (ii) Let $f:\mathbb{R} \rightarrow [0, \infty)$ and $g:\mathbb{R} \rightarrow [0, \infty)$, and suppose that $\displaystyle\lim_{x \rightarrow \infty}f(x) = \infty$ and $\displaystyle\lim_{x \rightarrow \infty}g(x) = l$, where $l > 0$. Define $h(x) = f(x)g(x)$ for all $x \in \mathbb{R}$. Show that $\displaystyle\lim_{x \rightarrow \infty}h(x) = \infty$.
    
    (iii) Let $p: \mathbb{R} \rightarrow \mathbb{R}$ be an even polynomial of degree $m$, where the leading coefficient (i.e. the coefficient of $x^{m}$) is positive. Show that $\displaystyle\lim_{x \rightarrow \infty}p(x) = \lim_{x \rightarrow -\infty}p(x) = \infty$. What happens when $m$ is odd?

## 3. Continuity

(13)=
13. Return to [Problem 1](#1). Consider each function there, defined on the largest subset $A$ of $\mathbb{R}$
which can be taken as its domain, as found in that problem. For each function, what is the maximum subset of $A$ on which it is continuous?

(14)=
14. Let $f: \mathbb{R} \rightarrow \mathbb{R}$ be continuous at a point $a$.
Prove that $|f|$ is continuous at $a$, where $|f|(x) = |f(x)|$, for all $x \in \mathbb{R}$.
<br>
[Hint: Use the formulation of continuity with sequences (Theorem 3.1(ii)) and Corollary 1.1 from the notes.]

(15)=
15. Prove Theorem 3.3 in the notes (i.e. that composition of continuous functions is continuous). [Hint: Use sequences.]

(16)=
16. Define $f:\mathbb{R} \setminus \{0\}\to \mathbb{R}$ and $g: \mathbb{R} \rightarrow \mathbb{R}\setminus \{0\}$ by $f(x) = \frac{1}{x}$, and $g(x) = 1 + x^{2}$. Write down the functions $f \circ g$, and $g \circ f$, giving their domains explicitly. What can you say about continuity of these functions?

(17)=
17. For each of the functions in [Problem 7](#7):

    (i) Find the maximum subset of $\mathbb{R}$ on which it is continuous.
    
    (ii) Identify those discontinuities which are jumps, and calculate the size of each jump.

(18)=
18. (Homework 2 question)
    
    (i) Define $f:  \mathbb{R} \setminus \{0\} \rightarrow \mathbb{R}$ by
   
    $$
    f(x) = \displaystyle\frac{(1 + x)^{2} - 1}{x}.
    $$

    Find an extension of $f$ to the whole of $\mathbb{R}$ that is continuous there.
   
    (ii) Write down the largest subset of $\mathbb{R}$ which can be taken as the domain $A$ of the function $f$ given by
    
    $$
    f(x) = \displaystyle\frac{x^{3}-8}{x^{2} - 4}
    $$

    and explain why $f$ is continuous at every point of $A$. The complement $A^{c}$ of $A$ in $\mathbb{R}$ comprises two points. Show that $f$ may be extended to be continuous at only one of these points, and write down this continuous extension.

(19)=
19. Suppose that the function $g: \mathbb{R} \rightarrow \mathbb{R}$ is continuous at $a$ with $g(a) > 0$. Show that there exists $\delta > 0$ such that $g(x) > 0$  for all $ x \in (a - \delta, a + \delta)$. [Hint: Assume $g(a) > 0$ and try a proof by contradiction.]

(20)=
20.
    (i) For any $x, y \in \mathbb{R}$ show that
    
    $$
    \max\{x, y\} = \frac{1}{2}(x + y) + \frac{1}{2}|x - y|.
    $$
    
    Hence show that if both $f:A\to \mathbb{R}$ and $g: B \rightarrow \mathbb{R}$ are continuous at $a$, then so is $\max\{f, g\}$, where for all $x \in A\cap B$,
    
    $$
    \max\{f, g\}(x)  = \max\{f(x), g(x)\}.
    $$
    
    (ii) Find a similar expression for $\min\{x, y\}$, and hence prove continuity of $\min\{f, g\}$ at $a$.

(21)=
21. The aim of this question is to prove the following: the only functions $f: \mathbb{R} \rightarrow \mathbb{R}$ which are continuous at zero and satisfy $f(x+y) = f(x) + f(y)$ for all $x,y \in \mathbb{R}$ are the linear mappings $f(x) = kx$ for all $x \in \mathbb{R}$, where $k \in \mathbb{R}$ is fixed.
<br>
Begin by considering $f: \mathbb{R} \rightarrow \mathbb{R}$, such that $f(x+y) = f(x) + f(y)$ for all $x,y \in \mathbb{R}$.

    (i) Prove that $f(0) = 0$.
    
    (ii) Show that $f(-x) = -f(x)$ for all $x \in \mathbb{R}$.
    
    (iii) If $f$ is continuous at zero, prove that it is continuous at every $x \in \mathbb{R}$.
    
    (iv) If $f(1) = k$, prove that $f(n) = kn$ for all $n\in \mathbb{Z}$.
    
    (v) If $f(1) = k$, prove that $f\left(\frac{p}{q}\right) = k\frac{p}{q}$ for all $\frac{p}{q} \in \mathbb{Q}$.
    
    (vi) If $f(1) = k$ and $f$ is continuous at zero, prove that $f(x) =kx$ for all $x \in \mathbb{R}$.

(22)=
22. Show that Dirichlet's "other" function, as discussed in Example 3.8 in the notes, is discontinuous at every rational point in its domain.

(23)=
23. (Homework 2 question) <br>
What can you say about left/right continuity of the function  ${\bf 1}_{(a, b)}:\mathbb{R}\to\mathbb{R}$ at the points $a$ and $b$?

(23)=
23. Prove Corollary 3.1. [Hint: Apply the intermediate value theorem to the function $g(x) = f(x) - \gamma$, for $x \in [a, b]$.]

(25)=
25. Use Corollary 3.1

    (i) Every continuous function from $\mathbb{R}$ to $\mathbb{Z}$ is constant.

    (ii) Every continuous function from $\mathbb{R}$ to $\mathbb{Q}$ is constant.

(26)=
26. Prove the following {\it fixed point theorem}: if $f:[a,b] \rightarrow (a,b)$ is continuous, then there exists $c \in (a, b)$ such that $f(c) = c$.
<br>
[Hint: This is a similar proof to that of [Problem 24](#24). This time you need to consider a function of the form $g(x) = f(x) - $ (*something*). What is *something*?] Give a counter-example to demonstrate that the claim is false if the domain of $f$ is restricted to $(0, 1)$.

(27)=
27. Complete the proof of the extreme value theorem (Theorem 3.5), i.e. prove that a continuous function $f:[a,b]\to\mathbb{R}$ attains its infimum.

(28)=
28. Show that if $f:[0,1] \rightarrow \mathbb{R}$ is continuous and $0$ is not in the range of  $f$, then the function $\frac{1}{f}:[0,1]\to \mathbb{R}$ is bounded, where for each $x \in [0,1], \left(\frac{1}{f}\right)(x) = \frac{1}{f(x)}$.

(29)=
29. Explain why there are no continuous functions having domain $[0, 1]$ and range $\mathbb{R}$. [Hint: Use Theorem 3.5.]

(30)=
30. Suppose that the function $f:[0,1] \rightarrow [0,1]$ is continuous, and fix $0 < r < 1$. Suppose that we are given a sequence $(x_{n})$ in $[0,1]$ such that $f(x_{n+1}) \leq rf(x_{n})$ for all $n\in\mathbb{N}$. Show that there exists $c \in [0, 1]$ for which $f(c) = 0$. [Hint: Use the Bolzano-Weierstrass theorem.]

(31)=
31. Show that for each $n\in\mathbb{N}$, the function $f: [0, \infty)\to\mathbb{R}$ given by $f(x) =x^{n}$ is strictly monotonic increasing.

(32)=
32. Show that the function $f(x) = \sin(x)$ has a continuous inverse when restricted to the interval $\left[-\frac{\pi}{2}, \frac{\pi}{2}\right]$. What goes wrong outside this interval? [Hint: Use an appropriate trigonometric identity.]

(33)=
33. Find $\displaystyle\lim_{x \rightarrow 1}\frac{1 - x}{1 - x^{\frac{m}{n}}}$, where $m, n \in \mathbb{N}$.

(34)=
34. If $f:[a, b] \rightarrow \mathbb{R}$ is continuous and bijective, and $f(a) < f(b)$, show that $f$ is strictly monotonic increasing.

(35)=
35. $^*$ Show that if $f, g: \mathbb{R} \rightarrow \mathbb{R}$  are monotonic increasing, with $f+g$ continuous, then both $f$ and $g$ are continuous.

(36)=
36. $^*$ 

    (i) Let $(x_{n})$ be a sequence in $\mathbb{R}$ for which $x_{1} = a > 0$ and $x_{n+1} = \sqrt{x_{n}}$, for all $n\in\mathbb{N}$. Show that $\displaystyle\lim_{n \rightarrow \infty} x_{n} = 1$.

    (ii) Let $f: \mathbb{R} \rightarrow \mathbb{R}$ be a continuous function for which $f(x) = f(x^{2})$ for all $x \in \mathbb{R}$. Use the result of (i) to show that $f$ is constant.

## 4. Differentiation

(37)=
37. Let $f:A\to\mathbb{R}$ and let $a\in\mathbb{R}$ be such that there is some sequence $(x_n)$ in $A$ with
$x_n\neq a$ for all $n$ and $\displaystyle\lim_{n\to\infty} x_n=a$. What does it mean to say that
the function $f$ has limit $l$ at the point $a$? What notation do we use to write this?
<br>
[This question is asking you to recall (or revise if you can't recall) Definition 2.2 from the lecture notes.That's a key definition and we build on it when we define what it means to be differentiable --- see the next question.]

(38)=
38. 
    (i) Give the definition of what it means for a function $f:A\to\mathbb{R}$ to be differentiable at $a \in A$.
   
    (ii) State carefully what this means in terms of limits of sequences.
   
    (iii) State carefully what this means in terms of the $\varepsilon-\delta$ criterion.
    [The first part is just asking you to give Definition 4.1 and the other parts are checking that you know what this means.
    <br>
    The key points from Chapter 2 are `Definition `2.2 of a limit of a function and Theorem 2.1 giving the sequential criterion. But you need to see how to apply these, not just copy them out. Here they have to be applied to the relevant function for the definition of differentiability, not $f$ itself. ]

(39)=
39. Give a rigorous proof that the function $f:\mathbb{R}\setminus\{0\}\to \mathbb{R}$ given by
$f(x) = \frac{1}{x}$ is differentiable for all $x \in \mathbb{R} \setminus \{0\}$ from the definition of the derivative and find $f'(x)$ explicitly. Can we extend the function so that it is differentiable on the whole of $\mathbb{R}$ by defining its value at zero to be zero?

(40)=
40. Let $k\in \mathbb{R}\setminus\{0\}$. Give a rigorous proof from the definition of the derivative that  $f:\mathbb{R}\to \mathbb{R}$ given by  $f(x) = e^{kx}$ is differentiable for all $x \in \mathbb{R}$, and find $f'(x)$ explicitly.
<br>
[Hint: For fixed $k\in \mathbb{R}$, let $g:\mathbb{R}\to\mathbb{R}$ be given by $g(h)=e^{kh} - 1 - kh $.
You may use the fact that  $\displaystyle\lim_{h \rightarrow 0}\frac{g(h)}{h} = 0$. (This follows from the series expansion of the exponential function, which you already know, and we will study more later.) ]

(41)=
41. Consider the function  $f:\mathbb{R}\to \mathbb{R}$ given by $f(x) = \begin{cases} x\sin\left(\frac{1}{x}\right) & \text{if }x \neq 0,\\ 0 & \text{if }x = 0.\end{cases}$

    (i) Show that $f$ is differentiable at every $x \neq 0$. (You can use standard derivatives and facts about derivatives, such as the product and chain rules.)
    
    (ii) Show that $f$ is not differentiable at $x = 0$. (Use the definition of the derivative as a limit. You may assume that $\sin\left(\frac{1}{x}\right)$ has no limit as $x$ tends to $0$. This was [Problem 8](#8).)

(42)=
42. Show that the function  $f:\mathbb{R}\to \mathbb{R}$ given by 

$$
f(x) = \begin{cases} x^2\sin\left(\frac{1}{x}\right) & \text{if }x \neq 0,\\ 0 & \text{if }x = 0.\end{cases}
$$

is differentiable at every $x \in \mathbb{R}$. What can you say about its second derivative?
<br>
[Hint: You will need to consider the case $x=0$ separately from $x\in\mathbb{R}\setminus\{0\}$. You may assume that the limit as $x$ tends to $0$ of $x\sin\left(\frac{1}{x}\right)$ exists and equals $0$. This was studied in [Problem 10](10).]

(43)=
43.
    (i) Sketch the graph of any continuous function $f:[0,1]\to \mathbb{R}$ which is not differentiable at $x=\frac{1}{2}$, but is differentiable at all other points. [You do *not* need to give a formula.]

    (ii) Sketch the graph of any continuous function $f:[0,1]\to \mathbb{R}$ which is not differentiable at $x=\frac{1}{3}$ and is not differentiable at $x=\frac{2}{3}$, but is differentiable at all other points. [You do *not* need to give a formula.]

(44)=
44. Let $f:\mathbb{R}\to \mathbb{R}$ be given by $f(x) = x - [x]$ for all $x \in \mathbb{R}$, where $[x]$ denotes the integer part of $f$ (see [](#eq:[x])).
<br>
Explain carefully at which points $f$  is differentiable, and find the value of its derivative there. [It will probably help to sketch the graph!]

(45)=
45. Show that if $f:\mathbb{R} \rightarrow \mathbb{R}$ is differentiable at $a$ then

$$
\lim_{h \downarrow 0} \displaystyle\frac{f(a + h) - f(a - h)}{2h} = f'(a).
$$

By considering $f:\mathbb{R}\to\mathbb{R}$ given by $f(x) = |x|$, show that the limit on the left-hand side may exist, even when $f$ is not differentiable at $a$.

(46)=
46. A function $f:\mathbb{R} \rightarrow \mathbb{R}$ is defined by $f(x) = \begin{cases} -x^{2} & \text{if }x < 0,\\ x^{2} & \text{if }x \geq 0. \end{cases}$
<br>
Determine whether each of the following is true or false. Justify your answers.

    (i) $f$ is continuous at $0$.

    (ii) $f'(0)$ exists.

    (iii) $f':\mathbb{R}\to\mathbb{R}$ is continuous at $0$.

    (iv) $f^{\prime \prime}(0)$ exists.

(47)=
47.
    (i) Must any differentiable function $f:[a, b] \rightarrow \mathbb{R}$ have a maximum and minimum value? Why?
   
    (ii) If $f:[a, b] \rightarrow \mathbb{R}$ is differentiable  and $f(a) = f(b)$, must $f$ have a maximum and minimum value in $(a, b)$?

(48)=
48. Let $a_{0}, a_{1}, \ldots, a_{n}$ be real numbers such that

$$
a_{0} + \frac{a_{1}}{2} + \frac{a_{2}}{3} + \cdots + \frac{a_{n}}{n+1} = 0.
$$

Consider $f:\mathbb{R}\to\mathbb{R}$ given by $f(x) = a_{0}+ a_{1}x + a_{2}x^{2} + \cdots + a_{n}x^{n}$. Show that there is some $c\in (0,1)$ such that $f(c)=0$. [Hint: Integrate the function $f$ term--by--term, and think about how to use Rolle's theorem.]

(49)=
49.
    (i) Use the mean value theorem to show the following. If $f:\mathbb{R} \rightarrow \mathbb{R}$ is continuous on $[a, b]$ and differentiable on $(a, b)$ with $f'(c)= 0$ for all $c \in (a, b)$, then $f$ is constant on $[a, b]$.
   
    (ii) Use part (i) to show that if $g, h:\mathbb{R}\to\mathbb{R}$ are both continuous on $[a, b]$ and differentiable on $(a, b)$ with $h'(x) = g'(x)$ for all $x \in (a, b)$, then there exists $k \in \mathbb{R}$ such that $h(x) = g(x) + k$, for all $x \in [a, b]$.

(50)=
50. If $f:\mathbb{R} \rightarrow \mathbb{R}$ is continuous on $[a, b]$ and differentiable on $(a, b)$ and there exist $m, M \in \mathbb{R}$ such that $m \leq f'(c) \leq M$, for all $c \in (a, b)$, show that

$$
f(a) + m(b - a) \leq f(b) \leq f(a) + M(b-a).
$$

(51)=
51. If $r > 0$ and $q \in \mathbb{R}$ show that the polynomial $p(x) = x^{3} + rx + q$ has exactly one real zero.
[ You may assume the result of Corollary 3.2: $p$ has at least one real root. So you need to show that there can't be more than one. ]

(52)=
52. Let $r>1$ and fix $y\in (0,1)$. By applying the mean value theorem to the function $f(x)=x^r$ on $[y,1]$, show that

$$
1 - y^r < r(1 - y).
$$

(53)=
53. Let $f:\mathbb{R} \rightarrow \mathbb{R}$ be twice differentiable at $a$ with $f'(a) = 0$. If $f^{\prime \prime}(a) < 0$, show that $f$ has a local maximum at $a$, while if $f^{\prime \prime}(a) > 0$, show that $f$ has a local minimum at $a$.

## 5. Sequences and series of functions

(54)=
54. Consider the sequence of functions  $(f_n)$, where $f_n:[0,\pi ]\to \mathbb{R}$ is defined by $f_n(x) = \sin^n (x)$ for each $n\in\mathbb{N}$. Show that the sequence $(f_n)$ converges pointwise. Does the sequence $(f_n)$  converge uniformly? Justify your answer.

(55)=
55. For each of the following sequences of functions $(f_n)$ determine the pointwise limit (if it exists), and decide whether $(f_n)$ converges uniformly to this limit.

    (i) $f_n:[0,1]\to\mathbb{R}$, $f_n (x) = x^{\frac{1}{n}}$.
   
    (ii) $f_n:\mathbb{R}\to\mathbb{R}$, where $\displaystyle f_n (x)  = \left\{ \begin{array}{ll} 0 & x\leq n, \\ x-n & x\geq n \\ \end{array} \right.$.
   
    (iii) $f_n:(1,\infty)\to\mathbb{R}$, $f_n(x) = \frac{e^x}{x^n}$.
   
    (iv) $f_n:[-1,1]\to\mathbb{R}$, $f_n(x) = e^{-nx^2}$.
   
    (v) $f_n:\mathbb{R}\to\mathbb{R}$, $f_n(x) = e^{-x^2}{n}$.

(56)=
56. For each of the following sequences of functions $(g_n)$ find the pointwise limit, and determine whether the sequence converges uniformly on $[0,1]$, and on $[0,\infty)$.

    (i) $\displaystyle g_n(x) = \frac{x}{n}$.
   
    (ii) $\displaystyle g_n(x) = \frac{x^n}{1+x^n}$.
   
    (iii) $\displaystyle g_n (x) = \frac{x^n}{n+x^n}$.

(57)=
57. For each of the following sequences of functions $(h_n)$, where $h_n\colon [0,1]\rightarrow \mathbb{R}$, find the pointwise limit, if it exists, and in that case determine whether the sequence converges uniformly.

    (i) $h_n(x) = \left(1-\frac{x}{n}\right)^2$.
    
    (ii) $h_n(x) = x-x^n$.
    
    (iii) $h_n (x) = \sum_{k=0}^n x^k$.

(58)=
58. Define $f_n\colon \mathbb{R}\rightarrow \mathbb{R}$ by $f_n (x) = \frac{n+\cos x}{2n+\sin^2 x}$.

    (i) Find the pointwise limit of the sequence of functions $(f_n)$.

    (ii) Show that the sequence $(f_n)$ converges uniformly.

    (iii) Calculate $f_n'$ and show that $f'(x) = \lim_{n\rightarrow \infty} f_n'(x)$. Does $(f_n)$ satisfy the conditions of Theorem 5.2?

(59)=
59.
    (i) Let $n\in \mathbb{N}$. Show that we can define a continuous function $f_n\colon [0,1]\rightarrow \mathbb{R}$ by

    $$
    f_n(x) = \left\{ \begin{array}{ll}
    \displaystyle 0 & x=0, \\
    \displaystyle\frac{x^{\frac{1}{n}}-1}{\ln x} & 0<x<1, \\
    \displaystyle\frac{1}{n} & x=1. \\
    \end{array} \right.
    $$

    (Note: you only need check continuity at $x=0$ and $x=1$.)

    (ii) Does the sequence $(f_n)$ converge  uniformly to a limit? Justify your answer. If you wish, you may assume without proof that each function $f_n$ is monotone increasing.

(60)=
60. Let $f_n:[a,b]\to\mathbb{R}$. Suppose that $\sum_{n=1}^\infty f_n$ converges uniformly to $f$. Show that the sequence $(f_n)$ converges uniformly to the zero function.



(61)=
61. The functions $c,s:\mathbb{R}\to\mathbb{R}$ are defined by the infinite series $s(x) = \sum_{n=0}^\infty\frac{(-1)^nx^{2n+1}}{(2n+1)!}$, $c(x) = \sum_{n=0}^\infty\frac{(-1)^kx^{2n}}{(2n)!}$.

    (i) Prove that these functions are well-defined as pointwise limits, and that their series converge absolutely.

    (ii) Show that when restricted to a closed bounded interval $[-R,R]$, where $R>0$, both series' converge uniformly.

    (iii) Prove that $s$ and $c$ are differentiable everywhere, with $s'(x)=c(x)$ and $c'(x)=-s(x)$.
    [Hint: Mimic the approach of Example 5.7 in the notes.]
    
    (iv) Prove that $c^2+s^2=1$. [Hint: Differentiate the function $f:\mathbb{R}\to\mathbb{R}$ given by $f(x)=c(x)^2+s(x)^2$ for each $x$.]
    
    (v)* Show that $\exp(ix)=c(x)+is(x)$ for all $x\in\mathbb{R}$, where $\exp$ is the function from Example 5.7. You should justify any rearrangements of terms in infinite series (MAS107 Theorem 4.18 may help).

(62)=
62. By using the Weierstrass $M$-test or otherwise, for each of the following series, determine whether it  converges uniformly on $\mathbb{R}$ and  whether it converges uniformly on $[0,1]$.

    (i) $\displaystyle\sum_{n=1}^\infty \frac{1}{n^2 +x^2}$
    
    (ii) $\displaystyle\sum_{n=0}^\infty \frac{(-1)^nx^{2n+1}}{(2n+1)!}$
    
    (iii) $\displaystyle\sum_{n=1}^\infty \sin (nx)$

    (iv)* $\displaystyle\sum_{n=1}^\infty \frac{\sin (nx)}{n}$

(63)=
63. 
    (i) Show the series $\sum_{n=1}^\infty x^n$ converges uniformly for $x\in [0,a]$ whenever $0<a<1$.
   
    (ii) Does the series converge uniformly on $[0,1)$~? Explain.

(64)=
64. Prove that there is a function $f\colon [0,2\pi] \rightarrow \mathbb{R}$ defined by

$$
f(x) = \sum_{n=1}^\infty \frac{\sin n x }{n^2}
$$

and that this function is continuous.

## 6. Integration

(65)=
65. Let $f:[1,4]\to\mathbb{R}$; $\displaystyle f(x)=\frac{1}{x}$. Let $P$ be the partition consisting of points $\left\{1,\frac{3}{2},2,4\right\}$.

    (i) Compute $L(f,P)$, $U(f,P)$ and $U(f,P)-L(f,P)$.
   
    (ii) What happens to the value of $U(f,P)-L(f,P)$ when we add the point $3$ to the partition?
   
    (iii) Find a partition $P'$ of $[1,4]$ for which $U(f,P')-L(f,P')<\frac{2}{5}$.

(66)=
66. Let $g:[0,1]\to\mathbb{R}$; $\displaystyle g(x)=\left\{\begin{array}{cc} 1 & \text{for } 0\leq x<1 \\ 2 &\text{for } x=1 \end{array}\right.$.

    (i) Show that $L(g,P)=1$ for every partition $P$ of $[0,1]$.
    
    (ii) Construct a partition $P$ for which $U(g,P)<1+\frac{1}{10}$
    
    (iii) Given $\varepsilon>0$, construct a partition $P_\varepsilon$ such that $U(g,P_\varepsilon)<1+\varepsilon$.

(67)=
67. (Exam question)

    (i) Define step functions $r,s\colon \mathbb{R} \rightarrow \mathbb{R}$ by
   
    $$
    r = {\bf{1}}_{[0,1)} + e {\bf{1}}_{[1,2)} + e^4 {\bf{1}}_{[2,3]}, \qquad  s = e {\bf{1}}_{[0,1]} + e^4 {\bf{1}}_{(1,2]} + e^9 {\bf{1}}_{(2,3]}.
    $$

    Evaluate the integrals

    $$
    \int_0^3 r(x)dx, \qquad \int_0^3 s(x)dx.
    $$

    (ii) Why is the function $f\colon [0,3]\rightarrow \mathbb{R}$ defined by $f(x)=e^{x^2}$ Riemann integrable?

    (iii) Prove that

    $$
    1+e+e^4 \leq \int_0^3 e^{x^2}\ dx \leq e+e^4+e^9.
    $$

    [Hint: there's no need to calculate the integral in the middle; use the previous parts to prove the inequalities.]

(68)=
68. Let $f,g:[a,b]\to\mathbb{R}$ be integrable functions.

    (i) Show that if $P$ is a partition of $[a,b]$, then
    
    $$
    U(f+g,P) \leq U(f,P)+U(g,P)
    $$
    
    and
    
    $$
    L(f+g,P) \geq L(f,P)+L(g,P).
    $$
    
    Can you think of a particular example where these inequalities are strict?
    
    (ii) Let $P_1$ and $P_2$ be partitions of $[a,b]$. Show that

    $$
    U(f+g,P_1\cup P_2) \leq U(f,P_1) + U(g,P_2)
    $$
    
    and
    
    $$
    L(f+g,P_1\cup P_2) \geq L(f,P_1) + L(g,P_2)
    $$
    
    [Hint: Lemma 6.1 may be helpful.]
    
    (iii) Deduce that
    
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

(69)=
69. Show that if $k\in\mathbb{R}$ and $f:[a,b]\to\mathbb{R}$ is integrable, then so is $kf:[a,b]\to\mathbb{R}$; $x\mapsto kf(x)$, and

$$
\int_a^b kf(x)dx = k\int_a^bf(x).
$$

[Hint: It may help to treat the cases $k\geq 0$ and $k<0$ separately.]

(70)=
70. Let $f$ be bounded on a set $A\subseteq\mathbb{R}$, let $M=\sup\{f(x):x\in A\}, \; m=\inf\{f(x):x\in A\}$, and let $M'=\sup\{|f(x)|:x\in A\}, \; \text{ and } \; m'=\inf\{|f(x)|:x\in A\}$.

    (i) Show that $M-m\geq M'-m'$.

    (ii) Show that if $f$ is integrable $[a,b]$, then
    
    $$
    U(|f|,P)-L(|f|,P) \leq U(f,P) - L(f,P)
    $$

    for any partition $P$ of $[a,b]$.
    
    (iii) Complete the proof of Proposition 6.3(iii) that is, show that $|f|$ is integrable whenever $f$ is.

(71)=
71.  Let $f\colon \mathbb{R} \rightarrow \mathbb{R}$ be a continuous function, and let $a,b\colon \mathbb{R} \rightarrow \mathbb{R}$ be differentiable functions. Prove that

$$
\frac{d}{dx} \int_{a(x)}^{b(x)} f(t)dt = b'(x)f(b(x))-a'(x)f(a(x)).
$$

(72)=
72. Define a function $l:(0,\infty ) \rightarrow \mathbb{R}$ by $l(x) = \int_1^x \frac{1}{t}dt$.
<br>
Show the following directly from the definition of $l$ via an integral (that is, *without* using any properties of the function $\ln$).
    
    (i) $l$ is differentiable, and $l'(x) = \frac{1}{x}$.

    (ii) $l(xy) = l(x)+l(y)$ for all $x,y >0$.

(73)=
73.$^*$ Let $f\colon [a,b]\rightarrow \mathbb{R}$ be Riemann integrable. Prove that there is a number $x\in [a,b]$ such that

$$
\int_a^x f(t)dt = \int_x^b f(t)dt.
$$

[Hint: apply the intermediate value theorem to the function $F$ given by

$$
F(x) = \int_a^x f(t)dt - \int_x^b f(t)dt .\qquad ]
$$

(74)=
74.
    (i) Let $f\colon [a,b]\rightarrow \mathbb{R}$ be Riemann integrable. Suppose there are $m,M\in \mathbb{R}$ such that $m\leq f(x)\leq M$ for all $x\in [a,b]$. Prove that there is a number $\mu \in [m,M]$ such that

    $$
    \int_a^b f(x)\ dx = (b-a)\mu .
    $$
    
    (ii) Let $f\colon [a,b]\rightarrow \mathbb{R}$ be continuous. Prove that there is some $c \in [a,b]$ such that
    
    $$
    \int_a^b f(x)\ dx = (b-a)f(c) .
    $$
    
    [Hint: The intermediate value theorem is useful.]

(75)=
75. Let $f\colon [a,b]\rightarrow \mathbb{R}$ be continuous, and let $g\colon [a,b]\rightarrow [0,\infty )$ be integrable. Prove that there is some $c \in [a,b]$ such that

$$
\int_a^b f(x)g(x)\ dx = f(c) \int_a^b g(x)\ dx .
$$

Do we need the assumption $g(x)\geq 0$? Justify your answer.