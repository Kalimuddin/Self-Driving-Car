# Self-Driving-Car

## Problem Definition and Data Requirements :

- In simplified minimal version, we have total 45406 sequence of images (25 minutes of video) with the corresponding Steering wheel angles as a Dataset.
- Primary Objectives are to learn the Deep Learning techniques and by applying them Predict the Sequence of Steering wheel angles.
- We choosed end to end model in which we predict Steering wheel angle for each single images. And for visualizing the output OpenCV is used.
- Required Data available at : https://drive.google.com/drive/folders/1JviaSKSBVP4z22Y5gyfwjRz-UH2C0d1q?usp=sharing
- 
- Split the dataset : Train vs Test :-
    - 80%:20%
    - 25min:5min
- Sequence of images -> Sequence of Steering wheel angle (regression problem)

## EDA :

- read images and steering angles from driving_dataset folder : train_y, test_y
- plotting : we seen, train_y and test_y are not fully overlap, some difference in train & test

![2](https://user-images.githubusercontent.com/54996809/154904867-d2027431-7a66-4de0-9892-6536d95c9fdf.png)

## Modelling :

- Deep-learning model : Deep Learning for regression : CNN, CNN+RNN :-
    - Case-1 : not using the sequence information : image -> predict the angle (simple CNN)
    - Case-2 : images + sequence -> angle + sequence (CNN+RNN)

- Batch load the dataset :- Refer "data.txt", driving_data.py

- NVIDIA’s end to end CNN model :- Refer model.py
 
- Train the model :- Refer train.py

- Test and visualize the output : Refer run_dataset.py






