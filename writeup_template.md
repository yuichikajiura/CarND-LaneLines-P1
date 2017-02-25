#**Finding Lane Lines on the Road** 

##Writeup Template ver2

###You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

###1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I apply Gaussian smoothing. Third, apply canny transform. Forth, mask image by 4 sided polygon, and, finally, run Hough on edge detected image and draw lines on a blank image. 

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by separating the line to right or left by their slope and area, changing the lines into matrix of x and y, and averaging the lines by appling polyfit function on the matrix. 

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]


###2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when it is applied on curve lines.

Another shortcoming could be when it applied on unusual situation such as bad weather.


###3. Suggest possible improvements to your pipeline

A possible improvement would be to devide several cases by such as straight or cave, rainy weather or not, etc.

Another potential improvement could be to apply machine learning with many data and learn feather and improve each coefficient.
