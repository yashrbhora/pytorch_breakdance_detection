# Breakdance Freeze/Powermove Object Detection

### Current Model Status (Sep 30, 2022):
- Airchair trained using poor training set.

This project aims to train breakdancing powermoves (windmills, flares, airflares, etc.) and freezes (airchair, baby-freeze, headstand, etc.) to the pre-trained [*Ultralytics YOLOv5*](https://github.com/ultralytics/yolov5) via transfer-learning.

The motivation for this project comes from:
- I'm a breakdancer myself
- There are various styles of powermoves/freezes
   - Creating a rating system for these moves would quantify the quality of these moves for breakdancers.
- It allows me to utilize the skills I garnered from [Andrew Ng's Machine Learning Specialization Coursera Course](https://www.coursera.org/specializations/machine-learning-introduction).

The model was trained on the [Discovery High Performance Computing Cloud Cluster](https://rc.northeastern.edu/) to leverage Northeastern University's access to GPUs.
- Training was initially attempted using Tensorflow on the SSD Mobilenet FPNLite model.
- However, due to tensorflow not detecting Discovery GPUs, the model was trained on PyTorch using the *YOLOv5* model.

The training set was webscraped off Google Images using **Selenium** and then manually labeled and filtered using [labelImg](https://github.com/heartexlabs/labelImg).

Although data augmentation was not necessary because data is pre-processed when training, for learning purposes, the images were augmented using the **Augmentor** library.
