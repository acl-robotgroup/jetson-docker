# jetson-docker

## Dockerfile.ros2-torch

This Dockerfile builds **PyTorch from source** on **Jetson Orin AGX** to ensure
compatibility with **NumPy >= 2.0**.

On Jetson platforms (CUDA 12.6), prebuilt PyTorch wheels are either unavailable
or incompatible with newer NumPy versions, so PyTorch must be compiled from source.

In addition, some ROS 2 packages (e.g. `cv_bridge`) do **not yet support NumPy >= 2.0**
in their binary distributions. These packages need to build from source
inside the container.

### Environment

- Hardware: Jetson Orin AGX
- OS / BSP: JetPack (L4T R36.4.7)
- CUDA: 12.6
- NumPy: >= 2.0

### Prebuild docker image
dididog/ros2-torch
