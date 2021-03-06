Probability
===========

Probability forms a foundation for statistics. You might already be
familiar with many aspects of probability, however, formalization of the
concepts is new for most. This chapter aims to introduce probability on
familiar terms using processes most people have seen before.

Defining probability {#basicsOfProbability}
--------------------

A "die", the singular of dice, is a cube with six faces numbered 1, 2,
3, 4, 5, and 6. What is the chance of getting 1 when rolling a
die?[\[probOf1\]]{#probOf1 label="probOf1"} If the die is fair, then the
chance of a 1 is as good as the chance of any other number. Since there
are six outcomes, the chance must be 1-in-6 or, equivalently, $1/6$.

What is the chance of getting a 1 or 2 in the next
roll?[\[probOf1Or2\]]{#probOf1Or2 label="probOf1Or2"} 1 and 2 constitute
two of the six equally likely possible outcomes, so the chance of
getting one of these two outcomes must be $2/6 = 1/3$.

What is the chance of getting either 1, 2, 3, 4, 5, or 6 on the next
roll?[\[probOf123456\]]{#probOf123456 label="probOf123456"} 100%. The
outcome must be one of these numbers.

What is the chance of not rolling a 2?[\[probNot2\]]{#probNot2
label="probNot2"} Since the chance of rolling a 2 is $1/6$ or
$16.\bar{6}\%$, the chance of not rolling a 2 must be
$100\% - 16.\bar{6}\%=83.\bar{3}\%$ or $5/6$.

Alternatively, we could have noticed that not rolling a 2 is the same as
getting a 1, 3, 4, 5, or 6, which makes up five of the six equally
likely outcomes and has probability $5/6$.

Consider rolling two dice. If $1/6^{th}$ of the time the first die is a
1 and $1/6^{th}$ of those times the second die is a 1, what is the
chance of getting two 1s?[\[probOf2Ones\]]{#probOf2Ones
label="probOf2Ones"} If $16.\bar{6}$% of the time the first die is a 1
and $1/6^{th}$ of *those* times the second die is also a 1, then the
chance that both dice are 1 is $(1/6)\times (1/6)$ or $1/36$.

### Probability

We use probability to build tools to describe and understand apparent
randomness. We often frame probability in terms of a giving rise to an .

  ------------- --------------- ---------------------
  Roll a die    $\rightarrow$   1, 2, 3, 4, 5, or 6
  Flip a coin   $\rightarrow$   H or T
  ------------- --------------- ---------------------

Rolling a die or flipping a coin is a seemingly random process and each
gives rise to an outcome.

The of an outcome is the proportion of times the outcome would occur if
we observed the random process an infinite number of times.

Probability is defined as a proportion, and it always takes values
between 0 and 1 (inclusively). It may also be displayed as a percentage
between 0% and 100%.

Probability can be illustrated by rolling a die many times. Let
$\hat{p}_n$ be the proportion of outcomes that are 1 after the first $n$
rolls. As the number of rolls increases, $\hat{p}_n$ will converge to
the probability of rolling a 1, $p = 1/6$.
Figure [1.1](#dieProp){reference-type="ref" reference="dieProp"} shows
this convergence for 100,000 die rolls. The tendency of $\hat{p}_n$ to
stabilize around $p$ is described by the .

![The fraction of die rolls that are 1 at each stage in a simulation.
The proportion tends to get closer to the probability
$1/6 \approx 0.167$ as the number of rolls
increases.[]{label="dieProp"}](appendix-probability/figures/dieProp/dieProp){#dieProp
width="80%"}

As more observations are collected, the proportion $\hat{p}_n$ of
occurrences with a particular outcome converges to the probability $p$
of that outcome.

Occasionally the proportion will veer off from the probability and
appear to defy the Law of Large Numbers, as $\hat{p}_n$ does many times
in Figure [1.1](#dieProp){reference-type="ref" reference="dieProp"}.
However, these deviations become smaller as the number of rolls
increases.

Above we write $p$ as the probability of rolling a 1. We can also write
this probability as $$\begin{aligned}
P(\text{rolling a 1})\end{aligned}$$ As we become more comfortable with
this notation, we will abbreviate it further. For instance, if it is
clear that the process is "rolling a die", we could abbreviate
$P($rolling a 1$)$ as $P($1$)$.

[\[randomProcessExercise\]]{#randomProcessExercise
label="randomProcessExercise"} Random processes include rolling a die
and flipping a coin. (a) Think of another random process. (b) Describe
all the possible outcomes of that process. For instance, rolling a die
is a random process with potential outcomes 1, 2, \..., 6.[^1]

What we think of as random processes are not necessarily random, but
they may just be too difficult to understand exactly. The fourth example
in the footnote solution to Guided
Practice [\[randomProcessExercise\]](#randomProcessExercise){reference-type="ref"
reference="randomProcessExercise"} suggests a roommate's behavior is a
random process. However, even if a roommate's behavior is not truly
random, modeling her behavior as a random process can still be useful.

It can be helpful to model a process as random even if it is not truly
random.

### Disjoint or mutually exclusive outcomes

Two outcomes are called or if they cannot both happen. For instance, if
we roll a die, the outcomes 1 and 2 are disjoint since they cannot both
occur. On the other hand, the outcomes 1 and "rolling an odd number" are
not disjoint since both occur if the outcome of the roll is a 1. The
terms *disjoint* and *mutually exclusive* are equivalent and
interchangeable.

Calculating the probability of disjoint outcomes is easy. When rolling a
die, the outcomes 1 and 2 are disjoint, and we compute the probability
that one of these outcomes will occur by adding their separate
probabilities: $$\begin{aligned}
P(\text{1 or 2}) = P(\text{1})+P(\text{2}) = 1/6 + 1/6 = 1/3\end{aligned}$$
What about the probability of rolling a 1, 2, 3, 4, 5, or 6? Here again,
all of the outcomes are disjoint so we add the probabilities:
$$\begin{aligned}
&&P(\text{1 or 2 or 3 or 4 or 5 or 6}) \\
    &&\quad= P(\text{1})+P(\text{2})+P(\text{3})+P(\text{4})+P(\text{5})+P(\text{6}) \\
    &&\quad= 1/6 + 1/6 + 1/6 + 1/6 + 1/6 + 1/6 = 1.\end{aligned}$$ The
guarantees the accuracy of this approach when the outcomes are disjoint.

If $A_1$ and $A_2$ represent two disjoint outcomes, then the probability
that one of them occurs is given by $$\begin{aligned}
P(A_1\text{ or } A_2) = P(A_1) + P(A_2)\end{aligned}$$ If there are many
disjoint outcomes $A_1$, \..., $A_k$, then the probability that one of
these outcomes will occur is $$\begin{aligned}
P(A_1) + P(A_2) + \cdots + P(A_k)\end{aligned}$$

We are interested in the probability of rolling a 1, 4, or 5. (a)
Explain why the outcomes 1, 4, and 5 are disjoint. (b) Apply the
Addition Rule for disjoint outcomes to determine $P($1 or 4 or 5$)$.[^2]

In the data set in
Chapter [\[introductionToData\]](#introductionToData){reference-type="ref"
reference="introductionToData"}, the variable described whether no
number (labeled none), only one or more small numbers (small), or
whether at least one big number appeared in an email (big). Of the 3,921
emails, 549 had no numbers, 2,827 had only one or more small numbers,
and 545 had at least one big number. (a) Are the outcomes none, small,
and big disjoint? (b) Determine the proportion of emails with value
small and big separately. (c) Use the Addition Rule for disjoint
outcomes to compute the probability a randomly selected email from the
data set has a number in it, small or big.[^3]

Statisticians rarely work with individual outcomes and instead consider
or of outcomes. Let $A$ represent the event where a die roll results in
1 or 2 and $B$ represent the event that the die roll is a 4 or a 6. We
write $A$ as the set of outcomes $\{$1, 2$\}$ and $B=\{$4, 6$\}$. These
sets are commonly called . Because $A$ and $B$ have no elements in
common, they are disjoint events. $A$ and $B$ are represented in
Figure [1.2](#disjointSets){reference-type="ref"
reference="disjointSets"}.

![Three events, $A$, $B$, and $D$, consist of outcomes from rolling a
die. $A$ and $B$ are disjoint since they do not have any outcomes in
common.[]{label="disjointSets"}](appendix-probability/figures/disjointSets/disjointSets){#disjointSets
height="0.7in"}

The Addition Rule applies to both disjoint outcomes and disjoint events.
The probability that one of the disjoint events $A$ or $B$ occurs is the
sum of the separate probabilities: $$\begin{aligned}
P(A\text{ or }B) = P(A) + P(B) = 1/3 + 1/3 = 2/3\end{aligned}$$

\(a\) Verify the probability of event $A$, $P(A)$, is $1/3$ using the
Addition Rule. (b) Do the same for event $B$.[^4]

[\[exerExaminingDisjointSetsABD\]]{#exerExaminingDisjointSetsABD
label="exerExaminingDisjointSetsABD"} (a) Using
Figure [1.2](#disjointSets){reference-type="ref"
reference="disjointSets"} as a reference, what outcomes are represented
by event $D$? (b) Are events $B$ and $D$ disjoint? (c) Are events $A$
and $D$ disjoint?[^5]

In Guided
Practice [\[exerExaminingDisjointSetsABD\]](#exerExaminingDisjointSetsABD){reference-type="ref"
reference="exerExaminingDisjointSetsABD"}, you confirmed $B$ and $D$
from Figure [1.2](#disjointSets){reference-type="ref"
reference="disjointSets"} are disjoint. Compute the probability that
either event $B$ or event $D$ occurs.[^6]

### Probabilities when events are not disjoint

Let's consider calculations for two events that are not disjoint in the
context of a , represented in
Table [\[deckOfCards\]](#deckOfCards){reference-type="ref"
reference="deckOfCards"}. If you are unfamiliar with the cards in a
regular deck, please see the footnote.[^7]

  ----------------- ----------------- ----------------- ----------------- ----------------- ----------------- ----------------- ----------------- ------------------ ----------------- ----------------- ----------------- -----------------
  2$\clubsuit$      3$\clubsuit$      4$\clubsuit$      5$\clubsuit$      6$\clubsuit$      7$\clubsuit$      8$\clubsuit$      9$\clubsuit$      10$\clubsuit$      J$\clubsuit$      Q$\clubsuit$      K$\clubsuit$      A$\clubsuit$
  2$\diamondsuit$   3$\diamondsuit$   4$\diamondsuit$   5$\diamondsuit$   6$\diamondsuit$   7$\diamondsuit$   8$\diamondsuit$   9$\diamondsuit$   10$\diamondsuit$   J$\diamondsuit$   Q$\diamondsuit$   K$\diamondsuit$   A$\diamondsuit$
  2$\heartsuit$     3$\heartsuit$     4$\heartsuit$     5$\heartsuit$     6$\heartsuit$     7$\heartsuit$     8$\heartsuit$     9$\heartsuit$     10$\heartsuit$     J$\heartsuit$     Q$\heartsuit$     K$\heartsuit$     A$\heartsuit$
  2$\spadesuit$     3$\spadesuit$     4$\spadesuit$     5$\spadesuit$     6$\spadesuit$     7$\spadesuit$     8$\spadesuit$     9$\spadesuit$     10$\spadesuit$     J$\spadesuit$     Q$\spadesuit$     K$\spadesuit$     A$\spadesuit$
  ----------------- ----------------- ----------------- ----------------- ----------------- ----------------- ----------------- ----------------- ------------------ ----------------- ----------------- ----------------- -----------------

  : Representations of the 52 unique cards in a
  deck.[]{label="deckOfCards"}

\(a\) What is the probability that a randomly selected card is a
diamond? (b) What is the probability that a randomly selected card is a
face card?[^8]

are useful when outcomes can be categorized as "in" or "out" for two or
three variables, attributes, or random processes. The Venn diagram in
Figure [1.3](#venn){reference-type="ref" reference="venn"} uses a circle
to represent diamonds and another to represent face cards. If a card is
both a diamond and a face card, it falls into the intersection of the
circles. If it is a diamond but not a face card, it will be in part of
the left circle that is not in the right circle (and so on). The total
number of cards that are diamonds is given by the total number of cards
in the diamonds circle: $10+3=13$. The probabilities are also shown
(e.g. $10/52 = 0.1923$).

![A Venn diagram for diamonds and face
cards.[]{label="venn"}](appendix-probability/figures/venn/venn){#venn
height="1.4in"}

Using the Venn diagram, verify $P($face card$) = 12/52=3/13$.[^9]

Let $A$ represent the event that a randomly selected card is a diamond
and $B$ represent the event that it is a face card. How do we compute
$P(A$ or $B)$? Events $A$ and $B$ are not disjoint -- the cards
$J\diamondsuit$, $Q\diamondsuit$, and $K\diamondsuit$ fall into both
categories -- so we cannot use the Addition Rule for disjoint events.
Instead we use the Venn diagram. We start by adding the probabilities of
the two events: $$\begin{aligned}
P(A) + P(B) = P({\color{redcards}\diamondsuit}) + P(\text{face card}) = 12/52 + 13/52
\label{overCountFaceDiamond}\end{aligned}$$ However, the three cards
that are in both events were counted twice, once in each probability. We
must correct this double counting: $$\begin{aligned}
P(A\text{ or } B) &=&P(\text{face card or }{\color{redcards}\diamondsuit})  \notag \\
 &=& P(\text{face card}) + P({\color{redcards}\diamondsuit}) - P(\text{face card and }{\color{redcards}\diamondsuit}) \label{diamondFace} \\
 &=& 12/52 + 13/52 - 3/52 \notag \\
 &=& 22/52 = 11/26 \notag\end{aligned}$$
Equation ([\[diamondFace\]](#diamondFace){reference-type="ref"
reference="diamondFace"}) is an example of the .

If $A$ and $B$ are any two events, disjoint or not, then the probability
that at least one of them will occur is $$\begin{aligned}
P(A\text{ or }B) = P(A) + P(B) - P(A\text{ and }B)
\label{generalAdditionRule}\end{aligned}$$ where $P(A$ and $B)$ is the
probability that both events occur.

When we write "or" in statistics, we mean "and/or" unless we explicitly
state otherwise. Thus, $A$ or $B$ occurs means $A$, $B$, or both $A$ and
$B$ occur.

\(a\) If $A$ and $B$ are disjoint, describe why this implies $P(A$ and
$B) = 0$. (b) Using part (a), verify that the General Addition Rule
simplifies to the simpler Addition Rule for disjoint events if $A$ and
$B$ are disjoint.[^10]

[\[emailSpamNumberVennExer\]]{#emailSpamNumberVennExer
label="emailSpamNumberVennExer"} In the data set with 3,921 emails, 367
were spam, 2,827 contained some small numbers but no big numbers, and
168 had both characteristics. Create a Venn diagram for this setup.[^11]

\(a\) Use your Venn diagram from Guided
Practice [\[emailSpamNumberVennExer\]](#emailSpamNumberVennExer){reference-type="ref"
reference="emailSpamNumberVennExer"} to determine the probability a
randomly drawn email from the data set is spam and had small numbers
(but not big numbers). (b) What is the probability that the email had
either of these attributes?[^12]

### Probability distributions

A is a table of all disjoint outcomes and their associated
probabilities. Table [\[diceProb\]](#diceProb){reference-type="ref"
reference="diceProb"} shows the probability distribution for the sum of
two dice.

  ------------- ---------------- ---------------- ---------------- ---------------- ---------------- ---------------- ---------------- ---------------- ---------------- ---------------- ----------------
                                                                                                                                                                                          
  Dice sum             2                3                4                5                6                7                8                9                10               11               12
  Probability    $\frac{1}{36}$   $\frac{2}{36}$   $\frac{3}{36}$   $\frac{4}{36}$   $\frac{5}{36}$   $\frac{6}{36}$   $\frac{5}{36}$   $\frac{4}{36}$   $\frac{3}{36}$   $\frac{2}{36}$   $\frac{1}{36}$
  ------------- ---------------- ---------------- ---------------- ---------------- ---------------- ---------------- ---------------- ---------------- ---------------- ---------------- ----------------

  : Probability distribution for the sum of two
  dice.[]{label="diceProb"}

A probability distribution is a list of the possible outcomes with
corresponding probabilities that satisfies three rules:

1.  The outcomes listed must be disjoint.

2.  Each probability must be between 0 and 1.

3.  The probabilities must total 1.

[\[usHouseholdIncomeDistsExercise\]]{#usHouseholdIncomeDistsExercise
label="usHouseholdIncomeDistsExercise"}
Table [\[usHouseholdIncomeDists\]](#usHouseholdIncomeDists){reference-type="ref"
reference="usHouseholdIncomeDists"} suggests three distributions for
household income in the United States. Only one is correct. Which one
must it be? What is wrong with the other two?[^13]

    Income range (\$1000s)   0-25   25-50   50-100   100+
  ------------------------ ------ ------- -------- ------
                     \(a\)   0.18    0.39     0.33   0.16
                     \(b\)   0.38   -0.27     0.52   0.37
                     \(c\)   0.28    0.27     0.29   0.16

  : Proposed distributions of US household incomes (Guided
  Practice [\[usHouseholdIncomeDistsExercise\]](#usHouseholdIncomeDistsExercise){reference-type="ref"
  reference="usHouseholdIncomeDistsExercise"}).[]{label="usHouseholdIncomeDists"}

Chapter [\[introductionToData\]](#introductionToData){reference-type="ref"
reference="introductionToData"} emphasized the importance of plotting
data to provide quick summaries. Probability distributions can also be
summarized in a bar plot. For instance, the distribution of US household
incomes is shown in
Figure [1.4](#usHouseholdIncomeDistBar){reference-type="ref"
reference="usHouseholdIncomeDistBar"} as a bar plot.[^14] The
probability distribution for the sum of two dice is shown in
Table [\[diceProb\]](#diceProb){reference-type="ref"
reference="diceProb"} and plotted in
Figure [1.5](#diceSumDist){reference-type="ref"
reference="diceSumDist"}.

![The probability distribution of US household
income.[]{label="usHouseholdIncomeDistBar"}](appendix-probability/figures/usHouseholdIncomeDistBar/usHouseholdIncomeDistBar){#usHouseholdIncomeDistBar
width="68%"}

![The probability distribution of the sum of two
dice.[]{label="diceSumDist"}](appendix-probability/figures/diceSumDist/diceSumDist){#diceSumDist
width="73%"}

In these bar plots, the bar heights represent the probabilities of
outcomes. If the outcomes are numerical and discrete, it is usually
(visually) convenient to make a bar plot that resembles a histogram, as
in the case of the sum of two dice. Another example of plotting the bars
at their respective locations is shown in
Figure [1.11](#bookCostDist){reference-type="ref"
reference="bookCostDist"} on page .

### Complement of an event

Rolling a die produces a value in the set $\{$1, 2, 3, 4, 5, 6$\}$. This
set of all possible outcomes is called the ($S$) for rolling a die. We
often use the sample space to examine the scenario where an event does
not occur.

Let $D=\{$2, 3$\}$ represent the event that the outcome of a die roll is
2 or 3. Then the of $D$ represents all outcomes in our sample space that
are not in $D$, which is denoted by $D^c = \{$1, 4, 5, 6$\}$. That is,
$D^c$ is the set of all possible outcomes not already included in $D$.
Figure [1.6](#complementOfD){reference-type="ref"
reference="complementOfD"} shows the relationship between $D$, $D^c$,
and the sample space $S$.

![Event $D=\{$2, 3$\}$ and its complement, $D^c = \{$1, 4, 5, 6$\}$.
$S$ represents the sample space, which is the set of all possible
events.[]{label="complementOfD"}](appendix-probability/figures/complementOfD/complementOfD){#complementOfD
width="40%"}

\(a\) Compute $P(D^c) = P($rolling a 1, 4, 5, or 6$)$. (b) What is
$P(D) + P(D^c)$?[^15]

Events $A=\{$1, 2$\}$ and $B=\{$4, 6$\}$ are shown in
Figure [1.2](#disjointSets){reference-type="ref"
reference="disjointSets"} on page . (a) Write out what $A^c$ and $B^c$
represent. (b) Compute $P(A^c)$ and $P(B^c)$. (c) Compute $P(A)+P(A^c)$
and $P(B)+P(B^c)$.[^16]

A complement of an event $A$ is constructed to have two very important
properties: (i) every possible outcome not in $A$ is in $A^c$, and (ii)
$A$ and $A^c$ are disjoint. Property (i) implies $$\begin{aligned}
P(A\text{ or }A^c) = 1
\label{complementSumTo1}\end{aligned}$$ That is, if the outcome is not
in $A$, it must be represented in $A^c$. We use the Addition Rule for
disjoint events to apply Property (ii): $$\begin{aligned}
P(A\text{ or }A^c) = P(A) + P(A^c)
\label{complementDisjointEquation}\end{aligned}$$ Combining
Equations ([\[complementSumTo1\]](#complementSumTo1){reference-type="ref"
reference="complementSumTo1"})
and ([\[complementDisjointEquation\]](#complementDisjointEquation){reference-type="ref"
reference="complementDisjointEquation"}) yields a very useful
relationship between the probability of an event and its complement.

The complement of event $A$ is denoted $A^c$, and $A^c$ represents all
outcomes not in $A$. $A$ and $A^c$ are mathematically related:
$$\begin{aligned}
\label{complement}
P(A) + P(A^c) = 1, \quad\text{i.e.}\quad P(A) = 1-P(A^c)\end{aligned}$$

In simple examples, computing $A$ or $A^c$ is feasible in a few steps.
However, using the complement can save a lot of time as problems grow in
complexity.

Let $A$ represent the event where we roll two dice and their total is
less than 12. (a) What does the event $A^c$ represent? (b) Determine
$P(A^c)$ from Table [\[diceProb\]](#diceProb){reference-type="ref"
reference="diceProb"} on page . (c) Determine $P(A)$.[^17]

Consider again the probabilities from
Table [\[diceProb\]](#diceProb){reference-type="ref"
reference="diceProb"} and rolling two dice. Find the following
probabilities: (a) The sum of the dice is *not* 6. (b) The sum is at
least 4, i.e. $\{$4, 5, \..., 12$\}$. (c) The sum is no more than 10.
That is, determine the probability of the event $D=\{$2, 3, \...,
10$\}$.[^18]

### Independence {#probabilityIndependence}

Just as variables and observations can be independent, random processes
can be independent, too. Two processes are if knowing the outcome of one
provides no useful information about the outcome of the other. For
instance, flipping a coin and rolling a die are two independent
processes -- knowing the coin was heads does not help determine the
outcome of a die roll. On the other hand, stock prices usually move up
or down together, so they are not independent.

Example [\[probOf2Ones\]](#probOf2Ones){reference-type="ref"
reference="probOf2Ones"} provides a basic example of two independent
processes: rolling two dice. We want to determine the probability that
both will be 1. Suppose one of the dice is red and the other white. If
the outcome of the red die is a 1, it provides no information about the
outcome of the white die. We first encountered this same question in
Example [\[probOf2Ones\]](#probOf2Ones){reference-type="ref"
reference="probOf2Ones"} (page ), where we calculated the probability
using the following reasoning: $1/6^{th}$ of the time the red die is a
1, and $1/6^{th}$ of *those* times the white die will also be 1. This is
illustrated in Figure [1.7](#indepForRollingTwo1s){reference-type="ref"
reference="indepForRollingTwo1s"}. Because the rolls are independent,
the probabilities of the corresponding outcomes can be multiplied to get
the final answer: $(1/6)\times(1/6)=1/36$. This can be generalized to
many independent processes.

![$1/6^{th}$ of the time, the first roll is a 1. Then $1/6^{th}$ of
*those* times, the second roll will also be a
1.[]{label="indepForRollingTwo1s"}](appendix-probability/figures/indepForRollingTwo1s/indepForRollingTwo1s){#indepForRollingTwo1s
width="65%"}

What if there was also a blue die independent of the other two? What is
the probability of rolling the three dice and getting all
1s?[\[threeDice\]]{#threeDice label="threeDice"} The same logic applies
from Example [\[probOf2Ones\]](#probOf2Ones){reference-type="ref"
reference="probOf2Ones"}. If $1/36^{th}$ of the time the white and red
dice are both 1, then $1/6^{th}$ of *those* times the blue die will also
be 1, so multiply: $$\begin{aligned}
P(white=\text{\small1 and } red=\text{\small1 and } blue=\text{\small1})
    &= P(white=\text{\small1})\times P(red=\text{\small1})\times P(blue=\text{\small1}) \\
    &= (1/6)\times (1/6)\times (1/6)
    = 1/216\end{aligned}$$

Examples [\[probOf2Ones\]](#probOf2Ones){reference-type="ref"
reference="probOf2Ones"}
and [\[threeDice\]](#threeDice){reference-type="ref"
reference="threeDice"} illustrate what is called the Multiplication Rule
for independent processes.

If $A$ and $B$ represent events from two different and independent
processes, then the probability that both $A$ and $B$ occur can be
calculated as the product of their separate probabilities:
$$\begin{aligned}
\label{eqForIndependentEvents}
P(A \text{ and }B) = P(A) \times  P(B)\end{aligned}$$ Similarly, if
there are $k$ events $A_1$, \..., $A_k$ from $k$ independent processes,
then the probability they all occur is $$\begin{aligned}
P(A_1) \times  P(A_2)\times  \cdots \times  P(A_k)\end{aligned}$$

[\[ex2Handedness\]]{#ex2Handedness label="ex2Handedness"} About 9% of
people are left-handed. Suppose 2 people are selected at random from the
U.S. population. Because the sample size of 2 is very small relative to
the population, it is reasonable to assume these two people are
independent. (a) What is the probability that both are left-handed?
(b) What is the probability that both are right-handed?[^19]

[\[ex5Handedness\]]{#ex5Handedness label="ex5Handedness"} Suppose 5
people are selected at random.[^20]

1.  What is the probability that all are right-handed?

2.  What is the probability that all are left-handed?

3.  What is the probability that not all of the people are right-handed?

Suppose the variables and are independent, i.e. knowing someone's
provides no useful information about their and vice-versa. Then we can
compute whether a randomly selected person is right-handed and
female[^21] using the Multiplication Rule: $$\begin{aligned}
P(\text{right-handed and female}) &=& P(\text{right-handed}) \times  P(\text{female}) \\
&=& 0.91 \times  0.50 = 0.455\end{aligned}$$

Three people are selected at random.[^22]

1.  What is the probability that the first person is male and
    right-handed?

2.  What is the probability that the first two people are male and
    right-handed?.

3.  What is the probability that the third person is female and
    left-handed?

4.  What is the probability that the first two people are male and
    right-handed and the third person is female and left-handed?

Sometimes we wonder if one outcome provides useful information about
another outcome. The question we are asking is, are the occurrences of
the two events independent? We say that two events $A$ and $B$ are
independent if they satisfy
Equation [\[eqForIndependentEvents\]](#eqForIndependentEvents){reference-type="eqref"
reference="eqForIndependentEvents"}.

If we shuffle up a deck of cards and draw one, is the event that the
card is a heart independent of the event that the card is an ace? The
probability the card is a heart is $1/4$ and the probability that it is
an ace is $1/13$. The probability the card is the ace of hearts is
$1/52$. We check whether
Equation [\[eqForIndependentEvents\]](#eqForIndependentEvents){reference-type="ref"
reference="eqForIndependentEvents"} is satisfied: $$\begin{aligned}
P({\color{redcards}\heartsuit})\times P(\text{ace}) = \frac{1}{4}\times \frac{1}{13} = \frac{1}{52} 
                    = P({\color{redcards}\heartsuit}\text{ and ace})\end{aligned}$$
Because the equation holds, the event that the card is a heart and the
event that the card is an ace are independent events.

Conditional probability {#conditionalProbabilitySection}
-----------------------

Are students more likely to use marijuana when their parents used drugs?
The data set contains a sample of 445 cases with two variables, and ,
and is summarized in
Table [\[contTableOfParStDrugUse\]](#contTableOfParStDrugUse){reference-type="ref"
reference="contTableOfParStDrugUse"}.[^23] The variable is either uses
or not, where a student is labeled as if she has recently used
marijuana. The variable takes the value used if at least one of the
parents used drugs, including alcohol.

  --------- ------- ------ ----- ------- -- --
                                            
                      used   not   Total    
            uses       125    94     219    
  \[0pt\]   not         85   141     226    
            Total      210   235     445    
  --------- ------- ------ ----- ------- -- --

  : Contingency table summarizing the data
  set.[]{label="contTableOfParStDrugUse"}

![A Venn diagram using boxes for the data
set.[]{label="drugUseVenn"}](appendix-probability/figures/drugUseVenn/drugUseVenn){#drugUseVenn
width="65%"}

If at least one parent used drugs, what is the chance their child ()
uses? We will estimate this probability using the data. Of the 210 cases
in this data set where = used, 125 represent cases where = uses:
$$\begin{aligned}
P(\text{\var{student} = uses given \var{parents} = used}) = \frac{125}{210} = 0.60\end{aligned}$$

A student is randomly selected from the study and she does not use
drugs. What is the probability that at least one of her parents
used?[\[drugUseProbOfParentsGivenStudents\]]{#drugUseProbOfParentsGivenStudents
label="drugUseProbOfParentsGivenStudents"} If the student does not use
drugs, then she is one of the 226 students in the second row. Of these
226 students, 85 had at least one parent who used drugs:
$$\begin{aligned}
P(\text{\var{parents} = used given \var{student} = not}) = \frac{85}{226} = 0.376\end{aligned}$$

### Marginal and joint probabilities {#marginalAndJointProbabilities}

Table [\[drugUseProbTable\]](#drugUseProbTable){reference-type="ref"
reference="drugUseProbTable"} includes row and column totals for each
variable separately in the data set. These totals represent for the
sample, which are the probabilities based on a single variable without
conditioning on any other variables. For instance, a probability based
solely on the variable is a marginal probability: $$\begin{aligned}
P(\text{\var{student} = uses}) = \frac{219}{445} = 0.492\end{aligned}$$
A probability of outcomes for two or more variables or processes is
called a : $$\begin{aligned}
P(\text{\var{student} = uses and \var{parents} = not}) = \frac{94}{445} = 0.21\end{aligned}$$
It is common to substitute a comma for "and" in a joint probability,
although either is acceptable.

             : used   : not   Total
  -------- -------- ------- -------
  : uses       0.28    0.21    0.49
  : not        0.19    0.32    0.51
  Total        0.47    0.53    1.00

  : Probability table summarizing parental and student drug
  use.[]{label="drugUseProbTable"}

If a probability is based on a single variable, it is a *marginal
probability*. The probability of outcomes for two or more variables or
processes is called a *joint probability*.

We use to summarize joint probabilities for the sample. These
proportions are computed by dividing each count in
Table [\[contTableOfParStDrugUse\]](#contTableOfParStDrugUse){reference-type="ref"
reference="contTableOfParStDrugUse"} by 445 to obtain the proportions in
Table [\[drugUseProbTable\]](#drugUseProbTable){reference-type="ref"
reference="drugUseProbTable"}. The joint probability distribution of the
and variables is shown in
Table [\[drugUseDistribution\]](#drugUseDistribution){reference-type="ref"
reference="drugUseDistribution"}.

  Joint outcome     Probability
  ---------------- -------------
  = used, = uses       0.28
  = used, = not        0.19
  = not, = uses        0.21
  = not, = not         0.32
  Total                1.00

  : A joint probability distribution for the data
  set.[]{label="drugUseDistribution"}

Verify
Table [\[drugUseDistribution\]](#drugUseDistribution){reference-type="ref"
reference="drugUseDistribution"} represents a probability distribution:
events are disjoint, all probabilities are non-negative, and the
probabilities sum to 1.[^24]

We can compute marginal probabilities using joint probabilities in
simple cases. For example, the probability a random student from the
study uses drugs is found by summing the outcomes from
Table [\[drugUseDistribution\]](#drugUseDistribution){reference-type="ref"
reference="drugUseDistribution"} where = uses: $$\begin{aligned}
&&P(\text{\underline{\color{black}\var{student} = uses}}) \\
&& \quad =  P(\text{\var{parents} = used, \underline{\color{black}\var{student} = uses}}) + \\
&& \quad \quad \quad \quad P(\text{\var{parents} = not, \underline{\color{black}\var{student} = uses}}) \\
&& \quad = 0.28 + 0.21 = 0.49\end{aligned}$$

### Defining conditional probability

There is some connection between drug use of parents and of the student:
drug use of one is associated with drug use of the other.[^25] In this
section, we discuss how to use information about associations between
two variables to improve probability estimation.

The probability that a random student from the study uses drugs is 0.49.
Could we update this probability if we knew that this student's parents
used drugs? Absolutely. To do so, we limit our view to only those 210
cases where parents used drugs and look at the fraction where the
student uses drugs: $$\begin{aligned}
P(\text{\var{student} = uses given \var{parents} = used}) = \frac{125}{210} = 0.60\end{aligned}$$
We call this a because we computed the probability under a condition: =
used. There are two parts to a conditional probability, and the . It is
useful to think of the condition as information we know to be true, and
this information usually can be described as a known outcome or event.

We separate the text inside our probability notation into the outcome of
interest and the condition: $$\begin{aligned}
&& P(\text{\var{student} = uses given \var{parents} = used}) \notag \\
&& = P(\text{\var{student} = uses } | \text{ \var{parents} = used}) = \frac{125}{210} = 0.60
\label{probStudentUsedIfParentsUsedInFormalNotation}\end{aligned}$$ The
vertical bar "$|$" is read as *given*.

In
Equation ([\[probStudentUsedIfParentsUsedInFormalNotation\]](#probStudentUsedIfParentsUsedInFormalNotation){reference-type="ref"
reference="probStudentUsedIfParentsUsedInFormalNotation"}), we computed
the probability a student uses based on the condition that at least one
parent used as a fraction: $$\begin{aligned}
&& P(\text{\var{student} = uses } | \text{ \var{parents} = used}) \notag \\
&&\quad = \frac{\text{\# times \var{student} = uses and \var{parents} = used}}{\text{\# times \var{parents} = used}} \label{ratioOfBothToRatioOfConditionalForParentsAndStudent} \\
&&\quad = \frac{125}{210} = 0.60 \notag\end{aligned}$$ We considered
only those cases that met the condition, = used, and then we computed
the ratio of those cases that satisfied our outcome of interest, the
student uses.

Counts are not always available for data, and instead only marginal and
joint probabilities may be provided. For example, disease rates are
commonly listed in percentages rather than in a count format. We would
like to be able to compute conditional probabilities even when no counts
are available, and we use
Equation ([\[ratioOfBothToRatioOfConditionalForParentsAndStudent\]](#ratioOfBothToRatioOfConditionalForParentsAndStudent){reference-type="ref"
reference="ratioOfBothToRatioOfConditionalForParentsAndStudent"}) as an
example demonstrating this technique.

We considered only those cases that satisfied the condition, = used. Of
these cases, the conditional probability was the fraction who
represented the outcome of interest, = uses. Suppose we were provided
only the information in
Table [\[drugUseProbTable\]](#drugUseProbTable){reference-type="ref+page"
reference="drugUseProbTable"}, i.e. only probability data. Then if we
took a sample of 1000 people, we would anticipate about 47% or
$0.47\times 1000 = 470$ would meet our information criterion. Similarly,
we would expect about 28% or $0.28\times 1000 = 280$ to meet both the
information criterion and represent our outcome of interest. Thus, the
conditional probability could be computed: $$\begin{aligned}
P(\text{\var{student} = uses } | \text{ \var{parents} = used})
    &= \frac{\text{\# (\var{student} = uses and \var{parents} = used)}}{\text{\# (\var{parents} = used)}} \notag \\
    &= \frac{280}{470} = \frac{0.28}{0.47} = 0.60
\label{stUserPUsedHypSampSize}\end{aligned}$$ In
Equation ([\[stUserPUsedHypSampSize\]](#stUserPUsedHypSampSize){reference-type="ref"
reference="stUserPUsedHypSampSize"}), we examine exactly the fraction of
two probabilities, 0.28 and 0.47, which we can write as
$$\begin{aligned}
P(\var{student} = uses\ \text{and}\ \var{parents} = used)
    \quad\text{and}\quad
    P(\var{parents} = used).\end{aligned}$$ The fraction of these
probabilities represents our general formula for conditional
probability.

The conditional probability of the outcome of interest $A$ given
condition $B$ is computed as the following: $$\begin{aligned}
P(A | B) = \frac{P(A\text{ and }B)}{P(B)}
\label{condProbEq}\end{aligned}$$

[\[drugUseProbOfParentsEqualNotGivenStudents\]]{#drugUseProbOfParentsEqualNotGivenStudents
label="drugUseProbOfParentsEqualNotGivenStudents"} (a) Write out the
following statement in conditional probability notation: "*The
probability a random case has = not if it is known that = not*". Notice
that the condition is now based on the student, not the parent.
(b) Determine the probability from part (a).
Table [\[drugUseProbTable\]](#drugUseProbTable){reference-type="ref+page"
reference="drugUseProbTable"} may be helpful.[^26]

[\[whyCondProbSumTo1\]]{#whyCondProbSumTo1 label="whyCondProbSumTo1"}
(a) Determine the probability that one of the parents had used drugs if
it is known the student does not use drugs. (b) Using the answers from
part (a) and Guided
Practice [\[drugUseProbOfParentsEqualNotGivenStudents\]](#drugUseProbOfParentsEqualNotGivenStudents){reference-type="ref"
reference="drugUseProbOfParentsEqualNotGivenStudents"}(b), compute
$$\begin{aligned}
P(\text{\var{parents} = used}|\text{\var{student} = not})
    + P(\text{\var{parents} = not}|\text{\var{student} = not})\end{aligned}$$
(c) Provide an intuitive argument to explain why the sum in (b) is
1.[^27]

The data indicate that drug use of parents and children are associated.
Does this mean the drug use of parents causes the drug use of the
students?[^28]

### Smallpox in Boston, 1721

The data set provides a sample of 6,224 individuals from the year 1721
who were exposed to smallpox in Boston.[^29] Doctors at the time
believed that inoculation, which involves exposing a person to the
disease in a controlled form, could reduce the likelihood of death.

Each case represents one person with two variables: and . The variable
takes two levels: yes or no, indicating whether the person was
inoculated or not. The variable has outcomes lived or died. These data
are summarized in
Tables [\[smallpoxContingencyTable\]](#smallpoxContingencyTable){reference-type="ref"
reference="smallpoxContingencyTable"}
and [\[smallpoxProbabilityTable\]](#smallpoxProbabilityTable){reference-type="ref"
reference="smallpoxProbabilityTable"}.

  --------- ------- ----- ------ -------
                                 
                      yes     no   Total
            lived     238   5136    5374
  \[0pt\]   died        6    844     850
            Total     244   5980    6224
  --------- ------- ----- ------ -------

  : Contingency table for the data
  set.[]{label="smallpoxContingencyTable"}

  --------- ------- -------- -------- --------
                                      
                         yes       no    Total
            lived     0.0382   0.8252   0.8634
  \[0pt\]   died      0.0010   0.1356   0.1366
            Total     0.0392   0.9608   1.0000
  --------- ------- -------- -------- --------

  : Table proportions for the data, computed by dividing each count by
  the table total, 6224.[]{label="smallpoxProbabilityTable"}

[\[probDiedIfNotInoculated\]]{#probDiedIfNotInoculated
label="probDiedIfNotInoculated"} Write out, in formal notation, the
probability a randomly selected person who was not inoculated died from
smallpox, and find this probability.[^30]

Determine the probability that an inoculated person died from smallpox.
How does this result compare with the result of Guided
Practice [\[probDiedIfNotInoculated\]](#probDiedIfNotInoculated){reference-type="ref"
reference="probDiedIfNotInoculated"}?[^31]

[\[SmallpoxInoculationObsExpExercise\]]{#SmallpoxInoculationObsExpExercise
label="SmallpoxInoculationObsExpExercise"} The people of Boston
self-selected whether or not to be inoculated. (a) Is this study
observational or was this an experiment? (b) Can we infer any causal
connection using these data? (c) What are some potential confounding
variables that might influence whether someone lived or died and also
affect whether that person was inoculated?[^32]

### General multiplication rule

Section [1.1.6](#probabilityIndependence){reference-type="ref"
reference="probabilityIndependence"} introduced the Multiplication Rule
for independent processes. Here we provide the for events that might not
be independent.

If $A$ and $B$ represent two outcomes or events, then $$\begin{aligned}
P(A\text{ and }B) = P(A | B)\times P(B)\end{aligned}$$

It is useful to think of $A$ as the outcome of interest and $B$ as the
condition.

This General Multiplication Rule is simply a rearrangement of the
definition for conditional probability in
Equation ([\[condProbEq\]](#condProbEq){reference-type="ref"
reference="condProbEq"}) on page .

Consider the data set. Suppose we are given only two pieces of
information: 96.08% of residents were not inoculated, and 85.88% of the
residents who were not inoculated ended up surviving. How could we
compute the probability that a resident was not inoculated and lived? We
will compute our answer using the General Multiplication Rule and then
verify it using
Table [\[smallpoxProbabilityTable\]](#smallpoxProbabilityTable){reference-type="ref"
reference="smallpoxProbabilityTable"}. We want to determine
$$\begin{aligned}
P(\text{\var{result} = lived and \var{inoculated} = no})\end{aligned}$$
and we are given that $$\begin{aligned}
P(\text{\var{result} = lived }|\text{ \var{inoculated} = no})=0.8588 \\
P(\text{\var{inoculated} = no})=0.9608\end{aligned}$$ Among the 96.08%
of people who were not inoculated, 85.88% survived: $$\begin{aligned}
P(\text{\var{result} = lived and \var{inoculated} = no}) = 0.8588\times 0.9608 = 0.8251\end{aligned}$$
This is equivalent to the General Multiplication Rule. We can confirm
this probability in
Table [\[smallpoxProbabilityTable\]](#smallpoxProbabilityTable){reference-type="ref"
reference="smallpoxProbabilityTable"} at the intersection of no and
lived (with a small rounding error).

Use $P($ = yes$) = 0.0392$ and $P($ = lived $|$ = yes$) = 0.9754$ to
determine the probability that a person was both inoculated and
lived.[^33]

If 97.45% of the people who were inoculated lived, what proportion of
inoculated people must have died?[^34]

Let $A_1$, \..., $A_k$ represent all the disjoint outcomes for a
variable or process. Then if $B$ is an event, possibly for another
variable or process, we have: $$\begin{aligned}
P(A_1|B)+\cdots+P(A_k|B) = 1\end{aligned}$$

The rule for complements also holds when an event and its complement are
conditioned on the same information: $$\begin{aligned}
P(A | B) = 1 - P(A^c | B)\end{aligned}$$

Based on the probabilities computed above, does it appear that
inoculation is effective at reducing the risk of death from
smallpox?[^35]

### Independence considerations in conditional probability

If two processes are independent, then knowing the outcome of one should
provide no information about the other. We can show this is
mathematically true using conditional probabilities.

[\[condProbOfRollingA1AfterOne1\]]{#condProbOfRollingA1AfterOne1
label="condProbOfRollingA1AfterOne1"} Let $X$ and $Y$ represent the
outcomes of rolling two dice. (a) What is the probability that the first
die, $X$, is 1? (b) What is the probability that both $X$ and $Y$ are 1?
(c) Use the formula for conditional probability to compute $P(Y =$ 1
$| X =$ 1$)$. (d) What is $P(Y=1)$? Is this different from the answer
from part (c)? Explain.[^36]

We can show in Guided
Practice [\[condProbOfRollingA1AfterOne1\]](#condProbOfRollingA1AfterOne1){reference-type="ref"
reference="condProbOfRollingA1AfterOne1"}(c) that the conditioning
information has no influence by using the Multiplication Rule for
independence processes: $$\begin{aligned}
P(Y=\text{1}|X=\text{1})
    &=& \frac{P(Y=\text{1 and }X=\text{1})}{P(X=\text{1})} \\
    &=& \frac{P(Y=\text{1})\times \color{oiGB}P(X=\text{1})}{\color{oiGB}P(X=\text{1})} \\
    &=& P(Y=\text{1}) \\\end{aligned}$$

Ron is watching a roulette table in a casino and notices that the last
five outcomes were black. He figures that the chances of getting black
six times in a row is very small (about $1/64$) and puts his paycheck on
red. What is wrong with his reasoning?[^37]

### Tree diagrams

are a tool to organize outcomes and probabilities around the structure
of the data. They are most useful when two or more processes occur in a
sequence and each process is conditioned on its predecessors.

The data fit this description. We see the population as split by : yes
and no. Following this split, survival rates were observed for each
group. This structure is reflected in the shown in
Figure [1.9](#smallpoxTreeDiagram){reference-type="ref"
reference="smallpoxTreeDiagram"}. The first branch for is said to be the
branch while the other branches are .

![A tree diagram of the data
set.[]{label="smallpoxTreeDiagram"}](appendix-probability/figures/smallpoxTreeDiagram/smallpoxTreeDiagram){#smallpoxTreeDiagram
width="93%"}

Tree diagrams are annotated with marginal and conditional probabilities,
as shown in Figure [1.9](#smallpoxTreeDiagram){reference-type="ref"
reference="smallpoxTreeDiagram"}. This tree diagram splits the smallpox
data by into the yes and no groups with respective marginal
probabilities 0.0392 and 0.9608. The secondary branches are conditioned
on the first, so we assign conditional probabilities to these branches.
For example, the top branch in
Figure [1.9](#smallpoxTreeDiagram){reference-type="ref"
reference="smallpoxTreeDiagram"} is the probability that = lived
conditioned on the information that = yes. We may (and usually do)
construct joint probabilities at the end of each branch in our tree by
multiplying the numbers we come across as we move from left to right.
These joint probabilities are computed using the General Multiplication
Rule: $$\begin{aligned}
&& P(\text{\var{inoculated} = yes and \var{result} = lived}) \\
    &&\quad = P(\text{\var{inoculated} = yes})\times P(\text{\var{result} = lived}|\text{\var{inoculated} = yes}) \\
    &&\quad = 0.0392\times 0.9754=0.0382\end{aligned}$$

Consider the midterm and final for a statistics class. Suppose 13% of
students earned an A on the midterm. Of those students who earned an A
on the midterm, 47% received an A on the final, and 11% of the students
who earned lower than an A on the midterm received an A on the final.
You randomly pick up a final exam and notice the student received an A.
What is the probability that this student earned an A on the midterm?
[\[exerciseForTreeDiagramOfStudentGettingAOnMidtermGivenThatSheGotAOnFinal\]]{#exerciseForTreeDiagramOfStudentGettingAOnMidtermGivenThatSheGotAOnFinal
label="exerciseForTreeDiagramOfStudentGettingAOnMidtermGivenThatSheGotAOnFinal"}
The end-goal is to find
$P(\text{\var{midterm} = A} | \text{\var{final} = A})$. To calculate
this conditional probability, we need the following probabilities:
$$\begin{aligned}
P(\text{\var{midterm} = A and \var{final} = A}) \qquad\text{and}\qquad
P(\text{\var{final} = A})\end{aligned}$$ However, this information is
not provided, and it is not obvious how to calculate these
probabilities. Since we aren't sure how to proceed, it is useful to
organize the information into a tree diagram, as shown in
Figure [1.10](#testTree){reference-type="ref" reference="testTree"}.
When constructing a tree diagram, variables provided with marginal
probabilities are often used to create the tree's primary branches; in
this case, the marginal probabilities are provided for midterm grades.
The final grades, which correspond to the conditional probabilities
provided, will be shown on the secondary branches.

![A tree diagram describing the and
variables.[]{label="testTree"}](appendix-probability/figures/testTree/testTree){#testTree
width="87%"}

With the tree diagram constructed, we may compute the required
probabilities: $$\begin{aligned}
&&P(\text{\var{midterm} = A and \var{final} = A}) = 0.0611 \\
&&P(\text{\underline{\color{black}\var{final} = A}})  \\
&& \quad= P(\text{\var{midterm} = other and \underline{\color{black}\var{final} = A}}) + P(\text{\var{midterm} = A and \underline{\color{black}\var{final} = A}}) \\
&& \quad= 0.0611 + 0.0957 = 0.1568\end{aligned}$$ The marginal
probability, $P($ = A$)$, was calculated by adding up all the joint
probabilities on the right side of the tree that correspond to = A. We
may now finally take the ratio of the two probabilities:
$$\begin{aligned}
P(\text{\var{midterm} = A} | \text{\var{final} = A}) &=& \frac{P(\text{\var{midterm} = A and \var{final} = A})}{P(\text{\var{final} = A})} \\
&=& \frac{0.0611}{0.1568} = 0.3897\end{aligned}$$ The probability the
student also earned an A on the midterm is about 0.39.

After an introductory statistics course, 78% of students can
successfully construct tree diagrams. Of those who can construct tree
diagrams, 97% passed, while only 57% of those students who could not
construct tree diagrams passed. (a) Organize this information into a
tree diagram. (b) What is the probability that a randomly selected
student passed? (c) Compute the probability a student is able to
construct a tree diagram if it is known that she passed.[^38]

Random variables {#randomVariablesSection}
----------------

Two books are assigned for a statistics class: a textbook and its
corresponding study guide. The university bookstore determined 20% of
enrolled students do not buy either book, 55% buy the textbook only, and
25% buy both books, and these percentages are relatively constant from
one term to another. If there are 100 students enrolled, how many books
should the bookstore expect to sell to this
class?[\[bookStoreSales\]]{#bookStoreSales label="bookStoreSales"}
Around 20 students will not buy either book (0 books total), about 55
will buy one book (55 books total), and approximately 25 will buy two
books (totaling 50 books for these 25 students). The bookstore should
expect to sell about 105 books for this class.

Would you be surprised if the bookstore sold slightly more or less than
105 books?[^39]

The textbook costs \$137 and the study guide \$33. How much revenue
should the bookstore expect from this class of 100
students?[\[bookStoreRev\]]{#bookStoreRev label="bookStoreRev"} About 55
students will just buy a textbook, providing revenue of
$$\begin{aligned}
\$137 \times  55 = \$7,535\end{aligned}$$ The roughly 25 students who
buy both the textbook and the study guide would pay a total of
$$\begin{aligned}
(\$137 + \$33) \times  25 = \$170 \times  25 = \$4,250\end{aligned}$$
Thus, the bookstore should expect to generate about
$\$7,535 + \$4,250 = \$11,785$ from these 100 students for this one
class. However, there might be some *sampling variability* so the actual
amount may differ by a little bit.

![Probability distribution for the bookstore's revenue from a single
student. The distribution balances on a triangle representing the
average revenue per
student.[]{label="bookCostDist"}](appendix-probability/figures/bookCostDist/bookCostDist){#bookCostDist
width="69%"}

What is the average revenue per student for this
course?[\[revFromStudent\]]{#revFromStudent label="revFromStudent"} The
expected total revenue is \$11,785, and there are 100 students.
Therefore the expected revenue per student is
$\$11,785/100 =  \$117.85$.

### Expectation

We call a variable or process with a numerical outcome a , and we
usually represent this random variable with a capital letter such as
$X$, $Y$, or $Z$. The amount of money a single student will spend on her
statistics books is a random variable, and we represent it by $X$.

A random process or variable with a numerical outcome.

The possible outcomes of $X$ are labeled with a corresponding lower case
letter $x$ and subscripts. For example, we write $x_1=\$0$, $x_2=\$137$,
and $x_3=\$170$, which occur with probabilities $0.20$, $0.55$, and
$0.25$. The distribution of $X$ is summarized in
Figure [1.11](#bookCostDist){reference-type="ref"
reference="bookCostDist"} and
Table [\[statSpendDist\]](#statSpendDist){reference-type="ref"
reference="statSpendDist"}.

  $i$            1       2       3      Total
  ------------ ------ ------- ------- -------
  $x_i$         \$0    \$137   \$170       --
  $P(X=x_i)$    0.20   0.55    0.25      1.00

  : The probability distribution for the random variable $X$,
  representing the bookstore's revenue from a single
  student.[]{label="statSpendDist"}

We computed the average outcome of $X$ as \$117.85 in
Example [\[revFromStudent\]](#revFromStudent){reference-type="ref"
reference="revFromStudent"}. We call this average the of $X$, denoted by
$E(X)$. The expected value of a random variable is computed by adding
each outcome weighted by its probability: $$\begin{aligned}
E(X) &= 0 \times  P(X=0) + 137 \times  P(X=137) + 170 \times  P(X=170) \\
    &= 0 \times  0.20 + 137 \times  0.55 + 170 \times  0.25 = 117.85\end{aligned}$$

If $X$ takes outcomes $x_1$, \..., $x_k$ with probabilities $P(X=x_1)$,
\..., $P(X=x_k)$, the expected value of $X$ is the sum of each outcome
multiplied by its corresponding probability: $$\begin{aligned}
E(X)    &= x_1\times P(X=x_1) + \cdots + x_k\times P(X=x_k) \notag \\
    &= \sum_{i=1}^{k}x_iP(X=x_i)\end{aligned}$$ The Greek letter $\mu$
may be used in place of the notation $E(X)$.

The expected value for a random variable represents the average outcome.
For example, $E(X)=117.85$ represents the average amount the bookstore
expects to make from a single student, which we could also write as
$\mu=117.85$.

It is also possible to compute the expected value of a continuous random
variable. However, it requires a little calculus and we save it for a
later class.[^40]

In physics, the expectation holds the same meaning as the center of
gravity. The distribution can be represented by a series of weights at
each outcome, and the mean represents the balancing point. This is
represented in Figures [1.11](#bookCostDist){reference-type="ref"
reference="bookCostDist"} and [1.12](#bookWts){reference-type="ref"
reference="bookWts"}. The idea of a center of gravity also expands to
continuous probability distributions.
Figure [1.13](#contBalance){reference-type="ref"
reference="contBalance"} shows a continuous probability distribution
balanced atop a wedge placed at the mean.

![A weight system representing the probability distribution for $X$. The
string holds the distribution at the mean to keep the system
balanced.[]{label="bookWts"}](appendix-probability/figures/bookWts/bookWts){#bookWts
width="72%"}

![A continuous distribution can also be balanced at its
mean.[]{label="contBalance"}](appendix-probability/figures/contBalance/contBalance){#contBalance
width="65%"}

### Variability in random variables

Suppose you ran the university bookstore. Besides how much revenue you
expect to generate, you might also want to know the volatility
(variability) in your revenue.

The and can be used to describe the variability of a random variable.
Section [\[variability\]](#variability){reference-type="ref"
reference="variability"} introduced a method for finding the variance
and standard deviation for a data set. We first computed deviations from
the mean ($x_i - \mu$), squared those deviations, and took an average to
get the variance. In the case of a random variable, we again compute
squared deviations. However, we take their sum weighted by their
corresponding probabilities, just like we did for the expectation. This
weighted sum of squared deviations equals the variance, and we calculate
the standard deviation by taking the square root of the variance, just
as we did in
Section [\[variability\]](#variability){reference-type="ref"
reference="variability"}.

If $X$ takes outcomes $x_1$, \..., $x_k$ with probabilities $P(X=x_1)$,
\..., $P(X=x_k)$ and expected value $\mu=E(X)$, then the variance of
$X$, denoted by $Var(X)$ or the symbol $\sigma^2$, is $$\begin{aligned}
\sigma^2 &= (x_1-\mu)^2\times P(X=x_1) + \cdots \notag \\
    & \qquad\quad\cdots+ (x_k-\mu)^2\times P(X=x_k) \notag \\
    &= \sum_{j=1}^{k} (x_j - \mu)^2 P(X=x_j)\end{aligned}$$ The standard
deviation of $X$, labeled $\sigma$, is the square root of the variance.

Compute the expected value, variance, and standard deviation of $X$, the
revenue of a single statistics student for the bookstore. It is useful
to construct a table that holds computations for each outcome
separately, then add up the results.

  $i$                           1       2       3    Total
  ------------------------ ------ ------- ------- --------
  $x_i$                       \$0   \$137   \$170 
  $P(X=x_i)$                 0.20    0.55    0.25 
  $x_i \times  P(X=x_i)$        0   75.35   42.50   117.85

Thus, the expected value is $\mu=117.85$, which we computed earlier. The
variance can be constructed by extending this table:

  $i$                                     1        2         3    Total
  ------------------------------ ---------- -------- --------- --------
  $x_i$                                 \$0    \$137     \$170 
  $P(X=x_i)$                           0.20     0.55      0.25 
  $x_i \times  P(X=x_i)$                  0    75.35     42.50   117.85
  $x_i - \mu$                       -117.85    19.15     52.15 
  $(x_i-\mu)^2$                    13888.62   366.72   2719.62 
  $(x_i-\mu)^2\times P(X=x_i)$       2777.7    201.7     679.9   3659.3

The variance of $X$ is $\sigma^2 = 3659.3$, which means the standard
deviation is $\sigma = \sqrt{3659.3} = \$60.49$.

The bookstore also offers a chemistry textbook for \$159 and a book
supplement for \$41. From past experience, they know about 25% of
chemistry students just buy the textbook while 60% buy both the textbook
and supplement.[^41]

1.  What proportion of students don't buy either book? Assume no
    students buy the supplement without the textbook.

2.  Let $Y$ represent the revenue from a single student. Write out the
    probability distribution of $Y$, i.e. a table for each outcome and
    its associated probability.

3.  Compute the expected revenue from a single chemistry student.

4.  Find the standard deviation to describe the variability associated
    with the revenue from a single student.

### Linear combinations of random variables

So far, we have thought of each variable as being a complete story in
and of itself. Sometimes it is more appropriate to use a combination of
variables. For instance, the amount of time a person spends commuting to
work each week can be broken down into several daily commutes.
Similarly, the total gain or loss in a stock portfolio is the sum of the
gains and losses in its components.

John travels to work five days a week. We will use $X_1$ to represent
his travel time on Monday, $X_2$ to represent his travel time on
Tuesday, and so on. Write an equation using $X_1$, \..., $X_5$ that
represents his travel time for the week, denoted by $W$. His total
weekly travel time is the sum of the five daily values:
$$W = X_1 + X_2 + X_3 + X_4 + X_5$$ Breaking the weekly travel time $W$
into pieces provides a framework for understanding each source of
randomness and is useful for modeling $W$.

It takes John an average of 18 minutes each day to commute to work. What
would you expect his average commute time to be for the week? We were
told that the average (i.e. expected value) of the commute time is 18
minutes per day: $E(X_i) = 18$. To get the expected time for the sum of
the five days, we can add up the expected time for each individual day:
$$\begin{aligned}
E(W) &= E(X_1 + X_2 + X_3 + X_4 + X_5) \\
    &= E(X_1) + E(X_2) + E(X_3) + E(X_4) + E(X_5) \\
    &= 18 + 18 + 18 + 18 + 18 = 90\text{ minutes}\end{aligned}$$ The
expectation of the total time is equal to the sum of the expected
individual times. More generally, the expectation of a sum of random
variables is always the sum of the expectation for each random variable.

[\[elenaIsSellingATVAndBuyingAToasterOvenAtAnAuction\]]{#elenaIsSellingATVAndBuyingAToasterOvenAtAnAuction
label="elenaIsSellingATVAndBuyingAToasterOvenAtAnAuction"} Elena is
selling a TV at a cash auction and also intends to buy a toaster oven in
the auction. If $X$ represents the profit for selling the TV and $Y$
represents the cost of the toaster oven, write an equation that
represents the net change in Elena's cash.[^42]

Based on past auctions, Elena figures she should expect to make about
\$175 on the TV and pay about \$23 for the toaster oven. In total, how
much should she expect to make or spend?[^43]

[\[explainWhyThereIsUncertaintyInTheSum\]]{#explainWhyThereIsUncertaintyInTheSum
label="explainWhyThereIsUncertaintyInTheSum"} Would you be surprised if
John's weekly commute wasn't exactly 90 minutes or if Elena didn't make
exactly \$152? Explain.[^44]

Two important concepts concerning combinations of random variables have
so far been introduced. First, a final value can sometimes be described
as the sum of its parts in an equation. Second, intuition suggests that
putting the individual average values into this equation gives the
average value we would expect in total. This second point needs
clarification -- it is guaranteed to be true in what are called *linear
combinations of random variables*.

A of two random variables $X$ and $Y$ is a fancy phrase to describe a
combination $$aX + bY$$ where $a$ and $b$ are some fixed and known
numbers. For John's commute time, there were five random variables --
one for each work day -- and each random variable could be written as
having a fixed coefficient of 1:
$$1X_1 + 1 X_2 + 1 X_3 + 1 X_4 + 1 X_5$$ For Elena's net gain or loss,
the $X$ random variable had a coefficient of +1 and the $Y$ random
variable had a coefficient of -1.

When considering the average of a linear combination of random
variables, it is safe to plug in the mean of each random variable and
then compute the final result. For a few examples of nonlinear
combinations of random variables -- cases where we cannot simply plug in
the means -- see the footnote.[^45]

If $X$ and $Y$ are random variables, then a linear combination of the
random variables is given by $$\begin{aligned}
\label{linComboOfRandomVariablesXAndY}
aX + bY\end{aligned}$$ where $a$ and $b$ are some fixed numbers. To
compute the average value of a linear combination of random variables,
plug in the average of each individual random variable and compute the
result: $$\begin{aligned}
a\times E(X) + b\times E(Y)\end{aligned}$$ Recall that the expected
value is the same as the mean, e.g. $E(X) = \mu_X$.

Leonard has invested \$6000 in Google Inc. (stock ticker: GOOG) and
\$2000 in Exxon Mobil Corp. (XOM). If $X$ represents the change in
Google's stock next month and $Y$ represents the change in Exxon Mobil
stock next month, write an equation that describes how much money will
be made or lost in Leonard's stocks for the month. For simplicity, we
will suppose $X$ and $Y$ are not in percents but are in decimal form
(e.g. if Google's stock increases 1%, then $X=0.01$; or if it loses 1%,
then $X=-0.01$). Then we can write an equation for Leonard's gain as
$$\begin{aligned}
\$6000\times X + \$2000\times Y\end{aligned}$$ If we plug in the change
in the stock value for $X$ and $Y$, this equation gives the change in
value of Leonard's stock portfolio for the month. A positive value
represents a gain, and a negative value represents a loss.

[\[expectedChangeInLeonardsStockPortfolio\]]{#expectedChangeInLeonardsStockPortfolio
label="expectedChangeInLeonardsStockPortfolio"} Suppose Google and Exxon
Mobil stocks have recently been rising 2.1% and 0.4% per month,
respectively. Compute the expected change in Leonard's stock portfolio
for next month.[^46]

You should have found that Leonard expects a positive gain in Guided
Practice [\[expectedChangeInLeonardsStockPortfolio\]](#expectedChangeInLeonardsStockPortfolio){reference-type="ref"
reference="expectedChangeInLeonardsStockPortfolio"}. However, would you
be surprised if he actually had a loss this month?[^47]

### Variability in linear combinations of random variables

Quantifying the average outcome from a linear combination of random
variables is helpful, but it is also important to have some sense of the
uncertainty associated with the total outcome of that combination of
random variables. The expected net gain or loss of Leonard's stock
portfolio was considered in Guided
Practice [\[expectedChangeInLeonardsStockPortfolio\]](#expectedChangeInLeonardsStockPortfolio){reference-type="ref"
reference="expectedChangeInLeonardsStockPortfolio"}. However, there was
no quantitative discussion of the volatility of this portfolio. For
instance, while the average monthly gain might be about \$134 according
to the data, that gain is not guaranteed.
Figure [1.14](#changeInLeonardsStockPortfolioFor36Months){reference-type="ref"
reference="changeInLeonardsStockPortfolioFor36Months"} shows the monthly
changes in a portfolio like Leonard's during the 36 months from 2009 to
2011. The gains and losses vary widely, and quantifying these
fluctuations is important when investing in stocks.

![The change in a portfolio like Leonard's for the 36 months from 2009
to 2011, where \$6000 is in Google's stock and \$2000 is in Exxon
Mobil's.[]{label="changeInLeonardsStockPortfolioFor36Months"}](appendix-probability/figures/changeInLeonardsStockPortfolioFor36Months/changeInLeonardsStockPortfolioFor36Months){#changeInLeonardsStockPortfolioFor36Months
width="65%"}

Just as we have done in many previous cases, we use the variance and
standard deviation to describe the uncertainty associated with Leonard's
monthly returns. To do so, the variances of each stock's monthly return
will be useful, and these are shown in
Table [\[sumStatOfGOOGXOM\]](#sumStatOfGOOGXOM){reference-type="ref"
reference="sumStatOfGOOGXOM"}. The stocks' returns are nearly
independent.

           Mean ($\bar{x}$)   Standard deviation ($s$)   Variance ($s^2$)
  ------ ------------------ -------------------------- ------------------
  GOOG               0.0210                     0.0846             0.0072
  XOM                0.0038                     0.0519             0.0027

  : The mean, standard deviation, and variance of the GOOG and XOM
  stocks. These statistics were estimated from historical stock data, so
  notation used for sample statistics has been
  used.[]{label="sumStatOfGOOGXOM"}

Here we use an equation from probability theory to describe the
uncertainty of Leonard's monthly returns; we leave the proof of this
method to a dedicated probability course. The variance of a linear
combination of random variables can be computed by plugging in the
variances of the individual random variables and squaring the
coefficients of the random variables: $$\begin{aligned}
Var(aX + bY) = a^2\times Var(X) + b^2\times Var(Y)\end{aligned}$$ It is
important to note that this equality assumes the random variables are
independent; if independence doesn't hold, then more advanced methods
are necessary. This equation can be used to compute the variance of
Leonard's monthly return: $$\begin{aligned}
Var(6000\times X + 2000\times Y)
    &= 6000^2\times Var(X) + 2000^2\times Var(Y) \\
    &= 36,000,000\times 0.0072 + 4,000,000\times 0.0027 \\
    &= 270,000\end{aligned}$$ The standard deviation is computed as the
square root of the variance: $\sqrt{270,000} = \$520$. While an average
monthly return of \$134 on an \$8000 investment is nothing to scoff at,
the monthly returns are so volatile that Leonard should not expect this
income to be very stable.

The variance of a linear combination of random variables may be computed
by squaring the constants, substituting in the variances for the random
variables, and computing the result: $$\begin{aligned}
Var(aX + bY) = a^2\times Var(X) + b^2\times Var(Y)\end{aligned}$$ This
equation is valid as long as the random variables are independent of
each other. The standard deviation of the linear combination may be
found by taking the square root of the variance.

Suppose John's daily commute has a standard deviation of 4 minutes. What
is the uncertainty in his total commute time for the week?
[\[sdOfJohnsCommuteWeeklyTime\]]{#sdOfJohnsCommuteWeeklyTime
label="sdOfJohnsCommuteWeeklyTime"} The expression for John's commute
time was $$\begin{aligned}
X_1 + X_2 + X_3 + X_4 + X_5\end{aligned}$$ Each coefficient is 1, and
the variance of each day's time is $4^2=16$. Thus, the variance of the
total weekly commute time is $$\begin{aligned}
&\text{variance }= 1^2 \times  16 + 1^2 \times  16 + 1^2 \times  16 + 1^2 \times  16 + 1^2 \times  16 = 5\times 16 = 80 \\
&\text{standard deviation } = \sqrt{\text{variance}} = \sqrt{80} = 8.94\end{aligned}$$
The standard deviation for John's weekly work commute time is about 9
minutes.

The computation in
Example [\[sdOfJohnsCommuteWeeklyTime\]](#sdOfJohnsCommuteWeeklyTime){reference-type="ref"
reference="sdOfJohnsCommuteWeeklyTime"} relied on an important
assumption: the commute time for each day is independent of the time on
other days of that week. Do you think this is valid? Explain.[^48]

[\[elenaIsSellingATVAndBuyingAToasterOvenAtAnAuctionVariability\]]{#elenaIsSellingATVAndBuyingAToasterOvenAtAnAuctionVariability
label="elenaIsSellingATVAndBuyingAToasterOvenAtAnAuctionVariability"}
Consider Elena's two auctions from Guided
Practice [\[elenaIsSellingATVAndBuyingAToasterOvenAtAnAuction\]](#elenaIsSellingATVAndBuyingAToasterOvenAtAnAuction){reference-type="ref"
reference="elenaIsSellingATVAndBuyingAToasterOvenAtAnAuction"} on page .
Suppose these auctions are approximately independent and the variability
in auction prices associated with the TV and toaster oven can be
described using standard deviations of \$25 and \$8. Compute the
standard deviation of Elena's net gain.[^49]

Consider again Guided
Practice [\[elenaIsSellingATVAndBuyingAToasterOvenAtAnAuctionVariability\]](#elenaIsSellingATVAndBuyingAToasterOvenAtAnAuctionVariability){reference-type="ref"
reference="elenaIsSellingATVAndBuyingAToasterOvenAtAnAuctionVariability"}.
The negative coefficient for $Y$ in the linear combination was
eliminated when we squared the coefficients. This generally holds true:
negatives in a linear combination will have no impact on the variability
computed for a linear combination, but they do impact the expected value
computations.

[^1]: Here are four examples. (i) Whether someone gets sick in the next
    month or not is an apparently random process with outcomes sick and
    not. (ii) We can *generate* a random process by randomly picking a
    person and measuring that person's height. The outcome of this
    process will be a positive number. (iii) Whether the stock market
    goes up or down next week is a seemingly random process with
    possible outcomes up, down, and no\_. Alternatively, we could have
    used the percent change in the stock market as a numerical outcome.
    (iv) Whether your roommate cleans her dishes tonight probably seems
    like a random process with possible outcomes cleans\_ and leaves\_.

[^2]: \(a\) The random process is a die roll, and at most one of these
    outcomes can come up. This means they are disjoint outcomes.
    (b) $P($1 or 4 or
    5$) = P($1$)+P($4$)+P($5$) = \frac{1}{6} + \frac{1}{6} + \frac{1}{6} = \frac{3}{6} = \frac{1}{2}$

[^3]: \(a\) Yes. Each email is categorized in only one level of . (b)
    Small: $\frac{2827}{3921} = 0.721$. Big: $\frac{545}{3921} = 0.139$.
    (c) $P($small or
    big$) = P($small$) + P($big$) = 0.721 + 0.139 = 0.860$.

[^4]: \(a\) $P(A) = P($1 or
    2$) = P($1$) + P($2$) = \frac{1}{6} + \frac{1}{6} = \frac{2}{6} = \frac{1}{3}$.
    (b) Similarly, $P(B) = 1/3$.

[^5]: (a) Outcomes 2 and 3. (b) Yes, events $B$ and $D$ are disjoint
    because they share no outcomes. (c) The events $A$ and $D$ share an
    outcome in common, 2, and so are not disjoint.

[^6]: Since $B$ and $D$ are disjoint events, use the Addition Rule:
    $P(B$ or
    $D) = P(B) + P(D) = \frac{1}{3} + \frac{1}{3} = \frac{2}{3}$.

[^7]: The 52 cards are split into four : $\clubsuit$ (club),
    $\diamondsuit$ (diamond), $\heartsuit$ (heart), $\spadesuit$
    (spade). Each suit has its 13 cards labeled: 2, 3, \..., 10, J
    (jack), Q (queen), K (king), and A (ace). Thus, each card is a
    unique combination of a suit and a label, e.g. 4$\heartsuit$ and
    J$\clubsuit$. The 12 cards represented by the jacks, queens, and
    kings are called . The cards that are $\diamondsuit$ or $\heartsuit$
    are typically colored red while the other two suits are typically
    colored black.

[^8]: \(a\) There are 52 cards and 13 diamonds. If the cards are
    thoroughly shuffled, each card has an equal chance of being drawn,
    so the probability that a randomly selected card is a diamond is
    $P({\color{redcards}\diamondsuit}) = \frac{13}{52} = 0.250$.
    (b) Likewise, there are 12 face cards, so $P($face
    card$) = \frac{12}{52} = \frac{3}{13} = 0.231$.

[^9]: The Venn diagram shows face cards split up into "face card but not
    $\diamondsuit$" and "face card and $\diamondsuit$". Since these
    correspond to disjoint events, $P($face card$)$ is found by adding
    the two corresponding probabilities:
    $\frac{3}{52} + \frac{9}{52} = \frac{12}{52} = \frac{3}{13}$.

[^10]: \(a\) If $A$ and $B$ are disjoint, $A$ and $B$ can never occur
    simultaneously. (b) If $A$ and $B$ are disjoint, then the last term
    of
    Equation ([\[generalAdditionRule\]](#generalAdditionRule){reference-type="ref"
    reference="generalAdditionRule"}) is 0 (see part (a)) and we are
    left with the Addition Rule for disjoint events.

[^11]: Both the counts and corresponding probabilities (e.g.
    $2659/3921 = 0.678$) are shown. Notice that the number of emails
    represented in the left circle corresponds to $2659 + 168 = 2827$,
    and the number represented in the right circle is $168 + 199 = 367$.

     

    ![image](appendix-probability/figures/emailSpamNumberVenn/emailSpamNumberVenn){height="13mm"}

[^12]: (a) The solution is represented by the intersection of the two
    circles: 0.043. (b) This is the sum of the three disjoint
    probabilities shown in the circles: $0.678 + 0.043 + 0.051 = 0.772$.

[^13]: The probabilities of (a) do not sum to 1. The second probability
    in (b) is negative. This leaves (c), which sure enough satisfies the
    requirements of a distribution. One of the three was said to be the
    actual distribution of US household incomes, so it must be (c).

[^14]: It is also possible to construct a distribution plot when income
    is not artificially binned into four groups.

[^15]: (a) The outcomes are disjoint and each has probability $1/6$, so
    the total probability is $4/6=2/3$. (b) We can also see that
    $P(D)=\frac{1}{6} + \frac{1}{6} = 1/3$. Since $D$ and $D^c$ are
    disjoint, $P(D) + P(D^c) = 1$.

[^16]: Brief solutions: (a) $A^c=\{$3, 4, 5, 6$\}$ and $B^c=\{$1, 2, 3,
    5$\}$. (b) Noting that each outcome is disjoint, add the individual
    outcome probabilities to get $P(A^c)=2/3$ and $P(B^c)=2/3$.
    (c) $A$ and $A^c$ are disjoint, and the same is true of
    $B$ and $B^c$. Therefore, $P(A) + P(A^c) = 1$ and
    $P(B) + P(B^c) = 1$.

[^17]: (a) The complement of $A$: when the total is equal to 12.
    (b) $P(A^c) = 1/36$. (c) Use the probability of the complement from
    part (b), $P(A^c) = 1/36$, and
    Equation ([\[complement\]](#complement){reference-type="ref"
    reference="complement"}): $P($less than
    12$) = 1 - P($12$) = 1 - 1/36 = 35/36$.

[^18]: (a) First find $P($6$)=5/36$, then use the complement: $P($not
    6$) = 1 - P($6$) = 31/36$. (b) First find the complement, which
    requires much less effort: $P($2 or 3$)=1/36+2/36=1/12$. Then
    calculate $P(B) = 1-P(B^c) = 1-1/12 = 11/12$. (c) As before, finding
    the complement is the clever way to determine $P(D)$. First find
    $P(D^c) = P($11 or 12$)=2/36 + 1/36=1/12$. Then calculate
    $P(D) = 1 - P(D^c) = 11/12$.

[^19]: \(a\) The probability the first person is left-handed is $0.09$,
    which is the same for the second person. We apply the Multiplication
    Rule for independent processes to determine the probability that
    both will be left-handed: $0.09\times 0.09 = 0.0081$.

    \(b\) It is reasonable to assume the proportion of people who are
    ambidextrous (both right and left handed) is nearly 0, which results
    in $P($right-handed$)=1-0.09=0.91$. Using the same reasoning as in
    part (a), the probability that both will be right-handed is
    $0.91\times 0.91 = 0.8281$.

[^20]: (a) The abbreviations RH and LH are used for right-handed and
    left-handed, respectively. Since each are independent, we apply the
    Multiplication Rule for independent processes: $$\begin{aligned}
    P(\text{all five are RH})
    &= P(\text{first = RH, second = RH, ..., fifth = RH}) \\
    &= P(\text{first = RH})\times P(\text{second = RH})\times  \dots \times P(\text{fifth = RH}) \\
    &= 0.91\times 0.91\times 0.91\times 0.91\times 0.91 = 0.624\end{aligned}$$

    (b) Using the same reasoning as in (a),
    $0.09\times 0.09\times 0.09\times 0.09\times 0.09 = 0.0000059$

    (c) Use the complement, $P($all five are RH$)$, to answer this
    question: $$\begin{aligned}
    P(\text{not all RH})
        = 1 - P(\text{all RH})
        = 1 - 0.624 = 0.376\end{aligned}$$

[^21]: The actual proportion of the U.S. population that is female is
    about 50%, and so we use 0.5 for the probability of sampling a
    woman. However, this probability does differ in other countries.

[^22]: Brief answers are provided. (a) This can be written in
    probability notation as $P($a randomly selected person is male and
    right-handed$)=0.455$. (b) 0.207. (c) 0.045. (d) 0.0093.

[^23]: Ellis GJ and Stone LH. 1979. Marijuana Use in College: An
    Evaluation of a Modeling Explanation. Youth and Society 10:323-334.

[^24]: Each of the four outcome combination are disjoint, all
    probabilities are indeed non-negative, and the sum of the
    probabilities is $0.28 + 0.19 + 0.21 + 0.32 = 1.00$.

[^25]: This is an observational study and no causal conclusions may be
    reached.

[^26]: \(a\)
    $P(\text{\var{parent} = not} | \text{\var{student} = not})$. (b)
    Equation ([\[condProbEq\]](#condProbEq){reference-type="ref"
    reference="condProbEq"}) for conditional probability indicates we
    should first find
    $P(\text{\var{parents} = not and \var{student} = not})=0.32$ and
    $P(\text{\var{student} = not})=0.51$. Then the ratio represents the
    conditional probability: $0.32/0.51 = 0.63$.

[^27]: (a) This probability is
    $\frac{P(\text{\var{parents} = used and \var{student} = not})}{P(\text{\var{student} = not})} = \frac{0.19}{0.51} = 0.37$.
    (b) The total equals 1. (c) Under the condition the student does not
    use drugs, the parents must either use drugs or not. The complement
    still appears to work *when conditioning on the same information*.

[^28]: No. This was an observational study. Two potential confounding
    variables include and . Can you think of others?

[^29]: Fenner F. 1988. *Smallpox and Its Eradication (History of
    International Public Health, No. 6)*. Geneva: World Health
    Organization. ISBN 92-4-156110-6.

[^30]: $P($ = died $|$ =
    no$) = \frac{P(\text{\var{result} = died and \var{inoculated} = no})}{P(\text{\var{inoculated} = no})} = \frac{0.1356}{0.9608} = 0.1411$.

[^31]: $P($ = died $|$ =
    yes$) = \frac{P(\text{\var{result} = died and \var{inoculated} = yes})}{P(\text{\var{inoculated} = yes})} = \frac{0.0010}{0.0392} = 0.0255$.
    The death rate for individuals who were inoculated is only about
    1 in 40 while the death rate is about 1 in 7 for those who were not
    inoculated.

[^32]: Brief answers: (a) Observational. (b) No, we cannot infer
    causation from this observational study. (c) Accessibility to the
    latest and best medical care. There are other valid answers for
    part (c).

[^33]: The answer is 0.0382, which can be verified using
    Table [\[smallpoxProbabilityTable\]](#smallpoxProbabilityTable){reference-type="ref"
    reference="smallpoxProbabilityTable"}.

[^34]: There were only two possible outcomes: lived or died. This means
    that 100% - 97.45% = 2.55% of the people who were inoculated died.

[^35]: The samples are large relative to the difference in death rates
    for the "inoculated" and "not inoculated" groups, so it seems there
    is an association between and . However, as noted in the solution to
    Guided
    Practice [\[SmallpoxInoculationObsExpExercise\]](#SmallpoxInoculationObsExpExercise){reference-type="ref"
    reference="SmallpoxInoculationObsExpExercise"}, this is an
    observational study and we cannot be sure if there is a causal
    connection. (Further research has shown that inoculation is
    effective at reducing death rates.)

[^36]: Brief solutions: (a) $1/6$. (b) $1/36$.
    (c) $\frac{P(Y = \text{ 1 and }X=\text{ 1})}{P(X=\text{ 1})} = \frac{1/36}{1/6} = 1/6$.
    (d) The probability is the same as in part (c): $P(Y=1)=1/6$. The
    probability that $Y=1$ was unchanged by knowledge about $X$, which
    makes sense as $X$ and $Y$ are independent.

[^37]: He has forgotten that the next roulette spin is independent of
    the previous spins. Casinos do employ this practice; they post the
    last several outcomes of many betting games to trick unsuspecting
    gamblers into believing the odds are in their favor. This is called
    the .

[^38]: \(a\) The tree diagram is shown to the right. (b) Identify which
    two joint probabilities represent students who passed, and add them:
    $P($passed$) = 0.7566+0.1254= 0.8820$. (c) $P($construct tree
    diagram $|$ passed$) = \frac{0.7566}{0.8820} = 0.8578$.\
     

    ![image](appendix-probability/figures/treeDiagramAndPass/treeDiagramAndPass){width="\\textwidth"}

[^39]: If they sell a little more or a little less, this should not be a
    surprise. Hopefully
    Chapter [\[introductionToData\]](#introductionToData){reference-type="ref"
    reference="introductionToData"} helped make clear that there is
    natural variability in observed data. For example, if we would flip
    a coin 100 times, it will not usually come up heads exactly half the
    time, but it will probably be close.

[^40]: $\mu = \int xf(x)dx$ where $f(x)$ represents a function for the
    density curve.

[^41]: \(a\) 100% - 25% - 60% = 15% of students do not buy any books for
    the class. Part (b) is represented by the first two lines in the
    table below. The expectation for part (c) is given as the total on
    the line $y_i\times P(Y=y_i)$. The result of part (d) is the
    square-root of the variance listed on in the total on the last line:
    $\sigma = \sqrt{Var(Y)} = \$69.28$.

                   $i$ (scenario)   1 (noBook)   2 (textbook)   3 (both)                   Total
      --------------------------- ------------ -------------- ---------- -----------------------
                            $y_i$         0.00         159.00     200.00 
                       $P(Y=y_i)$         0.15           0.25       0.60 
             $y_i\times P(Y=y_i)$         0.00          39.75     120.00         $E(Y) = 159.75$
                       $y_i-E(Y)$      -159.75          -0.75      40.25 
                   $(y_i-E(Y))^2$     25520.06           0.56    1620.06 
        $(y_i-E(Y))^2\times P(Y)$       3828.0            0.1      972.0   $Var(Y) \approx 4800$

[^42]: She will make $X$ dollars on the TV but spend $Y$ dollars on the
    toaster oven: $X-Y$.

[^43]: $E(X-Y) = E(X) - E(Y) = 175 - 23 = \$152$. She should expect to
    make about \$152.

[^44]: No, since there is probably some variability. For example, the
    traffic will vary from one day to next, and auction prices will vary
    depending on the quality of the merchandise and the interest of the
    attendees.

[^45]: If $X$ and $Y$ are random variables, consider the following
    combinations: $X^{1+Y}$, $X\times Y$, $X/Y$. In such cases, plugging
    in the average value for each random variable and computing the
    result will not generally lead to an accurate average value for the
    end result.

[^46]: $E(\$6000\times X + \$2000\times Y) = \$6000\times 0.021 + \$2000\times 0.004 = \$134$.

[^47]: No. While stocks tend to rise over time, they are often volatile
    in the short term.

[^48]: One concern is whether traffic patterns tend to have a weekly
    cycle (e.g. Fridays may be worse than other days). If that is the
    case, and John drives, then the assumption is probably not
    reasonable. However, if John walks to work, then his commute is
    probably not affected by any weekly traffic cycle.

[^49]: The equation for Elena can be written as $$\begin{aligned}
    (1)\times X + (-1)\times Y\end{aligned}$$ The variances of $X$ and
    $Y$ are 625 and 64. We square the coefficients and plug in the
    variances: $$\begin{aligned}
    (1)^2\times Var(X) + (-1)^2\times Var(Y) = 1\times 625 + 1\times 64 = 689\end{aligned}$$
    The variance of the linear combination is 689, and the standard
    deviation is the square root of 689: about \$26.25.
