---
layout: post
title: Research in an Agile Framework--Timebox with a question
date: 2020-04-25 9:12:00 -0500
categories: [career]
tags: [agile]
---

# TL;DR

* Agile [scrum](https://www.scrum.org/resources/what-is-scrum) is designed for incremental improvements when you know what the goal is.
* Doing research in an Agile [scrum](https://www.scrum.org/resources/what-is-scrum) framework can be a challenge when you don't know how to get from 'here to there'.
* A tool that I have found that works well for doing research in the Agile [scrum](https://www.scrum.org/resources/what-is-scrum) framework is **Timebox with a question**.
    * **Timebox** Provide the researcher a period of time (or story points) to investigate or research a solution. You can give the story a set of points given the time box. 
    2. **Question**: Focus on answering a specific question such as "Investigate object recognition solutions and identify opportunities for our products."

# Research in Agile

When I was a professor at the University of Texas, Austin, I had a colleague that would refer to research as 'Wandering in the desert for the promise land'. The challenge is that the wandering, without direction, can lead to one quickly getting lost and wasting a lot of time. When conducting basic research, this can be effective because you are documenting your progress through scientific publications (which is the currency of academia). 

However, in industry, rarely can we afford years of 'wandering through the desert' with the hope of 'tripping over the golden rock'. The currency of industry is producing something of value to someone else. Often times this leads to a focused engineering approach where the 'there' is well defined and how to get from 'here-to-there' is an exercise of execution. But this can lead to a lot of 'near term', not very innovative or valuable solutions.

However, what do you do when the 'there' is not well defined and the path to get from 'here-to-over-there' is not clear or even currently possible. This is where the value of *research* is found in industry and where most of the high-value opportunities lie.

The agile process is very good when you have a good idea of how to get from 'here to there'. It focuses on small incremental steps that allow you to learn and adapt your product given the most recent information that you have. Interestingly enough, this is how the scientific process also works. Use the most recent research available, figure out the next question to ask, answer that question and add it to the body of human knowledge.

Although both Agile and Research have the same fundamental processes (incremental learning and adaptation) it can be difficult to do research in an agile framework. After more than 10 years doing Agile development and over 10 years doing basic research this is my assessment of *why* the challenge exists and the solutions that I have adopted in my every-day work.

## Differences between Engineering and Research

In my opinion one of the most valuable aspects of the Agile framework is the **Definition of Done** (DoD) criteria. As a product owner I spend a significant amount of my time with my teams ensuring that these DoDs are crisp, clear and understood by every team member for every story.

Typically, when doing research, one is focused on *understanding* and not necessarily on a 'demoable' deliverable. It is difficult to have a DoD that says 'Understand computer vision'. Furthermore, it can be difficult to actually size something like that (see [computer vision legend](http://www.lyndonhill.com/opinion-cvlegends.html)). The areas of research can be 'big, harry and audacious' intellectual spaces that have a lot of room for movement and wandering. In research, this guided wandering that typically leads one to 'trip over the golden rock'. However, this makes 'being done' difficult to define.

*Engineering* by contrast is a process of getting us from 'here to there'. It is goal directed and less worried about understanding than it is about arriving at the goal. As developers we often times leverage open source code or cloud infrastructure without fully understanding how it works (e.g., I can leverage AWS [SPICE storage](https://docs.aws.amazon.com/quicksight/latest/user/managing-spice-capacity.html) without understanding how [SPICE](https://docs.aws.amazon.com/quicksight/latest/user/managing-spice-capacity.html) works).

So how does one allow for someone to 'investigate' or 'understand' something in a framework that emphasizes getting things done. Two tools that I have successfully used over the years are **Timebox with Questions**.

## Timebox with Questions

In research there are typically a set of questions that one is either implicitly or explicitly trying to answer. When I was a professor I would push my students to continually hone and make crisp the question that they were trying to answer. They would often times get exasperated with me asking 'What question are you trying to answer with your research?' But that question was their guide and it needed to be crisp and relevant. Often times in the process of running experiments the question that they were asking would drift without them realizing it. So the second question that I would ask them is "How will the results of this study answer that question?" Sometimes they would give a clear and decisive answer. Sometimes they would pause and realize that there was a misalignment. This would either make them realize that they should abandon the study for a more appropriate study or identify a more important question that they wanted to answer.

The same holds true in the Agile framework. Just as generating a crisp DoD for to guide an engineering solution, one needs to have a crisp question to guide a research story. 

### Example Questions

Well defined questions.

* "Can *deep learning* be used to recognize the words on our products?"
* "What's the fastest face recognition algorithm available and what is the speed/accuracy tradeoff?"

Sometimes the research questions need to be more general when someone doesn't know much about the field.

* "How can we automate face recognition in our product?"

Sometimes the research is even more general to get a 'feel' for what might be possible.

* "Investigate object recognition solutions and identify opportunities for our products."

### The use of timebox

When doing research I ensure that everyone knows (especially the stakeholders) that this is research and we might come out the other end with nothing. In order to manage this risk I always emphasize that we will 'timebox' the effort. That is, we will at most, spend X amount of time (or story points) on this **Epic**. We will report back with progress and/or solutions and then determine if we believe it is advantageous to do more research.

In the Agile framework, I also break this down to timeboxes during a sprint. Although one can do a timebox that is less than a sprint (for small research efforts) typically a timebox is having at least one person focus all of their time for the entire sprint on answering one sub-question at a time. Interestingly enough, my experience is that many of these 'sub-questions' lend themselves well to typical stories. For example, "Identify and collect opensource python face recognition algorithms" with a **DoD** of "Documented summaries and links to opensource solutions".

### The need for trust and flexibility

As I mentioned, when I was a professor, I would always come back to "What question are you trying to answer" and sometimes (often times) this question would drift. In the case of doing research in [scrum](https://www.scrum.org/resources/what-is-scrum), you have to have a certain amount of trust in your team by giving them the flexibility to investigate questions adjacent to the question at hand. This is where innovation often comes from (i.e., tripping over the golden rock). When the question becomes too far away from the current question I'll bring the team together and discuss whether we should continue the current question or adapt to this new, possibly more valuable question. If we decide to continue on the current question, we will put the new question in the backlog for future research.


# References

* [Using Agile Methods in Research](https://www.3mhisinsideangle.com/blog-post/using-agile-methods-in-research/)
* [What is Scrum?](https://www.scrum.org/resources/what-is-scrum)

