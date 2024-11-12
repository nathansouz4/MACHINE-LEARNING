# Chapter 5: Feature Engineering

### Introduction
- The key to boosting ML model performance often lies in **feature engineering** rather than complex algorithms or hyperparameter tuning.
- This chapter explores common feature engineering techniques, pitfalls like data leakage, and strategies for creating effective features.

---

## 1. Learned Features vs. Engineered Features
- **Deep learning** can learn many features from raw data, reducing the need for manual feature engineering, especially in image and text data.
- However, most ML applications still require **handcrafted features**, particularly for structured data or domain-specific knowledge (e.g., spam detection in text).

---

## 2. Common Feature Engineering Operations
1. **Handling Missing Values**
   - **Types of Missing Values**:
     - **MNAR**: Missing Not At Random (e.g., high incomes are often undisclosed).
     - **MAR**: Missing At Random (e.g., certain groups omit specific values).
     - **MCAR**: Missing Completely At Random (rarely occurs).
   - **Strategies**: 
     - **Deletion**: Remove rows or columns with missing data, cautiously.
     - **Imputation**: Fill missing values with defaults or statistical values (mean, median), though it risks introducing bias.

2. **Scaling**: 
   - Scale features to a common range (e.g., [0, 1]) or standardize (zero mean and unit variance) to avoid disproportionate importance from larger values.

3. **Discretization**: 
   - Turn continuous features into categories (e.g., income brackets) to simplify learning, particularly useful when data is limited.

4. **Encoding Categorical Features**: 
   - For large, evolving categories (e.g., product brands on Amazon), use techniques like **hashing** to manage unseen or new categories without overwhelming model space.

5. **Feature Crossing**: 
   - Combine multiple features to capture nonlinear relationships (e.g., marital status with children). Important for simpler models (e.g., linear regression) but can lead to overfitting.

6. **Positional Embeddings**: 
   - Useful in **NLP** and **computer vision** tasks where position matters. Fixed or learned embeddings can encode position information for models processing data in parallel (e.g., transformers).

---

## 3. Data Leakage
- **Data Leakage** happens when information not available during inference "leaks" into training, leading to overly optimistic results and potential production failures.
- **Examples**:
  - **Patient position** on a scan inadvertently used as an indicator of illness.
  - **Font type** on scans linked with severity due to hospital-specific labeling.

- **Common Causes of Data Leakage**:
  - **Improper Time Splits**: Splitting time-correlated data randomly instead of by time.
  - **Scaling Before Splitting**: Using entire data stats instead of just training data for scaling or imputing.
  - **Duplicates in Data**: Failure to remove duplicates before splitting.
  - **Group Leakage**: Related examples (e.g., repeated CT scans of a patient) appearing in different splits.

---

## 4. Engineering Good Features
1. **Feature Importance**:
   - Measure feature importance using tools like **SHAP** or built-in functions (e.g., XGBoost). Helps understand feature contribution and aids interpretability.

2. **Feature Generalization**:
   - Good features should generalize well to unseen data.
   - Consider feature **coverage** and **distribution consistency** across train/test splits.
   - Strike a balance between **generalization and specificity** (e.g., using broad "rush hour" vs. precise "hour of the day").

---

## Summary of Best Practices
- Split data by time, especially for time-dependent tasks.
- Perform scaling and normalization after splitting to avoid leakage.
- Use train data stats for scaling and handling missing values.
- Understand data generation processes and involve domain experts when possible.
- Monitor feature importance and ensure features generalize well.
- Remove features that are no longer useful to avoid technical debt.

With a robust set of features, we’re ready to dive into model training, which we’ll explore in the next chapter. Remember, feature engineering is an ongoing process throughout the lifecycle of any production ML system.
