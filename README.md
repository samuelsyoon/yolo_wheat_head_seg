# YOLOv8-Seg Wheat Head Detection


# Training

YOLOv8m-seg (yolov8m-seg.pt) was trained for 10 epochs.

# Dataset
The Global Wheat Head Detection (GWHD) Dataset is a diverse dataset for wheat head detection. The wheat head images are collected from different countries at different growth stages with a variety of genotypes. 

Follow the link to below to view and download the dataset images.

https://universe.roboflow.com/23-cv-for-pa/gwhd_kaggle_instance_segmentation_3.0

In the Universe Dataset Repository, there are three versions:

* v1 - original GWHD
  * No augmentations

* v2 - data augmentations
  * Flip: Horizontal
  * 90° Rotate: Clockwise, Counter-Clockwise
  * Rotation: Between -15° and +15°
  * Shear: ±10° Horizontal, ±10° Vertical
  * Hue: Between -15° and +15°
  * Saturation: Between -25% and +25%
  * Brightness: Between -15% and +15%
  * Exposure: Between -10% and +10%
  * Blur: Up to 2.5px
 
* v3 - color augmentations
  * Hue: Between -15° and +15°
  * Saturation: Between -25% and +25%
  * Brightness: Between -15% and +15%
  * Exposure: Between -10% and +10%
