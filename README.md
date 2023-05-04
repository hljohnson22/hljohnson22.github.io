# hljohnson22.github.io
CS 766 : Computer Vision

Name : Hailey Johnson

# Research Description
I work in the People & Robots Laboratory, which is a Human Computer Interaction (HCI) lab. My research focuses on accessibility and educational aids for adults with Down syndrome. The first iteration of the research is to design and develop a tablet application that combines augmented reality, object detection, and multimodal feedback to assist the user in learning a new task. In this project I developed the first iteration of an object detection system that will determine if the user is construcing a Lego set in the correct order, using the correct Lego piece.

The main contribution of my research is the development of multimodal technology for adults with Down syndrome that centers on personal and occupational growth by decreasing the time it takes to learn essential skills through a readily available system. However, this work could be
more generalizable. For example, an object detection system that can assist an individual in working through a task step by step can be used in many other outlets, such as on-the-job training, educational classroom aids, and even home improvement projects with enough data and testing. It can also be used as an extra safety layer to increase quality assurance.

[figure1.pdf](https://github.com/hljohnson22/hljohnson22.github.io/files/11401113/figure1.pdf)

# Method

Throughout this semester, I have attempted to implement various techniques learned in class and found this challenge more difficult than I was originally anticipating. In the end I split the work into 4 individual parts. 

First, I preprocessed the video frames to enhance contrast, remove noise, and decrease glare.
Second, I attempted color-based detection through color thresholding to determine the various pieces in the build. 
Third, I attempted shape-based detection using contour analysis to identify each Lego piece by its shape. 
Fourth, assembly detection by comparing the current position of a piece to the expected position in the completed build.

I built my system from scratch in openCv with python to use the various techniques we learned in class.

# Results

I tested my program using videos I knew were the correct ones at a given steps and then tested it on videos I knew were the wrong steps to determine if it could tell me if I did something incorrectly or not. 

The video playing on the right here shows I was able to detect Legos on top of other Legos and I was able to determine the step the participant was on based on the number of bounding boxes found. 

I have found however the system could be improved. For example, when the pink Legos in the video are next to each other instead, it is not registered as two separate Legos, so building a Lego set with many overlapping colors can be difficult to detect the distinction. I also  realized how important the type of data is. I believe I will attempt to refilm the videos in a different way to have the ability to detect the changes between steps to determine if the user is on the right step at the right time. 


# Lessons Learned and Future Goals

I ran into tons of difficulties during the development of this project. First I had to collect my own data, I could not find a data set that was what I was looking for, so the data is minimal and very specific. 

I also had difficult time with processing the various images to isolate specific Legos since Legos are similar colors to each other, but also have a wide range of the same color on them due to glare and shadow effects no matter the lighting. I attempted a few ways to remedy this issue. The histogram equalization increased the contrast well, but also increased the shadows. In the 3rd image I filtered out the glare by eliminating a range of colors, and I was closer to what I was looking for. Finally I attempted mean shift filtering, the contrast is visible with less noise and changes in color. However this filtering technique was very slow on my laptop. But, after just arriving back from a conference, I noticed a fast way was presented and I hope to try to implement that in the next few days to test it out. 

It was difficult to determine if the correct Lego was being used and if it is was placed correctly on the set. 

This project could have been improved in many ways and I will continue to improve it for the next couple days and in the future. 
I would like to eventually collect more data and build this on an ML model opposed to the system I chose for this class project. Additionally I plan on integrating this technology within an AR platform for participant's to evaluate. 

I learned more about the difficulties of colors, videos, and shadows. I think I gained a lot from this project and look forward to making it more robust. !
