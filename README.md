
# EdgeDeepFake

### Attention-Enhanced and Computationally Efficient Deep Learning for Deepfake Detection

**Course:** CS4085 — Deep Learning  
**University:** Effat University  
**Supervisor:** Dr. Naila Marir

## Project Overview

EdgeDeepFake investigates whether attention mechanisms can improve deepfake detection performance while model quantization reduces computational requirements.

The project compares three models:

- **M0:** ResNet-18 baseline
- **M1:** ResNet-18 with CBAM attention
- **M2:** INT8-quantized version of M1

## Research Question

Can CBAM improve the deepfake detection F1-score of ResNet-18, and can INT8 quantization reduce computational cost while preserving detection performance?

## Datasets

- FaceForensics++
- DeepFake Detection Challenge (DFDC)

Dataset files are not stored in this repository.

## Evaluation Metrics

- Accuracy and F1-score
- Model size and parameter count
- CPU inference latency
- MACs/FLOPs
- Memory usage

## Repository Structure

- `data/` — Dataset preparation information
- `notebooks/` — Google Colab experiments
- `src/` — Model implementation and training code
- `results/` — Experimental results and figures
- `docs/` — Research documentation

## Team Members

- Kamar Bdair
- Layan Ziyadah
- Faisal Shamsi
- Sedra Aljundi

## Project Status

Stage 1: Research proposal completed.

Stage 2: Dataset preparation and baseline implementation pending.

## Acknowledgment

Developed as part of the CS4085 Deep Learning course at Effat University.
