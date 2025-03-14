(HW-feedback)=
# Homework feedback

Here is some general feedback comments about each piece of homework for MAS2004/9. Individual feedback can be viewed on Crowdmark --- let me know if you have any difficulty finding it.

Responding to individual feedback is the fastest way to improve as a mathematician. Hopefully your feedback will feel useful and make sense to you, but if it ever doesn't, please get in touch and I am more than happy to look at it with you. 

## Feedback for Homework 1

**Problems:** [P2](#P2), [P3](#P3), [2](#2), [3](#3); &ensp;**Solutions:** [P2](#P2sol), [P3](#P3sol), [2](#2sol), [3](#3sol).

Well done for completing the first analysis homework! Here are some general comments.

### General comments on mathematical writing

- The absolute best thing you can do is look at the individual comments on your work on Crowdmark, and [get help](https://calendar.app.google/vqdgru29fnbycVoY6) interpreting them as needed. Analysis proofs are notoriously picky, and all mathematicians go through this at some stage or other, so please don't feel embarassed about needing help with your proof writing.

- When using a definition to solve a problem, it's fine to write out the general definition, but make sure you also explicitly link it to the question at hand. So, for example, when solving [Problem 3](#3), you could (though don't have to) begin by copying out [Definition 2.2](https://rosiesb.github.io/Analysis-Notes/2LoF.html#functionlimit) from the notes. If you do that, make sure you then say something like "Therefore, given $\varepsilon>0$, we seek $\delta>0$ such that ..." and link it to the specific functions and limits you are working with.

- Remember to only use notation/variables after you have introduced them. This sometimes relates to the above point --- Definition 2.2 has a general limit $L$ in it, but there's no need to carry it around in your solution if you know the actual numerical limit you're aiming for (e.g. $5/2$).

### Problems P2 and P3
These were generally answered well, and most people were able to find the intended theorems from their MAS107/MAS117 notes in order to re-prove the Bolzano-Weierstrass theorem. We'll be using this theorem more than once this semester, so this revision will come in handy. 

In [P2](#P2), there were some issues with mathematical writing, so make sure you go and look at the individual comments on your work and see what comments you can use to improve this.

### Problem 2
For this question, it's fine to just write down what the limit points are, but of course we like proofs in this module. If you did include a proof, well done! And take a look for comments about its structure and presentation. The [solutions](#2sol) do now include proofs, if you would like to see how they go.

### Problem 3
The three parts of this question were not of equal difficulty, and this was intentional. I would say part (iii) is definitely the hardest, so well done if you got that one out. If you didn't, take a look at the individual feedback and see if you can make some progress, and/or, bring it to an office hour. You may find it easier to tackle now you have had more time to practise.

One of the more common issues people had in [Problem 3(iii)](#3) was defining a $\delta$ that depended on $x$ as well as $\varepsilon$. This is an understandable error: once you get to the stage
```{math}
:label: hw1
\left|f(x)-\frac{5}{2}\right|=\left|1-\frac{1}{2x}\right||x-2|
```
it can be hard to know how to deal with the $\left|1-\frac{1}{2x}\right|$ factor. However, letting $\delta=\frac{\varepsilon}{|1-\frac{1}{2x}|}$ does **not** work here --- we need a $\delta$ that is independent of $x$ (though it is allowed to depend on $\varepsilon$). One way to see why is to look at the order that different variables appear in the definition of the limit:

$$
\forall\varepsilon>0\;\exists\delta>0\;\text{s.t. }\forall x\in X \; |x-a|<\delta\Rightarrow|f(x)-L|<\varepsilon.
$$

Here, $\varepsilon$ appears first, and so cannot depend on anything, and $\delta$ appears second, so can only depend on $\varepsilon$. In particular, $\varepsilon$ and $\delta$ appear *before* $x$, so neither are allowed to depend on $x$. 

To progress past the point of [](#hw1) with a $\delta$ **independent** of $x$, the thing to do take a $\delta$ that is the minimum of two values, with on value controlling each factor. For example, if $|x-2|<1$, then $0<1-\frac{1}{2x}<1$, so put $\delta=\min\{1,\text{?}\}$. Now find "$\text{?}$" (or have a look at the [solutions](#3iiisol)).
