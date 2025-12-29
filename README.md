# Magnificent-Seven-Analysis-with-Python-and-Tableau

# Magnificent Seven Analysis with Python and Tableau

A comprehensive data analysis project examining the market dominance and financial performance of the "Magnificent Seven" tech stocks (Apple, Microsoft, Google, Amazon, Meta, Tesla, and Nvidia) compared to the broader S&P 500 universe.

[![Tableau Dashboard](https://img.shields.io/badge/Tableau-Dashboard-E97627?style=for-the-badge&logo=tableau)](https://public.tableau.com/app/profile/gourav.pal/viz/Mags/MagnificentSevenAnalysis)
[![Report](https://img.shields.io/badge/Report-Gamma-6C5CE7?style=for-the-badge)](https://gamma.app/docs/Magnificent-Seven-Analysis-ev80zimph1jbqrd)

## 📊 Project Overview

This project leverages Python for automated data collection and transformation, combined with Tableau for interactive visualization. The analysis explores the outsized influence of seven mega-cap technology companies on overall market performance, valuation, and growth metrics.

### Key Questions Addressed
- What percentage of S&P 500 market capitalization do the Magnificent Seven represent?
- How do price performance and returns compare between MAG7 and non-MAG7 stocks?
- What revenue growth and profitability trends distinguish these tech giants?
- How diversified are revenue streams across product segments?

## 🎯 Visualizations

The project generates data for six core visualizations:

1. **Market Cap Pie Chart** - MAG7 vs. Non-MAG7 market capitalization breakdown
2. **Close Prices** - Historical stock price trends across all tickers
3. **Returns Analysis** - All-time, monthly, and annual return calculations
4. **Revenue Estimates** - Forward-looking revenue projections from analyst consensus
5. **Income Statement Information** - Key profitability metrics and growth rates
6. **Revenue by Segment** - Product/service line breakdown for business composition analysis

## 🛠️ Technical Implementation

### Data Sources
- **Yahoo Finance API** - Primary data source via `yahooquery` library
- **S&P 500 Universe** - 500+ tickers including MAG7 constituents
- **Time Period** - Historical data through January 2025

### Technology Stack
- **Python 3.x** - Core programming language
- **Pandas & NumPy** - Data manipulation and numerical computing
- **yahooquery** - Yahoo Finance data extraction
- **Tableau Public** - Data visualization and dashboard creation

### Project Structure
```
├── Mags7_1.ipynb          # Data scraping for visualizations 1-3
├── Mags7_2.ipynb          # Data scraping for visualizations 4-6
├── README.md              # Project documentation
└── data/                  # Generated CSV files (gitignored)
```

## 🚀 Getting Started

### Prerequisites
```bash
pip install pandas numpy yahooquery tqdm
```

### Running the Analysis

1. **Clone the repository**
```bash
git clone https://github.com/ggpal7117/Magnificent-Seven-Analysis-with-Python-and-Tableau.git
cd Magnificent-Seven-Analysis-with-Python-and-Tableau
```

2. **Execute data collection notebooks**
```bash
jupyter notebook Mags7_1.ipynb  # Market cap, prices, returns
jupyter notebook Mags7_2.ipynb  # Revenue, income statements, segments
```

3. **Load generated CSVs into Tableau**
   - Import data files from the output directory
   - Connect to the provided Tableau workbook or create custom visualizations

### Rate Limiting Considerations

The scraping functions implement intelligent rate limiting to avoid Yahoo Finance API errors:
- 0.5-second delays between individual requests
- 2-second pauses every 50 tickers
- Exponential backoff retry logic for failed requests
- Estimated runtime: 4-5 minutes for full S&P 500 universe

## 📈 Key Findings

> **Explore the full interactive analysis:**
> - [Tableau Dashboard](https://public.tableau.com/app/profile/gourav.pal/viz/Mags/MagnificentSevenAnalysis)
> - [Executive Report](https://gamma.app/docs/Magnificent-Seven-Analysis-ev80zimph1jbqrd)

The Magnificent Seven companies demonstrate disproportionate influence on S&P 500 performance, representing a significant concentration of market value despite comprising less than 1.5% of constituent companies. The analysis reveals divergent growth trajectories, profitability margins, and revenue diversification strategies across these tech leaders.

## 🔄 Data Pipeline Architecture

```
Yahoo Finance API
        ↓
Python Data Scraping (yahooquery)
        ↓
Data Transformation (Pandas)
        ↓
CSV Export
        ↓
Tableau Visualization
        ↓
Interactive Dashboard
```

### Error Handling
- Session-based authentication management
- Crumb token refresh logic
- Graceful failure handling with detailed logging
- Failed ticker tracking and retry mechanisms

## 📝 Notebooks Description

### Mags7_1.ipynb
Extracts fundamental market data:
- Market capitalization snapshots
- Daily closing prices (historical and current)
- Total return calculations (cumulative, monthly, annual)
- Statistical return distributions

### Mags7_2.ipynb
Gathers forward-looking and financial statement data:
- Analyst revenue estimates (current + next quarter)
- Income statement line items (revenue, operating income, net income)
- Segment-level revenue breakdown
- Year-over-year growth rates

## 🤝 Contributing

Contributions are welcome! Areas for enhancement:
- Additional financial metrics (P/E ratios, FCF, margins)
- Expanded time-series analysis (volatility, correlations)
- Sector comparison beyond MAG7
- Real-time data refresh automation

## 📄 License

This project is available for educational and non-commercial use. Please cite appropriately if using in research or publications.

## 👤 Author

**Gourav Pal**
- GitHub: [@ggpal7117](https://github.com/ggpal7117)
- Tableau Public: [Profile](https://public.tableau.com/app/profile/gourav.pal)

## 🙏 Acknowledgments

- Yahoo Finance for providing accessible financial data APIs
- The Python data science community for excellent open-source tools
- Tableau Public for free visualization hosting

---

⭐ **Star this repository** if you find it useful for your own financial analysis projects!
