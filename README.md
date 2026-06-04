# SALMA: Structure-Aware Alignment Framework for Referring Image and Video Segmentation

<div align="center">

[![Paper](https://img.shields.io/badge/Paper-Under_Review-red.svg)](链接)
[![Model](https://img.shields.io/badge/Model-HuggingFace-yellow.svg)](链接)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

</div>

> **[TL;DR]** SALMA introduces a class-agnostic structural prior into the cross-modal alignment process via **Mask-Biased Attention (MBA)** and **Text-Mask Contrastive (TMC) Loss**, significantly mitigating attention drift and improving boundary quality in referring segmentation tasks.

## 📰 News
* **[2026.05]** 🚀 Code and pre-trained models for SALMA are released!
* **[2026.05]** 📝 The manuscript is currently under review.

## 💡 Methodology

*(请在这里插入一张高质量的模型架构矢量图，如 `docs/architecture.png`)*

SALMA tackles the attention drift problem caused by salient distractors in complex spatial relationships. The core contributions include:
* **Mask-Biased Attention (MBA):** Extracts class-agnostic structural priors using SAM-2 decoder's stop-gradient null-prompt pre-pass, injecting them via soft residual gating.
* **Text-Mask Contrastive Loss:** Enhances consistency between text semantics and target masks by aggregating visual representations on post-MBA feature maps.
* **Boundary Consistency Loss:** Refines fine-grained edge quality based on Sobel edge maps.

## 📊 Main Results

SALMA achieves state-of-the-art performance across multiple benchmarks compared to the strong Sa2VA-1B baseline.

| Benchmark | Metric | Sa2VA-1B | SALMA | $\Delta$ |
| :--- | :---: | :---: | :---: | :---: |
| **Ref-DAVIS17** | J&F | 68.47* | **71.87** | **+3.4** |
| **Ref-YouTube-VOS** | J&F | - | - | **+1.7** |
| **MeVis** | J&F | - | - | **+4.3** |
| **RefCOCOg (test)** | cIoU | - | **78.4** | - |

> *Note: End-to-end inference speed shifts minimally from 17.97 FPS to 17.84 FPS (only ~0.7% latency overhead).*

## 🚀 Quick Start

### 1. Environment Setup
Tested on Ubuntu 20.04, Python 3.9, PyTorch 2.1.2, and DeepSpeed ZeRO-2.
```bash
conda create -n salma python=3.9 -y
conda activate salma
pip install -r requirements.txt
