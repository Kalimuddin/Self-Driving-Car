# Steering wheel angle prediction using Deep Learning

## Problem Definition and Data Requirements :

- In simplified minimal version, we have total 45406 sequence of images (25 minutes of video) with the corresponding Steering wheel angles as a Dataset.
- Primary Objectives are to learn the Deep Learning techniques and by applying them Predict the Sequence of Steering wheel angles.
- We choosed end to end model in which we predict Steering wheel angle for each single images. And for visualizing the output OpenCV is used.
- Required Data available at : https://drive.google.com/drive/folders/1JviaSKSBVP4z22Y5gyfwjRz-UH2C0d1q?usp=sharing

- Split the dataset : Train vs Test :-
    - 80% : 20%
    - 25min : 5min
- Sequence of images -> Sequence of Steering wheel angle (regression problem)
- Dash-cam images :

![1](https://user-images.githubusercontent.com/54996809/155126005-0c5557c2-54a7-4d70-8010-00ab4e14b4f0.png)

## EDA :

- read images and steering angles from driving_dataset folder : train_y, test_y
- plotting : we seen, train_y and test_y are not fully overlap, some difference in train & test.
- Most of the case car go straight thats why we see that angle (radian) are around zero.

![2](https://user-images.githubusercontent.com/54996809/155775385-95c5f213-cef5-4ba2-b481-6f3968dc5694.png)

## Modelling :

- Deep-learning model : Deep Learning for regression :
    - Case-1 : not using the sequence information : image -> predict the angle (simple CNN)
    - Case-2 : images + sequence -> angle + sequence (CNN-RNN)

- Preparing the dataset : 
    - Refer : "driving_data.py"

- End to End CNN model : 
    - Refer "model.py"
    - We implement Network Architecture already designed from nvidia Self-Driving Cars model.
 
- Train the model :
    - It takes few hours to successfully run the code for low end cpu/gpu.
    - After training the model, model is saved in "save" folder as "model.ckpt"

## Test and visualize the output :
- The Steering wheel is rotatating as per predicted Steering wheel angle (in radian) :

https://user-images.githubusercontent.com/54996809/155835330-fff1d307-6fa8-4224-8da1-623cfc591f3f.mp4


