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



### Team members:
* Weiwei Song
* Changhao He
* Aurore Gosmant
* Zi Fang
* Jimmy Smiley


---

