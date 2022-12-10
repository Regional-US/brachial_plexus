# Brachial Plexus Nerve Segmentation

Code for the accompanying paper, "*Automated Real Time Delineation of Supraclavicular Brachial Plexus in Neck Ultrasonography Videos: A Deep Learning Approach*" 

### Dataset
We share a deidentified set of 163 ultrasound videos of supraclavicular brachial plexus region and their ground truth annotations.
- Videos available in the `data\us_videos\` folder
- Corresponding annotation text files available in the `data\bb_annotations\` folder. The union of bounding boxes in annotations is used as a single mask for each frame. Individual bounding boxes do not have any meaning.
- If you wish to change the location of data folder, edit the `DATA_DIR` path in `configurations.ini`
- These deidentified videos are shared with a non-commerical data use agreement.

### Examples

We show examples of supraclavicular brachial plexus segmentation for three distinct frequency gain settings in ultrasound.
- Red contours are ground truth annotated by expert anesthetists
- Blue masks are predictions by neural network

High Gain             |  Medium Gain          |  Low Gain
:-------------------------:|:-------------------------:|:-------------------------:
![](./other/high_gain.gif)  |  ![](./other/medium_gain.gif) |  ![](./other/Low_gain1.gif)

### Installation
Implemented for Python 3, with following dependencies:
- PyTorch
- Torchvision
- OpenCV
- PIL
- sklearn
- Numpy
- Pandas
- tqdm

### Usage
See `segmentation.ipynb` jupyter notebook
- Each video's evaluations is saved in folder :  `./data/output/video_evals/`
- More configurations and hyperparameters can be modified in `configurations.ini` 
