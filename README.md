# YOLOv8-Seg Wheat Head Detection


# Training

YOLOv8m-seg (yolov8m-seg.pt) was trained for 10 epochs. 
Follow this link to view the training script: https://colab.research.google.com/drive/1-iTP2w05qlLizFjPJWGrLWPu-mL4y4Ng#scrollTo=6FUlqegxq2SN

# Dataset
The Global Wheat Head Detection (GWHD) Dataset is contains wheat head images from several countries at different growth stages with a variety of genotypes. 

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

# SAM BBoxes to Masks
The Segment Anything Model is an image segmentation model with zero shot capabilties.
It was used to convert the bounding boxes of the GWHD into masks.
Follow this link to view the code: https://colab.research.google.com/drive/1qq2hd4isNUniNDoVW0uNeTmN_eY0qICR

# Repository Explanation

## Images
All of the repository's images can be found in the "imgs" directory with two sub-folders.

##### "example_train_imgs" folder
 * Example training image
 * Each set of images has an original and color augmented image

#### "predictions" folder
 * Examples of test images and YOLOv8-Seg predictions 
 * Four types of images
  * orig - original image of the test image
  * ground_truth - test image with ground truth masks (green)
  * predictions - test image with ground truth masks (green) and YOLOv8-Seg predictions (red)
  * predictions with numbers - test image with ground truth masks (green), YOLOv8-Seg predictions (red), and a number for each wheat head ground truth
