
# XAI Heart Disease Prediction

An Explainable AI project for predicting heart disease using a real-world Cleveland Heart Disease dataset and a Random Forest classification model.

The project focuses not only on prediction accuracy but also on understanding why a machine learning model makes a particular prediction using SHAP explainability.

## Project Overview

Machine learning models can predict whether a patient may have heart disease based on medical attributes. However, many models are difficult to interpret.

This project applies Explainable AI techniques to make model predictions easier to understand.

The project includes:

* Data loading and preprocessing
* Missing-value handling
* Exploratory data analysis
* Feature inspection and validation
* Random Forest classification
* Model evaluation
* Cross-validation
* Classification threshold tuning
* SHAP feature importance analysis
* Individual patient prediction explanations
* False-negative analysis

## Dataset

The project uses the Cleveland Heart Disease dataset.

The dataset contains medical attributes such as:

* Age
* Sex
* Chest-pain type
* Resting blood pressure
* Cholesterol
* Maximum heart rate
* Exercise-induced angina
* ST depression
* Number of major vessels
* Thalassemia-related test result

The original target is converted into a binary classification target:

* `0` → No heart disease
* `1` → Heart disease present

More information about the dataset is available in [`data/README.md`](data/README.md).

## Machine Learning Model

The project uses a Random Forest classifier for heart disease prediction.

Random Forest is an ensemble learning algorithm that combines multiple decision trees to improve prediction performance and reduce overfitting.

The model is evaluated using:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion matrix
* Cross-validation

The project also examines classification threshold tuning to understand the effect of changing the decision threshold on prediction results.

## Explainable AI

SHAP, or SHapley Additive exPlanations, is used to interpret the model.

The project includes:

### Global Explanation

SHAP summary plots are used to identify which features have the greatest influence on model predictions across the dataset.

### Local Explanation

SHAP waterfall plots are used to explain the prediction for an individual patient.

These explanations help show:

* Which features increased the predicted risk
* Which features decreased the predicted risk
* How individual features contributed to the model output

### False-Negative Analysis

The project also investigates false-negative predictions.

A false negative occurs when the model predicts no heart disease for a patient whose actual target indicates heart disease.

This analysis is important because missed positive cases can be significant in medical prediction tasks.

## Project Structure

```text
XAI-Heart-Disease-Prediction/
├── README.md
├── XAI_with_real_world_dataset.ipynb
├── data/
│   ├── README.md
│   └── processed.cleveland.data
├── requirements.txt
└── .gitignore
```

## Installation

Clone the repository:

```bash
git clone https://github.com/bedkemanojkumar/XAI-Heart-Disease-Prediction.git
```

Move into the project folder:

```bash
cd XAI-Heart-Disease-Prediction
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

## Running the Project

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
XAI_with_real_world_dataset.ipynb
```

Run the notebook cells in order.

## Technologies Used

* Python
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn
* Random Forest
* SHAP
* Jupyter Notebook

## Limitations

* The dataset is relatively small.
* The model is trained on a historical dataset.
* Dataset bias and class imbalance may affect the results.
* Model predictions should not be interpreted as medical diagnoses.
* The project is intended for educational and research purposes.

## Future Improvements

* Compare Random Forest with XGBoost and Logistic Regression.
* Add a Streamlit interface.
* Add probability calibration.
* Improve missing-value imputation.
* Perform more detailed fairness analysis.
* Add model monitoring and experiment tracking.
* Test the model on an independent dataset.

## Disclaimer

This project is for educational and machine learning research purposes only.

It is not a medical diagnostic system and should not be used to make healthcare decisions.
