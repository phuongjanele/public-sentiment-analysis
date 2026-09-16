# **Study Replication and Extension: Anti-Immigrant Rhetoric and ICE Reporting Interest**

---

**Overview**
This project replicates and extends the statistical methodology of the empirical study [*Anti-Immigration Rhetoric and ICE Reporting Interest: Evidence from a Large-Scale Study of Web Search Data*](https://www.cambridge.org/core/journals/british-journal-of-political-science/article/abs/antiimmigrant-rhetoric-and-ice-reporting-interest-evidence-from-a-largescale-study-of-web-search-data/AF982680AEC49AE65CACFD73352A44AD). The primary data pipeline processes high-frequency alternative data—specifically Google Trends and Bing search volume indices—integrated with unstructured text mining of media broadcast transcripts. The analytical framework models the transmission mechanism between external media signals and public information-seeking velocity across distinct temporal windows. In this replication, we systematically reproduced the OLS regression models (Table 3-4) and time-series data visualizations (Figure 2-3) using the core datasets and topic models specified below.

**Extension Research:** 
Our extension research expanded the econometric framework to isolate the direct impact of administrative policy shocks on search trend volatility. We engineered an automated signal-to-noise filtering algorithm, applying custom variance thresholds to isolate statistically significant wave patterns within the time-series data, followed by multivariate regression analysis to validate the out-of-sample statistical significance of selected trend variations.

**Replication Study and Extension Research Results:**

1.  **Environment Setup:**
Ensure your local environment has the required statistical computing dependencies installed: (`tidyverse` for data manipulation, `ggplot2` for data visualization, `dplyr`/`tidyr` for data wrangling, `lubridate` for time-series parsing, and `gt`/`broom` for tidy model coefficient extraction).

2.  **Pipeline Execution:** Run the main markdown notebook **`trends.Rmd`** to execute the data processing, statistical modeling, and visualization pipeline. Alternatively, you can bypass local execution and view the fully compiled, interactive analytical report directly via [this deployment link](https://htmlpreview.github.io/?https://github.com/msr-ds3/immigrant-news-2024-group-4/blob/main/trends.html).

**Data Sources & Feature Inputs:**
- **`crime.csv`**: High-frequency time-series search query volume indices tracking behavioral interest category A.
- **`report.csv`**: High-frequency time-series search query volume indices tracking behavioral interest category B.
- **`welfare.csv`**: High-frequency time-series search query volume indices tracking behavioral interest category C.
- **`TopicModel.RData`**: Pre-trained Structural Topic Model (STM) binary object mapping latent thematic distributions from media text corpora.
- **`gt_report_daily.csv`**: Daily aggregated time-series data frame utilized for the expanded multivariate regression models (Table 4 extension).
- **`zero_tolerance_policy.csv`**: Daily search velocity metrics capturing public information-seeking reactions to specific administrative shock timeline A.
- **`ICEdeportation.csv`**: Continuous search volume dataset mapping long-term macro trend variations under policy variable B.
