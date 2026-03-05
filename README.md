# Synthetic Image Generation with GAN (DCGAN)

Generate synthetic (“fake”) images using a **Generative Adversarial Network (GAN)**.  
This project trains a **DCGAN** to learn the distribution of a dataset and produce new, realistic-looking samples from random noise.

> **Note:** These images are *synthetic*, created by the model — not copied from the dataset.

---

## ✨ Project Highlights
- ✅ DCGAN training loop (Generator vs Discriminator)
- ✅ Stabilization tricks (label smoothing, noise injection optional)
- ✅ Saves generated image grids during training
- ✅ Checkpoint saving + inference script

---

## 🧠 How GAN Works (Quick)
- **Generator (G):** takes random noise `z` → produces a fake image
- **Discriminator (D):** receives an image → predicts real vs fake
- Training is adversarial: **G tries to fool D**, **D tries to catch G**

---

## 📦 Dataset
This repo is set up for:
- **Fashion-MNIST** (default, 28×28 grayscale)  
You can switch to CIFAR-10 or custom datasets with minor changes.

---

## 🏗️ Model Architecture (DCGAN)
**Generator**
- Dense → reshape → Conv2DTranspose blocks → output image (tanh)

**Discriminator**
- Conv2D blocks → flatten → sigmoid output (real/fake)

---

## 🚀 Getting Started

### 1) Clone the repo
```bash
git clone <YOUR_REPO_URL>
cd <YOUR_REPO_NAME>
