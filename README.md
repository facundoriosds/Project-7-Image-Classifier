## Gender Detector 

### Project Overview
* Produced an Image Classification model for detecting if the person in an image is male or female using a Convolutional Neural Network Model and Transfer Learning, obtaining 97% accuracy. 
* Implemented Transfer Learning using Inception-v3, optimized with learning rate schedulers.
* Directories design and images loading.
* Analized models errors.

### Code and Resources Used 
**Python Version:** 3.7  
**Packages:** pandas, numpy, matplotlib, seaborn, plotly, sklearn, tensorflow, keras.

### Dataset
Was developed by Hong Kong University Multimedia Laboratory and originally has 202599 images of celebrities faces and 40 binary attributes annotations per image in a different folder.  
A balanced smaller set with 40000 images was made for computing power and time execution reasons, with the gender attribute as label.

Dataset: https://www.kaggle.com/datasets/jessicali9530/celeba-dataset

<!-- ![](images/capture_1.PNG)
![](images/capture_2.PNG)
![](images/capture_3.PNG) -->

### Data preparation
Images were assigned to its corresponding gender attribute and directories were created to divide the images by gender and then in train/test sets.
With the images loaded in an organized folder structure, data was prepared for the models training using ImageDataGenerator of the keras preprocessing module.

### Models Building and Performance
Two models were trained: a baseline CNN model with its learning rate tuned with the use of an scheduler and RMSprop optimizers, and a second CNN using the Inception v3 architecture loaded with weights pre-trained on ImageNet, also tuned with a scheduler.

* **CNN**: Accuracy=0.96.
* **CNN-Inception**: Accuracy=0.97.

### Metrics Chosen
**Accuracy** was considered a reliable metric  given that we had a perfectly balanced dataset.

---