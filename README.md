# Internship_Project_1-Customer-Segmentation-and-Prediction

# Customer Segmentation and Prediction

##  Project Overview
This project focuses on **customer segmentation** and **premium amount prediction** using demographic, behavioral, and policy-related data.  
The primary objectives are:
- Segment customers into meaningful groups based on purchasing and financial behavior.
- Predict **insurance premium amounts** using regression models.
- Generate insights to support **data-driven marketing strategies**.

---

##  Dataset
- **Source**: Kaggle (Customer Segmentation dataset)
- **Rows**: ~53,500  
- **Features**: 20 columns, including:
  - Demographics (Age, Gender, Education, Marital Status, Location, Occupation, Income Level)
  - Behavioral Data (Purchase History, Preferences, Communication Channels)
  - Insurance Details (Coverage Amount, Policy Type, Premium Amount, Products Owned)

---

##  Project Workflow
### 1. Data Preprocessing
- Handled missing values and duplicates (none found).
- Converted `Purchase History` to proper `datetime`.
- Dropped irrelevant identifiers (`Customer ID`).
- Encoded categorical variables (Gender, Education, Policy Type, Marital Status).
- Standardized numerical features (Age, Income Level, Coverage Amount, Premium Amount).

### 2. Exploratory Data Analysis (EDA)
- Gender distribution, education levels, marital status, and policy types explored via **SQL queries** and visualizations.
- Geographic segmentation analyzed (35 states/UTs).
- Income, coverage, and premium distributions plotted with histograms and boxplots.

### 3. Feature Engineering
- Created encoded and scaled versions of features.
- Prepared separate datasets for clustering and prediction.

### 4. Customer Segmentation (Clustering)
- **K-Means clustering** applied.
- Optimal clusters determined using the **Elbow Method**.
- Final segmentation: **3 customer groups**, visualized using `Income Level` vs. `Premium Amount`.

### 5. Predictive Modeling
- Target variable: **Premium Amount**  
- Models Used:
  - **Linear Regression** → R² ≈ 0.003 (weak performance, indicates non-linearity)
  - **Decision Tree Regressor** → R² ≈ 0.002 (slightly better splits but still weak)
- Metrics Evaluated: MAE, MSE, RMSE, R² Score.

---

##  Results & Insights
- **Segmentation** revealed 3 customer clusters:
  1. **High Income, Low Premium** → Potential for premium upgrades.
  2. **Low Income, High Coverage** → Require affordability-focused offers.
  3. **Average Customers** → Good candidates for cross-selling opportunities.
  
- **Prediction Models**: Both Linear Regression and Decision Tree showed very low R², indicating that **premium amount cannot be reliably predicted with the given features**.  
  👉 Suggests the need for more **behavioral and claims-related data**.

---

##  Tools & Technologies
- **Languages**: Python, SQL
- **Libraries**: Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
- **Techniques**: Data Cleaning, Feature Engineering, Clustering (K-Means), Regression (Linear & Decision Tree)

---

##  How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/Veer7733/Internship_Project_1-Customer_Segmentation-and-Prediction
   ``` 
2. Navigate to the project folder:
   ```bash
   cd Internship_Project_1-Customer_Segmentation-and-Prediction
   ```
3. Install the required libraries:
   ```bash
   pip install -r requirements.txt
   ```
4. Open the Jupyter Notebook:
   ```bash
   jupyter notebook Customer Segmentaion and prediction.ipynb
   ```
