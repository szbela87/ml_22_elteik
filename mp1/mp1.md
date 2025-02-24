# 1st Mini-project - Competition Rules

## **Objective:**  
The task is to predict the **"income"** column in the evaluation dataset, determining whether a person’s annual income exceeds $50,000 (binary classification: 0 or 1).  

The dataset is originally derived from the [UCI Adult Census Income](https://www.kaggle.com/datasets/uciml/adult-census-income/data)  dataset, but we are using a **modified version** for this competition.  

---

## **Dataset**  
The following files must be used during the competition (from this directory):

- **Training set:** `train.csv` (includes labels)  
- **Test set:** `test.csv` (does not include labels)  

The input data consists of various demographic and employment-related features.

---

## **Models**  
- **First competition:** Only **Random Forest** is allowed  
- **Second competition:** Any model can be used  

---

## **Evaluation Metric**  
Performance is measured using **balanced accuracy**:

$$
\text{Balanced Accuracy} = \frac{TPR + TNR}{2}
$$

Where:  
- **TPR (True Positive Rate):** $$ \frac{TP}{TP + FN} $$
- **TNR (True Negative Rate):** $ \frac{TN}{TN + FP} $

(Where TP, FP, TN, and FN are the counts of true positives, false positives, true negatives, and false negatives, respectively).

---

## **Submission Format**  

### **‼ IMPORTANT ‼**  
**A Google Drive folder link must be submitted on the course’s Canvas page under the assignment.**  
This folder must contain the following files:

1. **Prediction Files (`submission_census_income_[your_name]_[competition_id].csv`)**  
   - Contains predictions for the **test.csv** dataset.  
   - **Format:** One label per line (0 or 1).  
   - **Important:** The predictions must be in the same order as in `test.csv`.  

2. **Jupyter Notebook (`.ipynb`)**  
   - The complete workflow must be included.  
   - All **random seeds must be fixed** to ensure that results are **fully reproducible**.  

3. **Exported Notebook (`.html` or `.pdf`)**  
   - A static version of the notebook showing the results.  

4. **Google Drive Shared Folder**  
   - Any additional working files (e.g., auxiliary data, experiment logs) can be stored in this folder.  
   - **The link to this shared folder must be submitted on the Canvas page under the assignment!**  

**File Naming Format:**  
- `census_income_[your_name]_[competition_id].ipynb`  
- `census_income_[your_name]_[competition_id].html` or `.pdf`  
- **Prediction Files:** `submission_census_income_[your_name]_[competition_id].csv`  

---

## **Deadline**  
The final submission deadline is **March 21, 23:59**.  

In the following weeks, during practical sessions, there will be opportunities to consult and ask questions. However, to be eligible for this, a **work-in-progress version** must be submitted **by the next Friday (03.07) following the announcement**.  

After the competition closes, winners will be announced, and some participants will be invited to present their solutions.

---

## **Grading & Evaluation**  
The mini-project grading **does not** depend on competition rankings but on meeting the following criteria:

1. **Participation in at least one competition**  
2. **Fine-tuning of hyperparameters**  
3. **Well-commented and clean code**  
4. **Complete submission** (all required files included, including `submission_census_income_[your_name]_[competition_id].csv`)  
5. **Ensuring reproducibility** (fixed random seeds)  
6. **Anything can be used, with proper citations**
