# Video Game Sales — Exploratory Data Analysis

## Project Overview

This project explores video game sales data using Python. The goal is to understand sales patterns, inspect data quality, identify potential outliers, and examine relationships between regional and global sales.

## Dataset

- **Dataset:** Video Game Sales
- **Source:** [Kaggle — Video Game Sales](https://www.kaggle.com/datasets/gregorut/videogamesales)
- **Rows:** 16,598
- **Columns:** 11

The dataset includes game names, platforms, release years, genres, publishers, and sales figures across different regions.

## Tools and Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## Analysis Performed

- Dataset profiling and summary statistics
- Missing-value and duplicate checks
- Sales data validation
- Outlier detection using the Interquartile Range (IQR) method
- Histograms of global and regional sales
- Boxplot of global sales
- Correlation heatmap of regional and global sales
- Scatterplots comparing regional sales
- Consistency check between regional sales and recorded global sales

## Key Findings

- The dataset contains 16,598 rows and 11 columns.
- There are 329 missing cells: 271 in `Year` and 58 in `Publisher`.
- No duplicate rows were found.
- No negative values were found in the five sales columns.
- Global sales are right-skewed: most games have relatively low sales, while a smaller number have very high sales.
- The IQR method flagged 1,893 potential global-sales outliers. These were retained because high sales do not automatically indicate errors.
- Regional sales have positive correlations with one another and with global sales. North American and European sales show strong positive correlations with global sales.
- Small differences between summed regional sales and recorded global sales were observed, consistent with rounding.

## Data Cleaning Decisions

- Missing release years and publisher names were retained rather than replaced with guessed values.
- No duplicate rows required removal.
- No negative sales values required correction.
- Potential sales outliers were retained because they may represent genuine sales performance.
- Original sales figures were retained after the regional/global consistency check.

## Project Structure

```text
task-1-eda/
├── task1_eda.ipynb
├── README.md
└── figures/
    ├── global_sales_distribution.png
    ├── global_sales_boxplot.png
    ├── regional_sales_distributions.png
    ├── sales_correlation_heatmap.png
    └── regional_sales_scatterplots.png
```

## How to Run

1. Install Python and Jupyter Notebook.
2. Install the required libraries: `pandas`, `numpy`, `matplotlib`, and `seaborn`.
3. Ensure the dataset is available at the file path used in the notebook.
4. Open `task1_eda.ipynb` in Jupyter Notebook.
5. Run all cells from top to bottom.

## Conclusion

This analysis provides an overview of video game sales patterns, regional relationships, and dataset quality. The findings highlight the concentration of sales among a smaller number of high-performing games while documenting missing values and other data-quality checks.