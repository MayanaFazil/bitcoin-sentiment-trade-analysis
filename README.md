# Sentiment-Based Trading Performance Analysis

This project was developed as part of the **Data Science Internship assignment** for **Primetrade.ai**. The goal is to investigate the impact of **Bitcoin market sentiment (Fear/Greed)** on **trader behavior and performance** using historical trading data from **Hyperliquid**.

---

## Why This Project

In crypto trading, emotional market phases such as *Fear* and *Greed* often influence trader decisions. This project aims to explore whether such sentiment can be used as a predictive signal for:
- Profitability (Closed PnL),
- Trader performance (Win rate),
- Trading activity (Volume, Trade Side).

This aligns with Primetrade.ai’s focus on understanding trading psychology, behavior, and decision-making by leveraging real-time market indicators and historical trader data. The insights derived can contribute to building smarter AI-driven trading assistants or advisory tools.

---

## Problem Statement

To identify whether trader behavior and profitability are influenced by market sentiment, particularly in terms of:
- Closed PnL
- Win rate (profitable trades)
- Trade volume
- Buy vs Sell preferences

---

## Objectives

- Merge market sentiment data with trading data by date.
- Analyze and compare PnL, win rate, and trading volume under different sentiment phases.
- Study trade side distribution (Buy/Sell) per sentiment.
- Visualize these insights through intuitive plots.

---

## Datasets Used

1. **Bitcoin Market Sentiment Data**
   - Columns: `Date`, `Classification` (Fear/Greed)

2. **Hyperliquid Historical Trading Data**
   - Columns: `Account`, `Coin`, `Execution Price`, `Size Tokens`, `Size USD`, `Side`, `Timestamp IST`, `Start Position`, `Closed PnL`, etc.

---

## Methods and Steps

1. **Data Preprocessing**:
   - Parsed timestamps and derived date.
   - Checked for nulls, cleaned data, and ensured consistency.

2. **Data Merging**:
   - Combined both datasets on the `Date` column.

3. **Feature Engineering**:
   - Calculated win rate using binary classification on `Closed PnL`.
   - Aggregated trade volume and side.

4. **Visualization & Analysis**:
   - Boxplot: PnL distribution by sentiment.
   - Bar chart: Win rate by sentiment.
   - Bar chart: Trade volume by sentiment.
   - Stacked bar: Buy vs Sell by sentiment.

---

## Visual Outputs

- 📊 **PnL Distribution by Sentiment**: Compares profitability across fear vs greed days.
- 📈 **Win Rate Chart**: Indicates how sentiment affects trader success rates.
- 📉 **Trade Volume Comparison**: Shows total trading activity in different sentiment phases.
- 📦 **Buy vs Sell Breakdown**: Reveals directional preference per sentiment.

These plots are available as `.png` images and embedded in the final analysis notebook.

---

## Conclusion

- **Higher win rate and better PnL** observed during *Greed* sentiment periods.
- **Trade volume** increases significantly in *Greed*, reflecting active participation.
- Traders show **buy-side preference** in greedy markets and **more cautious sell-side actions** in fearful markets.

These findings suggest that **market sentiment can act as a useful signal** in strategy formulation and risk profiling for trading platforms.

---

## Technologies Used

- Python (Pandas, NumPy)
- Visualization: Seaborn, Matplotlib
- Jupyter Notebook for EDA and Reporting

---

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/sentiment-trader-analysis.git
   cd sentiment-trader-analysis
   ```

2. Ensure the following files are present:
   - `historical_data.csv`
   - `fear_greed_index.csv`

3. Run the analysis notebook:
   ```bash
   jupyter notebook sentiment_analysis.ipynb
   ```

---

## Project Structure

```
📁 sentiment-trader-analysis/  
├── Task Report.pdf  
├── historical_data.csv  
├── fear_greed_index.csv  
├── sentiment_analysis.ipynb  
├── plots/  
│   ├── pnl_boxplot.png  
│   ├── winrate_bar.png  
│   ├── volume_bar.png  
│   └── trade_side_stack.png  
├── README.md
```

---

## Author

**Mayana Mohammed Fazil Khan**  
Python Developer | Data Science Enthusiast  
GitHub: [mayana-fazil-khan](https://github.com/MayanaFazil)

---

## Assignment Context

Submitted as part of the selection process for the **Data Science Internship** at **Primetrade.ai**, dated **27 July 2025**.

Due to large size of datasets, historical_data.csv cannot be uploaded but the link is provided below for 2 datasets. If you want you can access them.

Historical Data 

https://drive.google.com/file/d/1IAfLZwu6rJzyWKgBToqwSmmVYU6VbjVs/view?usp=sharing

Fear Greed Index link:

https://drive.google.com/file/d/1PgQC0tO8XN-wqkNyghWc_-mnrYv_nhSf/view?usp=sharing


