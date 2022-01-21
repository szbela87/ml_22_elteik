# Project work instructions

**Exploratory Data Analysis (EDA)**
- data consistency:
    - missing data -> data imputation
    - class names (for categorical variables) -> cleaning up
- distributions
    - outlier detection (e.g. boxplot)
    - skewness (e.g. histograms, scatterplot matrix)
    - correlations (e.g. corrplot)
    - bias in categories
- for classification
    - projection (e.g. PCA, t-SNE, Self-organizing Map)
    - feature aggregation for 2D plots

Some examples:
- Water potability:
https://www.kaggle.com/jaykumar1607/water-quality-analysis-plotly-and-modelling/notebook
- House Prices: https://www.kaggle.com/pmarcelino/comprehensive-data-exploration-with-python
- Titanic data: 
https://www.kaggle.com/startupsci/titanic-data-science-solutions

**Model building**
- set up the pipeline
    - train-test-validation: enable random splitting and selection (for later stages)
    - metrics - e.g. confusion matrix for classification, RMSE for regression
    - plots 
        - training curve
        - e.g. checking misclassified/badly predicted data points
- try with simple architectures to get impression about complexity
    - model: decision tree/random forest (try some setups)
    - input: search for some useful features 
- analyze first results
    - training curve: check convergence, avoid overfitting
    - search for some "difficult" data points and understand the difficulty
- try with more complex architectures
    - model: neural network / boosting|ensembling technique
    - check training curve to avoid overfitting
    - check "still difficult" data points
    - try some cross-validation method to optimize hyperparameters
