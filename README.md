# PoRA: Population-Routed Low-Rank Adaptation of Frozen Foundation Models for Camouflaged Object Detection

> **Preface:** This repository provides the official code for the paper "PoRA: Population-Routed Low-Rank Adaptation of Frozen Foundation Models for Camouflaged Object Detection".
> **Note:** The complete source code will be released once the paper is accepted.

---

## 📖 Introduction
Camouflaged object detection (COD) aims to segment targets that exhibit high visual similarity to their surroundings. Given the limited availability of annotated data, recent parameter-efficient transfer learning (PETL) methods adapt large-scale frozen vision foundation models using small, trainable adapters. However, these adapters typically apply a uniform transformation to all image tokens, which ignores the inherent spatial heterogeneity of camouflaged scenes.

To address this limitation, we propose **PoRA**, a **Po**pulation-**R**outed low-rank **A**dapter that employs a per-token router to dynamically mix *K* zero-initialized low-rank experts. Designed as a strictly pointwise mechanism without explicit spatial priors, PoRA autonomously learns to specialize across diverse token populations. 

Integrating PoRA with a frozen **DINOv2-L** encoder requires training only **6.83 M parameters (2.2% of the total)**. Experiments on four standard COD benchmarks show that PoRA achieves state-of-the-art results, outperforming existing methods on all sixteen metric-dataset combinations!

## 🚀 Training and Testing

### Datasets
We utilize four standard Camouflaged Object Segmentation benchmarks for our experiments:
*   **NC4K**
*   **COD10K**
*   **CAMO**
*   **CHAMELEON**

📥 **Download the datasets from the following link:**
*   **Baidu Pan:** [https://pan.baidu.com/s/1JeIBYdc_WlMquFeL_KmDKg](https://pan.baidu.com/s/1JeIBYdc_WlMquFeL_KmDKg) 
*   **Extraction Code:** `hb9c`

## 📊 Results and Checkpoints

PoRA achieves state-of-the-art results across the board. For example, it reduces the Mean Absolute Error (MAE) on the challenging CAMO dataset from 0.036 to 0.027 and improves the structure measure ($S_{\alpha}$) from 0.889 to 0.918.

📥 **Pre-trained Checkpoints:**
*   **Baidu Pan:** [https://pan.baidu.com/s/1OaNTnDbXfn0hVApugE01UA?pwd=8373](https://pan.baidu.com/s/1OaNTnDbXfn0hVApugE01UA?pwd=8373)
*   **Extraction Code:** `8373`

📥 **Pre-computed Segmentation Results:**
*   **Baidu Pan:** [https://pan.baidu.com/s/15vctUfYDdjuTz80SF7uAnQ](https://pan.baidu.com/s/15vctUfYDdjuTz80SF7uAnQ)
*   **Extraction Code:** `t53k`

## 🛠️ Architecture Highlights
Our framework utilizes a fully frozen **DINOv2-L** encoder where every block is preceded by a PoRA prompt stream. Features are extracted at intermediate blocks and processed by:
1.  **CSCA (Cross-Scale Contrast Aggregation):** Fuses multi-scale pyramid levels using their cross-scale statistics.
2.  **GBTC (Gated Boundary-Aware Texture Contrast):** Extracts boundary evidence from local texture contrast, gated by a consistency ratio to distinguish true boundaries from artificial camouflage textures.

## 📧 Contact
If you have any questions, please feel free to contact me via email at: **lixujie101@aliyun.com**
README.md
目前显示的是“README.md”。
