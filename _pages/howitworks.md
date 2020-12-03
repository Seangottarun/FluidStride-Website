---
layout: page
title: How FluidStride works
include_in_header: true
---

# How FluidStride works
In order to analyze your gait, FluidStride processes your video, tracks your movement
in the video, identifies different running phases, and then calculates common metrics
like symmetry and stride length.

This happens in 4 main steps.

1. [**Capture Running Video**](#capture-running-video){:target="_self"}
- Use a camera or load an existing video
2. [**2D Keypoint Analysis**](#2d-keypoint-analysis){:target="_self"} (i.e. pixels to 2D stick figure)
- Identify joints and body parts from video frame pixels
3. [**3D Depth Prediction**](#3d-depth-prediction){:target="_self"} (i.e. 2D stick figure to 3D person)
- Predict the 3D location of previously found joints and bodyparts
4. [**Gait Analysis**](#gait-analysis){:target="_self"}
- Identify running phases, study symmetry, calculate running stats, etc.

This kinematic gait analysis is powered by 2 separate machine learning
models for 2D and 3D pose estimation.


## Capture Running Video
First we need to get a running video to analyze. Just like any other video-based
app, you can use the built-in camera to record a new video or load an existing
video from your phone.


## 2D Keypoint Analysis
Next, machine learning based computer vision is used to identify 2D keypoints
(joints or body parts). This allows us to identify the position of the runner in
the 2D video. We later use this position data for analyzing gait.

We also draw a 2D stick figure on the video to mark the detected gait. Here is
an example of an image annotated with the 2D joints.

<br>
<br>
<img width="100%" alt="2D pose analysis example"  src="/assets/pose2D.jpg">
<br>
<br>


## 3D Depth Prediction
So far we have a flat stick figure of the runner, but running is a 3D sport! We
need to be able to check symmetry from different angles and track movement in
different directions.

To solve this issue, we then predict a 3D depth for each keypoint from step 2.
This allows FluidStride to properly analyze running gait from different angles.

As you can see from the example below from our software, we can now rotate the
runner and study their gait from the front, side, or any other position!

<br>
<br>
<video width="100%" autoplay="autoplay" controls="controls" loop="loop">
  <source src="/assets/pose3D.mp4" type="video/mp4">
  <source src="/assets/pose3D.webm" type="video/webm">
Your browser does not support the video tag.
</video>
<br>
<br>


## Gait Analysis
Now that we know how the person is running in 3D space, we can then analyze the
3D data to see how good their running form is. This involves identifying running
phases to identify key gait characteristics and to compare with baselines from
biomechanics research literature. The different running phases are shown below.

Furthermore, we can compare the same running phases to check overall symmetry.
These are just some of the things that FluidStride analyzes!

<br>
<br>
<img width="100%" alt="2D pose analysis example"  src="/assets/running-phases.png">
<br>
<br>
