# Multi-Parametric-EC-MRI
Multi-Parametric MRI-Based Staging of Early Endometrial Cancer Dataset Construction and Benchmarking with  CNN and Transformer Models

Multi-Parametric-EC-MRI
Multi-Parametric MRI-Based Staging of Early Endometrial Cancer Dataset and Benchmark Models
This repository provides a multi-parametric MRI dataset for the staging of early endometrial cancer (EEC), including T2-weighted sagittal (T2sag), T2-weighted axial (T2ax), and diffusion-weighted axial (DWIax) imaging sequences.
The dataset is accompanied by benchmark implementations using CNN (ResNet-34, EfficientNet-B0) and Transformer-based models (Swin-T, Swin-S) for comparative analysis on FIGO Stage 1A vs. Stage 1B classification.

Dataset Description

The dataset includes preprocessed and de-identified MRI image patches used for model training and evaluation.
Two categories are provided:

Stage 1A

Stage 1B

For each category, three MRI parameters are included:

T2sag

T2ax

DWIax

Dataset Structure
Multi-Parametric-EC-MRI/
│
├── 1A T2sag.zip
├── 1A T2ax.zip
├── 1A DWIax.zip
│
├── 1B T2sag.zip
├── 1B T2ax.zip
├── 1B DWIax.zip
│
└── pytorch_classification.zip   # Training & evaluation scripts

 Task Overview

The primary task is binary classification of early endometrial cancer:

Stage 1A

Stage 1B

We provide:

✔ Multi-parametric dataset
✔ Clean training pipeline (PyTorch)
✔ Benchmark results for CNN and Transformer models
✔ Confusion matrices and training curves for reproduction

 Benchmark Models

The following models are included or supported:

Model	Type	Notes
ResNet-34	CNN	Strong baseline, stable performance
EfficientNet-B0	CNN	Lightweight, good recall
Swin Transformer (Swin-T)	Transformer	Good multi-parametric learning
Swin Transformer (Swin-S)	Transformer	Strongest overall performance
 How to Use
1. Clone Repository
git clone https://github.com/LxiangFeng/Multi-Parametric-EC-MRI.git
cd Multi-Parametric-EC-MRI

2. Unzip Data
unzip "1A T2sag.zip"
unzip "1A T2ax.zip"
...

3. Run Training Scripts

All training code is inside pytorch_classification.

Example:

python train_resnet34.py


Example:

Model	T2sag Acc	T2ax Acc	DWIax Acc	Multi-Param Acc
ResNet-34	0.99	0.98	0.99	0.987
EfficientNet-B0	0.97	0.97	0.96	0.973
Swin-T	0.96	0.93	0.97	0.965
Swin-S	0.99	0.96	0.97	0.978
 Data Availability

This repository contains a processed and de-identified subset of the dataset.
The full DICOM dataset can be accessed upon reasonable request and pending approval under institutional data-sharing policies.

 Citation

If you use this dataset or code, please cite:

Feng L., et al. Multi-Parametric MRI-Based Staging of Early Endometrial Cancer:
Dataset Construction and Benchmarking with CNN and Transformer Models, 2025.
