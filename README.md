# Masked Face Classification

## About Masked Face Classification
This web-based application is developed to classify two classes of people's faces: wearing mask and not wearing mask.

### Project Goal
To accurately identify whether a person is wearing mask or not.
Further goal: To help monitor compliance of people wearing mask in public places.

### Possible Implementation

Since monitoring compliance is expensive and time consuming, this mask classification project can be deployed further for a real-time masked/unmasked face recognition in CCTV surveillance system to help government enforce the regulation of wearing mask in public places. Hence, the system can help contribute to suppress the spread of coronavirus in Indonesia.

## Dataset
The dataset used in this project is from: 
* [Prajnasb](https://github.com/prajnasb/observations/)

## Model Building

### Baseline model
* Using basic CNN (3 Convolution and 3 Pooling):
* Adding Augmentation of rotation: 0 – 40°, width shift: 0 – 20%, height shift: 0 – 20%, shear: 0 – 20%, zoom: 0 – 20%, fill mode: nearest, and horizontal flip.

### Improvement
We choose transfer learning (MobileNetV2) as our improvement because the dataset is considered small and it supports Faster Learning.

### Result
The time for training reduced from 16-17s to 14-15s per epoch. 
|               | Training      | Validation  |
| ------------- |:-------------:| -----------:|
| Accuracy      | 0.924         | 0.975       |
| Loss          | 0.2118        | 0.062       |

Even though the accuracy was a bit lower, and loss was higher than baseline model. The result from our manually collected Test Images is better.

You can download our Test Images [here](https://drive.google.com/file/d/1Na4YrEI1W-F75qIsz-6QhKehATeH-POz/) (or [centered ver.](https://drive.google.com/file/d/1sQoxVUmCXWbIfZQT-lkCVNqMIDJH69Dr/))

## Deployment 
This model is a web-based and deployed in [Github Pages](https://hoboroots.github.io/masked_face_classification).
You can select an image of a face that having mask on it or not, and click Predict button, the wait for the result.

## Reproduction

These instructions will get you a copy of the project up and running on your local machine for development, testing, and deployment purposes. 

### Prerequisites

The things you need to install and how to install them

```
git clone url_of_this_repo
```

### Installing

This project can be run with any of web servers available. 

For development/testing, you can run locally with your web server or if you run in a Visual Studio Code editor, you can install Live Server plugin, then right-click index.html file, choose Open with Live Server.

For deployment, you can use Apache, Nginx, or any web servers to deliver web pages to your user's browser. 

## Presentation

For more details about this project, you can find it in this [Slide](https://docs.google.com/presentation/d/1lhoT7nwMqcDaze_fCHscIxv8dQY-PGUUmW9yoF_b6wo/).

### Authors

This project is to fulfill final assignment of Bangkit Program.
> Team member: Emma Suryani and Handaru Sandy
