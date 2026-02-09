# Introduction to Machine Learning and Deep Learning

Additional course materials, ELTE Faculty of Informatics - 2024/25 spring semester

## Course Structure and Grading

- **40%** of the final grade comes from homework assignments.
- **60%** comes from three mini-projects (each has a two-week deadline, see schedule below).
- **No final exam** for this course.

## About the Mini-Projects

- There will be **3 mini-projects** throughout the semester.
- You must complete at least **2** mini-projects to receive a grade.
- Solutions must be submitted via **Canvas** before the strict deadline.
- Late submissions (up to 24 hours) will receive **half** the available points.
- Plagiarism is strictly prohibited.
- You are encouraged to use external resources but must **cite them properly**.

### Grading Scale

- **50%** → Pass (2)
- **60%** → Satisfactory (3)
- **80%** → Good (4)
- **90%** → Excellent (5)

## Homework and Practice Work Instructions

- Submit a **shared link** to a Google Colab notebook.
- Ensure that the notebook executes correctly using **"Run all"**.
- Perform a **"Kernel restart and run all"** before submission.

## Mini-Project Instructions

- Submit a **Google Colab notebook**.
- Ensure the notebook executes properly using **"Run all"**.
- Each mini-project includes:
  - A **dataset**.
  - A **task** (e.g., classification, clustering, etc.).
  - A **competition**: best performance using any technique.
- Achieving high scores is **not mandatory**, but:
  - Placing in the **top 3 at least 2 times** guarantees a **grade of 5**.
- You must submit a **work-in-progress notebook** by the following **Friday**.
- The final deadline is **three weeks** after assignment, on **Fridays at 23:59:59 PM**.
- Winners are announced and students must present their solutions in a **maximum 10-minute presentation** (no slides required).

### Submission Format

- Submit as a **Google Colab notebook**.
- Include an **HTML file** containing the outputs.
- Provide a **text file** summarizing results and methods.
- The notebook should be **reproducible** (restart kernel, run all).
- Code should be **clear, well-commented, and documented**.
- Consider using a **GitHub repository** for better organization.
- Example notebook: [`project_work_1/project_1.ipynb`](https://github.com/szbela87/ml_22_elteik)

## Machine Learning Pipeline

1. **Loading data**
2. **Describing data** (categorical, continuous, etc.)
3. **Data cleaning** (handling NaNs, duplicates, text conversion)
4. **Feature distribution and correlation analysis**
   - Histograms
   - Box plots
   - Scatter plots
5. **Data normalization**
6. **Training models**
7. **Evaluation metrics**:
   - Accuracy, confusion matrix
   - ROC-AUC curve
   - Positive predictive value (PPV), Negative predictive value (NPV)

## Weekly Schedule

| Week  | Topics & Activities |
|-------|---------------------|
| **1** | Introduction to ML, Types of ML, NumPy, Pandas, Matplotlib |
| **2** | Linear Regression, Logistic Regression, Naive Bayes, Decision Trees, Overfitting vs. Underfitting |
| **3** | Scikit-learn, First Mini-Project Assignment |
| **4** | Clustering: KNN, DBSCAN, K-Means; PCA, SVMs |
| **5** | Boosting: XGBoost. Hyperparameter tuning with GridSearchCV, Optuna/Hyperopt. |
| **6** | Neural networks: The structure, abilities and corresponding supervised teaching algorithms of the elementary neuron. Error correction procedures (gradient methods, random search procedures). Single and multilayer feedforward neural network, teaching feedforward networks: backpropagation algorithm. |
| **7** | Neural Networks in Pytorch. Motivation and structure of convolutional neural networks, basic building blocks: pooling, upsampling, convolutions. |
| **8** | Simple CNN application examples: classification - MNIST, CIFAR10, Fashion MNIST datasets. Optimization procedures. Transfer learning, feature extraction. |
| **9** | Overfitting, underfitting again. Batch normalization, dropout, early stopping. Transpose convolution. Special architectures: ResNet, DenseNet, Inception. |
| **10** | Autoencoders, Variational Autoencoders, Object Detection, Segmentation |
| **11** | Time series classification, forecasting, Attention mechanism |
| **12** | Transformers, Vision Transformers |
| **13** | Large Language Models, fine-tuning, prompt engineering, RAG |

## Mini-Project Schedule

| Week | Assignment | Deadline |
|------|-----------|----------|
| 3    | Mini-Project 1 | Week 6 |
| 6    | Mini-Project 2 | Week 9 |
| 9    | Mini-Project 3 | Week 12 |
