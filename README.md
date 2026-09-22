# Heart-Stroke-Prediction


# ❤️ Heart Disease Prediction using Machine Learning

A machine learning project that predicts the likelihood of heart disease based on patient health-related features.

The project includes data preprocessing, comparison of multiple machine learning algorithms, selection of the best-performing model, model serialization using Joblib, and a **Streamlit web application** for interactive predictions.

## 📌 Project Overview

Heart disease is one of the major health conditions that can be influenced by various medical and lifestyle factors.

In this project, multiple machine learning models are trained and evaluated using a heart disease dataset. Their performance is compared, and the best-performing model is selected for further use.

The selected model is then saved using **Joblib** and integrated into a **Streamlit application** that provides a simple user interface for making predictions.

## 🚀 Project Workflow

```text
Heart Disease Dataset
        ↓
Data Preprocessing
        ↓
Exploratory Data Analysis
        ↓
Train/Test Split
        ↓
Train Multiple ML Models
        ↓
Compare Model Performance
        ↓
Select Best Model
        ↓
Save Model + Scaler + Columns
        ↓
Build Streamlit Application
        ↓
Heart Disease Prediction
```

## 🧠 Machine Learning

The project tests multiple machine learning algorithms and compares their performance using evaluation metrics such as accuracy.

The **K-Nearest Neighbors (KNN)** model was selected for the final application based on the model evaluation performed in the notebook.

### KNN

KNN predicts the class of a new data point based on the classes of its nearest neighbors.

For this project, feature scaling is applied before making predictions because KNN is distance-based.

## 📊 Dataset

The project uses `heart.csv`, which contains health-related features used for predicting heart disease.

The dataset is used for:

* Data preprocessing
* Exploratory data analysis
* Model training
* Model evaluation
* Heart disease prediction

## 🛠️ Technologies Used

### Programming Language

* Python

### Machine Learning

* Scikit-learn
* K-Nearest Neighbors (KNN)
* Model evaluation
* Feature scaling

### Data Analysis

* NumPy
* Pandas
* Matplotlib
* Seaborn

### Deployment / Application

* Streamlit
* Joblib

### Development Tools

* Jupyter Notebook
* VS Code
* Git
* GitHub

## 📁 Project Structure

```text
Heart-Disease-Machine-Learning/
│
├── HeartDisease_MachineLearningProject_2.ipynb
├── heart.csv
│
├── KNN_heart.pkl
├── scaler.pkl
├── columns.pkl
│
├── app.py
│
└── README.md
```

### File Description

| File                                          | Description                                                                 |
| --------------------------------------------- | --------------------------------------------------------------------------- |
| `HeartDisease_MachineLearningProject_2.ipynb` | Data analysis, preprocessing, model training, testing, and model comparison |
| `heart.csv`                                   | Heart disease dataset                                                       |
| `KNN_heart.pkl`                               | Trained KNN model                                                           |
| `scaler.pkl`                                  | Feature scaler used during preprocessing                                    |
| `columns.pkl`                                 | Feature column information required by the application                      |
| `app.py`                                      | Streamlit application                                                       |
| `README.md`                                   | Project documentation                                                       |

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone <your-repository-url>
```

### 2. Navigate to the project directory

```bash
cd Heart-Disease-Machine-Learning
```

### 3. Install dependencies

```bash
pip install numpy pandas matplotlib seaborn scikit-learn joblib streamlit
```

## ▶️ Run the Streamlit Application

Run the following command from the project directory:

```bash
streamlit run app.py
```

The application will open in your browser.

## 🖥️ Streamlit Application

The Streamlit application provides an interactive interface where users can enter the required health-related information.

The application then:

1. Collects user input.
2. Converts the input into the required format.
3. Applies the saved scaler.
4. Loads the trained KNN model.
5. Performs the prediction.
6. Displays the prediction result.

## 🔄 Model Deployment Workflow

The trained components are saved using Joblib:

```python
joblib.dump(model, "KNN_heart.pkl")
joblib.dump(scaler, "scaler.pkl")
joblib.dump(columns, "columns.pkl")
```

The Streamlit application loads these files:

```python
model = joblib.load("KNN_heart.pkl")
scaler = joblib.load("scaler.pkl")
columns = joblib.load("columns.pkl")
```

This allows the trained model to be reused without retraining every time the application starts.

## 📈 Model Evaluation

Multiple machine learning models were tested in the notebook and their performance was compared.

The final KNN model was selected for integration into the Streamlit application based on the evaluation performed during the project.

> Note: Model accuracy can vary depending on the dataset, preprocessing, train/test split, random state, and scikit-learn version.

## 🎯 Key Features

* 📊 Heart disease dataset analysis
* 🧹 Data preprocessing
* 🤖 Multiple ML model comparison
* 📈 Model evaluation
* 📏 Feature scaling
* 🧠 KNN-based prediction
* 💾 Model serialization using Joblib
* 🖥️ Interactive Streamlit UI
* 🔄 Reusable trained model for applications

## 🔮 Future Improvements

* Add additional evaluation metrics such as Precision, Recall, F1-Score, and ROC-AUC.
* Perform hyperparameter tuning for KNN.
* Add cross-validation.
* Compare additional machine learning algorithms.
* Improve the Streamlit UI.
* Add prediction probability/confidence where appropriate.
* Deploy the application using a cloud platform.
* Add model monitoring and versioning.

## ⚠️ Disclaimer

This project is created for **educational and demonstration purposes only**.

The predictions generated by this application should not be considered medical advice or used as a substitute for professional medical diagnosis or treatment.

## 👨‍💻 Author

**Vaibhav Aher**

B.Tech Computer Science & Engineering (AI & ML)

GitHub: `github.com/vaibhavaherlazyprogrammer`
