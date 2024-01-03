---
title: "Introduction"
slug: project-novice-introduction
teaching: 10
exercises: 0
questions:
- "Why should I manage my software development?"
objectives:
- "Explain why academic software development requires management."
keypoints:
- "Well-made software is easier to expand and reuse"
- "You need to produce reproducible research."
- "You are a user of your own code."
---

There's a lot of guidance out there on how to develop *industrial* software, but developing academic software can be an unusual exercise.

## Academic Software

It can be difficult to provide guidance for academic software because the category is so *broad*. Anything developed within the framework of academic research qualifies, and most intensive examples include:

 * Writing drivers and firmware for cutting-edge equipment (e.g. exploratory submersibles)
 * Developing and managing databases of research data (e.g. chemical test results)
 * Machine-learning pipelines consuming GB of data (e.g. genome analysis pipelines)
 * High-performance simulation codes that run on supercomputers (e.g. radiation physics modelling)

 But the majority of academic software is less intensive - collections of smaller scripts, for purposes like:

 * Testing hypotheses on toy models developing full-scale codes
 * Cleaning data files for analysis (e.g. anonymising survey results)
 * Building pipelines from existing software
 * Plotting figures for use in papers

Some disciplines lean more heavily towards one end or the other, but there's people working on all scales of software within all domains.

### Commonalities

The one thing that unites academic software is that unlike in traditional development, the software itself isn't the end goal - it's the *papers* it enables that are. The software is **instrumental**, just a tool to accomplish your research. In addition, it's **experimental** - your understanding of what the software needs to do, or the exact data that will be available for it, is likely to evolve throughout the project. You aren't just writing a piece of software, you're trying to find out what software *could* be written (and if it would be any use!).

Plus, academic software is almost always developed by a small team, in many cases just a single PhD student or postdoc. Even for research groups where multiple people work on the same code, there's very rarely processes or standards that define how code should be written.

{: .callout}
> ## Caveats
>
> In Computer Science and Engineering, you're more likely to have research projects focused on the actual development of software to meet a clearly defined goal. However, they still take place within the framework of academia as a whole, and suffer from the same problems.

## Issues

The lack of firm goals and structured development often means that when you're writing academic code the focus is entirely on how to get the results needed for the latest paper, without considering how this works in the long run. As a result, a large proportion of academic software is **paperware** - ad-hoc, poorly-written code made without any real plans, and a common set of issues:

* **Unplanned:** Whilst you can't produce rigorous plans for exploratory and experimental code, much academic software is just made up on the fly without any real consideration for what it might need to do in future.
* **Undocumented:** Often, how academic software works and how to run it lives entirely within the heads of those who wrote it, often just a single researcher. It's impossible for anyone else to know how it works without investing a huge amount of effort trying to understand it line-by-line.
* **Unmaintainable:** With no plan and no documentation, academic software becomes increasingly hard to maintain. Bugs go unfixed because they'd require fundamental overhauls of the code to address, and the code becomes a rickety stack of twigs that collapses if you poke it wrong - but only the developers know where the limits are.
* **Unshareable:** New researchers can't just pick up and use the code or work on it, without a huge amount of support from the handful of people who *do* know how it works.
* **Disposable:** Fundamentally, **paperware** is disposable - it has to be thrown away after a couple of uses.

### Problems

These common issues end up causing serious problems for the whole of academia:

* **Poor Reproducibility:** Research should be reproducible, and if the code used to generate it is an incomprehensible mess, that's just bad science. Increasingly, journals are pushing back on this by requiring the code for the software used in a paper to be shared.
* **Wasted Effort:** It's tragically routine for a new PhD student joining a group to be handed the previous student's work, spend months trying to understand it, then have to throw it away and start from scratch because nobody *actually* knows how it works.
* **Limited Collaboration:** Whilst sharing software helps the field by advancing the rate of research, and individual academics by generating citations, with so much software being unclear and requiring detailed help to use collaboration is often slow and difficult.
* **Knowledge Decay:** If running a code depends entirely on the knowledge in the developer's head, it's vulnerable to knowledge decay. Returning to previous projects for new collaborations becomes increasingly hard as the researchers involved inevitably forget the quirks, limits and edge-cases for their code.
* **Low Bus Factor:** The 'Bus Factor' is a software engineering term for "The number of people who have to be hit by a bus for a project to be impossible to continue". For most academic software projects, the bus factor is 1. This leads to a huge amount of promising research projects ending up stuck in limbo or shelved entirely when that one person takes sick leave, runs out of time due to other commitments, or ends up leaving academia.

## Writing Sustainable Software

We really want to avoid these problems, because **better software** makes **better research** - organisations like the [Software Sustainability Institute](https://software.ac.uk/) exist to make this point.

If you plan your project out clearly in advance, openly list your future goals and the limitations of your software, and write code that's well-documented, consistent and designed to be easy-to-interpret, you'll find it to be much more **sustainable**. Sustainable software is easier to keep maintained, to expand to cover new problems, and to bring in new collaborators on. The benefits to your research from this will rapidly outweigh the time you spend on software project management.

## Project Management Tools

Fortunately, a lot of tools exist to help manage the development of your academic software. You should already be familiar with Git and [GitHub](https://github.com), already a great way to keep track of how your code evolves and share it with others. GitHub and other repository hosting sites (for example, [GitLab](https://gitlab.com)) have a whole range of project management tools that we can use - and we're going to start with them.
