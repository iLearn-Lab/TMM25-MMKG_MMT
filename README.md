<a id="top"></a>

<div align="center">

# 🌐 Exploiting Multimodal Knowledge Graph for Multimodal Machine Translation

<p>
  <b>Tianjiao Xu</b><sup>1</sup> &nbsp;
  <b>Xuebo Liu</b><sup>2</sup><sup>*</sup> &nbsp;
  <b>Derek F. Wong</b><sup>3</sup><sup>*</sup> &nbsp;
  <b>Yue Zhang</b><sup>4</sup> &nbsp;
  <b>Lidia S. Chao</b><sup>3</sup> &nbsp;
  <b>Min Zhang</b><sup>2</sup> &nbsp;
  <b>Tian Gan</b><sup>1</sup>
</p>

<p>
  <sup>1</sup>Shandong University &nbsp;
  <sup>2</sup>Harbin Institute of Technology, Shenzhen &nbsp;
  <sup>3</sup>University of Macau &nbsp;
  <sup>4</sup>Westlake University
</p>

<p>
  <sup>*</sup> Corresponding authors
</p>

<p>
  <a href="https://ieeexplore.ieee.org/document/11275894/">
    <img src="https://img.shields.io/badge/IEEE_TMM-2025-blue.svg?style=flat-square">
  </a>
</p>

<p>
  <b>A plug-and-play data augmentation framework that leverages multimodal knowledge graphs to enhance multimodal machine translation, especially under low-resource settings.</b>
</p>

</div>


## 📚 Table of Contents

* [📢 Updates](#-updates)
* [📖 Introduction](#-introduction)
* [✨ Highlights](#-highlights)
* [🧩 Pipeline](#-method--framework)
* [🗂 Dataset / Benchmark](#-dataset--benchmark)
* [🚀 Usage](#-usage)
* [📑 Citation](#-citation)
* [📜 License](#-license)

---

## 📢 Updates

* **[03/2025]** Initial release

---

## 📖 Introduction

Multimodal Machine Translation (MMT) improves translation quality by incorporating visual context. However, it suffers from a critical bottleneck: **Lack of large-scale aligned text-image bilingual data**

To address this issue, we propose a **Multimodal Knowledge Graph (MMKG)-based data augmentation framework**.

### 💡 Key Idea

* Align words in bilingual sentences with **entities in MMKG**
* Replace aligned words to generate **pseudo-parallel sentences**
* Retrieve entity-associated images from MMKG
* Apply MixUp-based image fusion

This effectively expands the training corpus and improves translation performance.

📌 As shown in the paper, the method significantly improves MMT performance, especially in low-resource scenarios .

---

## ✨ Highlights

* 🔌 Plug-and-play **data augmentation framework**
* 🧩 Supports **multimodal machine translation**
* 📉 Strong improvements in **low-resource settings**
* 🌐 Leverages **multimodal knowledge graphs (MMKG)**
* ⚡ Easy integration with **FairSeq-based models**

---

## 🧩 Pipeline

1. **MMKG Construction**

   * Extract entities, relations, and images from knowledge graphs

2. **Entity Alignment**

   * Match words in sentences with MMKG entities

3. **Pseudo Data Generation**

   * Replace aligned words to create new sentence pairs

4. **Image Augmentation**

   * Fuse original and KG images via MixUp

5. **Model Training**

   * Train MMT model with augmented data

---

## 🗂 Dataset / Benchmark

We evaluate on:

* 📦 **[Multi30k](https://github.com/multi30k/dataset)**
* 🛒 **[IKEA](https://github.com/sampalomad/IKEA-Dataset)**

### 🔽 Enhanced Dataset Download

* [https://pan.quark.cn/s/8c637d4a2572](https://pan.quark.cn/s/8c637d4a2572)
* Password: `tSJ2`

---

## 🚀 Usage

## ⚙️ 1. Installation

```bash
pip install -r requirements.txt
```
---

### 2. Build MMKG

```bash
python crawl_direct.py
python crawl_indirect.py
```

### 3. Generate Pseudo Data

```bash
python generate_pseudo_data.py
```

---

## 🤗 Citation

If you find this work useful for your research, please kindly cite our paper:

```bibtex
@article{mmkg_mmt,
  author  = {Xu, Tianjiao and Liu, Xuebo and Wong, Derek F. and Zhang, Yue and Chao, Lidia S. and Zhang, Min and Gan, Tian},
  title   = {Exploiting Multimodal Knowledge Graph for Multimodal Machine Translation},
  journal = {IEEE Transactions on Multimedia},
  volume={28},
  pages={1677-1688},
  year    = {2025}
}
```

---

## 📜 License

* Code: Apache License 2.0
* Dataset: CC BY-NC-SA 4.0
