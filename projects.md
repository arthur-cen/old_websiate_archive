---
layout: page
title: Projects
permalink: /projects/
---

### [Online Face Recognition](https://github.com/arthur-cen/face_recog_video) 
This face recognition project was built for PerceptIn Visual Inertial Module SDK v0.4.0 using OpenCv built-in face module.
***

### [First Aid-Alexa Skill](https://github.com/arthur-cen/alexa-skill-first-aid)

First Aid is an Alexa Skill that I developed using JavaScript under Node.js Framework. The code ran on the Amazon
 Lambda Function Service. In this project, I designed a Voice User Interface(VUI) with a T-shaped design.

I followed the First Aid Instructions in the American Red Cross Adult First Aid/CPR/AED Ready Reference, 
designed a Dialog that allow users to use voice commands to initiate First Aid Request from Alexa. 
Alexa will give step by step instructions for users on demanded First Aids. 
For example, when user request a CPR, Alexa will give instructions to user. 
And when user needs to move to next step, user only need to tell the Alexa to proceed. 
Also, Alexa can help user to count down the numbers in one minute when user is performing CPR to patients. 

***

## Other Projects

### [Machine Learning Bootcamp](https://github.com/arthur-cen/machine_learning_bootcamp)

I followed the face recognition procedure and designed a face detection and recognition system in C++ using OpenCV-3.2. 
And this program was built for the stereo-camera device released by PercetpIn Inc. 

I used OpenCV face detection model for face detection along with other image reading tools provided by OpenCV. 
Then I used FishFaceRecognizer as face recognition model, which is provided in OpenCV contribution module. 
I preprocessed training data by first using face detection to detect the face in the image, cropping face out and then resize them to uniform size. 
Then I used those face images with name tags as training data for face recognizer. Lastly, I implemented an online face recognizer using the trained model. 

I created the online face recognizer by reading streamed image from the device using OpenCV C++ API, and process the image with the same procedure during the data preprocessing. 
The last step was using the trained FisherRecognizer to classify the face. The next Step of this project is applying a better model for face detection and recognition. 
Using Deep learning models is one of my options. I may apply Caffe trained models to the program for future development on this project.
   
### [Crunch Time](https://github.com/arthur-cen/CrunchTime)

This is a toy project that I did for Android Development learning. 


## Contact me

[shengrui.cen-AT-gmail.com](mailto:shengrui.cen@gmail.com)
