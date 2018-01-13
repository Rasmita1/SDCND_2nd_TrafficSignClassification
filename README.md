# SDCND_2nd_TrafficSignClassification

# The goals / steps of this project are the following:
* Load the data set from the provided link in the classroom
* Design, train and test a model architecture
* Use the model to make predictions on new images
* Analyze the softmax probabilities of the new images
* Summarize the results with a written report

I could not commit the training and testing file in the samples folder as the file sizes are big. These files are available in the classroom link.

# Basic summary of the data set:
- Number of training examples = 34799
- Number of validation examples = 4410
- Number of testing examples = 12630
- Image data shape = (32, 32, 3)
- Number of classes = 43

# To train the model: 
Used 15 epochs, a batch size of 128 and a learning rate of 0.003.

# Design and Test a Model Architecture
Normalization is generally considered for data preparation in machine learning. Here Normalizing features is used to have values in the same range (between -1 and 1) to use a common scale, without distorting differences in the ranges of values or losing information.

The summary of Model Architecture:

Layer 1: Convolution 1. Input = 32x32x3. Output =28x28x6 ->relu activation -> Pooling. Input = 28x28x6, Output =14x14x6
Layer 2: Convolution 2. Output =10x10x16 ->relu activation -> Pooling. Input = 10x10x16, Output =5x5x16
Layer 3: Fully Connected. Input =400. Output =120 ->relu activation
Layer 4: Fully Connected. Input =120. Output =84 ->relu activation
Layer 5: Fully Connected. Input =84. Output =43


Used 15 epochs, a batch size of 128 and a learning rate of 0.003.
I Used the LeNet architecture presented in the lesson and made the neccssary modification. Traffic sign images are in color, so changed the input depth to 3 to match the 3 RGB color channels and changed the output classes to 43 as traffic sign classifier has 43 classes. Then I Used softmax_cross_entropy_with_logits to get a tensor representing the mean loss value to which I applied tf.reduce_mean to compute the mean of elements across dimensions of the result. Finally, applied minimize to the AdamOptimizer of the previous result.

 I tried several combinations learning rate to get more accurate result.Final model accuracy is 0.962.  

# Test a Model on New Images
Now I considered new set of six German traffic signs found on the web. The model performs well on images in the dataset. Here the model detected all images except the last image, because the sign is dark and  not visible clearly.

Here are the results of the prediction:

| Image			          |     Prediction	        					|   Remarks
|:---------------------:|:---------------------------------------------:|
| No entry       		  | No entry   									|
| General caution     | General caution 										|
| Speed limit (60km/h)| Speed limit (60km/h)							|
| End of speed limit (80km/h)	| End of speed limit (80km/h)	|
| Wild animals crossing  			| Wild animals crossing				|
| Speed limit (70km/h)	| Speed limit (30km/h)							|
| Speed limit (100km/h)			| Speed limit (120km/h)					| Image is not clear. Hence, it was hard to predict accurately


image1.png:
No entry: 100.00%
Stop: 0.00%
Speed limit (20km/h): 0.00%
Speed limit (30km/h): 0.00%
Yield: 0.00%

image2.png:
General caution: 100.00%
Traffic signals: 0.00%
Go straight or left: 0.00%
Speed limit (70km/h): 0.00%
Pedestrians: 0.00%

image3.png:
Speed limit (60km/h): 100.00%
Speed limit (80km/h): 0.00%
Speed limit (50km/h): 0.00%
No passing for vehicles over 3.5 metric tons: 0.00%
Dangerous curve to the left: 0.00%

image4.png:
End of speed limit (80km/h): 92.41%
Speed limit (80km/h): 3.75%
Speed limit (30km/h): 1.39%
Dangerous curve to the right: 0.92%
End of no passing by vehicles over 3.5 metric tons: 0.49%

image5.png:
Wild animals crossing: 100.00%
Double curve: 0.00%
Road work: 0.00%
Slippery road: 0.00%
Speed limit (80km/h): 0.00%

image6.png:
Speed limit (120km/h): 65.93%
Speed limit (70km/h): 10.66%
Speed limit (80km/h): 8.69%
Speed limit (100km/h): 5.01%
No vehicles: 1.95%

# Conclusion:
1. The model correctly predicted all the images except the last image.
  



