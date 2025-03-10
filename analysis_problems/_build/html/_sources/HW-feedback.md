(HW-feedback)=
# Homework feedback

Here is some general feedback comments about each piece of homework for MAS2004/9. Individual feedback can be viewed on Crowdmark --- let me know if you have any difficulty finding it.

Responding to individual feedback is the fastest way to improve as a mathematician. Hopefully your feedback will feel useful and make sense to you, but if it ever doesn't, please get in touch and I am more than happy to look at with you. 

## Feedback for Homework 1

**Problems:** [P2](#P2), [P3](#P3), [2](#2), [3](#3); &ensp;**Solutions:** [P2](#P2sol), [P3](#P3sol), [2](#2sol), [3](#3sol).

Well done for completing the first analysis homework! Here are some general comments.

### Problems [P2](#P2) and [P3](#P3)
These were generally answered well, and most people were able to find the intended theorems from their MAS107/MAS117 notes in order to re-prove the Bolzano-Weierstrass theorem. We'll be using this theorem more than once this semester, so this revision will come in handy. 

In [P2](#P2), there were some issues with mathematical writing, so make sure you go and look at the individual comments on your work and see what comments you can use to improve this.

### Problem [2](#2)
For this question, it's fine to just write down what the limit points are, but of course we like proofs in this module. If you did include a proof, well done! And take a look for comments about its structure and presentation. The [solutions](#2sol) do not currently include proofs, but I hope to add these in soon --- check back in a few days if you would like to see how they might go.

### Problem [3](#3)
The three parts of this question were not of equal difficulty, and this was intentional. I would say part (iii) is definitely the hardest, so well done if you got that one out. If you didn't, take a look at the indidual feedback and see if you can make some progress, and/or, bring it to an office hour. You may find it easier to tackle now you have had more time to practice.

One of the more common issues people had in [Problem 3(iii)](#3) was **defining a $\delta$ that depended on $x$ as well as $\varepsilon$**. This is an understandable error: once you get to the stage
```{math}
:label: hw1
\left|f(x)-\frac{5}{2}\right|=\left|1-\frac{1}{2x}\right||x-2|
```
it can be hard to know how to deal with the $\left|1-\frac{1}{2x}\right|$ factor. However, letting $\delta=\frac{\varepsilon}{|1-\frac{1}{2x}|}$ does **not** work here --- we need a $\delta$ that is independent of $x$ (though it is allowed to depend on $\varepsilon$). 

One way to see why is to look at the order that different variables appear in the definition of the limit:

$$
\forall\varepsilon>0\;\exists\delta>0\;\text{s.t. }\forall x\in X \; |x-a|<\delta\Rightarrow|f(x)-L|<\varepsilon.
$$

Here, $\varepsilon$ appears first, and so cannot depend on anything, and $\delta$ appears second, so can only depend on $\varepsilon$. In particular, $\varepsilon$ and $\delta$ appear *before* $x$, so neither are allowed to depend on $x$. 

To progress past the point of [](#hw1) with a $\delta$ independent of $x$, the thing to do take a $\delta$ that is the minimum of two values, with on value controlling each factor. For example, if $|x-2|<1$, then $0<1-\frac{1}{2x}<1$, so put $\delta=\min\{1,\text{?}\}$. Now find "$\text{?}$" (or have a look at the [solutions](#3iiisol)).
