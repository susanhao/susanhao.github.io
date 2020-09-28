---
title: "Project2_Markdown"
layout: single
author_profile: true
header:
    permalink: /cs194-26/Project2_Markdown/
permalink: /cs194-26/Project2_Markdown/
---


# CS 294-26 Project 2

## Overview

In this project, we learn more about convolution, straightening images, and filtering.

## Part 1.1 Finite Difference Operator

For the cameraman image, we first get partial derivatives in the x and y directions by convolving the humble finite difference vectors with the image.
<br>
![](https://imgur.com/agFkWhB.png)

Then we found the gradient magnitdue of the partial derivatives by summing the squares of the derivative, and then taking the square root.  We then got the binarized gradient magnitude by thresholding any pixels over 50 as 1 and any pixels under as 0.  We got decent signal where we're able to see the edges.
<br>
![](https://imgur.com/hrQp9TX.png)

## Part 1.2 Derivative of Gaussian (DOG) filters

For this part, we made a 2d gaussian kernel of (20, 20) with a sigma of 2.  We convolved this kernel with the cameraman image to blur the iamge and then calculated the partial derivatives and gradient magnitude of the blurred image.  We then binarized this with a threshold of 12 to get an even better binarized gradient magnitude image that shows the edges very clearly.
<br>
![](https://imgur.com/z70mKT5.png)

## Part 1.3 Image Straightening

For this part of the assignment, we calculated the partial derivatives of rotated images that were rotated every 2 degrees from [-10, 10].  We then tried to find the highest number of total edges so that we could have a way of measuring whether the image was straight or not.  We calculated the edges as having degrees that were close to 90, 0, or 180.  To calculate degrees, we took the arc tan of the partial derivative in the y direction divided by the partial derivative in the x derication.  The rotation angle we chose was then the angle that had the max number of edges. 
<br><br>
I tried this on a number of images including the image given as well as the philly skyline and the redwoods which the algorithm did well.  However, for circular objects in images, the object doesn't do well as shown in the picture of the tornado.
<br>
![](https://imgur.com/Wn1HYXG.png)

## Part 2.1 Image Sharpening

For the iamge sharpening, we again calculated a gaussian kernel of (20, 20) with sigma 3 this time, and applied an unmasking filter with one convolution for each channel.  For this, we did the $image + alpha*(image - convolved gaussian filter)$.  For this problem, an alpha of 2.5 was good enough to sharpen most images.
<br>
![](https://imgur.com/mUdbScl.png)

I also applied the gaussian filter to blur an already crisp image of a tortoise.  I think tried to sharpen the blurred image.  There are slight differences between the original and sharpened image.  The sharpened image looks a bit more grainy/unrealistic.
<br>![](https://imgur.com/teSr8ZS.png)

# Part 2.2 Hybrid Images

For Part 2.2, I applied a low pass filter to one image and a high pass filter to another image and averaged them to get the illusion high freq/low freq image as shown in class and the example.  I did this for 3 images.  One is of my professor David Whitney and the singer, Whitney Houston.  The algorithm did a pretty descent job there.  Another was of a dog and a cat.  The cat can only be seen at a distance squinty, but the illusion still works.  An example of when the illusion fails is with any picture of kim kardashinan.  I tried overlaying her face with so many celebrities, but her face is always the only one noticeable.  Here I tried to do a hybrid of kim and kylie, but you can't see kylie's face at all.
<br><br>
I also completed the **bells and whistles** and did the filtered images both as colored images, the low freq as the colored image, and the high freq as the colored image.  Personally, I find the high frequency as the colored image to be the best way to get this illusion to work.
<br>
![](https://imgur.com/ldxvdVf.png)

I additionally calculated the log magnitude of the  fast fourier transform.  Here it is with the first row of images (whitney/whitney illusion).
<br>
![](https://imgur.com/aDuiCGU.png)

## Part 2.3 Gaussian and Laplacian Stacks

For this part, to calculate the laplacian stacks, I took gaussian stack calculation of the next image and subtracted it from the current image.  When I reached the last iteration of my loop, I completed the stack with just the gaussian of the current image.
<br><br>
For the gaussian stack, I convolved the gaussian filter (20, 20) with sigma 5 with the image. Here it is for abe lincoln with the gaussian stack calculated on the top row and the laplacian stack calculated on the second.
<br>![](https://imgur.com/twG1esC.png)

Here it is with the whitney/whitney hybrid image.  Again gaussian stack is calculated for the first row and laplacian for the second.
<br>![](https://imgur.com/ahjN5kf.png)

## Part 2.4 Multiresolution blending

Unforutnately for this part, I couldn't really figure it out.  I applied the laplacian stack for both images and then did the gaussian stack for my mask.  I then followed the formula as stated in the paper that was referenced in the hw.  For some reason, I could not blend the two images.  Perhaps I was using the wrong mask.  I used a Dark gray box on one side and a light gray box on the other side for the apple/orange and bball/vball.  I used a white circle in the middle of a gray square for the hand/mouth.
<br>![](https://imgur.com/q8M4Vwq.png)


```python

```
