# Live-Human-Sign-Detection-with-Real-Time-Streaming-Data-using-MediaPipe-Holistic-Model-and-OpenCV

**Demo**
https://github.com/Arpit-Avasarmol/Live-Human-Sign-Detection-with-Real-Time-Streaming-Data-using-MediaPipe-Holistic-Model-and-OpenCV/assets/88440241/e8b4b1d4-f860-42ed-a2c6-51373b39949c


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
![extract](https://github.com/Arpit-Avasarmol/Live-Human-Sign-Detection-with-Real-Time-Streaming-Data-using-MediaPipe-Holistic-Model-and-OpenCV/assets/88440241/4bfde28f-9ce9-4c84-b679-77e17184cb34)


**LSTM Model for Gesture Sign Language**
For the gesture sign language dataset, we used an LSTM model with three LSTM layers and no batch normalization. The classification layers are similar to the static sign language LSTM model, with a softmax output layer in place of a sigmoid layer.

**Training and Evaluation**

Model were trained on the same dataset and whole dataset was utilized for Training. Optimal epochs were determined, and validation accuracy was monitored to avoid overfitting. Various evaluation metrics were employed to assess system performance. The Training was visualized on TensorBoard.
![epoch_categorical_accuracy](https://github.com/Arpit-Avasarmol/Live-Human-Sign-Detection-with-Real-Time-Streaming-Data-using-MediaPipe-Holistic-Model-and-OpenCV/assets/88440241/02fa0fec-26fe-4472-a988-a5f0d3b3c6fc)

https://github.com/Arpit-Avasarmol/Live-Human-Sign-Detection-with-Real-Time-Streaming-Data-using-MediaPipe-Holistic-Model-and-OpenCV/assets/88440241/5b7a4afd-c872-4c24-836d-9e20cd8b99b7

**Results**
The proposed system achieved high precision and performed well in sign language recognition tasks. The LSTM model excelled on the gesture sign language dataset, demonstrating the versatility of models.



https://github.com/Arpit-Avasarmol/Live-Human-Sign-Detection-with-Real-Time-Streaming-Data-using-MediaPipe-Holistic-Model-and-OpenCV/assets/88440241/d3456707-07c8-446c-8fca-af2135bfe3a8






**Output**
MediaPipe Holistic generates a set of key points or landmarks representing the pose, hand, and face of the individual in the video frame.
![test1](https://github.com/Arpit-Avasarmol/Live-Human-Sign-Detection-with-Real-Time-Streaming-Data-using-MediaPipe-Holistic-Model-and-OpenCV/assets/88440241/76cae28a-2945-4f3d-9551-ce9a647e80fe)
![test2](https://github.com/Arpit-Avasarmol/Live-Human-Sign-Detection-with-Real-Time-Streaming-Data-using-MediaPipe-Holistic-Model-and-OpenCV/assets/88440241/6c1ef064-0d1a-48db-8480-28331a152bee)

![test3](https://github.com/Arpit-Avasarmol/Live-Human-Sign-Detection-with-Real-Time-Streaming-Data-using-MediaPipe-Holistic-Model-and-OpenCV/assets/88440241/2187f0cf-802d-4a5b-be52-9e079fcae766)
