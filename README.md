# P9-Ecommerce-Descriptive-Analysis

**A. Project Overview**

- This project analyzes merchandising & marketing strategy. We want to explore more about how Shein định vị sản phẩm, sắp xếp, và push cái gì ra trước mắt khách.
- 

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

**1. Pricing & Discount**
- Top 3 categories by discount: Curve (-14.8%), Womens Clothing (-12.6%), Swimwear (-8.3%) → these categories are the most discount-dependent to drive sales.
- Home Textile, Appliances, Tools & Home Improvement show high average prices only because of extreme outliers. Without outliers, they do not appear in the top 5. After removing outliers, Shoes (12.5), Curve (12.3), Mens Clothing (11.8) are the categories with the highest average prices. Curve (plus-size niche) is positioned higher, but still heavily discounted → Shein seems to accept deep discounting to acquire market share.
- Overall average price: 7 USD (without outliers) vs 23 USD (with outliers) → outliers triple the mean.
→ Insight: Shein’s true positioning is low-price fast fashion, while a few very high-price products are likely serving niche markets.

**2. Merchadising Mix**

- SKU breadth: Top 3 = Shoes, Sports & Outdoors, Underwear & Sleepwear.
- Color variety: Top 3 = Shoes, Womens Clothing, Bags & Luggage.
- Best Sellers: Top 3 = Home & Kitchen, Sports & Outdoors, Beauty & Health.
→ Shoes is clearly being pushed as a flagship category (wide SKU + color options).
→ Beauty & Health ranks only 6th in SKU count but delivers the 3rd most Best Sellers → highly efficient.
→ Shoes, despite heavy investment in SKU & color, failed to rank among Best Sellers → likely due to higher price perception and/or weaker quality perception.
→ Home & Kitchen, with simple products (often single-color), achieved outstanding success.

**3. Marketing Tactics**

- Categories with the highest % of “Sold Recently” tag per SKU: Bags & Luggage, Curve, Kids.
→ Shein is actively pushing Curve (plus-size market entry) and Bags & Luggage via social proof tactic. However, effectiveness is mixed: Curve shows low Best Seller outcome despite high discount & push; Bags & Luggage suffers from low SKU count (bottom quartile) → limiting sales output.

_**Actionable Plans**_

- Shoes: Reevaluate strategy. Adjust pricing, strengthen product quality, and improve marketing messaging to avoid “SKU graveyards”.
- Sports & Outdoors: Well-balanced (high SKU + high Best Sellers) → continue investment.
- Home & Kitchen, Beauty & Health: Expand SKU variety → currently highly efficient (many Best Sellers with fewer SKUs/colors).
- Curve: Beyond discount & “sold recently” tactic, Shein should improve quality & user reviews to win trust in this niche.
- Bags & Luggage: Increase SKU breadth. Current low SKU count restricts Best Seller output despite marketing push.

**E. Appendix**

**F. About Me**

Hi, I'm Navin (Bao Vy) – an aspiring Data Analyst passionate about turning raw data into actionable business insights. I’m eager to contribute to data-driven decision making and help organizations translate analytics into business impact. For more details, please reach out at:

🌐 LinkedIn: https://www.linkedin.com/in/navin826/

📂 Portfolio: https://github.com/CallmeNavin/
