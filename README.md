# CAR-MARKET-TRENDS-ANALYSIS-WITH-CARDEKHO-DATA

## Project Overview

**Project Title:** Car Market Trends Analysis with CarDekho Data  
**Student:** Vishakha Vinod Rawat
**Internship ID:** IBMUEDA1055  
**Domain:** Automobile / Data Analytics  
**Development Environment:** Jupyter Notebook / Google Colab

This project analyzes a CarDekho dataset using Python to understand used-car market characteristics and relationships involving selling price, manufacturing year, fuel type, seller type, transmission, and other vehicle attributes.

The analysis is descriptive and exploratory. It uses statistical summaries and visualizations to identify patterns in the available dataset.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook / Google Colab

## Project Files

```text
CarDekho-Market-Trends-Analysis/
│
├── cardekho(1).ipynb
├── 1776311302-P3-Car Market Trends Analysis with Car Dekho Data.csv
├── requirements.txt
├── README.md
└── AICTE(1).pptx
```

> Keep the CSV dataset in the same working directory as the notebook, or update the CSV path in the notebook.

## Dataset

The notebook loads the dataset using:

```python
data = pd.read_csv(
    '/content/1776311302-P3-Car Market Trends Analysis with Car Dekho Data.csv'
)
```

The dataset contains **301 records and 9 columns**:

- `Car_Name`
- `Year`
- `Selling_Price`
- `Present_Price`
- `Kms_Driven`
- `Fuel_Type`
- `Seller_Type`
- `Transmission`
- `Owner`

### Dataset Summary

The notebook reports:

- Rows: **301**
- Columns: **9**
- Duplicate rows before removal: **2**
- Average selling price: **4.6613 lakh**
- Highest selling price: **35.0 lakh**
- Lowest selling price: **0.1 lakh**
- Average manufacturing year: **2013.63**
- Average kilometres driven: **36,947 km**

The notebook's `info()` output shows:

- 2 floating-point columns
- 3 integer columns
- 4 object/string columns
- All 301 rows are non-null in the displayed dataset information.

## Data Quality Checks

The notebook performs:

1. Data loading using Pandas.
2. First-five and last-five record inspection.
3. Descriptive statistics using `data.describe()`.
4. Dataset shape inspection.
5. Column-name inspection.
6. `data.info()` inspection.
7. Duplicate-row checking.
8. Category-frequency checks for car name, fuel type, transmission and year.
9. Calculation of average, maximum and minimum selling price.

The notebook reports **2 duplicate rows**.

## Analysis Performed

### 1. Cars by Fuel Type

The notebook calculates:

- Petrol: **239 cars**
- Diesel: **60 cars**
- CNG: **2 cars**

The corresponding pie chart reports approximately:

- Petrol: **79.4%**
- Diesel: **19.9%**
- CNG: **0.7%**

### 2. Distribution of Seller Types

The notebook reports:

- Dealer: **195 cars**
- Individual: **106 cars**

This corresponds to approximately:

- Dealer: **64.8%**
- Individual: **35.2%**

### 3. Count of Cars by Fuel Type

A bar chart visualizes the same fuel-type counts, showing Petrol as the largest category, followed by Diesel and then CNG.

### 4. Average Selling Price by Transmission Type

The notebook groups `Selling_Price` by `Transmission` and creates a bar chart.

The project presentation reports approximately:

- Manual: **₹4.8 lakh**
- Automatic: **₹7.2 lakh**

### 5. Number of Cars by Year

The notebook creates a line chart using year-wise counts.

The recorded counts include:

| Year | Cars |
|---:|---:|
| 2003 | 2 |
| 2004 | 1 |
| 2005 | 4 |
| 2006 | 4 |
| 2007 | 2 |
| 2008 | 7 |
| 2009 | 6 |
| 2010 | 15 |
| 2011 | 19 |
| 2012 | 23 |
| 2013 | 33 |
| 2014 | 38 |
| 2015 | 61 |
| 2016 | 50 |
| 2017 | 35 |
| 2018 | 1 |

