# DRISHTI

DRISHTI is a non-invasive biometric surveillance system that captures the face, expression, age, gender, gait, and activities of individuals (target persons or criminals) as well as possible weapons present in a distributed CCTV camera system. Also, it maintains a detailed log in the database. DRISHTI won 1st prize in Smart India Hackathon 2020.

## DRISTI has following sub-modules:
### 1. Face Recognition
![](https://github.com/bokey007/DRISHTI/blob/main/demo_vids/face%20recognition.gif)

We are able to identify both known and unknown person in images as well as in realtime video stream. 
### 2. Face Anti-Spoofing
![](https://github.com/bokey007/DRISHTI/blob/main/demo_vids/anti_spoofing.gif)

Most entry level Face Recognition systems are susceptible to presentation attacks.
But our system can identify if the face visible in camera frame is real or fake.
### 3. Emotion Recognition
![](https://github.com/bokey007/DRISHTI/blob/main/demo_vids/emotion_recognition.gif)

We are able to detect following emotions from input video feed
[Happy,Neutral,Surprise,Sad,Angry,Fear]
### 4. Age/Gender Detection
![](https://github.com/bokey007/DRISHTI/blob/main/demo_vids/gender_age_detection.gif)

Drishti can detect both gender as well as perceivable age of person present in the video frame. We still need to improve age detection accuracy further, we are working on it. 
### 5. Action Recognition
![](https://github.com/bokey007/DRISHTI/blob/main/demo_vids/action%20recognition.gif)

Currently we are not looking into temporal information to recognise action being performed. We are using simple neural network to classify the the skeletal data taken from Pose Estimation Module. 

We plan to accomodate temporal info by passing skeletal data to recently opensourced View Adaptive Recurrent Neural Networks.

![](https://github.com/microsoft/View-Adaptive-Neural-Networks-for-Skeleton-based-Human-Action-Recognition/blob/master/README.md)

Actions being recognised are:
[Kick, punch, sit, squat, stand, wave, walk, jump, run]
### 6. Gait Recognition
![](https://github.com/bokey007/DRISHTI/blob/main/demo_vids/gait_recognition.gif)

We are able to extract gait signature from the skeletal data given by Pose Estimaion Module and then further classify these gait signatures using SVM classifier. But currently we are highly overfitting on the training data. We are trying our best to come up with the model that generalises better and thus can be used in real-time.  
### 7. Person-Weapon Detection and Tracking
![](https://github.com/bokey007/DRISHTI/blob/main/demo_vids/object_face_track.gif)

We are able to detect persons and weapons present in the video frame using YOLOv3. The bounding box of each person is associated with his/her name using Face Recognition module. These detections along with their proper labels from both Face Recognition and YOLO are paased to DeepSort Tracking.

So you can see that we can detect weapon present in the video frame and issue warning.

Also even if we could capture the face of suspect in any one frame we can track the person no matter how hard he tries to hide his face. 
### 8. Server that aggregates ingormation from all the modules and updates GUI in real-time

In real time we plan that all these modules will run parallely and send the output to central server which then updates Dashboard GUI in realtime. 

Following is the screen-shot of the proposed GUI:
![Alt text](https://github.com/bokey007/DRISHTI/blob/main/demo_vids/gui.png)

### Details of each module are further available in readme files of respective folders 


#### Code will be made public soon. Stay tuined...!




 
