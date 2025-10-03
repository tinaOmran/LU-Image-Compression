# 📷 LU-Based High-Resolution Image Compression

This project explores the use of **LU decomposition** for compressing high-resolution grayscale images, comparing its performance with standard methods such as **SVD** and **JPEG**. It was developed as part of a Numerical Linear Algebra course at Amirkabir University of Technology.

---

## 📌 Overview

Image compression is essential for reducing storage and transmission costs while preserving visual quality. This project implements and evaluates several compression techniques:

- LU decomposition (with and without pivoting)
- LU combined with quantization and thresholding
- Singular Value Decomposition (SVD)
- JPEG compression
- Block-based filtering and quantization

Each method is assessed using standard image quality metrics: **PSNR** and **SSIM**.

---

## 🧠 Key Concepts

### ✅ LU Decomposition  
Used to approximate the pixel intensity matrix. Variants include:
- LU without pivoting
- LU with partial pivoting
- LU + quantization
- LU + thresholding

### 🧮 SVD Compression  
Keeps only the largest singular values to reduce matrix rank and compress image data.

### 🧊 Quantization & Filtering  
Reduces pixel intensity levels and removes low-variance blocks to shrink image size.

### 📊 Evaluation Metrics  
- **PSNR (Peak Signal-to-Noise Ratio)**: Measures reconstruction accuracy.
- **SSIM (Structural Similarity Index)**: Evaluates perceptual similarity.

---

## 🛠 Technologies Used

- Python 3.x
- NumPy
- OpenCV
- Matplotlib
- scikit-image

---

## 📸 Sample Results

| Method            | PSNR (dB) | SSIM | Compression Ratio |
|------------------|-----------|------|-------------------|
| LU               | 57.16     | 0.9997 | 1.00             |
| LU + Pivot       | 175.22    | 1.0000 | 1.00             |
| SVD              | 23.41     | 0.56   | 0.04             |
| JPEG             | 37.00     | 0.95   | 0.01             |
| Quantized        | 34.90     | 0.84   | 0.06             |
| LU + Quantized   | 41.14     | 0.93   | 0.99             |
| LU + Threshold   | 19.79     | 0.86   | 1.00             |

---

## 📚 References

- Gonzalez & Woods – *Digital Image Processing*
- [Wikipedia: SSIM](https://en.wikipedia.org/wiki/Structural_similarity_index_measure)
- [Wikipedia: PSNR](https://en.wikipedia.org/wiki/Peak_signal-to-noise_ratio)
- [GeeksforGeeks: Quantization](https://www.geeksforgeeks.org/quantization-in-deep-learning)

