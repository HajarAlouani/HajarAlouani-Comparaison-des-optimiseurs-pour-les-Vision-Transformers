# Optimizer Comparison for Vision Transformers on CIFAR-10

Master DSBD & IA — Module: Algorithmes d'Optimisation  
Faculté des Sciences Ben M'Sik, Université Hassan II de Casablanca

## Overview

Experimental benchmark of 5 optimizers (AdamW, Lion, SGD+Momentum, AdaBelief, RMSProp) applied to fine-tuning DeiT-Tiny and ResNet-18 on CIFAR-10 over 20 epochs on a Kaggle T4 GPU.

## Repository Structure

```
├── Optimizing_Vision_Transformers.pptx  # prezentation pptx
├── optimizer_comparison_report.pdf      # report pdf
├── optimizer_comparison_vit.ipynb       # Main training notebook
├── visualization_real_results.ipynb     # Visualization notebook (real results)
├── optimizer_results.csv                # Exported results from all 10 runs
└── README.md
```

## Requirements

```bash
pip install timm lion-pytorch adabelief-pytorch scikit-learn
```

## How to Run

1. Open `optimizer_kaggle_nocache.ipynb` on Kaggle with GPU T4 enabled
2. Run cells 1–4 (setup, data, models, functions)
3. Run each experiment cell independently (one per optimizer/model combination)
4. Run the figures and summary table cells after all experiments are complete

## Results Summary

| Model | Best Optimizer | Best Acc |
|---|---|---|
| DeiT-Tiny | AdamW | 96.40% |
| ResNet-18 | Lion | 96.30% |

SGD+Momentum and RMSProp failed to converge in the fine-tuning setting on both architectures.

## Hardware

- GPU: NVIDIA Tesla T4 (Kaggle)
- PyTorch 2.10.0 + CUDA 12.8
