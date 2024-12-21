 # Quantitative Momentum Strategy
This repository demonstrates a **Quantitative Momentum Strategy** for stock selection and portfolio creation using **S&P 500 companies** as a data universe. The project utilizes historical stock price data, calculates momentum metrics, and generates optimised portfolios based on momentum rankings.
## Features
- Retrieve and process **S&P 500 stock price data** using the Refinitiv API.
- Perform **momentum analysis** on price data for a 1-year period.
- Filter stocks based on **momentum thresholds**.
- Create a portfolio with user-defined parameters:
    - Number of stocks in the portfolio.
    - Number of shares per stock.
    - Option to weight stocks based on momentum scores.

- Export results to **Excel workbooks** for further analysis and reporting.

## Installation
1. Clone this repository:
``` bash
   git clone https://github.com/your-username/quantitative-momentum-strategy.git
   cd quantitative-momentum-strategy
```
1. Install the required dependencies:
``` bash
   pip install numpy pandas requests xlsxwriter scipy openpyxl
```
1. Set up and authenticate with the **Refinitiv API**:
    - Install the `refinitiv.data` library.
    - Ensure you have valid Refinitiv API credentials to initiate a data session successfully.

## How the Project Works
### 1. Retrieve S&P 500 Data
- Using the Refinitiv API, fetch a list of **S&P 500 constituents** and their **Reuter Instrument Codes (RIC)**.
- Download historical **daily closing prices** for a 1-year period.

### 2. Perform Momentum Analysis
- Calculate momentum as a percentage change in stock prices over a specified period (default: 12 days).
- Rank stocks based on momentum values, with higher ranks assigned to top momentum stocks.

### 3. Filter Top Momentum Stocks
- Filter stocks using a **momentum threshold** (e.g., top 25 by rank).
- Save the full momentum analysis and filtered results to separate Excel files.

### 4. Generate and Export Portfolio
- Create a portfolio based on the filtered stocks using the following inputs:
    - **Portfolio size**: Number of stocks in the portfolio.
    - **Shares per stock**.
    - Option to **weight stocks proportionally by momentum score**.

- Export the portfolio to an Excel file (user-specified name).

## Usage
### Step 1: Run the Notebook or Script
- Open the Jupyter Notebook or Python script in your environment.
- Execute the cells to calculate momentum and generate portfolio outputs.

### Step 2: Run Portfolio Setup
- When prompted, provide the following inputs to define your portfolio:
    - Number of stocks in the portfolio.
    - Number of shares per stock.
    - Whether to weight shares based on momentum.
    - File name to save the portfolio.

### Example
``` bash
How many stocks would you like in your portfolio? 10
How many shares would you like per stock? 50
Would you like to weigh the shares by momentum? (yes/no): yes
Enter a file name to save the portfolio (e.g., 'portfolio.xlsx'): my_portfolio.xlsx
```
The portfolio will be saved to the specified Excel file.
## File Outputs
The following files will be generated:
1. `momentum_data.xlsx`: Momentum analysis for all S&P 500 stocks.
2. `momentum_data_filtered.xlsx`: Filtered stocks based on momentum thresholds.
3. User-defined file, e.g., `portfolio.xlsx`: Final portfolio.

## Technologies Used
- **Programming Language**: Python
- **Libraries**:
    - **Data Manipulation**: `pandas`, `numpy`
    - **API Integration**: `refinitiv.data`, `requests`
    - **Data Analysis**: `scipy`
    - **Excel Export**: `xlsxwriter`, `openpyxl`

## Prerequisites
1. Python 3.9 or higher.
2. API credentials for the Refinitiv data service.

## Author
Developed by **[Ubayd Knight]**. If you have any questions or suggestions, feel free to contact me.
Let me know if you'd like to adjust the content further!
