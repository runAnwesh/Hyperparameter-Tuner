# Hyperparameter Optimization App (Regression Edition)

This project is a web-based application for hyperparameter tuning of regression models using Random Forests. Built with Streamlit, it allows users to upload their own datasets, configure hyperparameters, and visualize model performance interactively.

## Features
- **Upload your own CSV dataset** for regression tasks
- **Interactive hyperparameter tuning** for RandomForestRegressor:
  - Number of estimators (`n_estimators`)
  - Max features (`max_features`)
  - Minimum samples split (`min_samples_split`)
  - Minimum samples leaf (`min_samples_leaf`)
  - Criterion, bootstrap, oob_score, random state, n_jobs
- **Grid search** with cross-validation for optimal parameters
- **3D surface plot** of hyperparameter performance
- **Downloadable results** for further analysis
- Option to use the built-in Diabetes dataset as an example

## Installation

1. **Clone the repository:**
   ```bash
   git clone <repo-url>
   cd Hyperparameter-Tuner
   ```
2. **Install dependencies:**
   It is recommended to use a virtual environment.
   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. **Run the Streamlit app:**
   ```bash
   streamlit run hyper_tuner.py
   ```
2. **Open your browser** and go to the local URL provided by Streamlit (usually http://localhost:8501).
3. **Upload your CSV file** in the sidebar, or use the example Diabetes dataset.
4. **Set hyperparameters** using the sidebar controls.
5. **View results** including model performance, best parameters, and a 3D plot of the grid search.
6. **Download the results** as a CSV file for further analysis.

### Input Data Format
- The uploaded CSV should have features in all columns except the last, which should be the target variable (Y).
- The app automatically splits the data into training and test sets based on your chosen ratio.

## Customization
- You can modify the code in `hyper_tuner.py` to add more models, metrics, or hyperparameters.
- The app uses `RandomForestRegressor` from scikit-learn and `GridSearchCV` for hyperparameter optimization.

## Dependencies
See `requirements.txt` for the full list. Main packages:
- streamlit
- pandas
- numpy
- plotly
- scikit-learn
