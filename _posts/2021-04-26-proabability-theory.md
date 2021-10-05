---
layout: post-no-feature
title: "Probability Theory"
comments: true
category: articles
---
 Due to uncertainty in the world, we are talking about probability now. The cause of uncertainty is numerous ranging from noises to the limited data sizes. Probability Theory helps us by providing a consistent framework for the qualification and manipulation of the uncertainty and helps us get the foundation of pattern recognition.

There are two fundamental rules of probability theory viz;

- Sum rule
- Product rule

## Sum Rule

To understand the sum rule, we will start with an example from Khan Academy.

Suppose we have a bag with

- 8 Green Cubes
- 9 Green Spheres
- 5 Yellow Cubes
- 7 Yellow Spheres

So, what is the probability of getting a cube of any color,  P(Cube of any color) ? Before answering the question let's ponder on few things. There are altogether 29 objects in the bag and out of which 13 are the cubes. Let's see in the graph below:

<figure>
	<img src="/images/2_1.png">
	<figcaption></figcaption>
</figure>

So, considering that each outcome form the bag is equally likeable(we assume this unless mentioned), the probability of getting cube of any color from the bag is:

<figure>
	<img src="/images/2_2.png">
	<figcaption></figcaption>
</figure>

Similarly, let's find out the probability of popping out a yellow item from the bag. There are altogether 12 items in the bag, comprising 5 yellow cubes and 7 yellow spheres. In diagram:

<figure>
	<img src="/images/2_3.png">
	<figcaption></figcaption>
</figure>


Again, considering the each item from the bag equally probable to pop out, the probability of getting yellow item is:

<figure>
	<img src="/images/2_4.png">
	<figcaption></figcaption>
</figure>

So, what is the probability of getting a yellow cube? Well, we have 29 equal possibilities and hence, the probability of getting a yellow cube is:

<figure>
	<img src="/images/2_5.png">
	<figcaption></figcaption>
</figure>

So, this thing can be easily verified and visualized through a Venn diagram. The intersection portion of the diagram comprises the 5 yellow cubes, i.e., both cubes and yellows. In diagram:

<figure>
	<img src="/images/2_6.png">
	<figcaption></figcaption>
</figure>

Now that we are warmed up with some of the basic probability values, it is the right time to ask a question, What is the probability of getting a yellow item or cube of any color? In notation:

P(Yellow item or Cube of any color)=?
 
Now, we will take help from the Venn diagram. The denominator is 29, for sure, since there are total items as 29 and they are equally likely to pop put. For the numerator part, we need to encounter both yellow items and cubes. So, the total yellow items are 12 and the total 13 cubes. But remember that while considering 12 yellow items, we have already taken 5 yellow cubes into account, which is given by the intersection section of the Venn diagram. Hence,

<figure>
	<img src="/images/2_7.png">
	<figcaption></figcaption>
</figure>

So, we removed the hidden 5 yellow cubes under the yellow items because we have already taken total cubes into account. Now, we can replace these above numbers in probability terms as:

<figure>
	<img src="/images/2_8.png">
	<figcaption></figcaption>
</figure>

In General,

P(A or B)=P(A)+P(B)−P(A and B)

This is called the Addition rule. We can't just add two probabilities, because they might have some overlapping and we have to encounter them by subtraction. In case, if we don't have an overlap as in the diagram below, the intersection would be 0 and this would be simply adding the probabilities, i.e.,

P(A or B)=P(A)+P(B) since, P(A and B) = 0

<figure>
	<img src="/images/2_9.png">
	<figcaption></figcaption>
</figure>

In addition, such events are called mutually exclusive, since event A and event B can't happen at the same time. Occurrence of event A implies the non-occurance of event B.


Now, we will see another fundamental rule of the probability, the Product Rule.

## Product Rule
For the product rule, we will start with the formula and then interpret its meaning. But first, we will talk about the two types of events:

- Independent Events
- Dependent Events

Probability is all about determining the likelihood of the events.

