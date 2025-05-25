Here's a professional `README.md` file for your TradingView Market Movers data scraper:

---

# 📈 TradingView Market Movers Scraper

This Python script uses **Selenium WebDriver** to scrape real-time stock market data from [TradingView's Market Movers (USA Stocks)](https://www.tradingview.com/markets/stocks-usa/market-movers-all-stocks/). The script automates scrolling, loads dynamic content, and extracts key stock performance metrics into a structured Excel file.

---

## 🚀 Features

* Automatically scrolls and interacts with the "Load More" button.
* Extracts comprehensive market data from all listed U.S. stock movers.
* Skips incomplete rows and handles dynamic page behavior gracefully.
* Outputs clean data to an Excel file: `tradingview_data.xlsx`.

---

## 📊 Output

Each row in the Excel output contains:

* **Symbol**: Ticker symbol
* **Name**: Abbreviated company name or reference
* **Price**: Current market price
* **Change Price**: Price change (absolute or %)
* **Volume**: Trading volume
* **Relative Volume**: Relative volume compared to average
* **Market Cap**: Market capitalization
* **P/E**: Price to Earnings Ratio
* **EPS Growth YoY**: Earnings growth Year-over-Year
* **Div Yield**: Dividend Yield
* **Sector**: Industry sector

---

## 🛠 Requirements

* Python 3.x
* Google Chrome
* Compatible **ChromeDriver**

### 📦 Python Packages

Install dependencies using pip:

```bash
pip install selenium pandas openpyxl
```

---

## ⚙️ Configuration

### 🔧 Set ChromeDriver Path

Update the `chromedriver.exe` path in the script based on your system setup:

```python
path = r'C:\Users\ZA IT Park\Desktop\Hackaton\driver\chromedriver.exe'
```

Ensure ChromeDriver version matches your installed Chrome browser version.

---

## 🧠 How It Works

1. **Initialize Selenium WebDriver**

   * Loads TradingView's Market Movers page.
   * Sets script timeouts and initializes explicit waits.

2. **Dynamic Scrolling and Load More**

   * Scrolls down the page in increments.
   * Automatically clicks the "Load More" button if found.
   * Stops when the bottom of the page is reached or a scroll limit is hit.

3. **Data Extraction**

   * Extracts stock details from each table row (`row-RdUXZpkv`).
   * Gracefully skips rows with missing columns.

4. **Save to Excel**

   * Uses `pandas` to create a structured dataset.
   * Exports the data to `tradingview_data.xlsx`.

---

## 📤 Example Console Output

```bash
Scrolled 500 pixels
Scrolled 1000 pixels
Clicking Load More button...
AAPL Apple Inc. 189.25 +2.34% 78M 1.2x 2.9T 34.5 12.3% 0.56% Technology
✅ Data saved to tradingview_data.xlsx
```

---

## 📌 Notes

* This script is designed to handle dynamic web elements and minor DOM changes.
* For long-term use, periodic updates may be needed to reflect any front-end changes on TradingView.
* Use responsibly. Always check [TradingView’s Terms of Service](https://www.tradingview.com/terms/) before scraping.

---

## 🧾 License

This script is provided for **educational and research purposes only**.

---

## ✍️ Author

**Abdil Ahad**
Hackathon Project – 2025

---