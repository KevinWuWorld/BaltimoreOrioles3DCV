# CV Dimension Modeling Project 



## Description

This is a Python-based Computer Vision project originally proposed by the Baltimore Orioles. The goal is to model the dimensions of baseball bats from simple images, accurately and efficiently. 

For modularity considerations, the main program is divided into several sections. You can find the program in bat_dimension.ipynb.

## Getting Started


### Dependencies
1. Please make sure your browser supports Google Colab
2. Please download the folder /test_images to your local drive. You have 2 ways to use these test images when running the program in Google Colab:
	- a) Upload the folder /test_images to your Google Drive, and link your Google Drive in your Google Colab. If you go with this way, there's no need to run the 2nd cell in the Google Colab file.
	- b) Run the 2nd cell in the Google Colab file and upload file(s) from your local drive.


** The Google Colab file allows public edits. However, unless you have reasons to edit, please avoid making unintentional changes to the Google Colab file!!

### Important Usage Notes
- For visualizing results at this stage of the project, please use our most recent image - "actual_bat_take11.jpg". Other images in the folder suffer from various shortcomings in our preliminary data collection attempts, and thus will not lead to optimized precision. 



### Executing the program

####  Camera Calibration
First, you are suggested to conduct camera calibration to ensure the highest precision possible. However, the rest of the program can still function correctly if you skip this step.

Here are the steps in camera calibration:
- locate the camera you wish to use to conduct dimensions modeling
- produce a camera calibration grid
- take a photo of the camera calibration grid, following generally accepted camera calibration procedures
- run the cell under "Camera Calibration" and produce the calibration matrix (to be used later)

####  Image Segmentation
This is a required step. There are two segmentation methods that you can choose from:
- Histogram Thresholding: Uses a thresholding function to isolate the bat based on intensity values.
- K-Means Clustering: Clusters image colors to separate the bat from the background.

** Note: we also implemented a third segmentation method, Canny Edge Detection. However, this segmentation method is not a stand-alone function (see the last cell in the file for details).

####  Dimensions Modeling
This step will generate the diameter data. Run the cell under "Dimensions Modeling (Centerline Method)" - you can find detailed documentation within the code file. 

## Help

If you have any questions or suggestions, please direct them to Kevin Wu (jwu169@jhu.edu) and Jason Sun (xsun90@jhu.edu).


## Authors

Kevin Wu [@KevinWuWorld]
Jason Sun

## Version History


* 0.1
    * Initial Release


## Acknowledgments

Special thanks to JHU SARG, Dr. Anton Dahbura, and Tad Bekery for their support in the project.
Special thanks to the Baltimore Orioles and JHU Baseball for their assistance.
