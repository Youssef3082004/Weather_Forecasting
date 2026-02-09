# Weather Forecasting Project
<div align="center">

[![Python](https://img.shields.io/badge/Python-3.13+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Pandas](https://img.shields.io/badge/Pandas-2.2.3+-3776AB?style=for-the-badge&logo=pandas&logoColor=white)](https://python.org)
[![NumPy](https://img.shields.io/badge/NumPy-1.26+-013243?style=for-the-badge&logo=numpy&logoColor=white)](https://numpy.org)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.4+-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-3.9+-11557C?style=for-the-badge&logo=matplotlib&logoColor=white)](https://matplotlib.org)
[![Seaborn](https://img.shields.io/badge/Seaborn-0.13+-4C72B0?style=for-the-badge&logo=python&logoColor=white)](https://seaborn.pydata.org)


</div>

## 📌 Overview
This project focuses on predicting weather conditions based on meteorological data. Using a dataset of daily weather observations, the project applies various Machine Learning algorithms to classify the weather into categories such as **Rain, Sun, Drizzle, Snow, and Fog**.

## 📂 Project Structure
- **`Model.ipynb`**: The Jupyter Notebook containing the end-to-end workflow: data preparation, visualization, preprocessing, and model training.
- **`seattle-weather.csv`**: The dataset containing historical weather data used for training and testing.

## 📊 Dataset Description
The [**Dataset**](https://www.kaggle.com/datasets/mahdiehhajian/seattle-weather/data) consists of daily records with the following features:

| Column | Description |
| :--- | :--- |
| **date** | The date of the observation |
| **precipitation** | Amount of precipitation |
| **temp_max** | Maximum temperature recorded |
| **temp_min** | Minimum temperature recorded |
| **wind** | Wind speed |
| **weather** | Target Variable (drizzle, rain, sun, snow, fog) |

## 🛠️ Technologies & Libraries
The project is built using Python and the following libraries:
* **Data Manipulation**: `pandas`, `numpy`
* **Visualization**: `seaborn`, `matplotlib`
* **Machine Learning** (Scikit-Learn):
    * `RandomForestClassifier`
    * `GradientBoostingClassifier`
    * `AdaBoostClassifier`
    * `LogisticRegression`
    * `SVC`
    * `DecisionTreeClassifier`
* **Preprocessing**: `imblearn` (RandomOverSampler), `StandardScaler`

## ⚙️ Data Preprocessing
To improve model performance, the following preprocessing steps were applied:

1.  **Feature Engineering**:
    * Extracted the **Month** from the `date` column to capture seasonal trends.
    * Dropped the original `date` column after extraction.

2.  **Handling Imbalanced Data**:
    * Analyzed the target distribution and identified class imbalance (e.g., significantly more "Sun" or "Rain" days than "Snow").
    * Applied **`RandomOverSampler`** to balance the dataset, ensuring the model learns equally from all weather types.

3.  **Data Splitting**:
    * Split the data into training and testing sets to evaluate performance on unseen data.

## 📈 Modeling & Evaluation
The notebook explores multiple classification algorithms. The primary workflow includes:
1.  **Training**: Fitting models (like Random Forest) on the oversampled training data.
2.  **Evaluation**: Using metrics such as **Accuracy Score**, **Confusion Matrix**, and **Classification Report** to assess performance.
3.  **Prediction**: Testing the model with custom inputs (e.g., specific month, temp, and wind conditions) to predict the weather.

## ✅ Models Accuracy
![Demo Image](assets/acc.png)

## 🟢 Confusion Matrix
![Demo Image](assets/confusion.png)



## 🚀 How to Run
1.  Install the required dependencies:
    ```bash
    pip install pandas numpy seaborn matplotlib scikit-learn imbalanced-learn
    ```
2.  Ensure `seattle-weather.csv` is in the project directory.
3.  Open and run `Model.ipynb` to see the analysis and predictions.