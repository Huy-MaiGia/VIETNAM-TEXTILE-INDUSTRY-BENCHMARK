📋 Project Overview
This project provides a comprehensive overview of the Vietnam Textile Industry Benchmark for 2024. It transforms raw, unformatted financial data into a structured diagnostic tool, enabling stakeholders to understand industry composition and perform granular financial analysis through a custom-built Risk Indicator.
🛠️ Tech Stack
Data Engineering: Python (Pandas, NumPy) for complex ETL and statistical cleaning.

Analytics: DAX (Data Analysis Expressions) for dynamic KPI modeling and UX logic.

Visualization: Power BI for interactive, container-based dashboarding.

🎯 The Analytical Challenges 
1. Data Integrity & Structural AuditingThe raw dataset, covering financial reports from approximately 1,590 companies, was highly unformatted.

Challenge: Accounting inconsistencies where the fundamental equation Total Assets = Total Liabilities + Total Equity was not met.

Solution: Implemented a strict validation filter to remove non-compliant records, ensuring the final analysis is based on a reliable "Source of Truth".

2. Statistical Outlier Mitigation (IQR Method)
The Vietnamese textile landscape is highly right-skewed, dominated by a few massive entities that distort industry averages.

Challenge: Extreme anomalies (e.g., companies reporting a 9,000% ROE) made visualizations unreadable and skewed the "true" industry picture.

Solution: Applied the Interquartile Range (IQR) Method to isolate the middle 50% of the dataset. This prevented the dashboard from being "stretched" by extreme values while maintaining a realistic representation of the SME and Large segments.

3. Business Logic Validation
Challenge: Unrealistic ratios, such as a DSI (Days Sales in Inventory) exceeding 365 days—a logical impossibility for an annual report.

Solution: Established "Logical Upper Limits" for financial ratios to cap or remove records that exceeded realistic business scenarios, ensuring the benchmark remains actionable for investors.

🏗️ Key Insights & Business Impact
Dominance of the Cut & Make (CM) Model: The industry remains heavily reliant on the CM model, where Vietnamese companies act as manufacturing workshops for international brands.

Inventory Trends: Because CM firms rarely hold raw materials or finished goods, the industry shows uniquely low inventory levels, which significantly lowers the DSI for those specific clusters.

Strategic Shift: While CM dominates, the data reveals a gradual shift toward Mixed (CMP/FOB) models, suggesting an industry-wide move toward higher value-added services.

Leverage & Risk Profile: Due to the low-asset nature of the workshop model, the industry maintains a relatively safe leverage position, with 38% of firms classified as Safe/Conservative and 45% at Medium Risk.

🏗️ Project Workflow
Ingestion: Loading 1,590+ financial records with inconsistent formatting.

Cleaning: Applying Python-based logic to enforce accounting rules and remove unrealistic outliers.

Modeling: Developing DAX measures for Mean ROA, ROE, and Debt Ratios.

Synthesis: Designing a Power BI interface that translates raw figures into a "State-Aware" Risk Indicator system

⚠️ Project Limitations & Data Constraints
While this dashboard provides a robust benchmark, several inherent data constraints should be considered when interpreting the results:

1. Sector Granularity & Classification Bias
SIC Code Limitations: The current Vietnam Standard Industrial Classification (VSIC) does not sufficiently distinguish between sub-sectors such as fiber production, fabric weaving, and garment manufacturing.

Business Model Ambiguity: The benchmark lacks specific metadata regarding individual business models (e.g., OEM vs. ODM), which may lead to generalized results that do not fully capture the nuances of specialized niches.

2. Operational & Productivity Gaps
Lack of Footnotes/Qualitative Data: Without access to financial statement footnotes, it is challenging to interpret the "why" behind specific figures, limiting the depth of corporate insights.

Missing Productivity Metrics: The dataset does not provide operational capacity or manufacturing output data, making it impossible to calculate true productivity ratios or facility utilization rates.

3. Extreme Outliers & The "Cut and Make" (CM) Effect
Inventory Anomalies: The CM model involves minimal inventory ownership, occasionally producing extreme statistical outliers—such as inventory turnover ratios exceeding 7,000x—which can distort group averages.

Market Skewness: The coexistence of a massive SME base alongside "Extreme Giants" creates a heavily skewed distribution, making it difficult to establish a single "standard" for the entire industry.

4. Data Attrition & Quality Issues
Raw Data Integrity: Significant inconsistencies in the raw data (e.g., non-compliant balance sheets) necessitated a rigorous cleaning and dropping process.

Sample Loss: Approximately 50% of the initial records were removed during the data validation phase to ensure the accuracy of the remaining results. While this improved reliability, it significantly reduced the total sample size.
