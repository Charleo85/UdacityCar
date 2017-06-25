# **Finding Lane Lines on the Road** 
CarND Project 1 by Charlie Wu

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

1. Pipeline:
    1. create grayscale image to compute gradient
    2. use gaussian filter on grayscale image to reduce noise
    3. apply canny edge detection.
    4. define a four sided polygon to mask
    5. use hough transform method to get the lines.
    6. draw the lines on the image

The averaged lane slope is used in the draw lane method


2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when the most part of the lane is blocked, and the averaging draw lane method will trigger worse consequence

Another shortcoming could be in the curved lane, masking the lane as a straight lane might be a bad assumption. This is probably the problem waiting to solve in the optional challenge.


3. Suggest possible improvements to your pipeline

A possible improvement would be to fine tune the parameter to get better performance.