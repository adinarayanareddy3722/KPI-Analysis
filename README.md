# Lowell General Hospital KPI Analysis

Analysis of three patient safety and satisfaction KPIs for Lowell General Hospital, covering January 2020 to December 2024.

## Project Files

- `Healthcare.ipynb`: Python notebook. Cleans the raw dataset, explores each KPI, checks correlations, and plots monthly and yearly trends.
- `Health_Care.pbix`: Power BI dashboard. Builds on the cleaned dataset to give an interactive view of the same three KPIs by month, quarter, and year.
- `Healthcare.pptx`: 20-slide presentation. Walks through the problem statement, KPI definitions, correlation findings, trend charts, and benchmark comparisons.

These three files are one connected project. The notebook cleans and analyzes the raw data. The dashboard visualizes the same cleaned fields (Month, KPI1, KPI2, KPI3) for interactive exploration. The presentation reports the findings from both to stakeholders.

## Dataset

- Source: Lowell General Hospital internal data
- Size: 60 rows, monthly records from 01/2020 to 12/2024
- Columns after cleaning: Month, KPI1, KPI2, KPI3

KPI definitions:

1. **KPI1, Average Licensed Bed Occupancy Rate**: share of licensed hospital beds occupied in a period, shown as a percentage.
2. **KPI2, Unassisted Fall Rate per 1,000 Patient Days**: patient falls with no staff member present at the time, reported by NDNQI.
3. **KPI3, Staff Responsiveness Domain Top Box Score**: HCAHPS survey score based on how quickly staff responded to call buttons and bathroom assistance requests.

## Method

1. Load the raw Excel file and check its shape, date range, and duplicates.
2. Rename columns, drop unused benchmark fields, and convert KPI1 to a percentage.
3. Check each KPI for outliers with box plots.
4. Compute correlations between the three KPIs and plot a heatmap.
5. Plot each KPI by month and by year to see trends over time.
6. Compare each KPI against a published U.S. benchmark.
7. Export the cleaned data to `data.csv` for use in Power BI.

## Key Findings

- Bed occupancy and fall rate have a strong positive correlation (0.70). Higher occupancy tracks with more falls.
- Bed occupancy and staff responsiveness have a moderate negative correlation (-0.37).
- Fall rate and staff responsiveness have a strong negative correlation (-0.79). Higher responsiveness tracks with fewer falls.
- Bed occupancy averages 96.22%, well above the roughly 66% U.S. benchmark. This points to strain on staff and reduced patient satisfaction risk above 85% occupancy.
- Fall rate averages 2.61 per 1,000 patient days, at the low end of the 2.3 to 13 benchmark range. Fall prevention is working.
- Staff responsiveness averages 63.09%, below the 85 to 90% benchmark. This is the main area for improvement, and likely tied to high occupancy straining staff capacity.

## Recommendation

Elevated occupancy combined with low staff responsiveness points to operational strain. Improving staffing levels and response times during high-occupancy periods should raise the responsiveness score and help hold the fall rate at its current low level.

## Tools Used

Python (Pandas, NumPy, Seaborn, Matplotlib), Power BI, PowerPoint
