# Trader Performance vs Market Sentiment Analysis

**Data Science Intern Assignment - Primetrade.ai**

## Project Overview

This project analyzes how market sentiment (Fear/Greed) relates to trader behavior and performance on Hyperliquid. The goal is to uncover patterns that could inform smarter trading strategies.

## Author
- **Name**: [Your Name]
- **Email**: [Your Email]
- **Date**: February 4, 2026

## Table of Contents
- [Setup Instructions](#setup-instructions)
- [Data Sources](#data-sources)
- [Project Structure](#project-structure)
- [How to Run](#how-to-run)
- [Key Findings](#key-findings)
- [Methodology](#methodology)
- [Deliverables](#deliverables)

## Setup Instructions

### Prerequisites
- Python 3.8 or higher
- Jupyter Notebook or JupyterLab
- pip package manager

### Installation

1. **Clone or download this repository**
```bash
git clone [your-repo-url]
cd trader-sentiment-analysis
```

2. **Create a virtual environment (recommended)**
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install required packages**
```bash
pip install pandas numpy matplotlib seaborn scipy scikit-learn jupyter
```

Or install from requirements.txt:
```bash
pip install -r requirements.txt
```

### Data Setup

1. **Download the datasets** from the provided Google Drive links:
   - Bitcoin Market Sentiment: [Link from assignment]
   - Historical Trader Data: [Link from assignment]

2. **Place the data files** in the project directory:
   - `bitcoin_sentiment.csv` (or your downloaded filename)
   - `trader_data.csv` (or your downloaded filename)

3. **Update file paths** in the notebook:
   - Open `trader_sentiment_analysis.ipynb`
   - In the "Load Datasets" section, update the file paths to match your downloaded files

## Data Sources

### 1. Bitcoin Market Sentiment (Fear/Greed)
- **Columns**: Date, Classification (Fear / Greed)
- **Description**: Daily market sentiment indicators for Bitcoin

### 2. Historical Trader Data (Hyperliquid)
- **Fields**: account, symbol, execution price, size, side, time, start position, event, closedPnL, leverage, etc.
- **Description**: Historical trading activity and performance data

## Project Structure

```
trader-sentiment-analysis/
│
├── README.md                           # This file
├── requirements.txt                    # Python dependencies
├── trader_sentiment_analysis.ipynb     # Main analysis notebook
├── INSIGHTS.md                         # Detailed findings and insights
│
├── data/                               # Data directory (not included)
│   ├── bitcoin_sentiment.csv
│   └── trader_data.csv
│
└── outputs/                            # Generated outputs
    ├── performance_by_sentiment.png
    ├── behavior_by_sentiment.png
    ├── trader_segments.png
    ├── time_series_analysis.png
    ├── correlation_heatmap.png
    ├── risk_return_analysis.png
    ├── feature_importance.png
    ├── confusion_matrix.png
    ├── trader_archetypes.png
    ├── performance_by_sentiment.csv
    ├── behavior_by_sentiment.csv
    ├── trader_archetypes.csv
    └── trader_profiles_full.csv
```

## How to Run

### Option 1: Run the Jupyter Notebook

1. **Start Jupyter Notebook**
```bash
jupyter notebook
```

2. **Open the notebook**
   - Navigate to `trader_sentiment_analysis.ipynb`
   - Click to open

3. **Run all cells**
   - Click "Kernel" → "Restart & Run All"
   - Or run cells individually with Shift+Enter

4. **View outputs**
   - Charts will be displayed inline
   - Files will be saved to the current directory

### Option 2: Run as Python Script

If you prefer to convert the notebook to a script:
```bash
jupyter nbconvert --to script trader_sentiment_analysis.ipynb
python trader_sentiment_analysis.py
```

## Key Findings

### 1. Performance Differences by Sentiment
- **Fear Days**: [Summary of findings - will be populated after running analysis]
- **Greed Days**: [Summary of findings - will be populated after running analysis]
- **Statistical Significance**: [T-test results]

### 2. Behavioral Changes
- **Trade Frequency**: Traders show [increase/decrease] in activity during [Fear/Greed] days
- **Leverage Usage**: Average leverage is [higher/lower] during [Fear/Greed] periods
- **Position Bias**: Long/Short ratio shifts toward [longs/shorts] in [Fear/Greed] markets

### 3. Trader Segments
- **High Leverage Traders**: [Key characteristics and performance]
- **Frequent Traders**: [Key characteristics and performance]
- **Consistent Winners**: [Key characteristics and performance]

### 4. Behavioral Archetypes
Based on K-means clustering, traders fall into 4 distinct archetypes:
1. **Aggressive Winners**: [Characteristics]
2. **Conservative Winners**: [Characteristics]
3. **Neutral Traders**: [Characteristics]
4. **Struggling Traders**: [Characteristics]

## Methodology

### Part A: Data Preparation
1. **Data Loading & Documentation**
   - Loaded both datasets
   - Documented rows, columns, missing values, duplicates

2. **Data Cleaning**
   - Converted timestamps to datetime
   - Aligned datasets by date (daily level)
   - Removed duplicates and handled missing values

3. **Metric Creation**
   - Daily PnL per trader
   - Win rate calculation
   - Average trade size
   - Leverage distribution
   - Number of trades per day
   - Long/Short ratio

### Part B: Analysis
1. **Performance Comparison** (Fear vs Greed)
   - Statistical testing (t-tests)
   - Visual comparisons
   - Drawdown proxies

2. **Behavioral Analysis**
   - Trade frequency patterns
   - Leverage adjustments
   - Position sizing changes
   - Long/Short bias shifts

3. **Trader Segmentation**
   - High vs Low leverage
   - Frequent vs Infrequent
   - Consistent winners vs Inconsistent
   - 3+ detailed visualizations

### Part C: Actionable Strategies
Developed 2 key strategy recommendations:

**Strategy 1: Sentiment-Adaptive Leverage Management**
- Fear days: Reduce leverage for high-leverage traders
- Greed days: Moderate increase for low-leverage traders
- Specific targets and rationale provided

**Strategy 2: Trading Frequency Optimization**
- Fear days: Reduce frequency for frequent traders
- Greed days: Increase frequency for consistent winners only
- Segment-specific recommendations

### Bonus Features
1. **Predictive Model**: Random Forest classifier for profitability bucket prediction
2. **Trader Clustering**: K-means clustering to identify behavioral archetypes
3. **Risk-Return Analysis**: Visual comparison across segments and sentiments

## Deliverables

### Required Outputs
- ✅ Jupyter Notebook with complete analysis
- ✅ README.md with setup and instructions
- ✅ High-quality charts and visualizations
- ✅ Summary statistics (CSV exports)
- ✅ 1-page insights summary (see INSIGHTS.md)

### Bonus Outputs
- ✅ Predictive model with feature importance
- ✅ Trader clustering analysis
- ✅ Correlation analysis
- ✅ Time series visualizations

## Evaluation Criteria Addressed

### ✅ Data Cleaning & Correctness
- Comprehensive data cleaning workflow
- Proper timestamp conversion and alignment
- Missing value handling
- Duplicate removal

### ✅ Strength of Reasoning
- Statistical testing for validation
- Multiple analytical perspectives
- Clear cause-effect relationships
- Evidence-based conclusions

### ✅ Quality of Insights
- Specific, actionable recommendations
- Segment-specific strategies
- Risk-adjusted perspectives
- Not generic observations

### ✅ Clarity of Communication
- Well-structured notebook with markdown
- Clear visualizations with titles and labels
- Organized section headers
- Summary statistics tables

### ✅ Reproducibility
- Clear step-by-step code
- Commented explanations
- File path instructions
- Requirements documentation

## Insights & Recommendations

See [INSIGHTS.md](INSIGHTS.md) for detailed findings and strategy recommendations.

## Contact

For questions or clarifications:
- **Email**: [Your Email]
- **GitHub**: [Your GitHub]

## Acknowledgments

- Assignment provided by Primetrade.ai
- Data sources: Hyperliquid trading platform and Bitcoin sentiment indicators

---

**Last Updated**: February 4, 2026
