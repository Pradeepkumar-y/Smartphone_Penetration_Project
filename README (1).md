# Smartphone Penetration Web Scraping & Data Analysis Project

## Overview
This project focuses on scraping smartphone penetration data from Wikipedia using Python.  
The scraped data is cleaned, processed, and analyzed to generate insights based on KPIs and visualizations.  
This project is submitted as part of the Web Scraping & Data Processing course at **ESILV – MSc Computer Science & Data Science, Paris**.
## Project Structure

Smartphone_Penetration_Project/
│
├── notebook/
│ └── smartphone_analysis.ipynb
│
├── data/
│ └── smartphone_penetration_clean.csv
│
├── output/
│ ├── top10_smartphone_penetration.png
│ ├── bottom10_smartphone_penetration.png
│ ├── distribution_penetration.png
│ ├── penetration_ranges.png
│ └── country_scatter.png
│
├── presentation/
│ └── Smartphone_Penetration_Project_Final_Presentation.pptx
│
├── requirements.txt
└── README.md

---

## Technologies & Libraries

- **Python 3.x**
- **Libraries Used:**
  - requests  
  - beautifulsoup4  
  - pandas  
  - numpy  
  - matplotlib  
  - seaborn  
  - html5lib  
  - lxml  

-

## Project Workflow

### 1. Web Scraping**
- Fetched the Wikipedia page using `requests` with a custom User-Agent header (to avoid 403).
- Parsed the HTML using **BeautifulSoup**.
- Extracted structured tables using `pandas.read_html()`.

### **2. Data Cleaning**
- Removed `%` symbols and formatted numeric values.
- Converted population and user numbers from `M` format to float.
- Standardized column names and data types.
- Created penetration range bins using `pd.cut()`.

### **3. Data Analysis**
Calculated **10+ KPIs**, including:
- Mean, Median, Standard Deviation  
- Highest & Lowest Penetration Countries  
- Penetration Range & Interquartile Range (IQR)  
- Weighted Penetration  
- Share of Countries ≥ 70%  
- Top-3 vs Bottom-3 comparison  
- Skewness indicator  

### **4. Visualizations**
Generated professional charts, including:
- Top 10 smartphone penetration  
- Bottom 10 smartphone penetration  
- Histogram distribution  
- Penetration range groups  
- Scatter plot (penetration by country)

All charts are stored in the /output/ folder.

---

## How to Run the Project

### **Step 1 — Install dependencies**
pip install -r requirements.txt

### **Step 2 — Start JupyterLab**
jupyter lab

### **Step 3 — Open notebook**
Navigate to:
notebook/smartphone_analysis.ipynb

### **Step 4 — Run all cells**
The notebook will:
- Fetch and scrape the data
- Clean the dataset
- Generate KPIs and visualizations
- Export `.csv` and `.png` files

---

##Key Findings (Summary)

- Smartphone penetration varies widely across countries.
- The U.S., Japan, and Russia show very high adoption.
- Pakistan and Nigeria show low penetration, indicating growth potential.
- Most countries fall in the **50–70% range**, suggesting moderate adoption levels.
- Clear digital divide exists between developed and developing nations.

## Author
**Yarragangi Reddy Pradeep Kumar Reddy**  
MSc Computer Science & Data Science  
ESILV – Paris La Défense

-- License
This project is intended for academic use only.
---
