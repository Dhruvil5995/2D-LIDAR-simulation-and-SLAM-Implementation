# 2D LIDAR Simulation and SLAM Implementation in Python

Welcome to the repository where we tackle the intricacies of robotic perception through a robust line segment extraction algorithm coupled with SLAM (Simultaneous Localization and Mapping). Our focus here is on leveraging laser data and implementing a seeded region growing algorithm to discern line segments even in the presence of noise. This forms a foundational component for robotic applications requiring high levels of mapping, navigation precision, and object recognition.

## Project Overview

The core of this project is the `Line Segment Extraction Algorithm`, which processes laser scan data to identify and extract line segments that are critical for robotic perception tasks. We've developed a simulated 2D LIDAR sensor system that uses our custom `LaserSensors` class. This class is responsible for calculating distances to obstacles and sensing the environment, introducing a controlled level of uncertainty to mimic real-world conditions.

Our `featuresDetection` class is the heart of the SLAM algorithm, processing sensor data to pinpoint and delineate environmental features. It employs a suite of methods for computations such as line fitting with the Orthogonal Distance Regression (ODR) method and managing seed segments for the growing process.

We harness the power of the Pygame library to visually simulate sensor data collection and feature detection in a mapped environment. Through an interactive display, users can witness the SLAM algorithm in action, as it collects data, processes it, and identifies features on the map.


The simulation was implemented using Pygame library which provides an interactive and visual way to display the sensor data and detected features. <br>

![feature](https://user-images.githubusercontent.com/85798077/213577668-76031d64-2ef1-4a42-8c25-2a74839d03f5.png)<br>


![ezgif com-optimize](https://user-images.githubusercontent.com/85798077/229351322-a78ef329-0bfb-45ca-a803-5bc1e7874be4.gif)<br><br>

### Features at a Glance

- Robust line segment extraction from noisy laser data using seeded region growing.
- Efficient handling of environmental clutter to deliver reliable detections.
- Orthogonal Distance Regression for precise line fitting tasks.
- A Pythonic interface that ensures easy integration into robotic projects.
- An `example.py` script included for demonstration and algorithmic validation.

### Installation Guide

To embark on using this line segment extraction toolkit, here are the steps:

1. Clone the repository:
```bash
git clone https://github.com/Dhruvil5995/2D-LIDAR-simulation-and-SLAM-Implementation
```

2. Install the necessary dependencies:
```bash
pip install -r requirements.txt
```

3. Make sure your environment is compatible with Python 3.7 or higher.

### How to Use

- Import the requisite classes from `feature_main.py` into your application.
- Set up your environmental map using the `Environment` class.
- Initialize your laser sensor via the `LaserSensors` class, setting the desired range and map.
- Utilize the `featuresDetection` class to process sensor data and extract line segments continually.
- Access the line segments with the `LINE_SEGMENTS` variable within `featuresDetection`.
- Update and visualize the extracted segments on the map using the `show_sensorData` function.


### What's Next?

We aim to expand the capabilities of this algorithm by:

- Adding more line fitting algorithms for versatile application scenarios.
- Boosting the computational efficiency perhaps by code optimization or parallelization.
- Combining this algorithm with other sensory data for a multi-faceted robotic perception system.

Dive into the `example.py` for a full-fledged example and get a hands-on experience of how this algorithm performs. Your journey to enhance robotic perception begins here!


**Acknowledgements:**<br>

- Refrence: https://journals.sagepub.com/doi/pdf/10.1177/1729881418755245 <br>




