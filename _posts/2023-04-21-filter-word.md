---
layout: post
title:  The overlooked "bad" word list ☠️
date:   2023-04-21 16:40:16
description: april, looking forward to summer
tags: nlp, social impact
categories: nlp-posts
---
<img src="https://www.voicesofyouth.org/sites/voy/files/images/2021-06/tempimageckmi1f.png" alt="Negative words can be harmful" style="width:100%">


## Motivation
The internet has become an indispensable part of our daily lives, providing a platform for communication, information, and entertainment. However, along with its many benefits, the internet has also become a breeding ground for harmful and offensive language, which can have a detrimental impact on the well-being of individuals and communities. While bad word lists have been a convenient and widely used tool for content moderation and filtering systems, they are not without their issues, including inherent biases and limitations. This is where our package, [ToxicTrig](), comes in to provide a better alternative for detecting and analyzing toxic language.

## Background


##### <i class="fas fa-vector-square"></i> Why bad word list?
Bad word lists have been widely used due to their convenience in providing reference material for content moderation and filtering systems. By identifying and potentially blocking offensive language, these lists aim to ensure that online spaces remain safe and inclusive for everyone.

##### <i class="fas fa-file-code"></i> What's the problem with the current bad word list?
The current "LDNOOBW/List-of-Dirty-Naughty-Obscene-and-Otherwise-Bad-Words" and other similar lists have several limitations that make them less effective and potentially problematic in addressing the issue of toxic language. Some of the main problems include:

- Outdated terms: Many lists contain outdated offensive terms that may not be relevant or prevalent in today's internet landscape, leading to less effective filtering systems.
- Inherent biases: These lists often fail to account for cultural, linguistic, and contextual nuances, which can result in over-blocking or under-blocking of content.

##### <i class="far fa-object-group"></i> Our patch to the problem

To overcome the limitations of existing bad word lists, we introduce ToxicTrig, a Python package that provides access to a dataset of text triggers that have been categorized as offensive or harmless to minorities. This package is inspired by the paper "Challenges in Automated Debiasing for Toxic Language Detection" by Xuhui Zhou, Maarten Sap, Swabha Swayamdipta, Noah A. Smith, and Yejin Choi.


<hr>

## Introduction to ToxicTrig
##### <i class="fas fa-mouse"></i> Categories
ToxicTrig offers a taxonomy of toxic triggers, which includes the following categories:

- Harmless-minority: Non-offensive minority identity mentions (NOI)
- Offensive-minority-reference: Possibly offensive minority identity mentions (OI)
- Offensive-not-minority: Possibly offensive non-identity mentions (ONI)

##### <i class="fas fa-arrows-alt-h"></i> How to use our package
Using ToxicTrig is simple and straightforward. After installing the package with `pip install toxicTrig`, you can import the package and use it to analyze a list of text strings. The `text_analysis` function will return a dictionary containing the categorized toxic triggers found in the input text.

<hr>

## Conclusion

ToxicTrig provides a more comprehensive and nuanced approach to detecting and analyzing toxic language compared to traditional bad word lists. By addressing the limitations of existing lists and offering a dataset that takes into account minority identities and offensive language, ToxicTrig can greatly contribute to making the internet a safer and more inclusive space for everyone.
