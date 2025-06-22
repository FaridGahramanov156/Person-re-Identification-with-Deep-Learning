# Person-re-Identification-with-Deep-Learning

This repository contains a deep learning project focused on **Person Re-Identification (ReID)** using the [Market-1501 dataset](https://github.com/zhunzhong07/Market-1501). The goal is to build a system that can recognize and match identities of people across multiple camera views using Convolutional Neural Networks (CNNs) and PyTorch.

---

## 📁 Project Structure
EE417_project/
├── data/
│ └── Market-1501/ # Contains bounding_box_train, bounding_box_test, query
├── EE417_Project(1).ipynb # Main notebook with dataset setup, transforms, and dataset class
├── models/ # Placeholder for saved models
├── README.md # This file


---


---

## 🧠 Methodology

### 🧩 Triplet Loss Function

This project uses the **Triplet Loss** function to train a model that minimizes the distance between embeddings of the **same person** and maximizes it for **different persons**.

- **Anchor** – an image of a person
- **Positive** – another image of the same person
- **Negative** – an image of a different person

The network learns to satisfy:
\[
\|f(a) - f(p)\|^2 + \text{margin} < \|f(a) - f(n)\|^2
\]

Where:
- \(f(.)\) is the embedding function (usually a CNN)
- margin is a constant (e.g., 0.3)

---

## 📊 Dataset: Market-1501

- 1,501 identities
- 32,668 bounding box images
- Captured across 6 cameras
- Structured into:
  - `bounding_box_train/`
  - `bounding_box_test/`
  - `query/`

---

## 🧪 Features

- ✅ Custom PyTorch Dataset class for Market-1501
- ✅ Embedding network using ResNet50 (or MobileNet, customizable)
- ✅ Triplet loss-based embedding training
- ✅ Top-k gallery matching based on Euclidean distance
- ✅ Results visualization

---

## 📸 Sample Results

> Below is a sample result showing a **query image** and its **top-5 most similar gallery images** predicted by the model.

| Query Image | Top-5 Predicted Matches |
|-------------|--------------------------|
| ![Query](results/query_example.jpg) | ![Top1](results/top1.jpg) ![Top2](results/top2.jpg) ![Top3](results/top3.jpg) ![Top4](results/top4.jpg) ![Top5](results/top5.jpg) |

✅ **Correct matches are bordered in green**, incorrect in red.

> You can generate your own results using the `evaluate()` section in the notebook.

---
