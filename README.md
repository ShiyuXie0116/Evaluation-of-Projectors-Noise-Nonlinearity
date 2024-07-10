# An Evaluation of State-of-the-Art Projectors in the Presence of Noise and Nonlinearity in the Beer-Lambert Law

This repository accompanies our MICCAI 2024 paper, "An Evaluation of State-of-the-Art Projectors in the Presence of Noise and Nonlinearity in the Beer-Lambert Law." The work investigates the accuracy of state-of-the-art projectors for low dose CT imaging under realistic conditions.

## Abstract

Efficient computation of forward and back projection is key to scalability of iterative methods for low dose CT imaging at resolutions needed in clinical applications. State-of-the-art projectors provide computationally-efficient approximations to X-ray optics calculations in the forward model that strike a balance between speed and accuracy. While computational performance of these projectors are well studied, their accuracy is often analyzed in idealistic settings. When choosing a projector a key question is whether differences between projectors can impact image reconstruction in realistic settings where nonlinearity of the Beer-Lambert law and measurement noise may mask those differences. We present an approach for comparing the accuracy of projectors in practical settings where the effects of the Beer-Lambert law and measurement noise are captured by a sensitivity analysis of the forward model. Our experiments provide a comparative analysis of state-of-the-art projectors based on the impact of their approximations to the forward model on the reconstruction error. Our experiments suggest that the differences between projectors, measured by reconstruction errors, persists with noise in low-dose measurements and become significant in few-view imaging configurations.

## Overview

This repository contains the data and code used in the paper titled "An Evaluation of State-of-the-Art Projectors in the Presence of Noise and Nonlinearity in the Beer-Lambert Law" presented at MICCAI 2024.

Our study compares the reconstruction performance of three fast projectors: Separable Footprint (SF), Look-Up Table-Based Ray Integration Framework (LTRI), and Convolutional Forward Models (CNSF) against a reference projector, in the presence of the Beer's law and Poisson Noise.

## Contents

- `data/`: Contains the datasets used in the experiments.
- `code/`: Contains the Python scripts for data processing, analysis, and visualization.
- `results/`: Contains the results and plots generated from the experiments.

## Data Source

The data used in this study is based on the FORBILD phantom generator, which can be found at:
[https://github.com/ashkarin/forbild-gen](https://github.com/ashkarin/forbild-gen)

We have modified the original code to incorporate the effects of the Beer-Lambert law and noise, providing a more realistic simulation of CT imaging conditions.

## Projector Implementations

The implementations of the projectors used in this study can be found in the following repositories:

- Separable Footprint (SF): [https://github.com/JeffFessler/mirt](https://github.com/JeffFessler/mirt)
- Look-Up Table-Based Ray Integration Framework (LTRI): [https://github.com/sungsooha/LTRI](https://github.com/sungsooha/LTRI)
