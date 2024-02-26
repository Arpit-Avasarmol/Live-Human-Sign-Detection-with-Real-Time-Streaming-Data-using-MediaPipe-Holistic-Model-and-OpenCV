# Live-Human-Sign-Detection-with-Real-Time-Streaming-Data-using-MediaPipe-Holistic-Model-and-OpenCV

**Overview**
We manually extracted frames from sign language videos to generate two datasets: a static sign language dataset focusing on hand positions and gestures, and a gesture sign language dataset capturing entire sign language phrases, including full body movements, facial expressions, and hand gestures.

**Dataset Collection**
We collected video data of individuals performing sign language gestures using MediaPipe Holistic and OpenCV with a webcam. MediaPipe Holistic provides pose, hand, and face landmark estimation, aiding in identifying sign language hand and body movements. Video data was not saved to conserve storage space; instead, an array of extracted key elements from MediaPipe Holistic was stored.

**Video Input**
MediaPipe Holistic accepts video from a camera or a previously recorded file.

**Pose Estimation**
MediaPipe Holistic detects the person's pose within the video frame using the BlazePose machine learning model, locating important body components such as the head, shoulders, arms, hips, and legs.

**Hand and Face Landmark Estimation**
Distinct machine-learning models are used for estimating hand and visage landmarks. The face landmark model detects 468 key points on the visage, whereas the hand landmark model detects 21 key points on each hand.

**Integration of Keypoints**
MediaPipe Holistic combines the key points into a single coordinate space, creating a holistic representation of the individual in the video frame, enabling accurate monitoring of the person's movements.


# **LSTM Model for Gesture Sign Language**
For the gesture sign language dataset, we used an LSTM model with three LSTM layers and no batch normalization. The classification layers are similar to the static sign language LSTM model, with a softmax output layer in place of a sigmoid layer.

**Training and Evaluation**
Model were trained on the same dataset and whole dataset was utilized for Training. Optimal epochs were determined, and validation accuracy was monitored to avoid overfitting. Various evaluation metrics were employed to assess system performance. The Training was visualized on TensorBoard.

**Results**
The proposed system achieved high precision and performed well in sign language recognition tasks. The LSTM model excelled on the gesture sign language dataset, demonstrating the versatility of models.


**Output**
MediaPipe Holistic generates a set of key points or landmarks representing the pose, hand, and face of the individual in the video frame.

