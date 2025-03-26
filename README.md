# Time Series Feature Extraction for Human Activity Recognition

This project focuses on extracting meaningful time-domain features from multivariate time-series sensor data to classify different human activities. The dataset is derived from the AReM (Activity Recognition system based on Multisensor data fusion) dataset provided by the UCI Machine Learning Repository.

## 📂 Dataset

- **Source:** [UCI AReM Dataset](https://archive.ics.uci.edu/ml/datasets/Activity+Recognition+system+based+on+Multisensor+data+fusion+(AReM))
- **Structure:** 7 folders representing 7 different human activities (e.g., walking, standing, sitting, bending1, bending2, etc.)
- Each folder contains multiple `.csv` files with multivariate time-series data collected via 6 sensor channels (avg_rss12, var_rss12, avg_rss13, var_rss13, avg_rss23, var_rss23)

## 📊 Objective

The primary goal is to extract **time-domain features** from the sensor data that can later be used for time-series classification tasks.

---

## 🔍 Tasks Completed

### 1. Dataset Preprocessing
- Loaded sensor data from 7 activity folders.
- Separated the data into training and testing sets:
  - `bending1` and `bending2`: first 2 files used for testing.
  - Other activities: first 3 files used for testing.
  - Remaining used for training.

### 2. Time-Domain Feature Extraction
Extracted the following features for each sensor signal:
- Minimum
- Maximum
- Mean
- Median
- Standard Deviation
- First Quartile (25%)
- Third Quartile (75%)

These features were computed for each of the 6 sensor channels.

### 3. Statistical Confidence Estimation
- Estimated the **standard deviation** of each feature using Python’s `bootstrap` method.
- Calculated **90% bootstrap confidence intervals** for the standard deviation of each feature.

### 4. Feature Selection
- Based on the distribution and statistical importance, selected the top 3 most important features for further analysis.

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- SciPy
- Jupyter Notebook

---

## 📌 Future Work

- Apply classification models (Random Forest, SVM, etc.) on extracted features.
- Visualize feature importance using techniques like PCA or feature correlation heatmaps.
- Extend to frequency-domain features for better accuracy.

---


