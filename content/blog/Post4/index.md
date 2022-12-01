---
title: What the heck is a random variable?
tags: stats
date: 2022-11-25

math: true
---

<figure>
  <img src="CatInBox.jpg" alt="" style="width:150%">
  <figcaption></figcaption>
</figure>

Having no background in statistics, understanding what a random variable is was a nightmare for me. The funny part was when I realized that, in the end, a random variable can be different things, but never exclusively a single one (I am aware this is not helpful).

So, what the heck is a random variable!?  

To me (assume we can have our own idea about that), a random variable is something similar to the [Schrödinger's cat](https://en.wikipedia.org/wiki/Schrödinger%27s_cat) paradox: until you open the box, you don't know what's inside. The same idea holds for experiments: until you perform the experiment, you don't know what you are going to observe. The only thing you know is that something will eventually happen. Well, actually that is not the only thing you know in advance. Indeed, before an experiment takes place, one usually also has some guess about the potential value of whatever thing is going to be measured (at least, a range of values). Before flipping a coin (the experiment), we know it will land either head or coin.  

I have heard/read many definitions of what a random variable is. Some are more 'formal', some are more intuitive, others, well, I formulated them myself. Below, a list of definitions.

Math-oriented definition:

- A random variable is a function that maps the outcome of an experiment (i.e., one of its possible realizations) to a number belonging to the real domain ($\mathbb{R}$). So, basically, each time an experiment is carried out, something is observed and a measure is taken on the observation. The random variable is the function mapping the observation to a number associated with the measure. Note that the fact that the observation is 'transformed' to a number is crucial, as we will need to do math with these numbers (e.g., we will estimate means, variances or whatever other quantity of interest). In the 'coin-flipping' experiment, one possible outcome could be H (head), which the random variable will map to a number (e.g., 1).  

Informal, but more intuitive, definitions:

- A random variable is something you measure on something that is random. This means we are taking measures on something that potentially changes any time we repeat a procedure.

- A random variable is a measure whose value we do not know (or have limited knowledge of) because it depends on a yet to be performed procedure (such as an experiment). As long as we don't know flip the coin, we can just wonder whether it will land head or tail.

- A random variable is a placeholder for a value associated with the realization of an experiment (this definition will probably make more sense after reading about notation below).

Programming-oriented definition:

- If you are familiar with the R programming language, you may find useful thinking of a random variable as arguments of a function. When we write a function, arguments are used as symbols that assume a value only when the function is run (and arguments are needed, see [lazy evaluation](https://adv-r.hadley.nz/functions.html?q=lazy%20eva#lazy-evaluation)).

#### Sample spaces, outcomes and events

To more formally introduce the concept of random variable, we need to talk about sample spaces, outcomes and events. In a nutshell, outcomes, as said above, are individual realizations of an experiment. Sample spaces include all possible outcomes of an experiment (the sample space is the space where outcomes live). Indeed, sample spaces are represented as sets of outcomes. If our experiment consisted in flipping a coin twice, then the sample space would be represented as \{ HH, HT, TH, TT \}. There exists different types of samples spaces: discrete finite, discrete infinite and continuous. Depending on the type of sample space, the random variable will be ..

#### Some words on notation

When working with random variables, notation has a crucial importance. Unfortunately, notation can differ among textbooks or other sources (potentially, everyone can set up her/his own notation's rule). Usually, a random variable is written in capital letters, e.g. $X$. Back to the Schrödinger's cat, when the random variable is expressed in capital letter it means that the cat is still within the box: we know there is a cat inside the box, but we don't know whether is death or alive (or black or white). So, the capital letter $X$ is there to remind us that we don't have observed any outcome yet, and, therefore, we don't have any specific measure in our hands. Once we open the box, $X$ becomes $x$, which does not any longer represent 'a potential, still unknown, measure', but its actual value. As such, $x$ is not a random variable. Be aware of the difference between $x$ and the bold $\pmb{x}$: the former represents an actual value, the latter represents a random vector, which is a collection of random variables. Also, mind the difference between $X$ and $\pmb{X}$, as the latter (usually) represents a random matrix!  
