# Introduction to Machine Learning and Deep Learning

Additional course materials, ELTE Faculty of Informatics - 2024/25 spring semester

## Course Structure and Grading

- **20%** of the final grade comes from homework assignments.
- **20%** comes from practical session performance.
- **60%** comes from four mini-projects (each has a two-week deadline, see schedule below).
- **No final exam** for this course.

## About the Mini-Projects

- There will be **4+1 mini-projects** throughout the semester.
- You must complete at least **3** mini-projects to receive a grade.
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
  - Two **competitions**: 
    1. Best performance using a specific method.
    2. Best performance using **any** technique.
- Achieving high scores is **not mandatory**, but:
  - Placing in the **top 3 at least 3 times** guarantees a **grade of 5** (if all 3 projects are submitted).
- You must submit a **work-in-progress notebook** by the following **Friday**.
- The final deadline is **three weeks** after assignment, on **Fridays at 23:59:59 PM**.
- Winners are announced and some students will present their solutions.

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

### Week 1: Introduction
- Overview of machine learning.
- Types of ML: Supervised, Unsupervised, Reinforcement Learning.
- Introduction to **NumPy, Pandas, Matplotlib**. 
- [Practice Notebooks](https://drive.google.com/drive/folders/1nGrjHiYWcQ-JkfTcMCgcysPgogIIxF7c?usp=drive_link) 
- [Homework](https://drive.google.com/drive/folders/1bE7fgjayMBCBk0EmSenng5iwegO4jkFL?usp=sharing) 

| Week  | Topics & Activities | Links |
|-------|---------------------|-------|
| **1** | Introduction to ML, Types of ML, NumPy, Pandas, Matplotlib | [Practice Notebooks](https://drive.google.com/drive/folders/1nGrjHiYWcQ-JkfTcMCgcysPgogIIxF7c?usp=drive_link), [Homework](https://drive.google.com/drive/folders/1bE7fgjayMBCBk0EmSenng5iwegO4jkFL?usp=sharing) |
| **2** | Linear Regression, Logistic Regression, Naive Bayes, Decision Trees, Overfitting vs. Underfitting | **Practice: Scikit-learn I** |
| **3** | End-to-End ML Workflow, Scikit-learn II, First Mini-Project Assignment |  |
| **4** | KNN, DBSCAN, K-Means, PCA, SVMs | **Practice: Scikit-learn** |
| **5** | XGBoost, GridSearchCV, Optuna/Hyperopt | **Practice: Notebooks** |
| **6** | Perceptron, Adaline, Backpropagation, First Mini-Project Presentations, Second Mini-Project Assignment |  |
| **7** | Introduction to PyTorch, Neural Networks | **Practice: Notebooks** |
| **8** | Holiday 🎉 |  |
| **9** | CNNs, MNIST, CIFAR10, Fashion MNIST, Second Mini-Project Presentations, Third Mini-Project Assignment |  |
| **10** | Advanced NN Architectures: ResNet, DenseNet, Inception, Transfer Learning | **Practice: Notebooks** |
| **11** | Unet for Segmentation, YOLO for Object Detection | **Practice: Notebooks** |
| **12** | Autoencoders, Scientific Paper Reproduction, Third Mini-Project Presentations, Fourth Mini-Project Assignment |  |
| **13** | Time Series Forecasting | **Lecture & Practice: Notebooks** |

## Mini-Project Schedule

| Week | Assignment | Deadline |
|------|-----------|----------|
| 3    | Mini-Project 1 | Week 6 |
| 6    | Mini-Project 2 | Week 9 |
| 9    | Mini-Project 3 | Week 12 |
| 12   | Mini-Project 4 | Week 15 |
| 15?   | Mini-Project +1 | Week ? |
