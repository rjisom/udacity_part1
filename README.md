[//]: # (Image References)
[image_0]: ./misc/rover_image.jpg

# Part 1: Search and Sample Return Project

![alt text][image_0] 

## Overview
This is my Part 1 project for udacity nano degree program. This project implements a series of transforms of the rover camera data to allowing it navigate martian terrain. This project is modeled after the [NASA sample return challenge](https://www.nasa.gov/directorates/spacetech/centennial_challenges/sample_return_robot/index.html). I borrowed heavily from [this video](https://www.youtube.com/watch?v=oJA6QHDPdQw) provided by the Udacity instructors. The main components fo this project are:  perception.py, decision.py, and drive_rover.py. 

## perception.py
This file contains the functions used for identifying the local terrain and applying matrix manipulations using opencv to map navigatable terrain and locate rocks of interest for collecting samples.

## decision.py
This file contains the functions used for making decisions based on the perception.py data. While I did not modify this file from it's original clone, it contains a decision tree for deciding where and how the rover should operate.

## drive_rover.py
This file contains the functions used for making decisions based on the perception.py data. While I did not modify this file from it's original clone, it contains a decision tree for deciding where and how the rover should operate.



