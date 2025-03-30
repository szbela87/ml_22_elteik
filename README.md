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
  - Placing in the **top 3 at least 3 times** guarantees a **grade of 5** (if at least 3 projects are submitted).
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

| Week  | Topics & Activities | Links |
|-------|---------------------|-------|
| **1** | Introduction to ML, Types of ML, NumPy, Pandas, Matplotlib | [Practice Notebooks](https://drive.google.com/drive/folders/1nGrjHiYWcQ-JkfTcMCgcysPgogIIxF7c?usp=drive_link), [Homework](https://drive.google.com/drive/folders/1bE7fgjayMBCBk0EmSenng5iwegO4jkFL?usp=sharing) |
| **2** | Linear Regression, Logistic Regression, Naive Bayes, Decision Trees, Overfitting vs. Underfitting | [Slides](https://drive.google.com/drive/folders/13fjIQ4We5F7USMLcZ023tZxlQlMhEe9B?usp=sharing) |
| **3** | Scikit-learn, First Mini-Project Assignment | [Practice Notebooks](https://drive.google.com/drive/folders/1KD1AB8gjM5fV2QoSZgUWTVs0QrXi62Mq?usp=sharing) |
| **4** | A Case study, Clustering: KNN, DBSCAN, K-Means, PCA, SVMs | [Practice Notebooks](https://drive.google.com/drive/folders/132VUZJVbCmu3SJUOa5ymO-UX6vPgsFw9?usp=sharing) |
| **5** | Boosting: XGBoost. Hyperparameter tuning with GridsearchCV Optuna/Hyperopt. | [Practice Notebooks](https://drive.google.com/drive/folders/14GKxKmjUZTwnOxwLqh66Sg4KveWsyRKq?usp=sharing) |
| **6** | Neural networks: The structure, abilities and corresponding supervised teaching algorithms of the elementary neuron. Error correction procedures (gradient methods, random search procedures). Single and multilayer feedforward neural network, teaching feedforward networks: backpropagation algorithm. | [Practice Notebooks](https://drive.google.com/drive/folders/11DFwU2dkEE28JwrEythUR12yUErQpcSD?usp=sharing)  |
| **7-8** | Neural Networks in Pytorch. Motivation and structure of convolutional neural networks, basic building blocks: pooling, upsampling, convolutions. Simple application examples: classification - MNIST, CIFAR10, Fashion MNIST datasets. | [Practice Notebook I.](https://drive.google.com/file/d/1LqYByhsIEa-f0Q4EFXOuZF-_p-VUkWZf/view?usp=sharing) [Practice Notebook II.](https://drive.google.com/file/d/1YeF9LqEOgfuDEaW_OmGpUmekmWTc9gcb/view?usp=sharing) |
| **8-9** | Main issues of the constructions of networks. Optimization procedures. Transfer learning, feature extraction. Overfitting, underfitting again. Batch normalization, dropout, early stopping. Transpose convolution. Special architectures: ResNet, DenseNet, Inception.  | [Practice Notebooks I.](https://drive.google.com/drive/folders/180Al_4mLO0ZYLcCJUHUY5LSz_GK2NmpL?usp=sharing) [Practice Notebook II.](https://drive.google.com/file/d/1UPj7iXpooIKMQMOIKiBs9YIpX-qTxk36/view?usp=sharing)|
| **10** |  Holiday 🎉 |  |
| **11** | ? | **Practice: Notebooks** |
| **12** | ? | **Practice: Notebooks** |
| **13** | ?  | **Lecture & Practice: Notebooks** |

## Mini-Project Schedule

| Week | Assignment | Deadline |
|------|-----------|----------|
| 3    | Mini-Project 1 | Week 6 |
| 6    | Mini-Project 2 | Week 9 |
| 9    | Mini-Project 3 | Week 12 |
| 12   | Mini-Project 4 | Week 15 |
| 15?   | Mini-Project +1 | Week ? |
