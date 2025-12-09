911 Calls Analysis Project
Project Overview

This project analyzes 911 emergency calls from Montgomery County, PA. The notebook demonstrates end-to-end data analysis, including:

Data cleaning and preprocessing

Feature extraction from timestamps (Hour, Month, DayOfWeek)

Exploratory Data Analysis (EDA) with visualizations

Classification model to predict the type of emergency (EMS, Fire, Traffic)

Dataset

Source: Montgomery County, PA 911 calls dataset

Columns: lat, lng, desc, zip, title, timeStamp, twp, addr, e

Note: Dataset is not included due to size. Place your 911.csv in the project folder or update the file path in the notebook.

Notebook Contents

Data Loading and Cleaning

Handle missing values (twp set to "Unknown")

Standardize call types (EMS, Fire, Traffic)

Drop unnecessary columns

Feature Engineering

Extract Hour, Month, DayOfWeek from timeStamp

Extract Class (EMS, Fire, Traffic) from title

Exploratory Data Analysis (EDA)

Line charts: Yearly call trends per class

Monthly and daily trends for seasonality

Heatmaps: Township vs Class, Hour vs Class

Bar charts and pie charts: Top townships, top addresses, class distribution

Machine Learning Model

Train a Random Forest classifier to predict emergency type

Evaluate using accuracy, precision, recall, and F1-score

Analyze model performance, noting challenges with class imbalance

Challenges Encountered

Missing township values: Filled with "Unknown" to retain data.

Inconsistent call titles: Standardized call types for analysis.

Class imbalance: Fire calls were underrepresented, reducing predictive performance.

Feature limitations: Only location and time features were available; adding more features could improve predictions.

Key Insights

EMS calls are most frequent, peaking in mornings and afternoons.

Fire calls are rare, with seasonal spikes in summer months.

Traffic calls are concentrated in specific townships.

Peak call hours differ by emergency type, highlighting resource allocation needs.

How to Run

Clone or download the repository:

git clone https://github.com/Samueljabez/911_Project_datacapstone.git


Place 911.csv in the project folder.

Install required libraries:

pip install pandas matplotlib seaborn scikit-learn


Open and run analysis.ipynb in Jupyter Notebook or VS Code.

Technologies & Libraries

Python 3.x

Pandas, NumPy

Matplotlib, Seaborn

Scikit-learn

Conclusion

This project demonstrates intermediate-level data science skills, including real-world data cleaning, visualization, feature engineering, and classification modeling. It forms a strong foundation for more advanced projects such as Recommender Systems or Generative AI.
