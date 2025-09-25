# 🎶 Singing Voice Separation – Replications

This repo contains two Jupyter notebooks replicating state-of-the-art **singing voice separation** methods.

## 📄 Papers

1. **Singing Voice Separation Using a Deep CNN Trained by Ideal Binary Mask and Cross Entropy**  
   Lin et al., Neural Computing and Applications (2019)  
   [arXiv:1812.01278](https://doi.org/10.48550/arXiv.1812.01278)  
   → [`ConvTrain.ipynb`](./ConvTrain.ipynb)

2. **Singing Voice Separation with Deep U-Net Convolutional Networks**  
   Jansson et al., ISMIR 2017  
   [PDF](https://archives.ismir.net/ismir2017/paper/000171.pdf)  
   → [`Utrain.ipynb`](./Utrain.ipynb)

## 🧠 Techniques

- **CNN + Ideal Binary Mask (Lin et al. 2019)**  
  - Treats spectrogram T–F bins as image pixels.  
  - Uses pixel-wise classification with cross-entropy loss.  
  - Trained on Ideal Binary Mask (IBM) labels → direct voice/accompaniment separation.  
  - Removes need for Wiener filtering post-processing.

- **U-Net (Jansson et al. 2017)**  
  - Encoder–decoder CNN with skip connections on spectrograms.  
  - Learns masks for vocals and accompaniment.  
  - Captures both local detail and global musical structure.

## ⚙️ Implementation

- Framework: Python + PyTorch (via notebooks)  
- Input: STFT log-magnitude spectrograms of music mixtures  
- Output: Separated vocals and accompaniment (via inverse STFT)  
- Dataset: MUSDB18 / iKala (recommended)  

---

### 🚀 Files
- `ConvTrain.ipynb` – CNN + IBM + cross-entropy model  
- `Utrain.ipynb` – U-Net based model  

---

### 📌 References
- Lin, K.W.E. et al., *Singing Voice Separation Using a Deep CNN Trained by Ideal Binary Mask and Cross Entropy*, arXiv:1812.01278 (2018)  
- Jansson, A. et al., *Singing Voice Separation with Deep U-Net Convolutional Networks*, ISMIR 2017  
