# 🔒 Privacy-First AI: Secure Image Classification with Federated Learning & Differential Privacy

## 📌 Overview
This project implements a **privacy-preserving image classification framework** that combines:
- **Federated Learning (FL)** – decentralized training across clients without sharing raw data.  
- **Differential Privacy (DP)** – protects against data reconstruction attacks by adding controlled noise.  
- **Secure Aggregation (SecAgg)** – ensures encrypted client updates during aggregation.  

The goal is to enable **trustworthy AI** in sensitive domains like healthcare and biometrics.

---

## 🚀 Key Features
- Federated setup across **5 simulated clients**.  
- Models adapted for domain-specific tasks:
  - **ResNet-18** → CIFAR-10 (general objects)  
  - **EfficientNet-B2** → ChestMNIST (medical X-rays)  
  - **MobileFaceNet** → CelebA (facial attributes)  
- Applied **Gaussian noise** for DP, achieving ε = 5–10 privacy budgets.  
- Tracked **accuracy, robustness, loss, and communication cost** per round.  

---

## 📂 Datasets
- **CIFAR-10** → 60,000 images, 10 classes (general object recognition).  
- **ChestMNIST (MedMNIST subset)** → 14 chest disease labels from X-rays.  
- **CelebA** → 200K celebrity images with 40 binary facial attributes (20K used).  

---

## 🏗️ Methodology
1. **Data Partitioning** – training data split across 5 clients (i.i.d.).  
2. **Model Training** – local epochs per round, followed by secure aggregation.  
3. **Differential Privacy** – Gaussian noise added to model weights during rounds.  
4. **Evaluation Metrics** – Accuracy, Robustness, Privacy Budget (ε), Communication Cost.  

---

## 📊 Results
- **ResNet-18 (CIFAR-10):** 92% accuracy, robust convergence, ~12 MB per round.  
- **EfficientNet-B2 (ChestMNIST):** 94% accuracy, robustness score ~0.92, ε = 5–10.  
- **MobileFaceNet (CelebA):** 81% accuracy with ε = 10, stable privacy-preserving performance.  

📈 Demonstrated that **privacy-preserving FL can maintain 82–94% accuracy** while ensuring strong privacy guarantees.  

---

## 🔮 Future Work
- Scale beyond 5 clients to reflect real-world FL deployments.  
- Support **non-i.i.d. data distributions** and client dropout scenarios.  
- Explore advanced privacy mechanisms like **homomorphic encryption** and **secure enclaves**.  
- Optimize for **edge deployment** on mobile/IoT devices.  

---

## 🛠️ Tech Stack
- **Languages/Frameworks**: Python, PyTorch, NumPy, Matplotlib  
- **Concepts**: Federated Learning, Differential Privacy, Secure Aggregation  
- **Models**: ResNet-18, EfficientNet-B2, MobileFaceNet  
- **Datasets**: CIFAR-10, ChestMNIST, CelebA  


---
