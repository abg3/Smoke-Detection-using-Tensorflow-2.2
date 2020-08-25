# Smoke-Detection-using-Tensorflow 2.2

## Author: Abhishek Ghosh, Moumita Mukherjee

# Team

#### Team Name- Project Skylab
#### Team Members- Kaniska Mandal(Mentor), Abhishek Ghosh, Moumita Mukherjee

# *Wildfire Smoke Detector*

In this repostiory, we implement The TensorFlow 2 Object Detection Library for training on our own dataset.

Our goal is to develop a wildfire smoke detector which will help California respond to wildfire concerns as quickly as possible. This is the submission project for [Lets Stop Wildfires Hackathon 2.0](https://aiformankind.org/lets-stop-wildfires-hackathon-2.0)

# Dataset

We will use 733 annotated smoke images. The training, validation and testing dataset is divided in the ratio 7:2:1 i.e. 513 images for training, 147 for validation and 73 images for testing. We would like to acknowledge [AIforMankind](https://github.com/aiformankind/wildfire-smoke-detection-camera) for providing this dataset.

We have used [Roboflow](https://roboflow.com) which is used to label the data, apply image preprocessing, data augmentation, generate TF Records and many other useful techniques in machine learning. We would also like to thank Roboflow for the excellent tutorials.

# Implementation

We will take the following steps to implement Tensorflow 2 object detection model on our smoke dataset-

1. Install TensorFlow2 Object Detection Dependencies
2. Download Smoke Images Dataset and necessary files
3. Write your own TensorFlow2 Object Detection Training Configuration
4. Train Custom TensorFlow2 Object Detection Model
5. Export Custom TensorFlow2 Object Detection Weights
6. Use Trained TensorFlow2 Object Detector For Inference on Test Images
7. Save your model for future applications

For best understanding and convenience, we recommend starting with the notebook in this repository using Google Colab. You will find step by step execution. Please follow along and avoid skipping any step. 

# Files

1. [Training Notebook](https://colab.research.google.com/drive/1KWNgx33jwsWssn6oxunm1EUoOx64KrL6?usp=sharing)
2. [Inference Notebook](https://colab.research.google.com/drive/1OVuBK3JoOKsf74MJOUSUZLFXMGeHQJ-5?usp=sharing)

# End Product

If you would like to head straight and make inference using our trained model, we have the saved_model.pb file under fine_tuned_model for quick access. We also have the  pipeline config file under this folder which was used to train our model. We have used cyclical learning rate optimization to yield better results. 

# Our Model

Our model is trained EfficientDet-D0, which is a state of the art object detection model. You will find EfficientDet useful for real time object detection. EfficientDet has an EfficientNet backbone and a custom detection and classification network. EffcientDet is designed to efficiently scale from the smallest model size. The smallest EfficientDet, EfficientDet-D0 has 4 million weight parameters - which is truly tiny. EfficientDets are developed based on the advanced backbone, a new BiFPN, and a new scaling technique:

* Backbone: we employ EfficientNets as our backbone networks.
* BiFPN: we propose BiFPN, a bi-directional feature network enhanced with fast normalization, which enables easy and fast feature fusion.
* Scaling: we use a single compound scaling factor to govern the depth, width, and resolution for all backbone, feature & prediction networks.

![image](https://github.com/google/automl/blob/master/efficientdet/g3doc/network.png)

[Read this paper to know the architecture in detail](https://arxiv.org/abs/1911.09070)

## Inferences and Results

# Wildfire Smoke Detector

## True Positives

1. 

![smokey](https://user-images.githubusercontent.com/61203589/90588540-79f05800-e1a1-11ea-8fd1-54dbe8170a68.gif)

2. 

![smokey2](https://user-images.githubusercontent.com/61203589/90589985-051f1d00-e1a5-11ea-9f94-a06bb98ad19e.gif)

3. 

![smokey3](https://user-images.githubusercontent.com/61203589/90589995-081a0d80-e1a5-11ea-8699-6cfa9a3a65fe.gif)

4.

![smokey4](https://user-images.githubusercontent.com/61203589/90590551-7a3f2200-e1a6-11ea-8d5a-9d16297b0788.gif)

5. 

![smokey5](https://user-images.githubusercontent.com/61203589/90666480-156de100-e213-11ea-856c-fcf7ee1fae4b.gif)

6.

![smokey6](https://user-images.githubusercontent.com/61203589/90666481-156de100-e213-11ea-98f1-de6949c99536.gif)

## False Positives
1.


![Falsepos1](https://user-images.githubusercontent.com/61203589/90985991-3ac95a80-e545-11ea-9573-334818c7a020.png)

2.


![Falsepos2](https://user-images.githubusercontent.com/61203589/90986035-9dbaf180-e545-11ea-8b5d-4b807807c8b0.png)

# Acknowledgement

We would like to thank HPWREN, AIForMankind, Google Tensorflow and Google Brain for the continuous support in this research project.

# References

1. https://github.com/google/automl/tree/master/efficientdet
2. https://github.com/tensorflow/models/tree/master/research/object_detection

# Next Steps
1. Try out different model architectures and scale your model
2. Try to reduce the loss further and improve upon accuracy
3. Test your model on varying set of smoke images
4. Build an app using TFLite and deploy the application
