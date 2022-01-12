# Corner-Detection

This script is a part of my experiments in finding the corners of an object present inside the image.
Steps:
- I used canny edge detector to find the corners and then findContours method from OpenCV to estimate contours from the thresholded image. 
- The estimated contours were grabbed out using the imutils module and then sorted the top 10 contours accordingly. 
- A for loop was used to check if any of those contours form a 4 point polygon, and to break out of the loop as soon as one was found
- The coordinates of the broken contours were written to a variable and plotted on the object to visualize the accuracy

Since this is a hard coded method, there is a high chance that our wished rectangle might be skipped estimating if contours of other rectangle shaped contours break out the for loop.
Harris corner detection algorithm might be used in case of mutliple polygons present inside the loop
