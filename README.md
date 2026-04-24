# 📊 Student Performance Prediction

A machine learning research project that predicts **student academic performance (final grade G3)** using regression techniques. Built with Python, trained on the **UCI Student Performance Dataset (student-mat.csv)**, and published as a research paper.

> \*\*Authors:\*\* Uday Aggarwal, Himanshu Sharma, Hargun Singh, Drishti Sharma
>
> \*\*Supervised by:\*\* Dr. Gurpreet Singh
>
> \*\*Institution:\*\* Chitkara University Institute of Engineering and Technology, Punjab, India

\---

## 📁 Project Structure

```
student-performance-prediction/
├── Student\_Performance\_Prediction.ipynb   # Full notebook
├── student-mat.csv                        # Dataset
└── README.md
```

\---

## 🚀 Getting Started

### Prerequisites

* Python 3.7+
* Jupyter Notebook or Google Colab
* pip

### 1\. Clone the Repository

```bash
git clone https://github.com/udayaggarwal-26/student-performance-prediction.git
cd student-performance-prediction
```

### 2\. Install Dependencies

```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
```

### 3\. Launch Jupyter Notebook

```bash
jupyter notebook
```

Then open `Student\_Performance\_Prediction.ipynb` and run all cells from top to bottom.

> \*\*Or open directly in Google Colab:\*\*
> Upload the notebook and `student-mat.csv` to your Google Drive, then run the cells.

\---

## 🧠 How It Works

1. **Data Loading** — Loads `student-mat.csv` (semicolon-separated) containing 395 student records with 33 features including demographics, social, and academic attributes. Target variable is `G3` (final grade, range 0–20).
2. **Exploratory Data Analysis** — Inspects dataset shape, column types, and checks for missing values.
3. **Data Preprocessing** — Encodes all categorical (object-type) columns using **Label Encoding** to convert them into numerical format suitable for ML models.
4. **Feature \& Target Split** — Separates features (`X`) from the target variable (`y = G3`), followed by an 80/20 train-test split with `random\_state=42`.
5. **Feature Scaling** — Applies **StandardScaler** to normalize feature values for improved model performance, especially for linear models.
6. **Model Training** — Trains four regression models:

   * Linear Regression
   * Ridge Regression
   * Decision Tree Regressor
   * Random Forest Regressor
7. **Evaluation** — Compares models using **MAE**, **MSE**, and **R² Score** metrics, with bar chart visualizations for each metric.
8. **Best Model Selection** — Identifies the best-performing model based on highest R² Score.
9. **Feature Importance** — Extracts and visualizes the **Top 10 most important features** from the Random Forest model.

\---

## 📊 Dataset

|File|Description|
|-|-|
|`student-mat.csv`|Math course student data with 395 records, 33 features|

Key columns: `age`, `studytime`, `failures`, `absences`, `G1`, `G2`, `G3` (target), and more.
Source: **UCI Machine Learning Repository — Student Performance Dataset**.

\---

## 📦 Dependencies

|Library|Purpose|
|-|-|
|`pandas`|Data loading and manipulation|
|`numpy`|Numerical operations|
|`scikit-learn`|ML models, preprocessing, evaluation|
|`matplotlib`|Plotting and visualization|
|`seaborn`|Enhanced visualizations|

\---

## ✅ Results

|Model|MAE|MSE|R² Score|Rank|
|-|-|-|-|-|
|Linear Regression|1.421|3.872|0.7614|3rd|
|Ridge Regression|1.418|3.855|0.7625|2nd|
|Decision Tree|1.734|5.190|0.6817|4th|
|**Random Forest**|**1.147**|**2.838**|**0.8288**|**1st**|

> \*\*Random Forest\*\* achieved the best performance with the highest R² Score of \*\*0.8288\*\* and lowest MAE of \*\*1.147\*\*.

\---

## 👥 Team Contributions

|#|Role|Contributor|Work|
|-|-|-|-|
|1|Project Lead \& Primary Developer|Uday Aggarwal|Project coordination, library setup, dataset loading, exploratory data analysis, preprocessing, model integration, and end-to-end workflow development|
|2|Data \& Preprocessing Lead|Himanshu Sharma|Label encoding, train-test split, feature scaling|
|3|Model Development Lead|Hargun Singh|Training Linear, Ridge, Decision Tree, and Random Forest models|
|4|Evaluation \& Writing Lead|Drishti Sharma|Metric evaluation, visualizations, feature importance, manuscript preparation|

\---

## 🛠️ Troubleshooting

* **FileNotFoundError for CSV?** Make sure `student-mat.csv` is uploaded to your Google Drive at `/content/drive/MyDrive/student-mat.csv`, or update the path in the notebook accordingly.
* **Google Drive not mounting?** Run this cell first and follow the authentication prompt:

```python
  from google.colab import drive
  drive.mount('/content/drive')
  ```

* **Module not found?** Install missing libraries using:

```bash
  pip install pandas numpy scikit-learn matplotlib seaborn
  ```

\---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

