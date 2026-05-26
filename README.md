# Athens Residential Real Estate Market Analysis

An end-to-end data analytics portfolio project focusing on scraping, cleaning, exploring, and modeling residential housing market trends in the Athens Center area. This repository showcases advanced pipeline engineering, data cleaning workflows, rigorous outlier detection, and analytical reporting designed to derive actionable market insights.

---

## Project Architecture & Workflow

The lifecycle of this project follows a disciplined data engineering and analytics pipeline:

1. **Extraction:** Automated extraction of ~10,000 tabular web listings using cloud-based infrastructure.
2. **Data Engineering & Cleaning:** Comprehensive parsing, language harmonization (Greek text handling), missing value handling, and column standardization.
3. **Statistical Outlier Detection:** Removal of anomalies using Interquartile Range (IQR) and domain-specific thresholds to protect data integrity.
4. **Exploratory Data Analysis (EDA):** Feature relationship investigations, spatial distribution analysis, and structural pricing trends.
5. **Reporting & Visualization:** Professional analytical reporting and interactive dashboard design elements.

---

## Data Ethics, Privacy & Legal Compliance

This project was built from the ground up with a strict commitment to **data protection regulations (GDPR)**, infrastructure respect, and professional data ethics.

* **GDPR Compliance & Data Minimization:** In adherence to the General Data Protection Regulation (GDPR), the dataset is entirely clear of Personal Identifiable Information (PII). No individual names, telephone numbers, contact details, or exact street addresses were collected or retained.
* **No Platform Correlation:** To ensure full anonymity, platform-specific unique Listing IDs were intentionally omitted or stripped during ingestion. The final dataset consists strictly of aggregate physical characteristics (e.g., area, floor, construction year, heating type) that cannot be reverse-engineered or linked back to the source platform's live database.
* **Infrastructure Respect & Rate-Limiting:** Automated extraction was handled responsibly using cloud infrastructure on the **Apify platform**. Requests were throttled, rate-limited, and executed during off-peak hours to guarantee zero infrastructure strain or performance impact on the target host's servers.
* **Educational Scope:** This repository and its underlying artifacts are created strictly as a non-commercial, static, offline **educational portfolio project**. The dataset serves as a historical snapshot to demonstrate data processing proficiency and is not offered as a commercial service, product, or live API.

---

## Data Cleaning & Preprocessing

Real-world web data is naturally messy. The preprocessing/processing engine implemented in Pandas addresses:

* **Regional Aggregation & Granular Neighborhood Mapping:** The raw scraped dataset contained 120 unique sub-localities (highly fragmented micro-locations, specific squares, street suffixes, and overlapping neighborhood definitions). By using text-tokenization search passes, the system cleaned specific suffixes and programmatically aggregated the 120 micro-zones into 16 structurally distinct urban districts.
* **Text Harmonization:** Standardizing Greek text encodings, stripping whitespace, and normalizing categorization across categorical features (e.g., parsing varying regional definitions for neighborhoods in the Athens Center).
* **Type Conversion & Parsing:** Transforming localized currency and metric strings into clean numerical integers and floats (`int64`, `float64`) ready for statistical analysis.
* **Structural Imputation:** Engineering robust logical paths for missing properties (e.g., evaluating missing building floors or handling complex overlapping heating systems).
* **Statistical Outlier Filtration:** Eliminating data entry anomalies—such as severe typographical errors in square footage or unrealistic price-to-size ratios—using programmatic IQR thresholds coupled with local real estate domain baselines.

---

## Key Analytical Focus Areas

* **Spatial Price Elasticity:** Analyzing price-per-square-meter variations across distinct administrative zones and neighborhoods within Athens.
* **Temporal & Structural Drivers:** Investigating how a property's age (construction year) and structural traits (energy-efficiency metrics, floor level, heating infrastructure) impact market valuations.
* **Market Segmentation:** Classification of listings into premium, baseline, and high-yield potential clusters based on multivariate characteristics.

---

## Technical Stack

* **Data Engineering & Extraction:** Apify Platform
* **Data Processing & Analytics:** Python 3.11+, Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn
* **Environment Management:** Jupyter Notebooks, Excel, Power BI

---

## 📜 Disclaimer & Terms

This repository is provided solely for educational, personal portfolio evaluation, and professional capability demonstration. All analysis is performed on historical snapshot data. The metrics, scripts, and visualizations are intended to demonstrate competency in data analysis methodology and toolsets, and should not be used as official financial, investment, or legal real estate advice.
