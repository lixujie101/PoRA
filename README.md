# PoRA: Population-Routed Low-Rank Adaptation of Frozen Foundation Models for Camouflaged Object Detection

> **Preface:** This repository provides the official code for the paper "PoRA: Population-Routed Low-Rank Adaptation of Frozen Foundation Models for Camouflaged Object Detection".
> **Note:** The complete source code will be released once the paper is accepted.

---

## 📖 Introduction
we propose **PoRA**, a **Po**pulation-**R**outed low-rank **A**dapter that employs a per-token router to dynamically mix *K* zero-initialized low-rank experts. Designed as a strictly pointwise mechanism without explicit spatial priors, PoRA autonomously learns to specialize across diverse token populations. 

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

PoRA achieves state-of-the-art results across the board. Experiments on four standard COD benchmarks show that PoRA achieves state-of-the-art results, outperforming existing methods on all sixteen metric–dataset combinations.

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

