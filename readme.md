ASL FINGERSPILLING

GROUP NO: 44

GROUP MEMBERS:

ESHWAR PALLEM

PAVAN KUMAR KONJETI

KUMAR SWAMY METTELA

VIJAY KUMAR PENUBOLU

PROJECT AIM-

To develop an application that can recognize/identify alphabets and words from prerecorded ASL videos (American Sign Language).

INTRODUCTION:

The American Sign Language (ASL) is widely utilized by the deaf community to communicate. It is a full language with grammar and linguistic traits, like English. Hands and facial expressions are used to portray ASL alphabets. Because of the widespread use of ASL, we decided to create an application that can accept an ASL input and provide the matching meaning as an output.

The 26 alphabets of English are supported by American Sign Language by employing basic hand movements that otherwise would be utilized for Fingerspelling. It is kind of alphabet borrowing from one language to another. The two letters, 'J' and 'Z,' of all the 26 letters are depicted by static motions.


SOFTWARE’S/TOOLS USED-

- ASL data set from Kaggle https://www.kaggle.com/grassknoted /asl-alphabet 
- Posenet
- Python3.7
- TensorFlow
- Keras
- Visual Studio

CODE-

The code performs following tasks. -

- OpenCV a python library is used for acquiring individual frames from the videos of alphabets and words that are to be predicted.
- Posenet is a real time pose detection technique, that is used to obtain Keypoints json file.
- Using Pandas library Json file is read using read\_json() and then by using to\_csv() function from same library we convert the Json file to csv file.
- Considering the co-ordinates of left and right wrist to the key\_points.csv file, individual frames are extracted using Posenets.
- After the images are extracted using Posenets, the images go through a segmentation process using a segmentation algorithm that we developed to examine each frame and detect the letter or words present in the frame.
- And, when using separate alphabets, a combination algorithm is used to combine the different frames of the video, resulting in a whole word as output.
- With the cropped image in hand, the image is fed to a pretrained CNN model (trained priorly by using the data from the Kaggle) and it predicts the ASL predicted alphabets and words.
- F1 score, precision, recall and support will be displayed for both the alphabets and words.

INSTRUCTIONS-

step1: Go to root folder run npm install

step2: pip3 install -r requirements given under.

step3: Place all the videos of alphabets in alphabet\_videos folder

step4: Place all the videos of words in word\_videos folder

step5: Run the project python main.py (python version >= 3.0)


REQUIREMENTS-

absl-py==0.12.0

astunparse==1.6.3

cachetools==4.2.2

certifi==2020.12.5

chardet==4.0.0

flatbuffers==1.12

gast==0.3.3

google-auth==1.30.0

google-auth-oauthlib==0.4.4

google-pasta==0.2.0

grpcio==1.32.0

h5py==2.10.0

idna==2.10

joblib==1.0.1

Keras-Preprocessing==1.1.2

Markdown==3.3.4

Naked==0.1.31

numpy==1.19.5

oauthlib==3.1.0

opencv-python==4.5.1.48

opt-einsum==3.3.0

pandas==1.2.4

protobuf==3.15.8

pyasn1==0.4.8

pyasn1-modules==0.2.8

python-dateutil==2.8.1

pytz==2021.1

PyYAML==5.4.1

requests==2.25.1

requests-oauthlib==1.3.0

rsa==4.7.2

scikit-learn==0.24.2

scipy==1.6.3

six==1.15.0

sklearn==0.0

tensorboard==2.5.0

tensorboard-data-server==0.6.0

tensorboard-plugin-wit==1.8.0

tensorflow==2.4.1

tensorflow-estimator==2.4.0

termcolor==1.1.0

threadpoolctl==2.1.0

torch==1.8.1

typing-extensions==3.7.4.3

urllib3==1.26.4

Werkzeug==1.0.1

wrapt==1.12.1

CONCLUSION:

In this project, we have proposed an application that can recognize ASL signs through recorded videos. We now have a comprehensive knowledge of how algorithms may be used to translate ASL into other languages. Going through other people’s work on this topic, we got an overview of the current research activities in the subject of language translation, as well as a good grasp of the various machine learning methods and their implementations. To increase the accuracy, a variety of ways were investigated. We got on overview of Posenet, a deep learning model that estimates human pose by detecting human parts.

