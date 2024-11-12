# Chapter 4: Training Data

## Overview
- **Focus on Data Science Perspective**: Unlike Chapter 3, this chapter examines data handling from the perspective of data science.
- **Challenges of Training Data**: Collecting, preparing, and maintaining quality data is complex and essential for effective ML model performance.
- **Bias and Iterative Process**: Emphasizes understanding biases in data and iterative refinement of training datasets for robust ML systems.

## Key Topics 

### 1. Sampling Techniques
- **Nonprobability Sampling**: Includes convenience, snowball, judgment, and quota sampling methods. Quick but may introduce biases.
- **Random Sampling**: Consists of simple random sampling, stratified sampling, weighted sampling, and reservoir sampling, ensuring diverse and representative data selection.
- **Importance Sampling**: Useful for cases where target distribution is unavailable, leveraging a similar distribution as a substitute.

### 2. Labeling Challenges and Techniques
- **Hand Labeling**: Essential but resource-intensive; often poses privacy issues and delays model iteration.
- **Label Multiplicity**: Variations in labeling due to multiple annotators or sources can cause ambiguity. Clear guidelines and data lineage tracking are critical to manage labeling inconsistencies.
- **Natural Labels**: Inherent labels obtained through system feedback, often in tasks like recommendation systems or ETA prediction.
- **Feedback Loop Length**: The delay between model predictions and feedback impacts training iterations and model adaptability.

### 3. Handling Lack of Labels
- **Weak Supervision**: Leverages noisy heuristics to generate labels using labeling functions, as seen in tools like Snorkel.
- **Semi-Supervision**: Uses structural assumptions with a small labeled subset to infer additional labels.
- **Transfer Learning**: Utilizes pretrained models (e.g., BERT, GPT-3) to improve performance on tasks with limited data.
- **Active Learning**: Models selectively request labels for uncertain samples, optimizing annotation efficiency and model performance.

### 4. Class Imbalance
- **Challenges**: Discrepancies in class distribution can lead to ineffective ML models, especially for rare or minority classes.
- **Handling Techniques**:
  - **Evaluation Metrics**: Use class-specific metrics (e.g., precision, recall, F1) over general accuracy, and ROC or precision-recall curves for insight on imbalanced data.
  - **Data-Level Methods**: Resampling methods like undersampling (Tomek links) and oversampling (SMOTE) help balance training datasets.
  - **Algorithm-Level Methods**: Modify loss functions, such as cost-sensitive learning, class-balanced loss, and focal loss, to focus on minority classes.

### 5. Data Augmentation
- **Simple Transformations**: Apply label-preserving changes like rotation, flipping (for images), or synonym replacement (for text) to enhance data volume.
- **Perturbation**: Adds noise to data, improving model robustness against adversarial examples.
- **Data Synthesis**: Generates new data via methods like template-based queries (NLP) or synthetic image generation (computer vision).

## Conclusion
- Training data is foundational to ML model success; creating high-quality data is essential.
- Techniques covered include sampling, labeling strategies, handling class imbalance, and data augmentation to improve model performance.
- These strategies are especially crucial as most ML tasks involve supervised learning, where labeled data directly influences model accuracy.
  
