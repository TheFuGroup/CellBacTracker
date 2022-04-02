# CellBackTracker - A Flexible Automated Cell Tracking and Lineage Construction Tool
Developed by Yu Fang and The Fu Lab

# Overview
The repo includes the link to downloads the model pretrained weights and the tracking script. The instance segmentation Mask-Rcnn model was trained on 600*600 segmented Hela images. The Normalizing Mean and Standard deviation of the model is calculated based on our training dataset. 

# Runnig The Code
## Installation
You'll need to install the following packages (possibly more):

```
opencv math numpy matplotlib sklearn torch PIL
```

In particular, the code has been tested with Python 3.7.12 and Pytorch 1.10.0 running on a single GTX 2060 GPU. 

I suggest to use anaconda to create vitual environment. Please visit anacondas page for more info.

## Pretrained Weights
Pre-Trained Model is a Mask Rcnn. The link of downloading the model is in model/models.ipynb

## Tracking cell instances
Tracking and lineage construction script is CellBacTracker.ipynb. The script currently supports a multi-frames TIF format as a video source. Notice that the tracking performance is dependent of segmentation prediction. So please retrain or tuning the models based on your training dataset. The current RESNET_MEAN and RESNET_STD are calculated through our training dataset. Please recalculate them before retraining.

## Save plots
The current algorithm will calculate the instensity of cells through the TIF Image. This function can be customized to any research goal as long as it can be calculated by bounding box position, binary mask and original image. 

# Issues
If there are any issues with the repository or process, please message Yu Fang at fangy35@uw.edu.