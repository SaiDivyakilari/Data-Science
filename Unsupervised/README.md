# Trade & Ahead – Stock Portfolio Segmentation Using Unsupervised Learning

## Project Overview
Trade & Ahead is an **unsupervised learning** project focused on segmenting NYSE-listed companies based on financial and performance indicators.  
Using clustering algorithms such as **K-Means** and **Hierarchical Clustering**, the project identifies groups of stocks with similar risk and return characteristics — helping investors design diversified, data-driven portfolios.

## Objective
To analyze stock market data and group companies into distinct clusters based on metrics such as **price change, volatility, ROE, P/E ratio, and cash ratio**, enabling smarter investment and diversification decisions.

## Dataset Description
The dataset includes **340 companies** from the **New York Stock Exchange (NYSE)** with the following key attributes:

- **Ticker Symbol / Company**
- **GICS Sector / Sub-Industry**
- **Price Change (% in 13 weeks)**
- **Volatility**
- **Return on Equity (ROE)**
- **Cash Ratio**
- **Net Income / Net Cash Flow**
- **Earnings Per Share (EPS)**
- **P/E Ratio** and **P/B Ratio**
- **Estimated Shares Outstanding**

##  Methodology
1. **Exploratory Data Analysis (EDA)**
   - Visualized price distributions and sectoral performance.
   - Analyzed correlations between financial indicators.
   - Examined volatility and profitability patterns across industries.

2. **Data Preprocessing**
   - Checked for missing values and duplicates (none found).
   - Scaled numerical features using **StandardScaler**.
   - Detected outliers using boxplots but retained them due to financial variability.

3. **K-Means Clustering**
   - Used **Elbow Method** and **Silhouette Analysis** to determine optimal clusters.
   - Optimal number of clusters: **k = 4** (Silhouette Score ≈ 0.45).
   - Interpreted segment profiles using mean and variance of financial indicators.

4. **Hierarchical Clustering**
   - Tested multiple linkage methods (single, complete, average, ward).
   - Best configuration: **Average Linkage** with **Euclidean Distance** (Cophenetic Correlation = 0.89).
   - Validated cluster consistency using dendrograms.

5. **Cluster Profiling**
   - Mapped each stock to a cluster to identify:
     - High-growth volatile stocks
     - Stable dividend-paying companies
     - Low-volatility defensive stocks
     - Underperforming or high-risk equities

##  Results and Evaluation
| Clustering Method        | Optimal Clusters | Silhouette Score | Key Metric / Indicator        |
|---------------------------|------------------|------------------|-------------------------------|
| K-Means                  | 4                | 0.45             | Clear segmentation, efficient |
| Hierarchical Clustering  | 4                | — (Cophenetic = 0.89) | Strong hierarchical structure |

- **K-Means**: Faster and ideal for large-scale deployment.  
- **Hierarchical**: More interpretable and useful for strategy analysis.  
- Both methods showed high consistency in stock grouping patterns.

##  Key Insights
- **Health Care** and **Information Technology** sectors showed the **highest 13-week price growth**.  
- **Energy** sector underperformed with negative price change on average.  
- Companies with **high ROE and P/E ratios** formed a distinct cluster representing **high-growth stocks**.  
- Stable **cash ratio** and low volatility indicated **defensive stocks** suitable for long-term portfolios.

##  Business Impact
- Helped investors identify diversified investment clusters for risk-balanced portfolios.  
- Enabled **data-driven sector allocation** and **volatility risk control**.  
- Provided interpretable segmentation to support financial consultancy recommendations.

## Tech Stack
- **Languages:** Python  
- **Libraries:** pandas, NumPy, scikit-learn, Matplotlib, Seaborn, Yellowbrick, SciPy  
- **Techniques:** StandardScaler, K-Means, Hierarchical Clustering, Silhouette Analysis, PCA, Correlation Heatmaps  

## Future Enhancements
- Integrate **PCA visualization** for cluster explainability.  
- Deploy an **interactive dashboard** for portfolio segmentation insights.  
- Test **DBSCAN** or **Gaussian Mixture Models** for advanced clustering.  

---
**Author:** Sai Divya Kilaru  
**Project Type:** Unsupervised Learning | Clustering | Financial Data Analytics
