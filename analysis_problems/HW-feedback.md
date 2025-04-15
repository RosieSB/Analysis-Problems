(HW-feedback)=
# Homework feedback

Here is some general feedback comments about each piece of homework for MAS2004/9. Individual feedback can be viewed on Crowdmark --- let me know if you have any difficulty finding it.

Responding to individual feedback is the fastest way to improve as a mathematician. Hopefully your feedback will feel useful and make sense to you, but if it ever doesn't, please get in touch and I am more than happy to look at it with you. 


## Feedback for Homework 3

**Problems:** [18](#18), [25](#25) ; &ensp;**Solutions:** [18](#18sol), [25](#25sol)

This homework was generally answered well, which is great to see. I'm particularly pleased to see proofs and mathematical presentation improving, so well done for your hard work there.

Remember to take the time to carefully review the feedback your work has received on Crowdmark, and attend [office hours](https://rosiesb.github.io/Analysis-Notes/0Intro.html#where-to-get-help) if you would like help interpreting or following the advice you are given.

### General presentation remarks

As I say, presentation is definitely getting better, which is great. Where there were issues, it's largely the same comments as previous times: 

- Remember to use words/short sentences to express a mathematical argument, not just equations. 

- Always introduce variables/functions *before* referring to them in a proof

- If you introduce a function, say what the domain is, as well as the rule. Different domains mean different functions, even when the rule is the same.

- If you are still getting significant comments on your work about presentation, it is probably worth your while to come to office hour and we can look over things together. I won't judge --- these things are just easier to explain in person.

### Problem 18

This question was generally answered well. The most frequent comments are below:

- It isn't essential to use $\varepsilon-\delta$ arguments every time now, as we have proven so many functions are continuous, and have results like [Theorem 3.2](https://rosiesb.github.io/Analysis-Notes/3Cty.html#AOL3) to combine them. Generally speaking, unless the question specifies differently, you can use results proved in the module, provided you indicate clearly that that is what you are doing. <br>
<br>
So for example, in 18(i), saying "We assume $f$ is continuous on $\mathbb{R}\setminus\{0\}$" is no good, but saying "Note that $f$ is continuous since it is a rational function" does constitute a valid proof at this stage --- even though it is brief and doesn't involve any $\varepsilon$s or $\delta$s.<br>
<br>
You will need to be able to do $\varepsilon-\delta$ arguments sometimes, though (e.g. in the exam).<br><br>

- In 18(ii), a few people fell into the trap of claiming $f$ can be defined on $A=\mathbb{R}\setminus\{-2\}$, because of the simplification $f(x)=\frac{x^3-8}{x^2-4}=\frac{x^2+2x+4}{x+2}$. However, this simplification is **only** valid on $\mathbb{R}\setminus\{\pm 2\}$, and this needs to be the set $A$. We have to use the formula for $f$ that we are given, and so $f(2)$ is not meaningful.
<br><br>
Unfortunately, if you made this mistake, the rest of 18 generally didn't work out. The progression of ideas is: $f$ has domain $A:=\mathbb{R}\setminus\{\pm 2\}$, has a continuous extension to $\mathbb{R}\setminus\{-2\}$, but cannot be extended to any continuous function with domain $\mathbb{R}$. In particular, $f$ does **not** have a discontinuity at $-2$, because $-2$ does not belong to the domain of $f$.

### Problem 25

Most people worked out that they needed to put $g:[a,b]\to\mathbb{R}$, $g(x)=f(x)-x$, but quite a few forgot to say what the domain of $g$ is. This is important, since [Proposition 3.1](https://rosiesb.github.io/Analysis-Notes/3Cty.html#ivt-sc) only applies to functions with certain kinds of domain. Once you have what $g$ needs to be, the solution is a straightforward application of Proposition 3.1 --- just make sure you write out your arguments as clearly as possible. 

This question was quite all or nothing, in that there was a trick to spot before you could really get anywhere. The good news is, there are only so many of these analysis "tricks" you need to know. And this is one of them! Similar things come up from time to time --- we already had one in Q24, and there will be more once we get to Rolle's theorem and the mean value theorem (see for example questions 3 and 5 in the [extra analysis exam-style questions](https://vle.shef.ac.uk/webapps/blackboard/content/launchLink.jsp?course_id=_119813_1&content_id=_8251522_1&mode=cpview), for example).

If you didn't get the trick for this question, have another go now you know what function $g$ to pick. The solutions are also available for when you are ready to see the full argument and check your answers.

## Feedback for Homework 2

**Problems:** [8](#8), [9](#9), [19](#19), [22](#22) ; &ensp;**Solutions:** [8](#8sol), [9](#9sol), [19](#19sol), [22](#22sol)

Thank you for your hard work completing this rather long set of exercises.

Remember to take the time to carefully review the feedback your work has received on Crowdmark, and attend [office hours](https://rosiesb.github.io/Analysis-Notes/0Intro.html#where-to-get-help) if you would like help interpreting or following the advice you are given.

### General presentation remarks

- It's fine to write out definitions, but be clear that's what you are doing by clearly delineating it from your proofs. If it is an $\varepsilon-\delta$ definition that you are trying to prove is true, try to convert it into a goal (e.g. "Given $\varepsilon>0$, we need to find $\delta>0$ such that...") rather than just rewriting the definition --- you haven't proven it applies yet!

- Make sure you introduce variables before using them ($\varepsilon$, $\delta$, $x$, $n$, etc.). This was a common issue in 8(b) --- see below.

- If you skipped questions because you were stuck or short of time, I'm happy to still look at them with you in office hours.

- There were still a few instances of people defining $\delta>0$ dependent on $x$. [See above](#3iiifeedback) for why this doesn't work! And/or ask me about it.

### Problem 8

In this question, you had to compute left and right limits of the given functions and comment on when they disagreed. You then had to prove you were right using [Definition 2.4](https://rosiesb.github.io/Analysis-Notes/2LoF.html#marg), or the equivalent definitions involving sequences. 

Nearly everyone was able to compute the limits in parts (a) and (c). For part (b), a lot of people looked at $\lim_{x\rightarrow n^+}g(x)$ and $\lim_{x\rightarrow n^-}g(x)$ without saying what $n$ is. If you are assuming $n$ is an integer, make sure you say so first. In fact, you get different answers depending on whether $n$ is a positive integer or a negative integer.

In the examples given, all functions had jump discontinuities (either a finite or countably infinite number of them). Proving that a function has a jump discontinuity requires more work than proving it is discontinuous at a point. For the former, you need to prove that two marginal limits exist, but disagree. If you are using sequences to do this, they need to be general --- picking a couple of specific sequences isn't enough. On the other hand, if all you aim to show is that a function is discontinuous somewhere, then you don't need a general sequence --- you just need one (or occasionally, two) examples that show the definition of continuity fails. 

In some cases, people had computed limits without any attempt at proving them. Be careful here! We already know you can compute limits: this was core syllabus at Level 1. The "new" content in this module is all about formal proofs --- make sure seek out help with this as much as you need.

Finally, many people made this question unecessarily hard for themselves by not drawing pictures. I especially recommend doing so for parts (b) and (c)! 

### Problem 9

This question was answered well on the whole, so well done! Presentation was also generally better for the question than the $\varepsilon-\delta$ proofs. I think the main cases where people didn't get the question out are because they didn't follow the hint. Please come to office hours for help with this if you struggled with this bit.

### Problem 19

Here, nearly everyone I saw who attempted the question knew they needed to put something like $\varepsilon=\frac{g(a)}{2}$ into the definition of continuity of $g$ at $a$, which shows good intuition! However, many struggled to turn this into a mathematical argument.

Remember, an inequality calculation on its own does not constitute a proof, you need to explicitly connect it in some way to the assumptions of the question (in this case, that $g$ is continuous and positive at $a$). In fact, most people did have the bare bones of what they needed to complete the question correctly. Remember, you can always ask for help with this. Once you get the trick for turning this kind of working out into a proof, it is the same nearly every time, but it does take most people some time for it to "click" (ask anyone).

If you are getting comments like "there is no argument here" or similar, that is a sign that you may need to come to an office hour for more support with your proof writing.


### Problem 22

Those who attempted this generally got it out, so well done! In future, if a "weird" question like this one is assigned as homework like this one, I'd much prefer you come and get some help with it than leave it blank. But I also appreciate that this time around, there was a lot to do.



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
The three parts of this question were not of equal difficulty, and this was intentional. I would say part (iii) is definitely the hardest, so well done if you got that one out. If you didn't, take a look at the individual feedback and see if you can make some progress, and/or, bring it to an [office hour](https://rosiesb.github.io/Analysis-Notes/0Intro.html#where-to-get-help). You may find it easier to tackle now you have had more time to practise.

(3iiifeedback)=
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