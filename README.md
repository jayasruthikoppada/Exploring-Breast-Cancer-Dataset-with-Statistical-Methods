Project Title:
# Exploring Breast Cancer Dataset with Statistical Methods and Identifying Benign or Malignant Tumors using Logistic Regression

#### **Objective:**
This project analyzes the Breast Cancer Wisconsin (Diagnostic) dataset using statistical methods and logistic regression to distinguish between benign and malignant tumors. It applies univariate, bivariate, and multivariate analyses, along with statistical testing, to extract meaningful insights and predict cancer diagnoses.

---

### **Dataset Information:**

#### **Source:**
- UC Irvine Machine Learning Repository:  
[Breast Cancer Wisconsin Dataset](https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic)  

#### **Description:**
- **Total Samples**: 569 (357 benign, 212 malignant)  
- **Attributes**: 32 columns, including an ID column, a diagnosis column, and 30 feature columns.  
- **Features**: Measurements of tumor cells (e.g., radius, texture, perimeter, area, etc.) in three variations:  
  - Mean  
  - Standard Error (SE)  
  - Worst (maximum value among the top three largest values)  

#### **Key Notes:**
- The dataset is complete with no missing values.  
- Feature values are real-valued and continuous.  

---

### **Methodology:**

#### **1. Data Exploration:**
- **Univariate Analysis**:
  - Generated density plots and normal probability plots for the mean of each feature.
  - Conducted Kolmogorov-Smirnov (K-S) test to assess normality.

- **Bivariate Analysis**:
  - Created scatter plots using "Diagnosis" as a color code to study relationships between variables.
  - Observed significant positive correlations, particularly among 'Radius Mean,' 'Area Mean,' and 'Perimeter Mean.'

- **Multivariate Analysis**:
  - Used heatmaps to visualize correlations between features.  
  - Highlighted strong positive correlations among "Worst" features, suggesting their importance in cancer diagnosis.

---

#### **2. Statistical Testing:**
- **Approach**:
  - Conducted a Two-Sample Independent t-Test to compare mean feature values between benign and malignant groups.
  - Used Welch's t-Test for unequal variances when necessary.

- **Hypotheses**:
  - Null Hypothesis (H0): Mean values for benign and malignant subsets are equal.  
  - Alternative Hypothesis (H1): Mean values differ significantly.

- **Results**:
  - Most features showed statistically significant differences (p < 0.05), indicating their potential for differentiation.  

---

#### **3. Logistic Regression:**
- **Model Development**:
  - Normalized the dataset to eliminate scale differences.  
  - Checked multicollinearity using Variance Inflation Factor (VIF).  
  - Developed a reduced model to focus on significant predictors.

- **Results**:
  - Observed strong predictors like "Concave Points Mean" (odds ratio ~162) for malignant diagnosis.  
  - The model fit was evaluated through changes in deviance and residuals, indicating a good predictive ability.

---

### **Key Findings:**
1. **Feature Importance**:
   - Features such as "Concave Points Mean" and "Texture Mean" strongly predict malignancy.
2. **Statistical Significance**:
   - Welch’s t-Test revealed substantial differences between benign and malignant cases for most features.
3. **Model Performance**:
   - Logistic regression provided a robust model with strong predictors for cancer diagnosis.

---

### **Discussion and Limitations:**
- The independence of data points remains ambiguous, as the dataset does not clarify if observations represent distinct patients or multiple samples from the same patient.  
- Future work should include validation datasets or cross-validation techniques to enhance model reliability.

---

### **How to Run the Project:**

1. **Requirements:**
   - Python libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `statsmodels`, `sklearn`.  

2. **Steps:**
   - Load the dataset and preprocess it by normalizing features.  
   - Perform exploratory data analysis (EDA) using the provided statistical tests and plots.  
   - Build the logistic regression model and interpret the results.  

3. **Expected Output:**
   - Detailed statistical summaries and plots for feature analysis.  
   - Logistic regression results with odds ratios and p-values.  

---

### **References:**

1. Mayo Clinic. Breast Cancer Overview:  
   [Mayo Clinic Link](https://www.mayoclinic.org/diseases-conditions/breast-cancer/symptoms-causes/syc-20352470)  

2. Street, W. N., Wolberg, W. H., & Mangasarian, O. L. Nuclear Feature Extraction for Breast Tumor Diagnosis.  
   [Semantic Scholar](https://api.semanticscholar.org/CorpusID:14922543)  

3. Julie, V. & David, H. Introductory Statistics for the Life and Biomedical Sciences.  
   [OpenIntro Biostatistics](https://www.openintro.org/book/biostat/)  

