# ** Project 1 Finding Lane Lines on the Road ** 

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report



### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I removed image noise
I used Gaussian blurring, then I detected Canny edges and defined the Region of interest, after that I found
lines using Hough transform.

![image1](./examples/grayscale.jpg "Grayscale")

In order to draw a single line for the left and right lanes, I modified the draw_lines() function and for every line 
found slope and intercept and I divided slopes into two parts positive slopes for left line and negative slopes for right line then I found from these mean of slope and intercept for left and right lines

![image2](./test_images_output/solidWhiteCurve.jpg "Solid White Curve")



### 2. Identify potential shortcomings with your current pipeline

 This approach will not work when road is curved and also when snow  also if road is not smooth the edge detector detects a lot of lines that are not lane lines


### 3. Suggest possible improvements to your pipeline

Try to take account curvatures, also maybe it will be good to detect lines by color by filtering image
using hsv conversion


