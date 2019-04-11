![Build Status](https://travis-ci.org/Human-Detection-In-Depth-Image/Human-Detection-In-Depth-Image.svg?branch=master)
The purpose of this project is to find a distance between a human and a wall in a corridor using depth camera observations. Here is an example of a depth image (right) received from a depth camera mounted on a robot. The darker the pixel the closer it is; black corresponds to 0 meters and white corresponds to 5 meters. Just for reference, the corresponding RGB image is shown on the left.

1) Which side is safer to avoid a human (“ ​ left” ​  or “ ​ right” ​ )? 
2) What is the clearance for avoidance maneuver? Clearance is defined as the smallest distance between a human and the obstacle closest to him (a wall or a shelf).

![RGB image](./rgb.png?raw=true ("RGB image")) ![depth image](./depth.png?raw=true ("Depth image[robot observation]"))

I did this task in three steps:

1. First have a preprocessing on the depth image due to the chaotic background.
2. Then, I got the edge image and used opencv functions to detect the human contour and box it.
3. At last, calculate the clearance distance by using the box coordinate.

This task is relatively easy compared with real life cases since the detection area and detection distance are constrained. For more complicated cases, such as human can walk within a larger area, longer distance, and behind obstacles, detection will be very hard if we still use simple method above. In such case, we may need more data to train a CNN model in order to do the detection and train a linear regression model to estimate the clearance distance.
