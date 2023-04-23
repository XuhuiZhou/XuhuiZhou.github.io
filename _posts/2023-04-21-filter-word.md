---
layout: post
title:  The overlooked "bad" word list ☠️
date:   2023-04-21 16:40:16
description: april, looking forward to summer
tags: nlp, social impact
categories: nlp-posts
---
<img src="https://www.voicesofyouth.org/sites/voy/files/images/2021-06/tempimageckmi1f.png" alt="Negative words can be harmful" style="width:100%">

*This blog post is insipred by [11-830 Computational Ethics in NLP](http://maartensap.com/11-830-Spring2023/index.html). Great course 🧑‍🏫 💃! Take it if you are interested in social good for NLP/AI.*

<span style="color:purple;font-size:110%;">TL;DR Stop using the <a href="https://github.com/LDNOOBW/List-of-Dirty-Naughty-Obscene-and-Otherwise-Bad-Words/tree/master">List-of-Dirty-Naughty-Obscene-and-Otherwise-Bad-Words</a>, use [ToxicTrig](https://github.com/XuhuiZhou/toxtrig/tree/master)</span>

## Motivation
The internet is rampant with toxic language, which can have a detrimental impact on the well-being of individuals and communities. Many ways to analyze toxic language exist, and although using word lists is fundamentally problematic due to the context-dependent nature of toxicity, they offer several advantages, such as convenience and ease of scaling (imaging one needs to analyze trillions-token-level corpus). However, current bad word lists, like [List-of-Dirty-Naughty-Obscene-and-Otherwise-Bad-Words](https://github.com/LDNOOBW/List-of-Dirty-Naughty-Obscene-and-Otherwise-Bad-Words/tree/master), are outdated and sometimes label words as toxic that may no longer be considered offensive (e.g., queer). This highlights the need for a new list that can better analyze toxic language. This is where our package, [ToxicTrig](https://github.com/XuhuiZhou/toxtrig/tree/master), comes in to provide a better alternative for this purpose.

## Background


##### <i class="fas fa-biohazard"></i> What is bad word list?
Bad word lists have been widely used due to their convenience in providing reference material for content moderation and filtering systems. By identifying and potentially blocking offensive language, these lists aim to ensure that online spaces remain safe and inclusive for everyone.

##### <i class="fas fa-exclamation-circle"></i> What's the problem with the current bad word list?
The current [List-of-Dirty-Naughty-Obscene-and-Otherwise-Bad-Words](https://github.com/LDNOOBW/List-of-Dirty-Naughty-Obscene-and-Otherwise-Bad-Words/tree/master) and other similar lists have several limitations that make them less effective and potentially problematic in addressing the issue of toxic language. Some of the main problems include:

- **Outdated terms**: Many lists contain outdated offensive terms that may not be relevant or prevalent in today's internet landscape, leading to less effective filtering systems.
- **Inherent biases**: These lists often fail to account for cultural, linguistic, and contextual nuances, which can result in over-blocking or under-blocking of content.

##### <i class="fas fa-vest-patches"></i> Our patch to the problem

To overcome the limitations of existing bad word lists, we introduce [ToxicTrig](https://github.com/XuhuiZhou/toxtrig/tree/master), a Python package that provides access to a dataset of words that is split into three distinct categories depending on the extent to which they carry profane or hateful meanings or are simply associated with
hateful contexts. We refer to the full set of words as toxicity triggers. This package is inspired by the paper [Challenges in Automated Debiasing for Toxic Language Detection](https://aclanthology.org/2021.eacl-main.274.pdf).

<hr>

## Introducing ToxicTrig
##### <i class="fas fa-th-large"></i> Categories
[ToxicTrig](https://github.com/XuhuiZhou/toxtrig/tree/master) offers a taxonomy of toxic triggers, which includes the following categories:

- **Harmless-minority**: Non-offensive minority identity mentions (NOI). It refers to descriptive mentions of minoritized demographic or social identities (e.g., gay, female, Muslim). Those words, though not offensive itself, are often found in offensive statements that are hateful towards minorities.
- **Offensive-minority-reference**: Possibly offensive minority identity mentions (OI). It refers to mentions of minoritized identities that could denote profanity or hate depending on pragmatic and contextual interpretations. This includes reclaimed slurs (queer, n*gga), which connote less offensive intent when spoken by in-group members compared to out-group members.
- **Offensive-not-minority**: Possibly offensive non-identity mentions (ONI). Note that these words are not necessrially offensive in specific context (e.g., "I f*cked up", "f*cking love this!").

##### <i class="fas fa-box"></i> How to use our package
Using [ToxicTrig](https://github.com/XuhuiZhou/toxtrig/tree/master) is simple and straightforward. After installing the package with `pip install toxicTrig`, you can import the package and use it to analyze a list of text strings. The `text_analysis` function will return a dictionary containing the categorized toxic triggers found in the input text.

<hr>

## Conclusion

[ToxicTrig](https://github.com/XuhuiZhou/toxtrig/tree/master) provides a more nuanced approach to analyzing toxic language compared to traditional bad word lists. By addressing the limitations of existing lists and offering a dataset that takes into account nuanced categories of words associated with toxicity, [ToxicTrig](https://github.com/XuhuiZhou/toxtrig/tree/master) can be a better alternative for content moderation and filtering systems. 
