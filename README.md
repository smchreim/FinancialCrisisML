# Code: Machine Learning for Financial Crisis Prediction
This repository contains the code used in the paper "**Using Machine Learning to predict Financial Crises: An Evaluation of different Learning Algorithms for Early Warning Models**" by Chris Reimann. 

The paper deals with the use of machine learning methods in early warning models of financial crises. Special interest was given to how the standard econometric model of Logistic Regression performs in comparison to more advanced machine learning algorithms. For this purpose, a cross-validation experiment was conducted, in which the out-of-sample predictions of the Logistic Regression were evaluated against those of k-nearest Neighbors, Random Forest, Extremely Randomized Trees, Support Vector Machine and artificial Neural Network models. The different machine learning methods operate on crisis observations between 1870-2020 from the MacroHistory database and up to 15 early warning indicators frequently used in the financial crisis literature. The best predictive performance is achieved by the Random Forest and Extremely Randomized Trees models, as measured by the area under the receiver operating characteristic (AUROC). This finding is robust to changes in crisis data sources, early warning indicator sets and model specifications used.

## Structure of the Code
The experiments of the paper are implemented in the Python programming language. The machine learning models were adapted from the [Scikit-Learn](https://github.com/scikit-learn/scikit-learn) package, while the [Pandas](https://github.com/pandas-dev/pandas), [Numpy](https://github.com/numpy/numpy) and [MatplotLib](https://github.com/matplotlib/matplotlib) packages provided the basis for more general data processing. The code was organized into the following files:
- *altCrisisData.py*: Manages access to alternative data sources for crisis events, namely ESRB and Laeven & Valencia 2018.
- *doExperiment.py*: Runs the actual experiment based on the collected data and machine learning models from SciKitLearn and allows the selection of different experimental designs (Cross-Validation, Strict Forecasting, In-Sample Prediction).
- *prepareData.py*: Loads and processes the crisis event and early warning indicator data. 
- *utils.py*: Provides custom data splitting methods (train/test) used in the experiments. 
