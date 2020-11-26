# FaceMaskDetection_CNN_openCV

![alt text](outputFile.gif?raw=true)

### COVID-19: Face Mask Detector with #OpenCV #Keras #TensorFlow and #deeplearning #covid 

A high-level explanation of how it works:
##### ⨷Training:  Load the data set for face mask recognition (with mask and without mask image samples) from the local disk. I then trained a model (using Keras / TensorFlow) on this dataset and then serialized the face mask detector to disk.

##### ⨷Deployment: Once the face mask detector is trained we can proceed to loading the mask detector model. I then perform face detection, and then classify each face as with_mask or without_mask.

Detailed steps:
1.	Load the dataset
2.	Perform data augmentation
3.	Split the data set 
4.	Build the model – I build the Sequential CNN model with various layers such as Conv2D, MaxPooling2D, Flatten, Dropout and Dense. In the last Dense layer, we use the ‘softmax’ function to output a vector that gives the probability of each of the two classes.
5.	Pre-Training the CNN model using Keras and Tensorflow.
6.	Training the CNN model – I trained the model for 40 epochs
7.	Labeling the Information - after building the model, we have two probabilities for the results. [‘0’ as ‘without_mask’ and ‘1’ as ‘with_mask’] and I also color coded the output - [‘RED’ for ‘without_mask’ and ‘GREEN’ for ‘with_mask]
8.	Import the Face detection program - I am using the Haar Feature-based Cascade Classifiers for detecting the features of the face.
