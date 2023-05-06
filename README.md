# hljohnson22.github.io
CS 766 : Computer Vision

Name : Hailey Johnson

# Research Description
I work in the People & Robots Laboratory, which is a Human Computer Interaction (HCI) lab. My research focuses on accessibility and educational aids for adults with Down syndrome. The first iteration of my research is to design and develop a tablet application that combines augmented reality, object detection, and multimodal feedback to assist the user in learning a new task. In this project I developed the first iteration of an object detection system that will determine if the user is construcing a Lego set in the correct order, using the correct Lego piece.

The main contribution of my research is the development of multimodal technology for adults with Down syndrome that centers on personal and occupational growth by decreasing the time it takes to learn essential skills through a readily available system. However, this work could be
more generalizable. For example, an object detection system that can assist an individual in working through a task step by step can be used in many other outlets, such as on-the-job training, educational classroom aids, and even home improvement projects with enough data and testing. It can also be used as an extra safety layer to increase quality assurance.

[figure1.pdf](https://github.com/hljohnson22/hljohnson22.github.io/files/11401113/figure1.pdf)

# Method

Throughout this semester, I have attempted to implement various techniques learned in class and found this challenge more difficult than I was originally anticipating. In the end I attempted to split the work into 4 individual parts. 

First, I preprocessed the video frames to enhance contrast, remove noise, and decrease glare.

Second, I attempted color-based detection through color thresholding to determine the various pieces in the build. 

Third, I attempted shape-based detection using contour analysis to identify each Lego piece by its shape. 

Fourth, assembly detection by comparing the current position of a piece to the expected position in the completed build.

I built my system from scratch in openCv with python to use the various techniques we learned in class.

# Results

I tested my program using videos I knew were the correct ones at a given steps.

The video playing below shows I was able to detect Legos on top of other Legos and I was able to determine the step the participant was on based on the number of bounding boxes found. 

https://user-images.githubusercontent.com/103539620/236588256-54666f8a-0a6c-4dac-9d7e-d88fbb8b5dd7.mov


The video below also shows I was able to detect a different color than just pink

https://user-images.githubusercontent.com/103539620/236588115-e780b024-76ce-4f38-8941-cb4c5f1a8e32.mov


I have found however the system could be improved in many ways. For example, when the pink Legos in the video are next to each other instead of seperated, it is not registered as two separate Legos, so building a Lego set with many overlapping colors can be difficult to detect the distinction. I also  realized how important the type of data is. I believe if the videos were made in a different way, i.e. to have the ability to detect the changes between steps to determine if the user is on the right step at the right time, the system may be able to handle Legos next to each other and Legos of the same color. 


# Lessons Learned and Future Goals

I ran into many difficulties during the development of this project. First I had to collect my own data, I could not find a data set that was what I was looking for, so the data is minimal and very specific. 

I also had difficult time with processing the various images to isolate specific Legos since Legos are similar colors to each other, but also have a wide range of the same color on them due to glare and shadow effects no matter the lighting. I attempted a few ways to remedy this issue. 

<img width="204" alt="image" src="https://user-images.githubusercontent.com/103539620/236572676-d758b594-3c9e-46d1-adb7-cba7e5f813cf.png">

The histogram equalization increased the contrast well, but also increased the shadows. 

<img width="186" alt="image" src="https://user-images.githubusercontent.com/103539620/236572709-4af618c8-f698-4347-8a40-ce4b07d002a2.png">

Filtering out the glare by eliminating a range of colors, and I was closer to what I was looking for. 

<img width="224" alt="image" src="https://user-images.githubusercontent.com/103539620/236572732-5fa87075-a66f-4f38-a373-e120d9efb697.png">

Mean shift filtering, the contrast is visible with less noise and changes in color. However this filtering technique was very slow on my laptop.
I ended up using the second option.

It was difficult to determine if the correct Lego was being used and if it is was placed correctly on the set. Overall, the project is not where I was hoping it would end up, but I am happy with all the knowledge I gained while learning how to design, develop, collect data, and test a system such as this one.

I will continue to improve this project in the future. I would like to eventually collect more data and build this on an ML model opposed to the system I chose for this class project. Additionally I plan on integrating this technology within an AR platform for participant's to evaluate. 

I learned more about the difficulties of colors, videos, and shadows. I think I gained a lot from this project and look forward to making it more robust. 
