# DATA-PIPELINE-DEVELOPMENT

*COMPANY*: CODTECH IT SOLUTIONS

*NAME*: N VASANTHA KUMAR

*INTERN ID*: CT08DG148

*DOMAIN*: Data Science

*DURATION*: 8 WEEKS

*MENTOR*: NEELA SANTOSH


# Data Science Internship Task 1 — ETL Pipeline

**Internship Organization:** CODTECH  
**Intern Name:** N Vasantha Kumar 
**Task Title:** Data Preprocessing, Transformation, and Loading Pipeline  
**Project Domain:** Pothole Detection (YOLOv10 Model Output)  

---

## Objective

This repository contains the completed deliverable for **Task 1** of the CODTECH Data Science Internship program. The task was to design and implement a complete **ETL (Extract, Transform, Load) pipeline** using tools like `pandas` and `scikit-learn`. The primary dataset used for this task was derived from the performance metrics of a YOLOv10 model trained for **pothole detection**, a real-world application with significance in smart city development and road safety.

The objective of this task is to simulate a common data science workflow where raw data must be cleaned, preprocessed, and prepared for model training or further analysis. A robust ETL process ensures that downstream models are trained on high-quality, normalized data.

---

## Dataset Information

The input dataset, `YOLOv10results.csv`, contains training and validation metrics across 100 epochs from a YOLOv10 model. The columns include:

- `epoch`: Epoch number
- Training loss components: `train/box_om`, `train/cls_om`, `train/dfl_om`, etc.
- Validation metrics: `metrics/precision(B)`, `metrics/recall(B)`, `metrics/mAP50(B)`, etc.
- Learning rates for parameter groups: `lr/pg0`, `lr/pg1`, `lr/pg2`

The dataset is entirely numeric and consists of 20 columns and 100 rows. There are no missing values.

---

## Tools & Technologies Used

- **Python 3.12**
- **Pandas** for data manipulation and analysis
- **Scikit-learn** for preprocessing, feature scaling, and dataset splitting
- **Joblib** for model serialization
- **Jupyter Notebook / VS Code** for implementation and documentation

---

## ETL Pipeline Steps

### 1. Extract
- The dataset was loaded using `pandas.read_csv()`.
- Initial inspection (`.head()`, `.info()`, `.isnull().sum()`) was performed to validate the integrity of the dataset.

### 2. Transform
- Column names were cleaned using `df.columns.str.strip()` to avoid formatting errors.
- The target variable selected was `metrics/mAP50(B)`.
- Features were separated from the target.
- The dataset was split into training and test sets using `train_test_split()` (80% train, 20% test).
- Feature scaling was applied using `StandardScaler` to ensure numerical consistency and optimize model convergence.

### 3. Load
- Transformed datasets (`X_train_scaled`, `X_test_scaled`, `y_train`, `y_test`) were saved to `.csv` format.
- The fitted `StandardScaler` was saved to a `.pkl` file using `joblib` for future use or deployment.

---

## Files in This Repository

| File Name                    | Description                                      |
|------------------------------|--------------------------------------------------|
| `YOLOv10results.csv`         | Raw input dataset from YOLOv10 model             |
| `Task1_ETL_Pipeline_Notebook.ipynb` | Jupyter Notebook with full ETL pipeline      |
| `X_train_scaled.csv`         | Scaled training feature matrix                   |
| `X_test_scaled.csv`          | Scaled test feature matrix                       |
| `y_train.csv`                | Training target values                           |
| `y_test.csv`                 | Test target values                               |
| `scaler.pkl`                 | Serialized fitted StandardScaler model           |
| `README.md`                  | Documentation and summary of this project        |

---

## How to Use

1. Clone or download the repository.
2. Open the `Task1_ETL_Pipeline_Notebook.ipynb` file in Jupyter Notebook or Google Colab.
3. Ensure that the file `YOLOv10results.csv` is in the working directory.
4. Run all notebook cells in sequence.
5. The pipeline will output processed CSVs and a saved scaler model.

---

## Purpose and Learning Outcomes

This task serves as a foundation for any data science or machine learning project. Proper data preprocessing is crucial for building reliable models. Through this project, I reinforced concepts such as:

- Data inspection and exploration
- Column cleanup and missing value analysis
- Feature-target separation
- Train-test splitting for validation
- Feature scaling using normalization techniques
- Efficient saving of model artifacts for deployment

These are essential components in real-world machine learning workflows.

---

## Submission

This repository is submitted as Task 1 in fulfillment of the Data Science Internship at CODTECH. It showcases my ability to design, automate, and document a professional ETL process, which is a fundamental skill for any aspiring data scientist.

## Output 

![Image](https://github.com/user-attachments/assets/ddda8635-7879-4d35-8c63-98dfe893f285)

![Image](https://github.com/user-attachments/assets/efe9e5d2-fe12-4efd-a0aa-dab65b06e7d9)

![Image](https://github.com/user-attachments/assets/95aa8bfc-3fa5-4004-b0b1-9e44155f24a8)
