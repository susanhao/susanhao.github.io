---
title: "Projects"
layout: single
author_profile: true
header:
    permalink: /projects/
permalink: /projects/
---
<span style="font-size: 12pt">
    
## Real Time Face Emotion Detection
This project was for the Berkeley GDSO 2019 Data Science Workshop and aimed to detect emotion of faces in real time using people's webcam.  We first used transfer learning with  pre-trained VGGFace to build a CNN that had ~64.4% accuracy (top 10 in the FER2013 Kaggle Challenge) in predicting basic face emotion. Then, we used Flask to develop an app that reads in frames from the webcam and inputs each frame's image into our model.  An emoji was then overlayed over the face on the webcam that corresponded to the model output.  Click [here](https://github.com/susanhao/emotion_project) for the github repo.
{% include realtimevideo.html %}

## Individual Differences in the Cortical Representation of Faces
How are complex, naturalistic features of emotional faces encoded in the brain?  How does this differ in individuals who don't perceive emotions as well as others? In my primary research project, I use fMRI to implement a multi-feature encoding model that shows how different areas of the brain are tuned to certain face and emotion features. Moreover, we can see how these models differ in individuals with autistic traits which may give us insights into the neural correlates of emotion perception in Autism.

## Capacity Estimation of CNNs for Classifying Motor Imagery Movements
In this project, we aimed to understand the generalization capacity of selected deep learning neural networks that were used in a Motor Imagery BCI experiment (Tayeb et al, 2019).  To examine generalization capacity, we measured  memory equivalent capcacity of the original neural networks and their training and test accuracy.  We then iteratively reduced the number of parameters in the neural networks until we obtained the optimal memory equivalent capacity that maximized the test accuracy while minimizing the training accuracy. Click [here](https://drive.google.com/open?id=0B9CSYeIMIq4VTF8xcGFXb2s2YnJPTF9kQnhTbWRtOEkyRG5v) to read the report. 


## Class Projects
- Visualizing Topographic Independent Component Analysis with Movies [paper](https://arxiv.org/abs/1901.08239)<br>
- Building an Operating System from Scratch [code](https://github.com/susanhao/Operating-System)<br>
- Make-a-Rap [code](https://github.com/susanhao/nets-final-project)<br>
- Health Inspection Reports for Philadelphia Restuarants [code](https://github.com/susanhao/cis550)
