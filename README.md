<!--
  GITHUB PROFILE README
  To use this on your GitHub profile:
  1. Create a new public repository with the exact same name as your GitHub username:
     https://github.com/new -> Repository name: "Looka-info"
  2. Initialize it with a README.md (or copy the contents of this file into its README.md).
  3. Commit and push. Your GitHub profile page will automatically display this overview!
-->

<div align="center">

# Hi, I'm Looka 👋
### Machine Learning Engineer · Computer Vision & Deep Learning Systems

[![GitHub](https://img.shields.io/badge/GitHub-Looka--info-181717?style=for-the-badge&logo=github)](https://github.com/Looka-info)
[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.6-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)](https://pytorch.org)
[![CUDA](https://img.shields.io/badge/NVIDIA-CUDA%2012.4-76B900?style=for-the-badge&logo=nvidia&logoColor=white)](https://developer.nvidia.com/cuda-zone)

Focused on **applied computer vision**, **production model calibration**, **rigorous data hygiene**, and **hardware-accelerated inference pipelines**.

</div>

---

## 🚀 Featured Project: PlantVision

<div align="center">

### [**PlantVision — Plant Leaf Disease Classifier**](https://github.com/Looka-info/Computer-vision-classifier)
*An end-to-end PyTorch computer vision system comparing empirical scratch CNNs against fine-tuned ResNet-18 for multi-crop pathology diagnosis across 38 categories in the PlantVillage dataset.*

[![GitHub Repo](https://img.shields.io/badge/Repository-Looka--info%2FComputer--vision--classifier-blue?style=flat&logo=github)](https://github.com/Looka-info/Computer-vision-classifier)
[![Accuracy](https://img.shields.io/badge/Test%20Top--1%20Acc-99.03%25-brightgreen.svg?style=flat)]()
[![Macro-F1](https://img.shields.io/badge/Macro--F1-0.9871-brightgreen.svg?style=flat)]()
[![ECE](https://img.shields.io/badge/ECE-0.0040-success.svg?style=flat)]()
[![Inference Latency](https://img.shields.io/badge/GPU%20Latency-3.28%20ms-informational.svg?style=flat)]()
[![Tests](https://img.shields.io/badge/Tests-29%20Passing-brightgreen.svg?style=flat)]()

</div>

#### Key Highlights & Engineering Innovations:
* **Zero Data Leakage:** Built an automated cryptographic pipeline (SHA-256 hashing and 64-bit `dHash` with Multi-Index Hashing) auditing 2.28M+ cross-split candidate image pairs to guarantee zero train-to-test duplicate leakage.
* **Specimen-Isolated Partitions:** Re-partitioned benchmark evaluation splits using per-class greedy grouped assignment, eliminating historical burst-photo specimen overlap (reducing shared physical leaves from 2,118 to exactly 0).
* **Two-Stage Fine-Tuning:** Trained ResNet-18 via head-warmup ($\eta=10^{-3}$) followed by differential learning-rate fine-tuning of residual block 4 ($\eta_{\text{backbone}}=10^{-4}, \eta_{\text{head}}=5\times 10^{-4}$), boosting Top-1 accuracy from 88.96% (scratch CNN) to **99.03%** on 8,133 held-out test images.
* **Model Calibration & Selective Classification:** Evaluated multiclass Expected Calibration Error (ECE: 0.0040) and implemented a validation-derived rejection gate ($\tau^* = 0.72$), achieving **99.56% selective test accuracy** with 98.52% coverage and a 55.7% error reduction.
* **Synchronized Hardware Profiling:** 5-stage latency profiler with explicit CUDA stream synchronization (`torch.cuda.synchronize()`), measuring steady-state forward pass (3.28 ms median) and 21 ms end-to-end serving pipeline (~47 FPS).
* **Interactive Web Deployment:** Single-image diagnostic UI built in Streamlit with top-3 predictions and automated reliability alerts.

```
Benchmark Comparison:
┌──────────────────────────────┬──────────────┬──────────────┬──────────────┬────────────────┐
│ Model Architecture           │ Top-1 Acc    │ Macro-F1     │ Latency (B=1)│ Throughput     │
├──────────────────────────────┼──────────────┼──────────────┼──────────────┼────────────────┤
│ Custom Baseline CNN (4-block)│ 88.96%       │ 0.8587       │ 2.54 ms      │ 1,726.5 img/s  │
│ ResNet-18 (Transfer Learning)│ 99.03%       │ 0.9871       │ 3.28 ms      │ 1,101.0 img/s  │
└──────────────────────────────┴──────────────┴──────────────┴──────────────┴────────────────┘
```

👉 **[Explore the Full Project Repository & Diagnostics](https://github.com/Looka-info/Computer-vision-classifier)**

---

## 🛠️ Technical Stack & Tooling

| Domain | Technologies & Libraries |
| :--- | :--- |
| **Deep Learning & Frameworks** | **PyTorch**, **TorchVision**, ResNet, CNN Architectures, Transfer Learning, Mixed Precision (AMP) |
| **Computer Vision & Imaging** | PIL / Pillow, OpenCV, Image Transforms & Augmentation, Difference Hashing (`dHash`) |
| **Evaluation & Statistics** | Scikit-Learn, Expected Calibration Error (ECE), Multiclass Brier Score, Selective Classification |
| **Inference & Benchmarking** | CUDA Stream Synchronization (`torch.cuda.synchronize`), Latency / Throughput Profiling, TorchScript |
| **Scientific Computing** | NumPy, Pandas, SciPy, Matplotlib, Seaborn |
| **Serving & Interfaces** | Streamlit, FastAPI, REST Endpoints |
| **Engineering & MLOps** | Pytest, Git, Git LFS, Virtual Environments, Modular Packaging (`pyproject.toml`) |

---

## 🔬 Engineering Philosophy

1. **Data Integrity Precedes Modeling:** Eliminating duplicate images, cross-split leakage, and specimen co-occurrence is as critical as network architecture.
2. **Empirical Benchmarking Over Guesswork:** Every model improvement is compared against an empirical baseline with identical evaluation pipelines and isolated test partitions.
3. **Calibrated Confidence Over Raw Softmax:** High accuracy on standard benchmarks is insufficient if the model cannot signal uncertainty on hard or ambiguous inputs.
4. **Synchronized Hardware Profiling:** Measuring true inference latency requires distinguishing cold startup costs (CUDA context, weights deserialization) from steady-state warm GPU kernels.

---

## 📊 GitHub Overview

<div align="center">

[![Looka's GitHub Stats](https://github-readme-stats.vercel.app/api?username=Looka-info&show_icons=true&theme=tokyonight&hide_border=true&count_private=true)](https://github.com/Looka-info)
[![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=Looka-info&layout=compact&theme=tokyonight&hide_border=true)](https://github.com/Looka-info)

</div>

---

## 📫 Connect

* **GitHub:** [@Looka-info](https://github.com/Looka-info)
* **Email:** [looka.yt123@gmail.com](mailto:looka.yt123@gmail.com)
* **Project Repo:** [Computer-vision-classifier](https://github.com/Looka-info/Computer-vision-classifier)
