# Monthly Stock Performance Analysis of NVIDIA (NVDA) Using WRDS CRSP Data

## 1. Problem & User
This project investigates NVIDIA’s monthly stock performance since 2022 using WRDS CRSP data.  
It is intended for retail investors and beginner financial analysts who want a clear and simple view of NVIDIA’s recent price trends, returns, and volatility.

## 2. Data
**Source:** WRDS – CRSP Monthly Stock File (`crsp.msf`) and CRSP Monthly Stock Header File (`crsp.msfhdr`)  
**Access date:** 26 April 2026  
**Company analysed:** NVIDIA Corporation (`NVDA`)

**Key fields used:**
- `date` – monthly observation date
- `prc` – stock price
- `ret` – monthly stock return
- `permno` – CRSP security identifier
- `htsymbol` – stock ticker symbol

**Note:** `ABS(prc)` was used in the analysis because CRSP price values may sometimes appear as negative due to database conventions.

## 3. Methods
The analysis was completed in Python with SQL-based extraction from WRDS. The main steps were:

1. Query monthly stock data for NVIDIA from WRDS
2. Join CRSP monthly stock data with header data to identify the ticker
3. Clean and prepare the dataset in Python
4. Convert variables into appropriate formats and handle missing values
5. Calculate and summarise monthly return behaviour
6. Create visualisations of stock price trends and return patterns
7. Interpret the results for a business-related audience

**Tools used:**
- Python
- pandas
- matplotlib
- seaborn
- WRDS / SQL

## 4. Key Findings
- NVIDIA’s stock price showed an overall upward trend during the sample period.
- Monthly returns were volatile, with both strong positive months and negative months.
- The stock delivered strong growth performance, but this was accompanied by substantial risk.
- The results suggest that NVIDIA may be attractive to growth-oriented investors.
- Return volatility means that caution is needed for more risk-averse investors.

## 5. How to run
To reproduce this project:

1. Ensure that you have institutional access to WRDS
2. Install the required Python packages:
   pip install pandas matplotlib seaborn wrds
3. Open the notebook:
   monthly_stock_performance_nvda_wrds.ipynb
 Run all cells in order.

**Important:** Reproducing the data extraction step requires valid WRDS access.

## 6. Product link / Demo
GitHub repository: [insert GitHub repository link here]
Demo video: [insert demo video link here]

## 7. Limitations & next steps
Limitations
This project focuses on only one company, so it does not provide cross-company comparison.
The analysis is mainly descriptive and does not include advanced forecasting models.
Reproducing the extraction step depends on access to WRDS.
Next steps
Compare NVIDIA with other major technology companies such as Apple, Microsoft, or AMD.
Add rolling volatility or cumulative return analysis.
Extend the project to daily stock data.
Include simple predictive modelling or event-based analysis.
