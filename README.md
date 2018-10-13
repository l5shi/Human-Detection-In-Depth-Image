I did this task in three steps:

1. First, I have a preprocessing on the depth image due to the chaotic background.
2. Then, I got the edge image and used opencv functions to detect the human contour and box it.
3. At last, I was able to calculate the clrearance distance by using the box coordinate.

This task is relatively easy compared with real life cases since the detection area and detection distance are constrained. For more complicated cases, such as human can walk within a larger area, longer distance, and behind obstacles, detection will be very hard if we still use simple method above. In such case, we may need more data to train a CNN model in order to do the detection and train a linear regression model to estimate the clearance distance.
