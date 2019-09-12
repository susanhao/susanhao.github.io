---
title: "Projects"
layout: single
author_profile: true
header:
    permalink: /projects/
permalink: /projects
---

## Real Time Face Emotion Detection
This project was for the Berkeley GDSO 2019 Data Science Workshop and aimed to detect emotion of faces in real time using people's webcam.  We first used transfer learning with  pre-trained VGGFace to build a CNN that had ~64.4% accuracy in predicting basic face emotion. Then, we used Flask to develop an app that reads in frames from the webcam and inputs each frame's image into our model.  An emoji was then overlayed over the face on the webcam that corresponded to the model output.  Click [here](https://github.com/susanhao/emotion_project) for the github repo.
{% include realtimevideo.html %}

## Individual Differences in the Cortical Representation of Faces
How are complex, naturalistic features of emotional faces encoded in the brain?  How does this differ in individuals who don't perceive emotions as well as others? In my primary research project, I use fMRI to implement a multi-feature encoding model that shows how different areas of the brain are tuned to certain face and emotion features. Moreover, we can see how these models differ in individuals with autistic traits which may give us insights into the neural correlates of emotion perception in Autism.

## Emotion Extraction in Natural Images of Crowds
In this project, I investigate how individuals extract emotions from a natural scene of a crowd.  By investigating what features are used to extract certain emotions, we can gain a deeper understanding of how we process social-emotional cues and what features are integral to that process.


## Class Projects
- Visualizing Topographic Independent Component Analysis with Movies [paper](https://arxiv.org/abs/1901.08239)<br>
- Building an Operating System from Scratch [code](https://github.com/susanhao/Operating-System)<br>
- Make-a-Rap [code](https://github.com/susanhao/nets-final-project)<br>
- Health Inspection Reports for Philadelphia Restuarants [code](https://github.com/susanhao/cis550)