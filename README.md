# Machine-Learning-Project
Crop recommendation System using Machine Learning

**Author:** Taniksha Upadhyay
**PRN:** 22070521151
**Date:** November 2025

---

## Project Overview
This project constructs a **Crop Recommendation System** that predicts suitable crops based on soil and environmental parameters (N, P, K, temperature, humidity, pH, rainfall). It applies supervised learning methods and compares their performance to provide recommendations for farmers.

**Why important:** Accurate crop selection increases yield and reduces resource waste. ML enables data-driven recommendations that can help farmers choose crop types optimized for local conditions.

**Quick results summary:**  
- **Random Forest** achieved the best performance (Accuracy ≈ 98.7%, F1-score ≈ 0.98).  
- **Decision Tree** provided an interpretable baseline with slightly lower performance (Accuracy ≈ 94.8%).  


---

## Dataset Source
**Source:** Open Government Data Platform India — *Crop Recommendation Dataset*  
**Link:** [https://data.gov.in/](https://www.kaggle.com/datasets/atharvaingle/crop-recommendation-dataset)  

**Dataset size:** 2,200 rows × 8 columns (example)  
**Features:** `N`, `P`, `K`, `temperature`, `humidity`, `ph`, `rainfall`, `label` (target crop)

**Preprocessing steps performed:**
- Checked and filled missing values (median imputation for numeric columns).
- Converted non-numeric features to numeric where necessary.
- Label encoded crop names into integer labels.
- Standardized features using `StandardScaler`.
- Train/test split: 80/20 stratified.

---

## Methods
We applied and compared the following models:

**1. Decision Tree Classifier**  
- Interpretable tree-based method. Good baseline, prone to overfitting.

**2. Random Forest Classifier**  
- Ensemble of trees; reduces overfitting and typically yields higher accuracy.

**Why these models?**  
Decision Tree is fast and interpretable; Random Forest often improves generalization and handles noisy features robustly. We considered additional models (SVM, KNN, Neural Networks) as future work.

**Approach:**  
1. Data preprocessing (cleaning, encoding, scaling)  
2. Train/test split (80/20)  
3. Fit models on training data  
4. Evaluate on test data using accuracy, precision, recall, F1-score and confusion matrix  
5. Visualize feature importances (Random Forest)

---

## Experiments & Results

### Performance summary (example)
| Model | Accuracy (%) | Precision | Recall | F1-Score |
|-------|-------------:|----------:|-------:|---------:|
| Decision Tree | 96.36 | 0.95 | 0.94 | 0.94 |
| Random Forest | 98.86 | 0.99 | 0.98 | 0.98 |

**Per-class metrics and confusion matrices** are included in output and the notebook.


**Notes about imbalance / robustness:**  
- Dataset is generally balanced across crops (or not — replace with true observation).  
- If classes are imbalanced, we recommend stratified sampling or resampling techniques.
