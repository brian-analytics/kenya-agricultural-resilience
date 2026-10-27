# FarmResilience Analytics: Agricultural Production Trends in Kenya (1961–2024)

## Project Overview

**FarmResilience Analytics** is a data analytics portfolio project examining long-term agricultural production, harvested area, crop yields, and annual production variability in Kenya between 1961 and 2024.

Using data from the Food and Agriculture Organization of the United Nations (FAOSTAT), the project explores how selected food crops have changed over time and identifies patterns that may be relevant to agricultural planning, food-system research, and resilience discussions.

The project combines Python-based data preparation and exploratory analysis with an interactive Power BI dashboard to communicate findings through data-driven visualizations.

## Research Questions

- How has the production of selected crops in Kenya changed between 1961 and 2024?
- How have harvested area and crop yields changed over the same period?
- Which selected crops exhibit greater year-to-year variability in production?
- What additional context is needed before using production trends to assess agricultural resilience?

## Crops Analysed

The analysis covers five selected crops:

- Maize (corn)
- Beans, dry
- Sorghum
- Millet
- Cassava, fresh

Three measures are examined for each crop:

- **Production:** quantity produced, measured in tonnes.
- **Area harvested:** harvested area, measured in hectares.
- **Yield:** production per unit of harvested area, measured in kilograms per hectare.

## Data Source

**Source:** [FAOSTAT — Crops and Livestock Products](https://www.fao.org/faostat/en/#data/QCL)

- Geographic scope: Kenya
- Time coverage: 1961–2024
- Data type: National-level annual agricultural statistics
- Selected observations: Five crops across three measures and 64 years
- Analytical dataset: 960 crop-measure-year records

The analysis retains available observation flags to preserve information about the reported status of the source data. These flags may distinguish official, estimated, imputed, or externally sourced observations.

## Tools and Technologies

- **Python:** data preparation, validation, exploratory analysis, and summary calculations
- **Pandas and NumPy:** data manipulation and numerical analysis
- **Jupyter Notebook:** documented analytical workflow
- **Power BI:** interactive dashboard and visual reporting
- **Git and GitHub:** version control and project documentation

## Project Workflow

### 1. Data audit and preparation

The first notebook examines the source dataset's structure, time coverage, missing values, zero values, duplicates, observation flags, and selected records for Kenya.

### 2. Crop trends and variability

The second notebook analyses historical production, harvested area, and yield trends. It also calculates year-to-year production changes and compares the variability of annual production changes across the selected crops.

### 3. Portfolio dataset preparation

The third notebook prepares and validates the final datasets for Power BI, retaining the relevant observation flags and generating a summary dataset comparing 1961 and 2024.

### 4. Power BI dashboard

The dashboard, **FarmResilience Analytics**, presents crop production trends, harvested-area comparisons, yield patterns, selected-year indicators, and historical production variability.

## Key Findings

The following findings describe the selected national-level observations. They should not be interpreted as proof of the causes of agricultural change.

### Long-term production changes

Comparing 1961 with 2024:

- **Beans, dry:** production increased from 55,000 tonnes to approximately 903,851 tonnes.
- **Maize:** production increased from 940,000 tonnes to 4,023,000 tonnes.
- **Cassava, fresh:** production increased from 420,000 tonnes to approximately 1,207,537 tonnes.
- **Sorghum:** production increased from 164,000 tonnes to 243,000 tonnes.
- **Millet:** production decreased from 130,000 tonnes to approximately 65,763 tonnes.

These comparisons describe changes between two endpoints; they do not imply that the changes occurred steadily throughout the period.

### Historical production variability

Using the standard deviation of annual percentage changes in production over 1962–2024, the crops ranked from highest to lowest variability as follows:

| Crop | Standard deviation of annual production change |
|---|---:|
| Millet | 71.89% |
| Cassava, fresh | 41.25% |
| Sorghum | 38.25% |
| Beans, dry | 21.19% |
| Maize | 19.10% |

Millet had the highest measured variability among the five selected crops, while maize had the lowest. These statistics measure variability in annual percentage changes, not the overall level of production or the complete resilience of a crop or farming system.

## Repository Structure

```text
kenya-agricultural-resilience/
├── README.md
├── 01_faostat_data_audit.ipynb
├── 02_crop_trends_and_resilience.ipynb
├── 03_portfolio_dataset_preparation.ipynb
└── portfolio_outputs/
    ├── kenya_crop_trends_powerbi.csv
    └── kenya_crop_summary_powerbi.csv
```

The structure above describes the intended organization. If your files are stored in folders such as `notebooks/` or `data/processed/`, update the paths in this section to match the actual repository.

## How to Explore the Project

1. Open `01_faostat_data_audit.ipynb` to review the data-quality checks and source structure.
2. Open `02_crop_trends_and_resilience.ipynb` to explore crop trends and annual production variability.
3. Open `03_portfolio_dataset_preparation.ipynb` to review the preparation and validation of the Power BI datasets.
4. Import `kenya_crop_trends_powerbi.csv` into Power BI to explore the crop-level annual records.
5. Use `kenya_crop_summary_powerbi.csv` to examine the endpoint comparisons.

To run the notebooks locally, install Python and Jupyter Notebook, then install the libraries used in the notebooks. Update any file paths to match your local environment.

## Limitations and Interpretation

- The analysis uses national-level data and cannot describe differences between counties, individual farms, or households.
- Production trends and annual percentage changes alone do not establish whether farmers are resilient or whether households are food secure.
- Production can change alongside harvested area, yield, weather, market conditions, policies, technology, and other factors. This descriptive analysis does not isolate their individual effects.
- The 1961–2024 endpoint comparison does not describe every intermediate change.
- Annual percentage changes can be sensitive to small previous-year values and exceptional observations.
- The simple average of the five crop yields is not a weighted national agricultural yield.
- Summed harvested area across crops represents crop-hectares and may count the same physical land more than once.
- Source observation flags should be considered when interpreting individual values.
- The analysis covers five selected crops rather than Kenya's entire agricultural sector.

These limitations mean the results are best understood as a descriptive exploration of selected crop trends, not a complete measurement of agricultural resilience.

## Potential Extensions

Future development could incorporate county-level agricultural statistics, rainfall and temperature indicators, food-price data, or household food-security indicators. These additional datasets could help investigate relationships that cannot be established from crop production data alone.

## Author

**Brian Kirigwi Mwangi**

Data Analytics | Python | Power BI | Exploratory Data Analysis

This project demonstrates an end-to-end analytical workflow, from data auditing and validation to trend analysis, visualization, and communication of findings.

---

*Data source: FAOSTAT, Crops and Livestock Products. Analysis period: 1961–2024.*