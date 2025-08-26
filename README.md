# P9-Ecommerce-Descriptive-Analysis

**A. Project Overview**

**B. Dataset Information**

- Source

- Period

**C. Methodoly**

_**I. EDA:**_
- Combine 21 files raw data thành 1 file master raw data
- Xử lý sơ ở file master raw data
  + Xóa các cột không có giá trị, số lượng giá trị < 5% tổng số lượng giá trị
  + Xóa các cột không quan trọng (link, url): goods-title-link--jump href, blackfridaybelts-content
- Check %blank, %error, %zero value, outlier, dtypes ở Python
- Xử lý sau khi có kết quả check
  + Xóa các cột %blank quá nhiều (>90%): goods-title-link--jump
  + Các cột có %blank ở vùng xám (70 - 90%): check ý nghĩa business.
  + Fill "Unknow" các blank ở color count do cột này quan trọng

**D. Key Findings and Actionable Plans**

_**I. Key Findings**_

_**Actionable Plans**_

**E. Appendix**

**F. About Me**

Hi, I'm Navin (Bao Vy) – an aspiring Data Analyst passionate about turning raw data into actionable business insights. I’m eager to contribute to data-driven decision making and help organizations translate analytics into business impact. For more details, please reach out at:

🌐 LinkedIn: https://www.linkedin.com/in/navin826/

📂 Portfolio: https://github.com/CallmeNavin/
