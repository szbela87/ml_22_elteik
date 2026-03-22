# **2. Project Assignment: Handwritten Digit Recognition**

## **Task Description**

Handwritten digit recognition is one of the foundational problems of computer vision and a classic benchmark task in machine learning and deep learning.
Reliable automatic digit recognition has widespread applications from postal mail sorting to bank check processing and digitizing handwritten documents.

In this project, your task is to work with the **Kannada-MNIST** dataset available through the *"Kannada-MNIST"* competition on Kaggle and build models that classify handwritten digits (0–9) written in the Kannada script, a Dravidian language spoken in southwestern India.
The key objective is to **compare traditional machine learning approaches with neural network-based methods** and analyze the differences in performance.
The dataset is available [here](https://www.kaggle.com/competitions/Kannada-MNIST).

---

## **Objective**

Your goal is to explore and compare different modeling strategies for image classification:
- First, establish **baseline results** using classical machine learning methods.
- Then, build **neural network models** (fully connected and convolutional) using PyTorch and demonstrate their advantages.

The dataset contains 28×28 grayscale images of handwritten Kannada digits (pixel values 0–255), with 60,000 labeled training samples and 10,000 test samples. An additional **Dig-MNIST** dataset (10,240 images) is also provided for cross-domain evaluation. Compared to the classic MNIST, Kannada-MNIST is a more challenging benchmark — baseline CNN models achieve ~96.8% accuracy, leaving more room for experimentation and improvement.

---

## **Submission**

**Important:** Your project submission must be a **Google Drive directory link** (via Teams assignment). Make sure the directory has **read access** enabled (shared with "Anyone with the link").

---

## **Important Dates**

| Date | Event |
|---|---|
| **8 April (Wednesday)** | Deadline to send a work-in-progress Google Drive link via email if you would like consultation on your solution |
| **13 April (Monday)** | In-person consultation for those who sent their WIP link (if no email feedback is provided beforehand) |
| **17 April (Friday), 23:59** | **Submission deadline** |
| **20 April (Monday)** | Results presentation and winner announcement in class |

- Late submissions **will not be accepted** for the competition. They can only be accepted for the assignment itself, with reduced points according to the rules.

---

## **Detailed Tasks**

For each subtask, it is worth studying the solutions available on the Kaggle page under the *Code* tab. Any sources used must be referenced (a link is sufficient). Similarly, please indicate in your submission which parts were created with the help of a generative model. This is based on self-reporting and carries no negative consequences, as the use of such models is encouraged for preparing and refining solutions.

### 1. **Data Exploration and Preparation**
- Visualize sample images from each digit class.
- Examine the class distribution (are the classes balanced?).
- Apply appropriate preprocessing: normalization (scaling pixel values to [0, 1]), and reshaping the data as needed for different model types.
- Optionally, experiment with data augmentation techniques (rotation, shifting, scaling) and analyze their effect on model performance.

### 2. **Classical Machine Learning Models (Baseline)**
- Train at least two different traditional machine learning models on the flattened pixel features, for example:
  - **K-Nearest Neighbors (KNN)**
  - **Support Vector Machine (SVM)**
  - **Random Forest**
- Optimize the hyperparameters of the models using cross-validation.
- These results serve as a **baseline** for comparison with neural network approaches.

### 3. **Neural Network Models (PyTorch)**
- Build and train at least two neural network architectures using **PyTorch**:
  - **Fully Connected Network (MLP):** At least 2 hidden layers. Experiment with different layer sizes, activation functions, and regularization (dropout).
  - **Convolutional Neural Network (CNN):** Use convolutional layers, pooling layers, and fully connected layers. Experiment with different architectures (number of layers, filter sizes, etc.).
- For each neural network model:
  - Plot the **training and validation loss/accuracy curves** across epochs.
  - Experiment with at least two hyperparameters (e.g., learning rate, batch size, number of layers, dropout rate) and document their effect.
  - Use appropriate techniques to prevent overfitting (e.g., dropout, early stopping, data augmentation).

### 4. **Model Evaluation and Comparison**
- Evaluate all models (classical and neural network) based on the following metrics:
  - Overall **Accuracy**
  - **Confusion matrix** (visualized as a heatmap)
  - **Per-class precision, recall, and F1-score**
- Perform the following error analysis:
  - Identify which digit pairs are most frequently confused with each other.
  - Visualize examples of misclassified images and provide a brief explanation of why the model may have failed.
- Create a **summary comparison table** of all models' performance and discuss:
  - How do classical ML models compare to neural networks?
  - What is the benefit of using convolutional layers compared to fully connected layers?

### 5. **Documentation and Presentation**
- Prepare a **report of at most 1 page** summarizing:
  - the data exploration and preprocessing steps,
  - the modeling process (classical ML and neural networks),
  - the achieved results and their comparison.
- Visualize your results: training curves, confusion matrices, misclassified examples, and model comparison charts.
- Each student must give a **short presentation** of their solution in class. Preparing slides is not mandatory — you may present directly from your notebook.

---

## **Evaluation Criteria**

The evaluation considers the following aspects with the corresponding weight:

| Criterion | Weight |
|---|---|
| **Quality of data exploration and preparation** | 15% |
| **Classical ML baseline models and optimization** | 15% |
| **Neural network implementation and experimentation (MLP + CNN)** | 30% |
| **Model evaluation, comparison, and error analysis** | 15% |
| **Quality of documentation / presentation** | 25% |
| **Bonus: Kaggle submission score** | 0% |

**Regarding the Kaggle submission bonus:** Your Kaggle competition score will be taken into account during the evaluation. To verify authenticity, a **screenshot** of your submission score and a **live demonstration** are required.
