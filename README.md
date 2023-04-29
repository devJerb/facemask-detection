# Facemask Detection using Custom Dataset on YOLOv7
On this project, it is a facemask detection tool using a state-of-the-art object detection model called [YOLOv7](https://github.com/WongKinYiu/yolov7) using a custom dataset. This mainly revolves towards the utilization of [Google Colab](https://colab.research.google.com/)'s free GPU usage for training a bulk dataset though changing the source file to be detected using webcam is disabled due to conflicts.

## Dataset
The dataset used in the project is available on [Kaggle](https://www.kaggle.com/datasets/andrewmvd/face-mask-detection). This dataset contains 853 images belonging to 3 classes (with, without, and incorrect), as well as their annotated files in PASCAL VOC format compatible for converting to YOLO format.

## Installation
Found on the repository is a [.ipynb](https://github.com/devJerb/facemask-detection/blob/main/facemask_detection.ipynb) file containing the set of instructions in order to run the facemask detection model.

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

## Conclusion
The project was to demonstrate the usage of a custom dataset for YOLOv7 model on facemask detection made on Google Colab.
