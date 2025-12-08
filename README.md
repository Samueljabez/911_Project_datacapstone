# 911 Calls Analysis Project

## Project Overview
This project analyzes 911 emergency calls from Montgomery County, PA. The notebook includes:

- Data cleaning and preprocessing
- Exploratory Data Analysis (EDA) with visualizations
- Feature extraction from timestamps (Hour, Month, Day of Week)
- Classification model to predict the type of emergency (EMS, Fire, Traffic)

## Dataset
- **Source:** Montgomery County, PA 911 calls dataset
- **Columns:** `lat`, `lng`, `desc`, `zip`, `title`, `timeStamp`, `twp`, `addr`, `e`
- **Note:** Dataset is **not included** due to file size. To run the notebook, place your `911.csv` in the same directory or update the file path in the notebook.

## Notebook Contents
1. **Data Loading and Cleaning**  
   - Handle missing values and drop unnecessary columns.

2. **Feature Engineering**  
   - Extract `Hour`, `Month`, `DayOfWeek`, and `Reason` from `title` and `timeStamp`.

3. **Exploratory Data Analysis (EDA)**  
   - Visualizations of 911 calls by Day of Week, Hour, Month, and Emergency Type.

4. **Machine Learning Model**  
   - Train a Random Forest classifier to predict emergency type.
   - Evaluate performance using precision, recall, and f1-score.

## How to Run
1. Clone or download this repository.
2. Install required libraries:
```bash
pip install pandas matplotlib seaborn scikit-learn
