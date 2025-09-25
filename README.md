# Singing-Voice-Separation

# 🎶 Singing Voice Separation – Replications

This repo contains two Jupyter notebooks replicating classic papers on **singing voice separation**.

## 📄 Papers

1. **Spleeter: Music Source Separation Tool with Pre-trained Models**  
   Hennequin et al., 2018  
   [arXiv:1812.01278](https://arxiv.org/abs/1812.01278)  
   → [`Utrain.ipynb`](./Utrain.ipynb)

2. **Monoaural Audio Source Separation using Deep Convolutional Neural Networks**  
   Chandna et al., ISMIR 2017  
   [PDF](https://archives.ismir.net/ismir2017/paper/000171.pdf)  
   → [`ConvTrain.ipynb`](./ConvTrain.ipynb)

## 🧠 Techniques

- **U-Net (Spleeter-inspired)**  
  Encoder–decoder with skip connections on STFT spectrograms, learning time–frequency masks.  
  Optimized with MSE on reconstructed vocals/accompaniment.

- **Fully Convolutional Network (ISMIR 2017)**  
  Deep CNN stack without dense layers, operating directly on spectrograms.  
  Learns binary masks for vocal vs. background.

## ⚙️ Implementation

- Framework: Python + PyTorch (in notebooks)  
- Input: Mixture audio → STFT log-magnitude spectrograms  
- Output: Separated vocals and accompaniment (via inverse STFT)  
- Dataset: MUSDB18 (or similar)  

---

### 🚀 Files
- `Utrain.ipynb` – U-Net training pipeline  
- `ConvTrain.ipynb` – CNN training pipeline  

---

### 📌 References
- Hennequin, R. et al., *Spleeter*, arXiv:1812.01278 (2018)  
- Chandna, P. et al., *Deep CNNs for Voice Separation*, ISMIR 2017  
