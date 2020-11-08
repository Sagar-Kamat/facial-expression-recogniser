# Facial-Expression-Recogniser

Dataset: https://www.kaggle.com/c/challenges-in-representation-learning-facial-expression-recognition-challenge
The data consists of 48x48 pixel grayscale images of faces. The objective is to classify each face based on the emotion shown in the facial expression into one of seven categories (0=Angry, 1=Disgust, 2=Fear, 3=Happy, 4=Sad, 5=Surprise, 6=Neutral). The training set consists of 28,709 examples. This dataset was prepared by Pierre-Luc Carrier and Aaron Courville, as part of an ongoing research project.

# Details of model:
First the training data is augmented by flipping the images horizontally. A CNN model consisting of 4 convulutional layers is created. Conv2D, Batch Normalisation, ReLU activation function, MaxPooling and a Dropout of 0.25 is applied on each layer. The Sequential model uses Adam optimizer and categorical cross entropy as the loss function.

# Training the model:
The model is trained for 15 epochs. On completion of each epoch, the accuracy and log-loss of the training and validation set is printed. The model is saved in the model.h5 file, which is then converted into JSON, for further use.
At the end of the final epoch, the accuracy of the training and validation sets comes out to be approximately 65% and 60% respectively.

# Using OpenCV:
After training the model and saving it as JSON, it is then fed to the OpenCV code, that returns camera frames, bounding boxes and predictions for each live image.

# Using Flask:
The output of the OpenCV model is presented to a web interface using Flask to perform real-time facial expression recognition on video and image data.

You can check out the demo videos on real time face emotion recognition (real time.mp4) or you can choose any video of your choice. 

Peace out. ✌
