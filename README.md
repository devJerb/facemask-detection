# Facemask Detection using Custom Dataset on YOLOv7
On this project, it is a facemask detection tool using a state-of-the-art object detection model called [YOLOv7](https://github.com/WongKinYiu/yolov7) using a custom dataset, the [paper](https://arxiv.org/pdf/2207.02696.pdf) explaining the model architecture. This mainly revolves towards the utilization of [Google Colab](https://colab.research.google.com/)'s free GPU usage for training a bulk dataset though changing the source file to be detected using webcam is disabled due to conflicts.

![yolov7-comparison](https://assets.website-files.com/5f6bc60e665f54db361e52a9/637f2a024b36bcd05e4f9baa_performance.png)

The figure shown above is an evaluation of other YOLO version models compared to YOLOv7's model on inference (x-axis) and accuracy (y-axis). 

## Dataset
The dataset used in the project is available on [Kaggle](https://www.kaggle.com/datasets/andrewmvd/face-mask-detection). This dataset contains 853 images belonging to 3 classes (with, without, and incorrect), as well as their annotated files in PASCAL VOC format compatible for converting to YOLO format.

## Installation
Found on the repository is a [.ipynb](https://github.com/devJerb/facemask-detection/blob/main/facemask_detection.ipynb) file containing the set of instructions in order to run the facemask detection model.

You can clone the repository to your local machine

`git clone https://github.com/<username>/facemask-detection.git`

1. Content found on `masks.yaml` placed inside the directory of /data.
```
train: ./train
val: ./val
test: ./test
 
# Classes
nc: 3  # number of classes
names: ['with_mask', 'without_mask', 'mask_weared_incorrect']
```

2. `yolov7-masks.yaml` copied from the yolov7.yaml found in yolov7/cfg/training; the only changed value are the number of classes to be detected.
```
# parameters
nc: 3  # number of classes
```
