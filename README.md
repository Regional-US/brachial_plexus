# Brachial Plexus Nerve Segmentation

Data for the accompanying paper, "*Automated Real Time Delineation of Supraclavicular Brachial Plexus in Neck Ultrasonography Videos: A Deep Learning Approach*" 

### Dataset
We share a deidentified set of 227 ultrasound videos of brachial plexus region and their ground truth annotations.
- `data` folder contains folders for each of the 3 ultrasound machines
- Corresponding annotation text files available in the `data\<machine>\bb_annotations\` folder. The union of bounding boxes in annotations is used as a single mask for each frame. Individual bounding boxes do not have any meaning.
- Active contour generated mask for each frame of each video chosen by anaesthesiologists in `ac_masks` folder
- These deidentified videos are shared with a non-commerical data use agreement.

### Examples

We show examples of supraclavicular brachial plexus segmentation for three distinct frequency gain settings in ultrasound.
- Red contours are ground truth annotated by expert anesthetists
- Blue masks are predictions by DeepLabv3 neural network

High Gain             |  Medium Gain          |  Low Gain
:-------------------------:|:-------------------------:|:-------------------------:
![](./other/high_gain.gif)  |  ![](./other/medium_gain.gif) |  ![](./other/Low_gain1.gif)
