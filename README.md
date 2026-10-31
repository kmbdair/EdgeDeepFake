
# AttentiQ

### Does Attention Survive Quantization?
**Trustworthy Deepfake Detection at the Edge**

**University:** Effat University  
**College:** College of Engineering  
**Course:** CS4085 — Deep Learning  
**Supervisor:** Dr. Naila Marir  
**Team:** AttentiQ

## Project Overview

AttentiQ investigates whether attention mechanisms remain
effective when deep learning models are compressed using
INT8 quantization.

The project focuses on trustworthy and computationally
efficient deepfake detection for resource-constrained devices.

Rather than measuring only accuracy and speed, AttentiQ
also investigates attention fidelity: whether quantization
changes the visual regions a detector focuses on.

## Research Questions

1. Does CBAM improve deepfake detection compared with
   ResNet-18 and channel-only SE attention?
2. Can INT8 quantization reduce model size and inference
   latency while preserving detection performance?
3. Does quantization change attention maps, and can
   quantization-friendly attention reduce this change?
4. Does attention improve generalization to unseen datasets?

## Models

| ID | Architecture | Purpose |
|---|---|---|
| B1 | MesoNet (Meso-4) | Lightweight reference |
| M0 | ResNet-18 (FP32) | Baseline |
| C1 | SE-ResNet-18 (FP32) | Channel-attention control |
| M1 | ResNet-18 + CBAM (FP32) | Attention enhancement |
| M2 | M1 with post-training INT8 quantization | Efficiency |
| M3 | ResNet-18 + QF-CBAM with QAT INT8 | Stretch goal |

## Datasets

**Primary:** FaceForensics++ (FF++)

- Training, validation, and in-domain testing
- c23 compression as primary evaluation
- c40 compression as optional robustness evaluation

**External:** Celeb-DF v2

- Cross-dataset generalization testing

**Fallback:** DFDC Preview

Dataset files are not distributed through this repository.

## Evaluation Metrics

### Detection Performance
- AUC
- F1-score
- Accuracy
- Precision and recall

### Computational Efficiency
- Model size
- Parameter count
- MACs
- Peak memory usage
- CPU and edge-device inference latency

### Attention Fidelity
- Attention-map cosine similarity
- Top-20% attention-region IoU
- Prediction-flip rate
- Grad-CAM visualizations

## Proposed Experimental Pipeline

1. Prepare and preprocess facial video datasets.
2. Train baseline and attention-based detectors.
3. Apply post-training INT8 quantization to M1.
4. Compare detection performance and computational costs.
5. Analyze attention maps before and after quantization.
6. Evaluate generalization on an external dataset.
7. Test inference on edge hardware when available.
8. Develop a demonstration of the accuracy-efficiency tradeoff.

## Tools

- Python
- PyTorch and timm
- torchao / ONNX Runtime
- Google Colab
- Google Drive
- VS Code
- GitHub

## Repository Structure

- `data/` — Dataset instructions and preprocessing details
- `notebooks/` — Experiments and Colab notebooks
- `src/` — Model, training, and evaluation code
- `results/` — Metrics, plots, and attention visualizations
- `docs/` — Research proposals and documentation

## Team Members

- Kamar Bdair — Data preparation and preprocessing
- Layan Ziyadah — Model development and training
- Faisal Shamsi — Quantization and edge benchmarking
- Sedra Aljundi — Literature review, attention analysis,
  evaluation, and documentation

**Supervisor:** Dr. Naila Marir

## Project Status

Research proposal completed.

Dataset preparation, baseline experiments, quantization,
attention-fidelity evaluation, and edge deployment are planned.

No experimental results are claimed at this stage.

## Research Objective

To investigate whether computational efficiency can be
improved without losing the detection and attention
benefits of attention-enhanced neural networks.

## Acknowledgment

Developed by Team AttentiQ at Effat University
under the supervision of Dr. Naila Marir.
