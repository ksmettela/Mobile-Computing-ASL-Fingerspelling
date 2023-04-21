# American Sign Language Recognition Application
This project aims to develop an application that can recognize/identify alphabets and words from prerecorded American Sign Language (ASL) videos. ASL is a widely used language by the deaf community for communication, and this application will provide a means to convert ASL input into corresponding meanings as output.

## Introduction
ASL is a complete language with its own grammar and linguistic traits, similar to English. ASL alphabets are portrayed using hand movements and facial expressions. This application utilizes ASL data sets from Kaggle [https://www.kaggle.com/grassknoted/asl-alphabet] and Posenet, a real-time pose detection technique, to recognize ASL alphabets and words from prerecorded videos. The code is implemented in Python3.7, using TensorFlow and Keras for deep learning, and OpenCV for image processing.

## Software/Tools Used
- ASL data set from Kaggle [https://www.kaggle.com/grassknoted/asl-alphabet]
- Posenet for real-time pose detection
- Python 3.7
- TensorFlow and Keras for deep learning
- OpenCV for image processing

## Code
The code performs the following tasks:

- Acquiring individual frames from the videos of alphabets and words using OpenCV.
- Obtaining Keypoints json file using Posenet, and converting it to a csv file using Pandas library.
- Extracting individual frames from the videos using Posenet by considering the coordinates of left and right wrist to the key_points.csv file.
- Segmentation process to examine each frame and detect the letter or word present in the frame.
- Combining different frames of the video using a combination algorithm to get the whole word as output when using separate alphabets.
- Feeding the cropped image to a pretrained CNN model trained on the Kaggle data, to predict the ASL alphabets and words.
- Displaying F1 score, precision, recall, and support for both alphabets and words.

## Instructions
Follow the below steps to run the ASL recognition application:

- Go to the root folder and run npm install.
- Install the required Python packages listed in the requirements.txt file using pip3 install -r requirements.txt.
- Place all the videos of alphabets in the alphabet_videos folder.
- Place all the videos of words in the word_videos folder.
