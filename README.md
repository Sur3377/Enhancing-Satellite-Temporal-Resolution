# Enhancing Temporal Resolution of Satellite Images Using Deep Learning

## Overview

Satellite imagery is typically captured at fixed time intervals, which can limit the continuous observation of rapidly changing atmospheric events.

This project develops a deep learning-based frame interpolation system to generate intermediate satellite images between consecutive observations, effectively enhancing the temporal resolution of satellite imagery.

## Approach

The project uses **UPR-Net** for frame interpolation. Given two consecutive satellite frames, the model learns to generate the intermediate frame.

**Pipeline:**

Previous Frame → UPR-Net → Interpolated Frame → Ground Truth Comparison

## Dataset

- Satellite: GOES-19
- Instrument: ABI
- Channel: 13 (Thermal Infrared)
- Temporal interval: 10 minutes
- Image format: JPG
- Original satellite data: NetCDF (.nc)

## Training

The model is trained using patch-based training to efficiently process the high-resolution satellite imagery.

- Framework: PyTorch
- Model: UPR-Net
- Training platform: Google Colab
- GPU: NVIDIA Tesla T4
- Patch size: 256 × 256

## Evaluation

The generated frames are evaluated using:

- PSNR
- SSIM
- MSE

## Project Status

🚧 Currently under development.

Training and evaluation are in progress, with results and visual comparisons being added to the repository.

## Future Work

- Improve interpolation quality
- Evaluate on different atmospheric conditions
- Generate visual comparisons and time-lapse sequences
- Develop an interactive visualization dashboard

## Technologies

Python | PyTorch | Deep Learning | UPR-Net | Google Colab | GOES-19 | NetCDF
