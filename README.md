# BLIP-2 Fine‑Tuning for Vision Navigation Assistance

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Results](#results)
- [Limitations](#limitations)
- [Future Work](#future-work)
- [License](#license)

## Introduction
This repository contains code and scripts for fine‑tuning the [BLIP‑2](https://arxiv.org/abs/2301.12597) vision‑language model on a custom navigation‑assistance dataset. Our goal is to assist visually impaired users by generating semantic and directional navigation instructions from scene images.

## Features
- Fine‑tuning with LoRA (PEFT) for efficiency
- Data augmentation pipeline for improving generalization
- Training and evaluation scripts based on Hugging Face Transformers and Datasets
- Weighted Enhanced BERTScore metric combining semantic correctness and directional accuracy


## Results
| Experiment                              | BERT F1 | Enhanced BERTScore |
|-----------------------------------------|--------:|-------------------:|
| Original BLIP‑2 (no fine‑tuning)        |    0.63 |              0.46  |
| LM fine‑tune only (9M params, 0.24%)    |    0.69 |              0.51  |
| LM fine‑tune + Augmented Dataset        |    0.72 |              0.55  |

## Limitations
- Path ambiguity remains an issue: multiple routes can lead to the same destination.
- Creating a large‑scale, diverse navigation dataset is challenging.
- Navigation based on a single image lacks temporal context.

## Future Work
- Extend from single‑image to video‑based navigation for richer context.
- Explore fine‑tuning the Q‑Former for end‑to‑end improvement.
- Incorporate multi‑modal sensor data (e.g., depth, LIDAR).

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
