# Hate Speech Detection on Twitter

This project replicates the findings of the 2017 research paper:  
**"Automated Hate Speech Detection and the Problem of Offensive Language" by Davidson et al.**,  
and extends it by evaluating additional machine learning models including XGBoost.

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Objective](#objective)
- [Models Implemented](#models-implemented)
- [Evaluation Metrics](#evaluation-metrics)
- [Results Summary](#results-summary)
- [License](#license)

---

## Project Overview
This project aims to automatically classify tweets into three categories:
- **Hate Speech**
- **Offensive Language**
- **Neither**

The classification is based on textual features such as n-grams, part-of-speech tags, and tweet-level metadata. The original methodology from Davidson et al. was faithfully replicated and expanded upon using modern techniques.

---

## Technologies Used

- Python
- Scikit-learn
- NLTK
- XGBoost
- Jupyter Notebook 

---

## Dataset

- **Name**: [Hate Speech and Offensive Language Dataset](https://github.com/t-davidson/hate-speech-and-offensive-language)
- **Size**: ~24,000 labeled English tweets
- **Labels**:
  - `0`: Hate Speech
  - `1`: Offensive Language
  - `2`: Neither

---

## Objective

1. **Replicate the methodology and results** of the Davidson et al. (2017) paper.
2. **Add additional classifiers** not tested in the original study (e.g., XGBoost).
3. **Compare the performance** of different models using precision, recall, and F1-score.

---

## Models Implemented

| Model               | Description                          |
|--------------------|--------------------------------------|
| Logistic Regression | Paper's final model (OvR, L2)       |
| Naive Bayes         | Classic baseline model               |
| Decision Tree       | Non-linear, interpretable model      |
| Random Forest       | Ensemble of decision trees           |
| Linear SVM          | Strong performer for text data       |
| **XGBoost**         | Extended model for performance boost |

---

## Evaluation Metrics

- **Accuracy**
- **Precision, Recall, F1-score (per class)**
- **Macro F1-score**
- **Confusion Matrix**

Each model was evaluated using **5-fold cross-validation** and a **10% hold-out test set**, consistent with the original paper's methodology.

---

## Results Summary

| Model            | Accuracy | Macro F1 | Notes                     |
|------------------|----------|----------|---------------------------|
| Logistic Reg.    | 91%      | 0.69     | Matches paper baseline    |
| Naive Bayes      | 87%      | 0.66     | Fast but weaker on Class 0|
| Decision Tree    | 89%      | 0.72     | Overfits slightly         |
| Random Forest    | 89%      | 0.68     | Strong but Class 0 suffers|
| Linear SVM       | 90%      | 0.71     | Best overall in paper     |
| **XGBoost**      | **~91%** | **0.72** | Best in extension phase   |


---

This project is for educational purposes. Attidution is given to Davidson et al. (2017) for the original dataset and methodology
 


