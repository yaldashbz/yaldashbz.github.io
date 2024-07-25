---
layout: page
title: Adapt Pifpaf
description: Explore domain adaptation methods on human keypoint detection on various infrared datasets.
img: assets/img/pifpaf.png
importance: 4
category: selected
redirect: false
github: https://github.com/yaldashbz/adaptpifpaf
---

I got admitted into the Summer@EPFL internship program as one of the top 1-2\% applicants and to intern at the Visual Intelligence for Transportation (<a href="https://www.epfl.ch/labs/vita/">VITA</a>) group at EPFL, supervised by Prof. Alexandre Alahi. I was immersed in a project targeting the detection of REM sleep Behavior Disorder (RBD),  in which people have sudden movements during sleep, and detecting this disorder and treating it would prevent Alzheimer’s in the future. Our videos were infrared, making this project even more challenging. In the initial stages of detecting motion, I delved into the realm of Deep Learning methodologies, like RAFT \& FlowFormer, only to discern that the outcomes fell short of optimal. Consequently, I pivoted towards implementing traditional vision techniques, like background subtraction \& optical flow to extract motion signals from video data. I used anomaly detection methods such as Isolation Forest to identify abnormal points, which unveiled instances of abrupt movements.


For the next phase, I wanted to extract keypoints to determine the part of the body that moved. Our dataset was not labeled, so there have been a lot of challenges due to the low performance of deep models (trained on RGB data) on infrared data. Here, the use of domain adaptation methods in real life showed up. For using existing keypoint detection models, I went through several papers, and found a few infrared human datasets. At first, I tried fine-tuning some keypoint detection models like Fast-RCNN, but the results needed improving. So, instead of Fast-RCNN to detect the movement part of the body, I used OpenPifPaf to detect the keypoints. For adapting OpenPifPaf on a related infrared dataset, I came up with an unsupervised domain adaptation method. Most unsupervised domain adaptation methods are in the classification field, and detecting the keypoints is a regression problem in Computer Vision. Few works exist for this problem, and with a lot of searching in this field, I found the most relevant paper to this solution, “From Synthetic to Real: Unsupervised Domain Adaptation for Animal Pose Estimation”, which uses the architecture of the mean-teacher network, and In a presentation, I presented it to Prof. Alahi and one of his postdocs. Then, I developed a  benchmark for domain adaptation for top-down keypoint detection deep models (like OpenPifPaf) that generate heatmaps using the mentioned paper. I also combined it with a test time adaptation method called TENT, which makes the adaptation in model parameters by entropy minimization. 
