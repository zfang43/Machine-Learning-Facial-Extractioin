# Facial Emotion Recognition: Machine Learning Model Evaluation & Selection
<img src="figs/CE.jpg" alt="Compound Emotions" width="500"/>
(Image source: https://www.pnas.org/content/111/15/E1454)

## Project Summary
In this project, we developed a classification engine for facial emotion recognition. Our primary goal was to conduct a rigorous model evaluation and selection process, balancing model complexity against computational efficiency. By analyzing **78 specific fiducial points** on facial images, we extracted geometric features to distinguish between various emotional states.



## Methodology

### Feature Engineering
We analyzed the distributions of vertical distances between key facial landmarks to identify emotional markers:
* **Brow Compression:** Distances between the right pupil (1) and right brow peak (21). Analysis shows the distance of an angry face tends to be shorter than that of a surprised face.
* **Mouth Shape:** Distances between the right mouth corner (50) and the midpoint of the upper lip (52). For instance, a happy face typically exhibits a shorter distance compared to a sad face.



### Models Evaluated
To find the optimal balance of complexity and efficiency, we benchmarked the following strategies:
* **Baseline Model:** Initial predictive benchmark for performance comparison.
* **XGBoost & XGBoost + SMOTE:** Gradient boosting with oversampling to handle class imbalance.
* **PCA + Linear Discriminant Analysis (LDA):** Dimensionality reduction combined with linear classification.
* **Random Forest:** Ensemble-based decision trees.
* **K-Nearest Neighbors (KNN):** Distance-based classification.
* **PCA + XGBoost:** Feature reduction combined with gradient boosting for optimized efficiency.

## Evaluation & Decision Making
As data scientists, our decisions were supported by sound evidence through model assessment, validation, and cross-comparison. We focused on reproducibility and the clear communication of evidence to justify our final model selection, walking the fine line between model complexity and computational cost.

### 1. Model Evaluation & Final Selection

After benchmarking multiple strategies, **XGBoost + SMOTE** was selected as our final model. The decision was driven by its ability to balance high predictive power with the computational efficiency required for real-time applications.

### 2. Predictive Performance
The model was evaluated on unseen test images, achieving strong results in both accuracy and class separability:
* **Accuracy:** 71.44%
* **AUC (Area Under Curve):** 0.8111



### 3. Computational Efficiency (Running Time)
A critical requirement for this project was minimizing **testing latency** without compromising prediction quality. While the training phase is computationally intensive, the resulting model is highly optimized for deployment.

| Phase | Task | Duration (Seconds) |
| :--- | :--- | :--- |
| **Preparation** | Feature Construction (Training) | 0.48s |
| **Preparation** | Feature Construction (Testing) | 0.13s |
| **Optimization** | Model Training (XGBoost + SMOTE) | 232.83s |
| **Execution** | **Model Prediction (Testing)** | **0.37s** |



## Conclusion of Evidence
While the **XGBoost + SMOTE** model achieved a similar accuracy to our baseline, it was chosen for two decisive reasons:
* **Higher AUC:** A result of 0.8111 indicates significantly better performance in distinguishing between emotion classes compared to the baseline.
* **Superior Speed:** The testing/prediction time is drastically lower (0.37s), making this engine efficient even when computational resources are limited.

#### Team members:
Weiwei Song, Changhao He, Aurore Gosmant, Zi Fang, Jimmy Smiley


---






