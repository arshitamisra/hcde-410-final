# A5 - Final Project - Diabetes in Washington State (Focus on Seattle)**  

---

## **1. Project Description**  
This project analyzes diabetes prevalence in Washington State from 2016 to 2021, focusing on King County's trends, the impact of Seattle's 2018 Sweetened Beverage Tax, and the relationship between socioeconomic factors such as median household income and diabetes rates. The analysis was conducted using Python with libraries such as Pandas, Plotly, and Scikit-learn.

---

## **2. Data Sources**  
The project used publicly available datasets:  

| **Source**                          | **Dataset**                               | **Link**                                      |
|--------------------------------------|--------------------------------------------|-----------------------------------------------|
| CDC U.S. Diabetes Atlas              | Diabetes Prevalence (2016-2021)           | [CDC Diabetes Atlas](https://www.cdc.gov/)   |
| County Health Rankings               | County-Level Median Income (2016-2021)    | [County Health Rankings](https://www.countyhealthrankings.org/) |
| Local Data Tool (Online Analysis)   | Obesity vs Diabetes Data (2021 only)      | Internal Analysis Tool                       |

---

## **3. Data Cleaning Process**  

### **A. Standardized Columns**  
- Renamed columns by converting to lowercase and replacing spaces with underscores.  
- Removed extra whitespace characters.  

### **B. Handled Missing and Invalid Data**  
- Removed rows with missing values in key columns such as:  
  - `diabetes_percentage`  
  - `median_income`  
- Ensured numerical columns were converted to the appropriate data types.  

### **C. Combined Yearly Data**  
- Loaded separate yearly `.csv` files (2016-2021).  
- Combined them into a single DataFrame using Pandas' `concat()` function.  

### **Final Columns After Cleaning**  
| **Column Name**           | **Description**                          |
|---------------------------|--------------------------------------------|
| `year`                    | Year of the dataset                      |
| `county`                  | County name                              |
| `diabetes_percentage`     | Diagnosed diabetes percentage            |
| `median_income`           | Median household income (in USD)         |
| `obesity_percentage`      | Percentage of the population with obesity (if available) |

---

## **4. Analysis Breakdown**  

### **Research Question 1: Statewide Diabetes Trends (2021)**  
- **Objective**: Examine the relationship between obesity and diabetes rates across Washington counties.  
- **Method**:  
  - Created a scatter plot of diabetes vs obesity rates.  
  - Highlighted King County in red.  

**Visualization Summary:**  
- Counties with high obesity rates generally showed higher diabetes percentages.  
- King County was a positive outlier, showing significantly lower rates than other counties.  

---

### **Research Question 2: Impact of Seattle’s Sweetened Beverage Tax**  
- **Objective**: Analyze how King County's diabetes rates changed from 2017 to 2021, focusing on the 2018 tax implementation.  
- **Method**:  
  - Created a time-series line chart of King County's diabetes rates.  
  - Added a vertical line marking the 2018 tax implementation.  

**Key Insight:**  
- Diabetes rates in King County declined by ~1% from 2018 to 2021, potentially linked to the tax.  

---

### **Research Question 3: Income vs Diabetes Prevalence**  
- **Objective**: Analyze the correlation between median household income and diabetes prevalence.  
- **Method**:  
  - Conducted a linear regression using Scikit-learn.  
  - Calculated regression metrics: slope, intercept, and R² value.  
  - Created residual and regression plots using Plotly.  

**Key Insight:**  
- The regression indicated a weak negative correlation (R² ~0.06).  
- Higher income was associated with slightly lower diabetes rates, though other factors likely played a more significant role.  

---

## **5. Visualizations Generated**  

1. **Scatter Plot:** Diabetes vs Obesity (2021)  
2. **Time-Series Plot:** Diabetes Rates in King County (2017-2021)  
3. **Histograms:** Distribution of Diabetes and Median Income  
4. **Regression Line:** Median Income vs Diagnosed Diabetes Rates  
5. **Residual Plot:** Validating the Linear Regression Model  

---

## **6. Libraries Used**  

- **Data Analysis:** Pandas, NumPy  
- **Visualization:** Plotly Express, Plotly Graph Objects  
- **Modeling:** Scikit-learn  
- **Environment:** Jupyter Notebook  

---

## **8. Project Folder Structure**  

```plaintext
📁 diabetes-analysis
│
├── 📁 data               # All CSV files
│   ├── 2016-income.csv
│   ├── 2017-income.csv
│   ├── 2018-income.csv
│   ├── 2019-income.csv
│   ├── 2020-income.csv
│   └── 2021-income.csv
│
├── 📁 visuals            # All generated plots
├── analysis.ipynb        # Jupyter Notebook file
├── requirements.txt      # Required libraries
├── LICENSE               # License file
└── README.md             # This file
```

---

## **9. Findings and Conclusions**  

| **Category**                    | **Finding**                               |
|----------------------------------|--------------------------------------------|
| **Diabetes vs Obesity**          | Strong positive correlation               |
| **Sweetened Beverage Tax**       | Modest decrease in King County diabetes   |
| **Income vs Diabetes**           | Weak negative correlation (R² = 0.06)    |

---

## **10. Acknowledgments**  

- **Data Sources:**  
  - CDC U.S. Diabetes Atlas  
  - County Health Rankings  

- **Research & Code Support:**  
  - Python Libraries: Pandas, Plotly, Scikit-learn  
  - ChatGPT for technical guidance and debugging assistance  

---

## **11. License**  
This project is licensed under the MIT License. See the `LICENSE` file for details.