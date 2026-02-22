# **1. Project Assignment: Credit Risk Prediction**

## **Task Description**

Banks play a key role in the market economy: they decide who gets access to financing and under what conditions.
For the stability of the financial system, it is essential that individuals and companies can obtain credit when needed.
**Credit risk prediction** plays a central role in this process, helping to assess how likely a loan applicant is to experience financial difficulties and how likely they are to repay their loan.

In this project, your task is to work with a real-world dataset — the *"Give Me Some Credit"* dataset available on Kaggle — and build a model that predicts whether a borrower will experience financial distress within the next two years.
The dataset is available [here](https://www.kaggle.com/c/GiveMeSomeCredit).

---

## **Objective**

Your goal is to create a model that can help borrowers make more informed financial decisions and identify risks in time.
To achieve this, you can use the demographic and financial data of 250,000 past loan applicants.

---

## **Submission**

**Important:** Your project submission must be a **Google Drive directory link**. Make sure the directory has **read access** enabled (shared with "Anyone with the link").

---

## **Detailed Tasks**

For each subtask, it is worth studying the solutions available on the Kaggle page under the *Code* tab. Any sources used must be referenced (a link is sufficient). Similarly, please indicate in your submission which parts were created with the help of a generative model. This is based on self-reporting and carries no negative consequences, as the use of such models is encouraged for preparing and refining solutions.

### 1. **Data Processing and Preparation**
- Clean the dataset: handle missing values and perform the necessary standardization or normalization.
- Examine the distribution of individual variables and handle outlier values so they do not distort model performance.

### 2. **Model Development**
- Train at least three different machine learning models, for example:
  - **Random Forest**
  - **SVM (Support Vector Machine)**
  - **At least one boosting algorithm**, such as XGBoost or LightGBM.
- Optimize the hyperparameters of the models using cross-validation. For example, using *grid search*, *random search*, *Optuna*, or *Hyperopt*.

### 3. **Stacking**
- Create an **ensemble model** using the stacking technique that combines the predictions of individual models.
- Compare the performance of the stacking model with the individual models and analyze whether the combination of models improves the results.

### 4. **Model Evaluation and Analysis**
- Evaluate model performance based on the following metrics:
  - Balanced Accuracy (*balanced_accuracy*)
  - Recall (*recall*)
  - Precision (*precision*)
  - F1-score
  - AUC–ROC
- Perform the following error analysis: examine which customer types the models perform worst on and what types of cases they make the most mistakes. Provide a brief written explanation.
- Rank the above metrics according to which metric is most appropriate for this task — in your opinion. Provide a brief written explanation.

### 5. **Documentation and Presentation**
- Prepare a **report of at most 5 pages** or a **presentation** in which you present:
  - the data processing steps,
  - the modeling process,
  - the achieved results and their comparison.
- Visualize your results: for example, create ROC curves, *feature importance* plots, or comparative diagrams of performance metrics.
- The presentation of the documentation/presentation is optional; bonus points can be earned for it.

---

## **Evaluation Criteria**

The evaluation considers the following aspects with the corresponding weight:

| Criterion | Weight |
|---|---|
| **Quality of data processing and preparation** | 20% |
| **Quality of model development and optimization** | 25% |
| **Implementation and performance of the stacking model** | 10% |
| **Visualization and interpretation of results** | 20% |
| **Quality of documentation / presentation** | 25% |
| **Bonus: Kaggle submission score** | 0% |

**Regarding the Kaggle submission bonus:** Your Kaggle competition score will be taken into account during the evaluation. To verify authenticity, a **screenshot** of your submission score and a **live demonstration** are required.
