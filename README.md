# Real-Time Chicken Counting using YOLOv8

This repository contains a real-time computer vision system for automatic chicken counting in poultry farms using YOLOv8. The project aims to support large-scale farm management by providing accurate, efficient, and automated flock monitoring.

## 1. Project Overview

- Task: Detect and count chickens in images and videos from farm environments.
- Motivation: Traditional manual counting is time-consuming, error-prone, and impractical for large farms.
- Solution: Use YOLOv8 for real-time object detection, combined with a simple counting logic on detection results.

## 2. Key Features

- YOLOv8-based object detection for chicken counting.
- Real-time inference on images, videos, or webcam streams.
- Support for training on custom datasets in YOLO format.
- Visualization of detection results with bounding boxes and total count overlay.
- Optional semi-supervised and active learning loop to reduce annotation workload.

## Data

Format: YOLO-style dataset with images/ and labels/ folders.
Each label file contains bounding boxes for chickens in the image.
Recommended image size: 640x640.
Tools: Roboflow or CVAT can be used for annotation.

The dataset is not included in this repository. Please prepare your own dataset and update data/chicken.yaml accordingly.

Example data/chicken.yaml:

path: ./data/chicken
train: images/train
val: images/val

nc: 1
names: ["chicken"]
