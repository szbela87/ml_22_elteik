# **3. Project Assignment: Image Segmentation – Salt Layer Identification in Seismic Images**

## **Task Description**

Image segmentation is one of the fundamental tasks in computer vision, where the goal is not
merely to classify an image as a whole, but to determine at the pixel level which segment each
pixel belongs to. Segmentation is widely used in medical image analysis, autonomous vehicles,
satellite imagery interpretation, and industrial inspection.

In this project, you will work with the **TGS Salt Identification Challenge** dataset available
through the *Kaggle* platform. The task is to identify salt layers in seismic images (depicting
underground geological formations): for each pixel, you must decide whether it belongs to a
salt deposit or not (binary segmentation). The key objective is to **compare different deep
learning segmentation architectures** using PyTorch.

The dataset is available [here](https://www.kaggle.com/c/tgs-salt-identification-challenge).

---

## **Objective**

Your goal is to build, train, and thoroughly compare at least three different deep learning
segmentation models:
- Implement and compare **at least 3 different encoder-decoder / segmentation architectures**
  of your choice (e.g., U-Net variants, Feature Pyramid Network, DeepLab, etc.).
- Analyze the differences between architectures in terms of performance, training dynamics,
  and generalization ability.

The dataset contains 101×101 grayscale seismic images (pixel values 0–255) with corresponding
binary masks (salt: 1, other: 0). The training set contains ~4,000 images and the test set
~18,000 images. The evaluation metric is **IoU (Intersection over Union)**, averaged over
thresholds from 0.5 to 0.95 (Kaggle-style mAP@IoU metric).

---

## **Submission**

**Important:** Your project submission must be a **Google Drive directory link** (via Teams
assignment). Make sure the directory has **read access** enabled (shared with "Anyone with
the link").

---

## **Important Dates**

| Date | Event |
|---|---|
| **April 29 (Wednesday) 23:59** | Deadline to send a work-in-progress Google Drive link via email for consultation |
| **May 4 (Monday)** | In-person consultation for those who sent their WIP link (if no email feedback is provided beforehand) |
| **May 9 (Saturday) 07:59 AM** | **Submission deadline** |
| **May 11 (Monday)** | Results presentation and winner announcement in class |

- Late submissions **will not be accepted** for the competition. They can only be accepted for
  the assignment itself, with reduced points according to the rules.

---

## **Detailed Tasks**

For each subtask, it is worth studying the solutions available on the Kaggle page under the
*Code* tab. Any sources used must be referenced (a link is sufficient). Similarly, please
indicate in your submission which parts were created with the help of a generative model.
This is based on self-reporting and carries no negative consequences, as the use of such
models is encouraged for preparing and refining solutions.

### 1. **Data Exploration and Preparation**
- Visualize sample images from different salt-coverage categories (empty mask, partial, full coverage).
- Examine the distribution of salt coverage (is the dataset balanced? how many empty masks are there?).
- Apply appropriate preprocessing: normalization (scaling pixel values to [0, 1]), and reshaping
  the data as needed for different model types.
- Experiment with data augmentation techniques (horizontal flipping, random cropping,
  brightness/contrast jitter) and analyze their effect on model performance.

### 2. **Deep Learning Segmentation Models (PyTorch)**
- Implement and train **at least 3 different deep learning segmentation architectures** using
  PyTorch. You may freely choose from the following (or others):
  - **U-Net** (original or simplified variant)
  - **U-Net++** (denser skip connections with nested encoder-decoder structure)
  - **Attention U-Net** (attention gates on skip connections)
  - **ResNet-based U-Net** (e.g., ResNet34 encoder with pretrained weights)
  - **FPN (Feature Pyramid Network)**
  - **DeepLabV3 / DeepLabV3+**
  - **SegFormer** (transformer-based segmentation)
- For each model:
  - Plot the **training and validation loss/IoU curves** across epochs.
  - Use an appropriate loss function (e.g., a combination of BCE and Dice loss).
  - Experiment with at least one hyperparameter per model (e.g., learning rate, encoder depth,
    augmentation strategy) and document its effect.
  - Apply overfitting prevention techniques (dropout, early stopping, data augmentation,
    learning rate scheduling).

### 3. **Model Evaluation and Comparison**
- Evaluate all models based on the following metrics:
  - Overall **IoU (Intersection over Union)**
  - **Dice coefficient (pixel-level F1-score)**
  - **Precision and Recall** at the pixel level
- Perform the following error analysis:
  - On which image types do the models fail most? (empty masks, small salt patches, full coverage)
  - Visualize misclassified images and provide a brief explanation of why the model may have failed.
- Create a **summary comparison table** of all models' performance and discuss:
  - What architectural differences explain the performance gaps?
  - What trade-offs emerge between model size, training time, and accuracy?

### 4. **Documentation and Presentation**
- Prepare a **report of at most 1 page** summarizing:
  - the data exploration and preprocessing steps,
  - a brief description and justification of the chosen model architectures,
  - the achieved results and their comparison.
- Visualize your results: training curves, segmentation mask visualizations
  (original image | predicted mask | ground truth mask), model comparison charts.
- Each student must give a **short presentation** of their solution in class. Preparing slides
  is not mandatory — you may present directly from your notebook.

---

## **Evaluation Criteria**

The evaluation considers the following aspects with the corresponding weight:

| Criterion | Weight |
|---|---|
| **Quality of data exploration and preparation** | 15% |
| **Deep learning model implementation and experimentation (min. 3 architectures)** | 45% |
| **Model evaluation, comparison, and error analysis** | 15% |
| **Quality of documentation / presentation** | 25% |
| **Bonus: Kaggle submission score** | 0% |

**Regarding the Kaggle submission bonus:** Your Kaggle competition score will be taken into
account during the evaluation. To verify authenticity, a **screenshot** of your submission
score and a **live demonstration** are required.
