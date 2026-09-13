
# Dataset Information

This folder contains the Cleveland Heart Disease dataset used in the project.

## Dataset

**File:** `processed.cleveland.data`

The dataset contains patient-level medical attributes related to heart disease prediction.

### Features

| Feature    | Description                                     |
| ---------- | ----------------------------------------------- |
| `age`      | Patient age                                     |
| `sex`      | Patient sex                                     |
| `cp`       | Chest-pain type                                 |
| `trestbps` | Resting blood pressure                          |
| `chol`     | Serum cholesterol                               |
| `fbs`      | Fasting blood sugar indicator                   |
| `restecg`  | Resting electrocardiographic result             |
| `thalach`  | Maximum heart rate achieved                     |
| `exang`    | Exercise-induced angina                         |
| `oldpeak`  | ST depression caused by exercise                |
| `slope`    | Slope of the peak exercise ST segment           |
| `ca`       | Number of major vessels observed by fluoroscopy |
| `thal`     | Thalassemia-related test result                 |
| `target`   | Heart disease outcome                           |

## Data Preparation

The original dataset uses `?` to represent missing values. These values are handled during preprocessing.

The original target contains multiple values representing different levels of heart disease. For binary classification, the target is converted as follows:

* `0` → No heart disease
* Values greater than `0` → Heart disease present

## Important Note

This dataset is used only for educational and machine learning research purposes. The model is not intended to provide medical diagnosis or replace professional medical advice.
