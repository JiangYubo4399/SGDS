# SGDS-Net: SAM-Guided Dual-Student Network for Weakly Supervised Semantic Segmentation

**Official PyTorch implementation of the paper: _"SGDS-Net: SAM-Guided Dual-Student Network for Weakly Supervised Semantic Segmentation via Generating Higher Quality CAM"._**
![fig3](https://github.com/user-attachments/assets/9a6154d5-9f83-4e7e-9f8d-dbb368035fdc)

## 🔍 Introduction

Semantic segmentation in remote sensing demands fine-grained annotations, which are costly and time-consuming. SGDS-Net addresses this challenge by introducing a weakly supervised approach relying only on **image-level labels**. It innovatively combines:

- A **Dual-Student Network** for mutual learning to suppress confirmation bias.
- A **SAM-Guided CAM (SGC)** module to refine Class Activation Maps using the powerful **Segment Anything Model (SAM)**.
- A **dynamic thresholding strategy** and **GMM-based denoising** to enhance pseudo-label quality.

Our method achieves **state-of-the-art mIoU** on benchmark remote sensing datasets: Potsdam, Vaihingen, and iSAID.

---

## 🧠 Architecture Overview

- **Backbone:** Vision Transformer (ViT-B)
- **Dual-Student Framework:** Two parallel segmentation branches with unshared weights
- **CAM Refinement:** Integration with frozen SAM using peak tokens
- **Loss Functions:**
  - Cross-Entropy Loss with pseudo-label supervision
  - Cosine discrepancy loss between student features
  - GMM-based loss filtering for noise reduction
  - Consistency regularization loss

![Model Overview](assets/overview.png)
##  Result
![fig5](https://github.com/user-attachments/assets/75f3634f-dfa2-40fc-8604-0d40e6445909)



The code will be released publicly in June 2025. Please stay tuned for updates and further information. ：)



