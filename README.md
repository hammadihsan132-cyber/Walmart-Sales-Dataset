#  Walmart Sales Prediction using XGBoost

##  Project Overview

This project focuses on analyzing Walmart sales data and building a machine learning model to predict weekly sales. The goal is to extract meaningful business insights and develop a high-performance predictive model using **XGBoost**.



##  Dataset Description

The dataset contains historical sales data of Walmart stores along with external factors such as:

* Store number
* Date
* Weekly Sales
* Holiday Flag
* Temperature
* Fuel Price
* CPI (Consumer Price Index)
* Unemployment rate



##  Exploratory Data Analysis (EDA)

###  Key Analysis Performed:

* Total sales per store
* Top 5 and bottom 5 performing stores
* Average sales per store
* Sales trends over time (weekly, monthly, yearly)
* Holiday vs Non-Holiday sales comparison
* Correlation analysis with external factors

###  Visualizations:

* Bar charts for avg sales per store performance
  <img width="695" height="429" alt="image" src="https://github.com/user-attachments/assets/c305e81f-d016-4151-8e8b-5df0152cb3db" />

* Time series plots for  total sales trends
<img width="657" height="458" alt="image" src="https://github.com/user-attachments/assets/3a595920-a1cf-4a28-a70b-77607d7283c9" />

* Heatmap for correlation analysis
<img width="611" height="439" alt="image" src="https://github.com/user-attachments/assets/67364268-7b65-411e-8deb-56d82d778453" />

* Scatter plots for feature relationships
  <img width="642" height="452" alt="image" src="https://github.com/user-attachments/assets/e4aa99f6-acbf-40ff-9826-baab1bbf480b" />


##  Feature Engineering

To improve model performance, several features were created:

###  Date Features:

* Year
* Month
* Week of Year
* Day of Week

###  Lag Features:

* Lag_1 (previous week sales)
* Lag_2 (two weeks previous sales)

###  Rolling Features:

* Rolling Mean (3-week average)

###  Interaction Features:

* Temperature × Fuel Price



##  Model Building

### Model Used:

* **XGBoost Regressor**

### Data Splitting:

* Time-based split (train/test)
* Also experimented with random split using `train_test_split`



##  Model Evaluation

The model was evaluated using:
* **Mean Squared Error: 1797385417.586713**
* **RMSE (Root Mean Squared Error): 42395.582524441306**
* **MAE (Mean Absolute Error): 21970.848817987568**
* **R² Score:  0.994775864802881**

These metrics help measure prediction accuracy and model performance.



##  Feature Importance

XGBoost feature importance was plotted to identify the most influential factors affecting sales.

<img width="704" height="462" alt="image" src="https://github.com/user-attachments/assets/a298fbe4-137c-4e46-8d92-4ef03ea33a65" />


##  Model Saving

The trained model was saved using:

```python
import joblib
joblib.dump(model, "sales_model.pkl")
```



##  How to Run the Project

1. Clone the repository:

```bash
git clone https://github.com/your-username/walmart-sales-prediction.git
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Run the notebook:

```bash
jupyter notebook walmart.ipynb
```



##  Requirements

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* XGBoost
* Joblib



##  Key Insights

* Certain stores consistently outperform others
* Holiday seasons significantly impact sales
* External factors like CPI and unemployment show correlation with sales
* Time-based features improve prediction accuracy



##  Future Improvements

* Hyperparameter tuning for XGBoost
* Use of advanced time series models (LSTM, Prophet)
* Deployment as a web app (Streamlit / Flask)
* Real-time sales prediction system



##  Author

**Hammad Ihsan**



##  If you like this project

Give it a star ⭐ on GitHub and share your feedback!
## Acknowledgment
This README was created with the assistance of AI tools  to improve clarity, structure, and presentation.
**The project implementation and analysis are my own work.**


