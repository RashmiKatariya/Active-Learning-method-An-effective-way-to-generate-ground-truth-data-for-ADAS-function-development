
# Active Learning for Auto-Labeling

## 🧠 Project Title
**Active-Learning Method: An Effective Way to Generate Ground Truth Data for ADAS Function Development**

## ✍️ Author
Rashmi M. Katariya  
Continental Automotive

---

## 📌 Problem Statement

In autonomous driving, a significant challenge is the lack of valid and labeled data to train models effectively—especially for rare or unusual situations. Manual labeling of the vast amount of data collected by vehicle sensors is time-consuming and inefficient.

**Objective**:  
To improve the data labeling process using an *Active Learning* method that reduces manual efforts and enhances data quality.

---

## 📚 Literature Survey

Referenced works span from foundational studies in Active Learning and Semi-Supervised Learning to domain-specific applications like remote sensing and art classification. Key references include:

- McCallum & Nigam (1998)
- Tuia et al. (2009)
- Hui Li et al. (2009)
- Burr Settles (2010)
- Wang et al. (2015)
- Zihao Yu (2022)

---

## 🔍 What is Active Learning?

Active Learning is a **semi-supervised machine learning** technique where the algorithm queries the most informative data to label, involving humans only where needed.

![Active Learning Loop](https://i.imgur.com/DZCvRt3.png)  
*Figure 1: Active Learning Process Overview*

---

## 🧪 Methodology

### Tools Used
- **YOLOv3** for initial object detection
- **YOLOv5 (s & n)** and **YOLOv8 (s & n)** for training and evaluation

### Steps:
1. Manually label a small subset of the data
2. Train a lightweight model
3. Use the model to predict on remaining data
4. Apply **Least Confident** and **Entropy-based** strategies to rank unlabeled frames
5. Label the most uncertain frames
6. Retrain the model with new data
7. Repeat steps 3–6 until performance stabilizes

---

## 📊 Querying Strategies

1. **Least Confident Sampling**: Selects samples where the model is least confident.
2. **Entropy-Based Sampling**: Uses entropy as a measure of uncertainty for each prediction.

Both approaches aim to maximize information gain with fewer labeled samples.

---

## ⚙️ Proposed Architecture

![Proposed Methodology Flow](https://i.imgur.com/bvZqzAf.png)  
*Figure 2: Flow of Proposed Methodology using Active Learning*

---

## 🖼️ Results (Output Images)

### YOLOv5 Results:

**Least Confident Strategy (10 iterations)**  
![YOLOv5 Least Confident](https://i.imgur.com/iv9sD7H.png)

**Entropy Based Strategy (10 iterations)**  
![YOLOv5 Entropy Based](https://i.imgur.com/kdK4ZFV.png)

### YOLOv8 Results:

**Least Confident Strategy (6 iterations)**  
![YOLOv8 Least Confident](https://i.imgur.com/GU5cFQx.png)

**Entropy Based Strategy (6 iterations)**  
![YOLOv8 Entropy Based](https://i.imgur.com/9YQqLaZ.png)

---

## ✅ Output Visualization

**Validated Labels for Each Frame**  
![Validated Labels](https://i.imgur.com/LLGHE9z.png)

**Predicted Labels with Confidence**  
![Predicted Labels](https://i.imgur.com/SxSRAgK.png)

---

## 🔮 Future Scope

- Explore additional models to enhance efficiency
- Reduce manual labeling effort by 5–35%
- Integrate the model with labeling tools like **Canvas**
- Draft in progress for SIAT (Symposium on International Automotive Technology)

---

## 📌 Summary

This project presents a significant step toward automated data labeling for ADAS development, combining modern deep learning techniques with uncertainty-driven sampling. The results show that informed labeling can save time, cost, and effort while improving model performance.
