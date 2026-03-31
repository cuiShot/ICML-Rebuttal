**Table 1: Configurations of the 10 fixed base models used in the controlled ensemble experiments.** *The models are selected to ensure algorithmic diversity (covering linear, tree-based, kernel, probabilistic, and distance-based paradigms) and complementary bias-variance trade-offs. Hyperparameters reflect an offline-tuned and frozen setup to guarantee reproducibility.*

| Model Name | Algorithm Paradigm | Key Hyperparameters (Offline Tuned & Frozen) | Description & Rationale |
| :--- | :--- | :--- | :--- |
| **Logistic Regression** | Linear Model | `max_iter=2000`, `C=0.8`, `solver='lbfgs'`, `class_weight='balanced'` | Provides a fast, stable, and interpretable high-bias linear baseline. |
| **Decision Tree** | Tree Model | `max_depth=8`, `min_samples_split=8`, `min_samples_leaf=3`, `class_weight='balanced'` | A basic tree model that captures fundamental non-linear feature interactions. |
| **Random Forest** | Tree Ensemble (Bagging) | `n_estimators=300`, `max_depth=14`, `min_samples_split=6`, `class_weight='balanced_subsample'` | A parallel ensemble method offering high generalization and balanced variance. |
| **Extra Trees** | Tree Ensemble (Bagging) | `n_estimators=300`, `max_depth=14`, `min_samples_split=6`, `bootstrap=True` | Injects stronger randomization into the splitting process, highly complementary to Random Forest. |
| **XGBoost** | Gradient Boosting | `n_estimators=300`, `max_depth=5`, `learning_rate=0.04`, `subsample=0.85`, `colsample_bytree=0.85` | A low-bias sequential boosting model with exceptionally strong learning capacity. |
| **CatBoost** | Gradient Boosting | `iterations=300`, `depth=6`, `learning_rate=0.04` | A highly stable gradient boosting framework, particularly robust with categorical distributions. |
| **SVM (RBF)** | Kernel Method | `kernel='rbf'`, `C=2.0`, `gamma='scale'`, `probability=True`, `class_weight='balanced'` | Utilizes the kernel trick for complex non-linear mapping in high-dimensional spaces. |
| **Gaussian Naive Bayes** | Probabilistic | *Default configurations* | A lightweight, fast probabilistic baseline that assumes feature independence. |
| **AdaBoost** | Boosting | `n_estimators=150`, `learning_rate=0.3`, `algorithm='SAMME'` | A sequential boosting method that explicitly focuses on hard-to-classify samples. |
| **K-Neighbors (KNN)** | Distance-based | `n_neighbors=9`, `weights='distance'`, `metric='euclidean'` | An instance-based learning method that captures local similarity and neighborhood structures. |
