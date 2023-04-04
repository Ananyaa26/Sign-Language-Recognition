# Sign-Language-Recognition

***Sign Language*** encompasses the movement of the arms and hands as means of communication for people with hearing disabilities

Deep Learning has networks capable of learning unsupervised data that is unstructured known as a deep neural network.

The ***vision-based approach*** used focuses on the detection of particular features and the categorization of particular input data.

# Dataset

We have used the Indian Sign Language dataset the Indian Sign Language Research and
Training Center provided. The dataset contains an extensive vocabulary of 10,000 fully
annotated videos of words with their signs recorded by multiple signers. There are some
technical terms, Legal terms, standard used terms, and Academic and Agricultural terms. The
video lengths range from 0.38 to 8.04 seconds, and the mean length of all the videos is 2.45 sec.
All the videos are processed into the same format (.mp4).

🔗 [ISL Dataset-Google Drive Link](https://drive.google.com/drive/folders/1XLxGQVn2AR6APGsoHnN_RxFxD63PO9hU?usp=sharing)

# Methodology

1. Extracting MediaPipe Holistic Key Points

2. Building a Sign Language model using an Action Detection powered by LSTM layers(i.e.,
Training a deep neural network with LSTM layers for sequences)

3. Predicting sign language in real-time using video sequences/OpenCV

<img width="850" alt="image" src="https://user-images.githubusercontent.com/89255668/229807227-426ce89c-394c-420e-8b96-9493c30ff619.png">

# Data Preprocessing

Real-world data is sometimes incomplete, inconsistent, redundant, and noisy. So, Data
Preprocessing is the process of simply transforming raw data into an understandable format.
This involves various steps that help to convert raw data into a processed and sensible format.
The step-by-step process of the techniques applied to the data for preprocessing can be understand with help of the flowchart—

<img width="150" alt="image" src="https://user-images.githubusercontent.com/89255668/229815216-151e579f-c218-4625-92ce-80297529ca97.png">

Extracting and isolating the frames in real time in order to map key-points on face,hands and shoulder to produce output based on a probability statistic bar.

# The Model

## MediaPipe Holistics
The MediaPipe Holistic pipeline integrates separate models for pose, face and hand components, each of which are optimized for their particular domain. 

On opening the webcam,it captures the landmarks point of face, hands, shoulders, hip and legs.

The video movement is captured in form of sequences of frames,which is used to train the LSTM Model and predict the sign language.

<img width="500" alt="image" src="https://user-images.githubusercontent.com/89255668/229803065-f945e78d-d147-4dda-99d2-1f7e45fc4d49.png">


## LSTM Neural Network

An **LSTM (Long Short-term Memory) Neural Network** is a type of Artificial Neural Network
that contains LSTM cells as neurons in some layers. The input in this model is a feature vector,
and each subsequent layer is a set of "neurons." Each neuron applies an affine (linear)
transformation to the output of the previous layer, followed by some non-linear function.The
neurons' output, a new vector, is fed to the next layer, and so on. A dropout layer is intended to
reduce the model's overfitting to the training data. The features extracted by the LSTM hidden
layer are then interpreted by a dense, fully connected layer before being used to make
predictions by a final output layer.

**Step-1** Tensorflow and Keras Dependencies were used to Build the LSTM Model.

**Step-2** The NN architecture by adding 3 layers of LSTM through Sequential Model.

**Step-3** The sequences of frames captured from videos get trained here.

**Step-4** The compilation of it was done by loss function and Adam Optimizer.



# Prediction and Accuracy

The summary of our Model—

<img width="450" alt="image" src="https://user-images.githubusercontent.com/89255668/229802358-bff24e0a-cc34-46b0-9f5a-ee5992259b5e.png">

***RESULT:Predicting the signs,the model works with 94% Accuracy***



