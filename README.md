# Smoke-Detection-using-Tensorflow 2.2

## Author: Abhishek Ghosh, Moumita Mukherjee

# *Wildfire Smoke Detector*

In this repostiory, we implement The TensorFlow 2 Object Detection Library for training on our own dataset.

Our goal is to develop a wildfire smoke detector which will help California respond to wildfire concerns as quickly as possible.

We will use 733 annotated smoke images. The training, validation and testing dataset is divided in the ratio 7:2:1 i.e. 513 images for training, 147 for validation and 73 images for testing. We would like to acknowledge HPWREN and AIforMankind for providing this dataset.

We have used Roboflow AI which is used to label the data, apply image preprocessing, data augmentation, generate TF Records and many other useful techniques in machine learning. We would also like to thank RoboFlow AI for the excellent tutorials.

We will take the following steps to a implement Tensorflow 2 object detection model on our smoke dataset-

1. Install TensorFlow2 Object Detection Dependencies
2. Download Smoke Images Dataset and necessary files
3. Write your own TensorFlow2 Object Detection Training Configuration
4. Train Custom TensorFlow2 Object Detection Model
5. Export Custom TensorFlow2 Object Detection Weights
6. Use Trained TensorFlow2 Object Detector For Inference on Test Images
7. Save your model for future applications

For best understanding and convenience, we recommend starting with the notebook in this repository using Google Colab. You will find step by step execution. Please follow along and avoid skipping any step. 

# End Product

If you would like to head straight and make inference using our trained model, we have the saved_model.pb file under fine_tuned_model for quick access.

## Inferences and Results

# Wildfire Smoke Detector

1. 

![smokey](https://user-images.githubusercontent.com/61203589/90588540-79f05800-e1a1-11ea-8fd1-54dbe8170a68.gif)

2. 

![smokey2](https://user-images.githubusercontent.com/61203589/90589985-051f1d00-e1a5-11ea-9f94-a06bb98ad19e.gif)

3. 

![smokey3](https://user-images.githubusercontent.com/61203589/90589995-081a0d80-e1a5-11ea-8699-6cfa9a3a65fe.gif)

4.

![smokey4](https://user-images.githubusercontent.com/61203589/90590551-7a3f2200-e1a6-11ea-8d5a-9d16297b0788.gif)