The largest number of cars is recorded for **2015 with 61 cars**.

### 6. Number of Cars per Year

A Seaborn count plot provides another visual representation of year-wise car counts.

The project presentation describes a noticeable increase from 2010 onward, reaching the highest count in 2015, followed by a decline.

### 7. Distribution of Car Selling Prices

A histogram with 20 bins is used to examine the distribution of `Selling_Price`.

The project presentation describes the distribution as concentrated in the lower price range, with fewer cars at higher prices and isolated observations above ₹15 lakh.

### 8. Year vs Selling Price

A scatter plot compares manufacturing year with selling price.

The project presentation describes the pattern as showing that newer cars generally tend to have higher selling prices, while also noting considerable variation within individual years.

The highest observed selling price in the notebook is **₹35 lakh**.

## Key Findings

- The dataset contains 301 used-car records and 9 variables.
- Petrol cars dominate the dataset with 239 records.
- Dealer listings account for 195 records, compared with 106 individual listings.
- Automatic cars have a higher average selling price than manual cars in the project presentation's transmission comparison.
- The number of records rises substantially from 2010 to 2015.
- 2015 has the highest number of cars in the dataset, with 61 records.
- Most selling prices are concentrated in the lower range.
- The dataset contains a small number of high-price observations, including a maximum selling price of ₹35 lakh.
- The Year vs Selling Price scatter plot indicates an overall relationship in which newer cars generally have higher selling prices, although the relationship is not uniform for every observation.

## Project Workflow

```text
Load CSV Dataset
       ↓
Inspect Records
       ↓
Descriptive Statistics
       ↓
Shape / Columns / Data Types
       ↓
Data Quality & Duplicate Check
       ↓
Category Frequency Analysis
       ↓
Selling Price Summary
       ↓
Visual Analysis
       ↓
Interpret Findings
```

## How to Run

### 1. Install Python

Use a supported Python 3 environment.

### 2. Create a virtual environment (optional)

Windows:

```bash
python -m venv venv
venv\Scripts\activate
```

macOS/Linux:

```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Place the dataset in the project folder

The notebook expects:

```text
1776311302-P3-Car Market Trends Analysis with Car Dekho Data.csv
```

### 5. Update the dataset path for local execution

The original notebook uses a Google Colab path:

```python
data = pd.read_csv(
    '/content/1776311302-P3-Car Market Trends Analysis with Car Dekho Data.csv'
)
```

For local Jupyter execution, change it to:

```python
data = pd.read_csv(
    '1776311302-P3-Car Market Trends Analysis with Car Dekho Data.csv'
)
```

### 6. Start Jupyter

```bash
jupyter notebook
```

Open:

```text
cardekho(1).ipynb
```

Run the cells from top to bottom.

## Expected Visualizations

The notebook produces:

1. Cars by Fuel Type — pie chart
2. Distribution of Seller Types — pie chart
3. Count of Cars by Fuel Type — bar chart
4. Average Selling Price by Transmission Type — bar chart
5. Number of Cars by Year — line chart
6. Number of Cars per Year — count plot
7. Distribution of Car Selling Prices — histogram
8. Year vs Selling Price — scatter plot

## Repository

The project presentation provides the repository:

https://github.com/Mruunali/car-dekho

## End Users

The project presentation identifies these potential users:

- **Car Buyers** — understand pricing trends and support purchasing decisions.
- **Car Sellers** — estimate competitive selling prices for used cars.
- **Car Dealers** — analyze market trends and vehicle demand.
- **Automotive Businesses** — understand factors affecting used-car prices.
- **Data Analysts and Researchers** — perform market analysis and identify useful patterns.

## Future Scope

Possible extensions of the project include:

- Predictive used-car price modeling
- Additional feature engineering
- More detailed brand/model analysis
- Regional or city-level analysis if location data is added
- Interactive dashboards
- Machine-learning-based price prediction

## Academic Use

This project is prepared for academic/internship submission and documents the exploratory analysis contained in the submitted Jupyter Notebook and AICTE presentation.
