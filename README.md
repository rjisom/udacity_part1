[//]: # (Image References)
[image_0]: ./misc/rover_image.jpg
[image_1]: ./calibration_images/map.jpg
[image_2]: ./calibration_images/example_rock2.jpg
[image_3]: ./calibration_images/console_update.png
[image_4]: ./calibration_images/mapRed.png
[image_5]: ./calibration_images/map2.png

# Part 1: Search and Sample Return Project

![alt text][image_0] 

## Overview
This is my Part 1 project for udacity nano degree program. This project implements a series of transforms of the rover camera data to allowing it navigate martian terrain. This project is modeled after the [NASA sample return challenge](https://www.nasa.gov/directorates/spacetech/centennial_challenges/sample_return_robot/index.html). I borrowed heavily from [this video](https://www.youtube.com/watch?v=oJA6QHDPdQw) provided by the Udacity instructors. The main components for this project are:  perception.py, decision.py, and drive_rover.py and the notebook Rover_Project_Test_Notebook.ipynb. 

## Requirements of this project
The requirements of this project were to add code to give our rover the ability to percieve the world around them by identifying navigatable terrain and spot rocks that might be of interest for sampling.

To do this we were tasked with modifying perception.py to take input from the rover's camera and perform functions upon this data. The process for this went as followed:

1. We modifed the `process_image()` function to make both a "warped" copy of the image for finding location relative of the rover and also a "masked" copy for identifying pixels that fell above or below a specified color threshold. This gave us a top down image of navigatable terrain relative to the rovers posistion.

![alt text][image_1] 

These new images were displayed on the rover console along with updates to the rover being displayed as a text file proving the rover was automously moving.

![alt text][image_3] 

![alt text][image_4] 

![alt text][image_5] 

2. After the warped and masked copies were finished, the data could be used to identify both navigatable terrain along with a warped perspective of rover relative to it's surroundings. 

3. The last step was to identify rocks that may be of interest based on their colors. This was done similarly to the mapping of terrain but we used a different color threshold in `find_rocks()` function that would detect rocks of interest.

![alt text][image_2] 

## perception.py
This file contains the functions used for identifying the local terrain and applying matrix manipulations using opencv to map navigatable terrain and locate rocks of interest for collecting samples.

## decision.py
This file contains the functions used for making decisions based on the perception.py data. While I did not modify this file from it's original clone, it contains a decision tree for deciding where and how the rover should operate.

## drive_rover.py
This file contains the functions used for making decisions based on perception.py and decision.py. This file runs the autonomous mode with the Roverism executable.  

## Rover_Project_Test_Notebook.ipynb
This notebook explains how the rover will process images and make transformations on based on the perception data. After the perception data is processed, it displays a video of the new mapping alongside the data already provided. 



