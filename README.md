
# Edge-Guided LoRA-Adapted DINOv2 for Building Change Detection

## Overview

This project investigates an edge-guided, LoRA-adapted DINOv2 architecture for building change detection in remote-sensing images.

The model predicts a pixel-level change mask from two images captured at different times.

## Dataset

- **Dataset:** LEVIR-CD+
- **Task:** Building change detection
- **Input:** Two RGB images captured at different times
- **Output:** Binary change mask
- **Image source:** [LEVIR-CD+ on Hugging Face](https://huggingface.co/datasets/blanchon/LEVIR_CDPlus)

## Methodology

The implementation uses a pretrained DINOv2-Small backbone with Low-Rank Adaptation (LoRA), temporal feature fusion, and a decoder for change-mask prediction.

The proposed approach adds edge-guidance components and edge-aware loss terms. A baseline model is evaluated against the proposed model under different training-label budgets.

## Experiments

The experiments compare baseline and proposed models using:

- Precision
- Recall
- F1-score
- Intersection over Union (IoU)
- Overall accuracy

Results are evaluated at 100%, 50%, 20%, and 10% training-label budgets.

## Implementation

The colab notebook contains the implementation, training procedure, evaluation and experimental comparisons.

## Reproducibility

The exact software dependencies, dataset preparation steps, random seeds and hardware requirements should be documented based on the environment used to run the experiments.

## Limitations

Results are based on the implemented experimental setup and should not be interpreted as evidence that edge guidance improves performance in every label-budget setting.

## Author

Feba Ann Joshy
