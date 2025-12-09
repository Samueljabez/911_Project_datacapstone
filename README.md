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
## Challenges Encountered

### Missing Township Values
- Some rows had missing `twp` (township) data.  
- **Solution:** Filled missing values with `"Unknown"` to retain all data for analysis.

### Inconsistent Call Titles
- Call titles had varying formats (e.g., `EMS: BACK PAINS/INJURY`, `Fire: ALARM`).  
- **Solution:** Standardized emergency call types into three main classes: **EMS**, **Fire**, **Traffic**.

### Class Imbalance
- **Fire calls** were significantly fewer than EMS or Traffic calls.  
- **Impact:** Lower predictive performance for Fire in the classification model.  
- **Future Improvement:** Oversampling techniques or additional features could improve balance.

### Feature Limitations
- Only time (`Hour`, `Month`, `DayOfWeek`) and location (`twp`, `addr`) features were available.  
- **Impact:** Limited information for modeling; predictive performance could improve with richer features.

---

## Key Insights

### EMS Calls
- Most frequent type of emergency call.  
- **Peak Times:** Morning and afternoon hours.  

### Fire Calls
- Rare compared to other call types.  
- Exhibit **seasonal spikes**, especially during summer months.  

### Traffic Calls
- Concentrated in **specific high-traffic townships**.  
- Patterns can help identify hotspots for traffic management.

### Peak Call Hours
- Vary by emergency type.  
- **Insight:** Helps in **resource allocation and planning** for emergency services.

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
## Conclusion

This project demonstrates an **intermediate-level data science workflow** on real-world 911 call data. Key takeaways include:

- **End-to-End Analysis:** From data cleaning and preprocessing to visualization and feature extraction.  
- **Exploratory Insights:** Identified patterns in call types, peak hours, seasonal trends, and township hotspots.  
- **Predictive Modeling:** Built a multi-class classification model to predict emergency type, highlighting challenges such as class imbalance and limited features.  
- **Practical Application:** Insights can help emergency services with **resource allocation, planning, and prioritization**.  

Overall, this project showcases the ability to handle messy real-world data, extract actionable insights, and apply machine learning — forming a solid foundation for more advanced projects like **Recommender Systems** or **Generative AI**.
