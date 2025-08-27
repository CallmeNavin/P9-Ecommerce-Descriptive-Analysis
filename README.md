# P9-Ecommerce-Descriptive-Analysis

**A. Project Overview**

**B. Dataset Information**

- Source: Dirty E-Commerce Data [80,000+ Products] from Kaggle
https://www.kaggle.com/datasets/oleksiimartusiuk/e-commerce-data-shein

- Notes: The original combined dataset has 14k+ rows and was too large for GitHub. For storage efficiency, it will be compressed.

- Period

**C. Methodoly**

_**I. EDA:**_
- Combine raw data: Merged 21 individual raw files into a single master dataset.
- Initial preprocessing on master dataset:
  + Dropped columns with less than 5% valid values.
  + Removed irrelevant columns such as goods-title-link--jump href and blackfridaybelts-content (link/URL fields).
- Data quality scanning in Python: Checked for %blank, %error, %zero values, outliers, and data types.
- Data cleaning based on scan results:
  + rank-title: Kept only the value “Best Sellers”.
  + price: Removed $ symbols and commas, converted to numeric type.
  + discount: Removed %, converted to numeric type.
  + selling_proposition: Kept only the value “sold recently”.
  + color-count: Filled missing values with “Unknown”.

_**Data Cleaning Rationale**_
- Column reduction: Columns with less than 5% valid data were dropped to avoid noise and reduce dimensionality. Irrelevant link/URL fields were also removed since they do not provide analytical value.
- Handling categorical noise: For fields such as rank-title and selling_proposition, only meaningful labels (“Best Sellers”, “sold recently”) were preserved. Other inconsistent or low-information values were discarded to improve clarity.
- Numeric standardization: Price values often contained $ and thousand separators (commas). These were stripped and converted into numeric format for accurate aggregation and statistical analysis.
- Discount normalization: Discount percentages were converted into numeric format, enabling quantitative comparison across records. Extreme values above 100% were treated as invalid and removed.
- Missing data handling: Columns with significant missingness were either dropped (if uninformative) or imputed with a placeholder (“Unknown”) in categorical cases such as color-count. This ensures dataset integrity while avoiding bias in numerical analysis.

**D. Key Findings and Actionable Plans**

_**I. Key Findings**_

_**Actionable Plans**_

**E. Appendix**

**F. About Me**

Hi, I'm Navin (Bao Vy) – an aspiring Data Analyst passionate about turning raw data into actionable business insights. I’m eager to contribute to data-driven decision making and help organizations translate analytics into business impact. For more details, please reach out at:

🌐 LinkedIn: https://www.linkedin.com/in/navin826/

📂 Portfolio: https://github.com/CallmeNavin/
