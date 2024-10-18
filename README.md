# What-you-should-know-about-nuScenes

The nuScenes dataset is one of the most widely used large-scale public datasets in the autonomous driving research community. For those new to the field, having a concise overview of what the nuScenes dataset offers and guidance on how to explore and experiment with it can be incredibly valuable. Unfortunately, there is a lack of dedicated quick-start guides, leaving beginners to figure out how to navigate the dataset independently. Hence, I am writing this document to provide a clear and concise guide, aimed at easing the learning curve for beginners. This guide will help you quickly understand the key features of the nuScenes dataset and offer practical steps to effectively explore and experiment with it, so you can get up to speed in the autonomous driving research community.

## Download:
One straight way is to download the entire dataset (approximate 66GB after unzip) through the nuScenes official website, but this will be time consuming. You can also use a quick command to download the entire file automatically by referring such as: 
([li-xl/nuscenes-download: script for downloading nuscenes (github.com](https://github.com/li-xl/nuscenes-download?tab=readme-ov-file)) 

## Source:
nuScenes is released by Motional (https://motional.com/)

## Vehicle:
nuScenes dataset is collected based on the vehicle: Renault Zoe
This type of vehicle has a **wheelbase of 2.588 meters** and maximum **acceleration is around 3m/s/s** (takes 9 seconds to accelerate from 0 to 60mph).

## Data size:
*Notice, here each **data sample** refers to a **collection of sensor data** captured at approximately the same time, providing synchronized information from multiple sensors.*

The dataset consists of 1,000 driving scenes collected in Boston and Singapore. Each scene is approximately 20 seconds long, effectively representing a 20-second sensor data collection period that includes inputs from six cameras, lidar, radar, IMU, and more. It's important to note that the scenes are not necessarily continuous from a single driving session; they may have been captured on different roads or maps, offering diverse driving environments. 

The annotated data samples for each scene is 2Hz, i.e., we will have roughly 20x2x1000 = 40,000 annotated data samples. Precisely, there are a total 34,149 data samples (28130 for training [700 scenes] and 6019 for validation [150 scenes]). And there are around 6,000 data samples [150 scenes] for testing, which do not provide the labels.    

To verify the above claims, you can run the following code:

```
from nuscenes.nuscenes import NuScenes
nusc = NuScenes(version='v1.0-trainval', dataroot=<path-where-you-saved-it>', verbose=True)
print(len(nusc.sample)) ### 34,149
```

## Data Structure
Each data sample has its own token (the data structure is stored with **SQL** structure).  

## Coordinate Systems


# TBC
