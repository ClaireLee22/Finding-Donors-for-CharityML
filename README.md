# Finding-Donors-for-CharityML
Supervised Learning Project [Udacity Machine Learning Nanodegree]

## Project Overview
### Project Description
Apply supervised learning techniques and an analytical mind on data collected for the U.S. census to help CharityML (a fictitious charity organization) identify people most likely to donate to their cause. 

### Project Procedure
- Explore the data
- Preprocesse the data
  - Transfered skewed continous features
  - One-hot encoding
- Evaluate performance of several supervised learning algorithms
  - Gaussian Naive Bayes (GaussianNB)
  - Decision Trees
  - Ensemble Methods (Bagging, AdaBoost, Random Forest, Gradient Boosting)
  - K-Nearest Neighbors (KNeighbors)
  - Stochastic Gradient Descent Classifier (SGDC)
  - Support Vector Machines (SVM)
  - Logistic Regression
- Choose the best model
- Tune model parameters using grid search
- Evaluate feature importance to optimize the model's performance
  - feature_importances_  attribute 
  - recursive feature elimination(RFE)

### Project Results
  - Gradient Boosting algorithm performed best in f-score and accuracy on the testing dataset
  - Improve model performance after model tuning using grid search
  
    | Metric | Unoptimized Model | Optimized Model |
    | :---:   | :-: | :-: |
    | Accuracy | 0.8630 | 0.8705 |
    | F-score | 0.7395 | 0.7513 |
    
  - Both accuracy score and f-score are slightly declined on the reduced data(top 5 important features) than the scores on the full data.     However, it decreases substantial training time. 
  
    | Metric | Final Model trained on full data |  Final Model trained on reduced data  |
    | :---:   | :-: | :-: |
    | Accuracy | 0.8705 | 0.8590 |
    | F-score | 0.7513 | 0.7252 |
    | Train time | 5.7013 | 54.9721|

## Getting Started
### Prerequisites
This project requires **Python 2.7** and the following Python libraries installed:

- [NumPy](http://www.numpy.org/)
- [Pandas](http://pandas.pydata.org)
- [matplotlib](http://matplotlib.org/)
- [scikit-learn](http://scikit-learn.org/stable/)

You will also need to have software installed to run and execute an [iPython Notebook](http://ipython.org/notebook.html)

### Run

In a terminal or command window, run one of the following commands:

```bash
ipython notebook finding_donors.ipynb
```  
or
```bash
jupyter notebook finding_donors.ipynb
```

This will open the iPython Notebook software and project file in your browser.

### Data

The modified census dataset consists of approximately 32,000 data points, with each datapoint having 13 features. This dataset is a modified version of the dataset published in the paper *"Scaling Up the Accuracy of Naive-Bayes Classifiers: a Decision-Tree Hybrid",* by Ron Kohavi. You may find this paper [online](https://www.aaai.org/Papers/KDD/1996/KDD96-033.pdf), with the original dataset hosted on [UCI](https://archive.ics.uci.edu/ml/datasets/Census+Income).

**Features**
- `age`: Age
- `workclass`: Working Class (Private, Self-emp-not-inc, Self-emp-inc, Federal-gov, Local-gov, State-gov, Without-pay, Never-worked)
- `education_level`: Level of Education (Bachelors, Some-college, 11th, HS-grad, Prof-school, Assoc-acdm, Assoc-voc, 9th, 7th-8th, 12th, Masters, 1st-4th, 10th, Doctorate, 5th-6th, Preschool)
- `education-num`: Number of educational years completed
- `marital-status`: Marital status (Married-civ-spouse, Divorced, Never-married, Separated, Widowed, Married-spouse-absent, Married-AF-spouse)
- `occupation`: Work Occupation (Tech-support, Craft-repair, Other-service, Sales, Exec-managerial, Prof-specialty, Handlers-cleaners, Machine-op-inspct, Adm-clerical, Farming-fishing, Transport-moving, Priv-house-serv, Protective-serv, Armed-Forces)
- `relationship`: Relationship Status (Wife, Own-child, Husband, Not-in-family, Other-relative, Unmarried)
- `race`: Race (White, Asian-Pac-Islander, Amer-Indian-Eskimo, Other, Black)
- `sex`: Sex (Female, Male)
- `capital-gain`: Monetary Capital Gains
- `capital-loss`: Monetary Capital Losses
- `hours-per-week`: Average Hours Per Week Worked
- `native-country`: Native Country (United-States, Cambodia, England, Puerto-Rico, Canada, Germany, Outlying-US(Guam-USVI-etc), India, Japan, Greece, South, China, Cuba, Iran, Honduras, Philippines, Italy, Poland, Jamaica, Vietnam, Mexico, Portugal, Ireland, France, Dominican-Republic, Laos, Ecuador, Taiwan, Haiti, Columbia, Hungary, Guatemala, Nicaragua, Scotland, Thailand, Yugoslavia, El-Salvador, Trinadad&Tobago, Peru, Hong, Holand-Netherlands)

**Target Variable**
- `income`: Income Class (<=50K, >50K)
