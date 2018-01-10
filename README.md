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

# Final model Validation Accuracy is 0.959

# Test a Model on New Images
I considered seven German traffic signs found on the web and detected very well,

image1.png:
No entry: 100.00%
Speed limit (70km/h): 0.00%
Speed limit (20km/h): 0.00%
Speed limit (30km/h): 0.00%
Speed limit (50km/h): 0.00%

image2.png:
Yield: 100.00%
Priority road: 0.00%
No passing for vehicles over 3.5 metric tons: 0.00%
Speed limit (50km/h): 0.00%
Ahead only: 0.00%

image3.png:
No entry: 99.75%
Speed limit (30km/h): 0.17%
Speed limit (50km/h): 0.05%
Speed limit (70km/h): 0.04%
Beware of ice/snow: 0.00%

image4.jpg:
No entry: 100.00%
Speed limit (20km/h): 0.00%
Speed limit (30km/h): 0.00%
Speed limit (50km/h): 0.00%
Speed limit (60km/h): 0.00%

image5.png:
Stop: 100.00%
No entry: 0.00%
No passing for vehicles over 3.5 metric tons: 0.00%
No passing: 0.00%
Speed limit (20km/h): 0.00%

image6.png:
Speed limit (70km/h): 96.07%
Speed limit (50km/h): 3.93%
Speed limit (30km/h): 0.01%
Dangerous curve to the left: 0.00%
Speed limit (80km/h): 0.00%

image7.png:
Keep right: 100.00%
Turn left ahead: 0.00%
Roundabout mandatory: 0.00%
Go straight or left: 0.00%
Yield: 0.00%

# Conclusion:
1. learning rate is a key factor to train the model accurately.  



