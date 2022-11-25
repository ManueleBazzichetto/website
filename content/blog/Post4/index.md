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

To me, a random variable is something similar to the [Schrödinger's cat](https://en.wikipedia.org/wiki/Schrödinger%27s_cat): until you open the box, you don't know what's inside. The same holds for experiments: until you actually perform the experiment, you don't know what you are going to observe. The only thing you know is that something will eventually happen. Actually, that is not the only thing you know. Indeed, before the experiment takes place, one usually also has some guess about the value potentially assumed by whatever thing is going to be measured. Before flipping a coin (the experiment), we know it will either land head or coin. The idea takes form..  

I have heard/read many definitions of what a random variable is. Some are more 'formal', some are more intuitive, other, well, I formulated them myself). I will make a list.

Math-oriented definition:

- A random variable is a function that maps the outcome of an experiment (i.e., one of its possible realizations) to a number belonging to the real domain ($\mathbb{R}$). So, basically, each time an experiment is carried out, an observation is made and the random variable maps the observation to a number. Note that the fact that the observation is 'transformed' to a number is crucial, as we will need to do math with these numbers (e.g., we will estimate means, variances or whatever other quantity of interest).  

Informal, but intuitive, definitions:

- A random variable is something you measure on something that is random. This means we are taking measures on something that dynamically changes any time we repeat a procedure.

- A random variable is some measure we either have an imperfect knowledge about it or we don't know its value, as it depends on a yet to be performed procedure (such as an experiment).

- A random variable is a placeholder for the value associated with the realization of an experiment. This definition will probably make more sense after reading about notations below.

Programming-oriented definition:

- If you are familiar with the R programming language, well, you can think of a random variable as the formals of a function. When we write a function, formals are used as symbols that will assume a value only when the function is run and they are needed (see lazy evaluation).

#### Sample spaces, outcomes and events

#### Some words on notation

When working with random variables, notation has a crucial importance. Notation is (unfortunately) a free spot, so everyone can set up her/his own rules. But, usually, a random variable is written in capital letters, e.g. $X$. When the letter is capital, the cat is still within the box: we know there is a cat inside the box, but we don't know whether is death or alive. So, capital letter $X$ is there to remind us that we don't have observed any outcome yet, and, therefore, we don't have any specific measure derived from it. Once we open the box, $X$ becomes $x$. $x$ is no longer 'a potential, still unknown, measure', but it's an actual value. As such, $x$ is not a random variable. Be aware of the difference between $x$ and the bold $\pmb{x}$: the former represents a value, the latter represents a random vector, which is a collection of random variables.  
