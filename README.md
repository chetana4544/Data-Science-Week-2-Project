# Data-Science-Week-2-Project
# Superstore Data Analysis and Sales Prediction Project

## 1. Project Overview

This project uses a Superstore sales dataset to practise the main steps of data analysis and machine learning. It contains three tasks:

- **Task 1 – Data Cleaning:** Prepare the raw dataset by checking missing values and duplicates, correcting data types, standardizing values and saving a cleaned dataset.
- **Task 2 – Exploratory Data Analysis (EDA):** Explore the cleaned data using descriptive statistics, charts and sales summaries to find patterns and trends.
- **Task 3 – Sales Prediction Model:** Build Linear Regression and Random Forest models to predict sales, compare their performance and tune the Random Forest model.

The project is designed to run in **Google Colab** or Jupyter Notebook.

## 2. Project Files

| File | Description |
|---|---|
| `Task_1_Data_Cleaning.ipynb` | Notebook for cleaning the raw dataset |
| `Task 2 Superstore_EDA_.ipynb` | Notebook for exploratory data analysis |
| `Task_3_sales_prediction_model.ipynb` | Notebook for sales prediction |
| `superstore_dirty_308_rows.csv` | Raw dataset used in Task 1 |
| `superstore_cleaned.csv` | Cleaned dataset used in Tasks 2 and 3 |
| `README.md` | Project instructions |

Keep the notebooks and datasets in one project folder so that they are easy to find.

## 3. Software and Libraries

**Software:** Python 3, Google Colab or Jupyter Notebook.

**Python libraries:**
- Pandas – loading and working with datasets
- NumPy – numerical calculations
- Matplotlib and Seaborn – creating charts
- Scikit-learn – training and evaluating machine learning models

Google Colab already includes most of these libraries. Install them if required:

```python
!pip install pandas numpy matplotlib seaborn scikit-learn
```

## 4. How to Run the Project in Google Colab

1. Open [Google Colab](https://colab.research.google.com/).
2. Select **File → Upload notebook** and upload the notebook you want to run.
3. Upload the CSV file required for that task by using the folder icon on the left, or use the file-upload code in the notebook.
4. Check that the file name in `pd.read_csv()` matches the uploaded file.
5. Run the notebook cells from top to bottom.

Example for loading a CSV file in Colab:

```python
df = pd.read_csv('/content/superstore_dirty_308_rows.csv')
```

## 5. Recommended Project Execution Order

### Task 1 – Data Cleaning
1. Open `Task_1_Data_Cleaning.ipynb`.
2. Upload `superstore_dirty_308_rows.csv`.
3. Run all cells in order.
4. The notebook checks and cleans the data, then saves the cleaned file as `superstore_cleaned.csv`.

### Task 2 – Exploratory Data Analysis
1. Open `Task 2 Superstore_EDA_.ipynb`.
2. Upload `superstore_cleaned.csv`.
3. Make sure the loading code points to the Colab file:

```python
df = pd.read_csv('/content/superstore_cleaned.csv')
```

4. Run all cells to view descriptive statistics, charts, sales summaries and trends.

### Task 3 – Sales Prediction Model
1. Open `Task_3_sales_prediction_model.ipynb`.
2. Upload `superstore_cleaned.csv`.
3. Check that the dataset-loading code uses the correct Colab file path.
4. Run all cells to create features, split the data, train the models, compare results, view charts and perform hyperparameter tuning.

**Run the tasks in this order:** Task 1 → Task 2 → Task 3. Tasks 2 and 3 use the cleaned dataset created in Task 1.

## 6. Model Evaluation in Task 3

The sales prediction models are evaluated using these measures:

- **RMSE (Root Mean Squared Error):** Measures prediction errors and gives larger errors more weight. A lower value is better.
- **MAE (Mean Absolute Error):** Shows the average absolute difference between actual and predicted sales. A lower value is better.
- **R-squared (R²):** Shows how much variation in sales is explained by the model. A value closer to 1 is generally better; a negative value indicates poor performance on the test data.

The notebook also creates a feature-importance chart and an actual-versus-predicted sales chart. GridSearchCV is used to test different Random Forest settings.

## 7. Expected Outputs

After running the notebooks, the project should produce:

- A cleaned dataset named `superstore_cleaned.csv`.
- Summary statistics and visualizations from the EDA notebook.
- A model comparison table showing RMSE, MAE and R².
- A feature-importance chart.
- An actual-versus-predicted sales chart.
- Final evaluation results for the tuned model.

Download important outputs from Colab if you need to include them in your submission. Colab session files may be cleared when the runtime disconnects.

## 8. Notes and Limitations

- Run notebook cells in order, from the first cell to the last.
- If you see a file-not-found error, check that the CSV is uploaded and that the file path and spelling are correct.
- Use the actual evaluation results printed by your notebook. Do not claim high prediction accuracy unless the metrics support it.
- The dataset is relatively small, so the prediction results may be limited.
- Task 3 uses previous-order sales features. This is suitable for a one-step-ahead setup where previous sales are already known; it is not automatically a multi-step forecast of future sales.

## 9. Conclusion

This project demonstrates a basic workflow for data cleaning, exploratory data analysis and machine learning using Python. It prepares the Superstore dataset, explores sales patterns and trains regression models to estimate sales. The results can help understand the dataset and practise model evaluation, while further data and improvements would be needed for dependable business forecasting.
