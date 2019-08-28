---

layout: post
title: "Foundation of Statistics"
date: 2019-06-23 12:37:46 +0530
categories: bayesian deep-learning
---

Welcome to the first article of the series of the Bayesian Methods for Deep Learning. In this article I will give out a basic foundation for Statistics as much as possible. 

## Probability

Most of us must have done at least a little bit of probability at some stage of their school education. Nevertheless this shall give you a small recap of the basics. 

When someone says "There's a high probability that we will win the match today". What exactly does it mean? The _chance_ of winning the game is presented as a fraction. And we sometimes multiply this by 100% and say that "I'm 72% sure that we will min the match today. What they are saying here is the chance that an event will happen in the future (It could be in the past as well if the data is obscure.) 

I shall be using the book _Introduction to the Theory of Statistics by Moods_ as a reference book in this article and future article

There are several ways to represent the _chance_ of some event happening and I have briefly introduced them below. Before we begin, let us get some terms out of the way that might be trvial yet required.
_Note: These definitions are not meant to be used in an examination of any sorts :) These are here for you to understand the terms_

1. Experiment :- An operation that can be made in a controlled environment with set number of outcomes.
2. Event :- An outcome(or a collection of outcomes) of an experiment. More formally an event is a subset of the sample space.
3. Sample Space :- The set of all possible events(outcomes) of an experiment
4. Event Space :- The power set of the sample space. THe set of all possible events that is possible from the sample space.
### Notation: 

Notation is quite important in the field of any science. Anyone who has tried to decipher the notation of a research paper written by someone with the wild imagination of a mad man when it comes to notation knows how important it is to have consistent notation. In this article I shall be using the following notation. I shall be defining the notation for every article so you won't have to keep a seperate book for notation. 

$$ A $$ - a capital letter in this format is used to denote an event

$$ Pr(A) $$ - the probability of an event A

### The Classical Probability

The definition of classical probability says that if a experiment(a simple trial or test) has $$n$$ mutually exclusive (no common) equally likely (same chance of occuring) outcomes and if the event $$A$$ has $$n_A$$ number of outcomes associated with it then the classical probability of the event $$A$$ or $$Pr(A) = \frac{n_A}{A}$$

For an example if the trial is rolling a die and the event A is defined as getting an even number then there are 3 outcomes associated with the event A (2,4,6) and there are 6 total outcomes as there are six sides in a die. Then \$$Pr(A) = \frac{\text{# of outcomes of A}}{\text{# of total outcomes}} = \frac{3}{6} = \frac{1}{2}$$

From the definition of the classical probability it is clear that a probability should be between 0 and 1 as $$ n > = n_A > = 0 $$ for all events. The classical probability model is also called _priori probability model_ This is because the probabilities can be obtained through deductive reasoning and without actually performing the experiment. 
The main drawback of the classical probability method is the fact that all events should be equally likely and mutually exclusive and random.

The counter examples for this is as follows.
* Equally Likely:
	* Suppose two coins are tossed and the event of 2 heads is considered. One can write the outcomes of the experiment as two heads, two tails, one heads or one tails instead of the usual powerset of the outcomes. In this case the probability is equal to $$\frac{1}{3}$$.The issue is evident as the outcomes are not equally likely and hence gives a wrong probability.
* Mutually Exclusive:e
	* Now consider a deck of 52 cards and the event of selecting an ace or a spade from two draws from this card pack. One might say that there 4 aces and 13 spades and therefore the probability is $$\frac{1}{17}$$ However there are aces that are spades as well. And therefore it is seen that mutually inclusive outcomes can not be used for classical probability method
* Random
	* A coin toss with a coin that is biased towards the head

Therefore with these drawbacks we move on to a better model. 

### Frequency Probability

The definition of frequency probability is somewhat hard to pin point but the main gist of it is that if we can perform the same experiment for a $$ n $$ number of times where $$n -> \infty $$ (n is large enough and is approaching infinity) and observe the outcomes for a certain event then we can find the true probability of the event occuring as a fraction. 

The difference from the classical probability method is that the frequency method does not assume equally likely outcomes and simply gives a probability from a set number of trials. Hence this method of frequency probability is called _posteriori probability model_ 

For an example suppose that we throw a die 300 times and record the observations. Then the following table can be recorded for example. 

| Outcome    |  Observed Frequency | Observed relative frequency | Expected relative frequency |
| :-----:    |  :----------------: | :-------------------------: | :-------------------------: |
| 1          |  51                 |  0.170                      | 0.1667                      | 
| 2          |  54                 |  0.180                      | 0.1667                      |
| 3          |  48                 |  0.160                      | 0.1667                      |
| 4          |  51                 |  0.170                      | 0.1667                      |
| 5          |  49                 |  0.163                      | 0.1667                      |
| 6          |  47                 |  0.157                      | 0.1667                      |

This example shows that even though we approximated that the die is fair and therefore equal probabilities should come to each outcome, the real story will always be different. The relative frequency method can be helpful in instances where the classical method can fail but even then this method also suffers with the requirement of selecting a large number of trials to provide an approximation. 

This issue is quite clear in instances where an experiment can not be repeated at will or under controlled test environments. For example what is the probability that the polar ice caps will melt in the year of 2025? 

It is here that we discuss the next method of formulating probabilities. 

### Probabilistic Models

The next method of formulating probability is through probability models. Normally a model might sound like a fancy term but in reality it is actually a relation between a set of inputs and a set of variables. For example $$ v = u + a*t $$ is a model that can give us the velocity of an object after $$t$$ time with the initial velocity of $$ u $$ , an acceleration of $$a$$. Likewise probabilistic models aim to use an input of some event to build a probabilty of that event happening. We will dive deeper into these in the future. For now know there are ways to build a mapping from inputs to probabilities. To illustrate this in an example, suppose it is known that there is 0.4 probability of a fish bun actually having fish in it. Now you have bought a six pack of fish buns for your friends and you want to know the probability that exactly 1 friend gets to eat the fish in the fish bun. This sort of phenomena can be modeled using a Binomial Probability Model as follows. 

Let $$X$$ be the event of finding $$x$$ number of fish buns with fish in them. 
Then the probability of finding 1 fish bun with fish in it can be written as follows.( _This notation and formula might be confusing at first. Bear in mind this is just an example and we will explain these probabilistic models in the future_) \$$Pr(X=1) = {6\choose 1} * (0.4)^1 * (0.6)^5 $$

## Overview of Random Variables and Distribution Functions

_todo fill this_
## Conditional Probability, Independence and Bayes Theorem

_todo fill this_
## Chain rule and Sum rule

_todo fill this_
