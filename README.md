# **Finding Lane Lines on the Road** 


---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road for a specific video captured by camera fixed in the car



### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

steps are as follows :
    1.Reading the video file
    2.Looping on the video frame by frame doing the following:
        1. Image pre-processing :
            1.Resizing image to speciic size  960*540 using OpenCV "resize"
            2.Doing some image smoothing using Gauessian filter with kernel size 5
            3.Converting smoothed image to gray scale
        2. Image processing :
            1.Get edges/contour of objects of the image using Canny edge detection alg. 
            2.Crop the unnecesary region that's not part of the road using a rectangle filter 
            3.Transforming the image using Hough Transform and detecting lines of the road 
            4.Drawing detected lines on the original image

### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when using images in different sizes that may give different results so that I'm fixing image size
Another shortcoming could be in sunlight streetview images need more preprocesing to have expected results 


### 3. Suggest possible improvements to your pipeline

make algorithm working regardless of image size and getting working region in more dynamic way such as defining center point and get the rectangular area around it after getting edges of the image
