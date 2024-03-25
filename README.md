# Needle Guidance for Autonomus UGRA

Data for the accompanying paper:

"*Nerve Block Target Localization and Needle Guidance for Autonomous Robotic Ultrasound Guided Regional Anesthesia*", Submitted to IROS-2024

### Dataset
We share a deidentified set of 227 ultrasound videos of brachial plexus region and their ground truth annotations.
- `data` folder contains folders for each of the 3 ultrasound machines
- Corresponding nerve plexus annotation text files available in the `data/<machine>/bb_annotations/` folder. The union of bounding boxes in annotations is used as a single mask for each frame. Individual bounding boxes do not have any meaning.
- Active contour generated mask of nerve plexus for each frame of each video chosen by anaesthesiologists in `ac_masks` folder
- Needle annotations available in `data/Sonosite/needle/` folder.
- These deidentified videos are shared with a non-commerical data use agreement.

### Demo Examples

Needle Trajectory guidance towards regional anesthesia target:
 - Green: The needle trajectory intersects with the target anesthesia region
 - Yellow: The trajectory is between the anesthesia targets
 - Red: The trahectory misses the anesthesia targets

![](./other/needle_trajectory.gif)


Supraclavicular brachial plexus segmentation for three distinct frequency gain settings in ultrasound.
- Red contours are ground truth annotated by expert anesthetists
- Blue masks are predictions by the neural network

High Gain             |  Medium Gain          |  Low Gain
:-------------------------:|:-------------------------:|:-------------------------:
![](./other/high_gain.gif)  |  ![](./other/medium_gain.gif) |  ![](./other/Low_gain1.gif)
