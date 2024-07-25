---
layout: page
title: Comic Segmentation
description: Created a specialized comic dataset, conducted fine-tuning of cutting-edge segmentation methods, and devised strategies to combat data imbalance.
img: assets/img/comic.png
importance: 1
category: selected
redirect: false
github: https://github.com/yaldashbz/comic-seg
---

I got admitted into the Summer@EPFL internship program another time as one of the top 1-2\% applicants to intern at the Image and Visual Representation Lab (<a href="https://www.epfl.ch/labs/ivrl/">IVRL</a>) group at EPFL, supervised by Prof. Sabine Süsstrunk. I undertook a project with a specific focus on applying semantic segmentation techniques to a proprietary comic dataset that was meticulously curated for the study, or for short, Comic Segmentation. Our dataset was not labeled, so I first conducted some data labeling with the help of Segment Anything (SAM). Subsequently, I employed cutting-edge segmentation methodologies on our dataset. I used Mask2Former as the mask classification method and DeepLabv2 as the per-pixel classification method. I fine-tuned different parts of the models to capture the best result and handle the domain gap between pre-trained data and our data. I successfully integrated the outcomes of a mask-classification-based segmentation approach with a pixel-classification method, achieving a cohesive result that mask-classification works much better than pixel-classification, and presented to the IVRL Lab.
