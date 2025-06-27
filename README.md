# 🩺 Healthcare Data Cleaning and Exploratory Data Analysis (EDA) with Python

## 📂 Project Description
This project demonstrates data cleaning and exploratory data analysis (EDA) on synthetic healthcare datasets using Python (Pandas, Matplotlib, Seaborn). Multiple CSV files representing procedures, patients, encounters, and payers were imported, cleaned, and analyzed to extract meaningful insights about medical procedures, patient demographics, encounters, and payer coverage.

---

## 📁 Data Sources

- `procedure.csv` – Records of medical procedures performed
- `patients.csv` – Patient demographic and personal information
- `encounters.csv` – Healthcare encounter events
- `payers.csv` – Insurance payer information

---

## 🛠️ Data Cleaning Workflow

### 1. **Procedures Data (`procedure.csv`):**
- Converted `START` and `STOP` columns to datetime, extracted dates and times.
- Removed timezone information.
- Renamed and reordered columns for clarity.
- Removed duplicates.

### 2. **Patients Data (`patients.csv`):**
- Converted `BIRTHDATE` to datetime.
- Dropped irrelevant columns (`SUFFIX`, `MAIDEN`).
- Set `Id` as the index.
- Standardized categorical fields (`MARITAL`, `GENDER`).
- Cleaned and formatted patient names.
- Handled missing values in names and address fields.

### 3. **Encounters Data (`encounters.csv`):**
- Converted `START` and `STOP` to datetime, extracted start/stop dates and times.
- Cleaned text fields (`ENCOUNTERCLASS`), removed special characters.
- Reordered columns, removed duplicates.
- Set `Id` as the index.

### 4. **Payers Data (`payers.csv`):**
- Set `Id` as the index.

---

## 🔎 Exploratory Data Analysis (EDA)

### **A. Procedures**
- **Top 10 Most Frequent Procedures:**  
  - Visualized using horizontal bar charts.
- **Average BASE_COST by Procedure:**  
  - Identified and visualized top 10 procedures with the highest average base cost.
- **Missing Data:**  
  - Analyzed presence of `REASONCODE` using a donut chart.
  - Visualized missing values heatmap.

### **B. Patients**
- **Gender Distribution:**  
  - Calculated counts and proportions, visualized as a bar chart.
- **Race vs. Ethnicity:**  
  - Created a cross-tabulation and heatmap to show distributions.
- **Age Distribution:**  
  - Computed age from birthdate, visualized using a histogram.

### **C. Encounters**
- **Encounter Class Frequency:**  
  - Tabulated and plotted frequency of each encounter class.
- **Average Encounter Cost:**  
  - Analyzed average base encounter cost by encounter class.
- **Payer Coverage:**  
  - Calculated average payer coverage per payer and visualized.

### **D. Additional Analyses**
- **Top 10 REASONCODE Frequencies:**  
  - Identified and visualized most common reason codes.
- **Missing Data Summary:**  
  - Tabulated and visualized missing data for key columns.

---

## 📊 Sample Visualizations

- Top Procedures by Frequency (Bar Chart)
- Procedures by Average Cost (Bar Chart)
- Gender Distribution (Bar Chart)
- Race vs. Ethnicity (Heatmap)
- Age Distribution (Histogram)
- Encounter Class Frequency (Bar Chart)
- Average Cost by Encounter Class (Bar Chart)
- Payer Coverage (Bar Chart)
- Reason Codes (Bar Chart)
- Missing Data (Heatmap, Donut Chart)

---

## 📝 Usage

1. Clone or download the repository.
2. Place the CSV files in your working directory.
3. Open and run the Jupyter Notebook (`data_cleaning_eda.ipynb`) to reproduce the analysis and visualizations.

---

## 📁 Files Included

| File Name                 | Description                                      |
|---------------------------|--------------------------------------------------|
| `procedure.csv`           | Raw procedure data                               |
| `patients.csv`            | Raw patient demographic data                     |
| `encounters.csv`          | Raw encounter event data                         |
| `payers.csv`              | Raw payer/insurance data                         |
| `data_cleaning_eda.ipynb` | Python notebook containing all code and analysis |
| `README.md`               | Project documentation (this file)                |

---

## 💡 Key Insights

- The most common procedures, patient characteristics, and encounter types are easily visualized.
- Significant missing data in some medical coding fields, as visualized by the heatmap and donut chart.
- Encounter costs and payer coverage vary significantly by class and payer.

---

## 📦 Requirements

- Python 3.x
- pandas
- matplotlib
- seaborn

Install requirements with:
```bash
pip install pandas matplotlib seaborn
```

---

## 🤝 Acknowledgements

This project uses synthetic healthcare data for demonstration and educational purposes.

---

## 📓 Notebook

For full code and step-by-step outputs, see [`data_cleaning_eda.ipynb`](./data_cleaning_eda.ipynb).
.
