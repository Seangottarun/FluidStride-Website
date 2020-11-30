---
layout: page
title: How FluidStride works
include_in_header: true
---

# How FluidStride works
FluidStride works by performing kinematic analysis on your videos. It does this
using separate machine learning models for 2D and 3D analysis


## 2D Keypoint Analysis
First, computer vision is used to identify 2D keypoints. This allows us to know the
position of joints in the 2D video. Here is an example of a video frame annotated
with the 2D joints.

<br>
<br>

<img width="100%" alt="2D pose analysis example"  src="/assets/pose2D.jpg">
<br>
<br>


## 3D Depth Prediction
However, we're not flat stick figures; running is a 3D sport. So we then predict
a depth for each keypoint, which lets FluidStride properly analyze running from
different angles.

<br>
<br>
<video width="100%" autoplay="autoplay" controls="controls" loop="loop">
  <source src="/assets/pose3D.mp4" type="video/mp4">
  <source src="/assets/pose3D.webm" type="video/webm">
Your browser does not support the video tag.
</video>
<br>
<br>
