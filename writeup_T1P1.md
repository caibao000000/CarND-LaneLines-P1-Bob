# **Finding Lane Lines on the Road** 

## Writeup
---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 6 steps: 
1. I converted the images to grayscale;
2. Apply Gaussian Filter to the grayscale images;
3. Use Canny Edge Detection to find the edges;
4. Use mask to select the region of interest;
5. Draw lane lines based on the lines in the region of interest into a empty image;
6. Combine the origional image the lane lines;


In order to draw a single line on the left and right lanes, I modified the draw_lines() function. I compute the difference of the line slope with the mean slope and delete the lines which difference are too big. Then use the lineal regression to get the lane lines.


### 2. Identify potential shortcomings with your current pipeline

One potential shortcoming would be what would happen when the position of the lane line changes.

Another shortcoming could be the lane lines disappear for a while.


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to change the region of the interest.

Another potential improvement could be to store the last detected lane lines if the lane lines disappear for a while.
