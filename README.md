# World University Rankings Analysis

Exploratory data analysis of the 2015 world university rankings from **Times Higher Education**, **CWUR** and **Shanghai (ARWU)**.

Dataset: [World University Rankings](https://www.kaggle.com/datasets/mylesoneill/world-university-rankings) on Kaggle.

## Data

| File | Description |
|------|-------------|
| `timesData.csv` | Times Higher Education rankings (2011–2016) |
| `cwurData.csv` | CWUR rankings (2012–2015) |
| `shanghaiData.csv` | Shanghai / ARWU rankings (2005–2015) |
| `school_and_country_table.csv` | University to country lookup |
| `education_expenditure_supplementary_data.csv` | OECD education spending (% of GDP) |
| `educational_attainment_supplementary_data.csv` | World Bank educational attainment |

## Data cleaning

- Checked for duplicates (none found), removed empty rows and stripped extra spaces
- Fixed country name typos and differences (e.g. `Unisted States of America`, `USA`, `Russia`, `Korea, Rep.`)
- Converted banded ranks such as `201-225` and `=12` to numbers
- Removed `%`, `,` and `-` from Times columns
- Filled a few missing student statistics with the median
- Left `total_score` missing where it isn't published (outside the Times top ~200 and the Shanghai top 100)

## Analysis (2015)

1. Average Times ranking factors
2. Number of universities in each ranking
3. Universities by country and the top 10 countries
4. Times vs CWUR: countries in the top 100
5. Average university score by country (at least 3 universities)
6. Correlation of ranking factors with total score
7. Top 10 universities by research score

## Key findings

- The **USA** has the most ranked universities (108 in Times), followed by the UK (45) and Germany (28).
- The USA dominates the top 100 in both Times (45) and CWUR (55).
- **Research (0.93)** and **teaching (0.91)** are most strongly linked to the Times total score.
- **Harvard** has the highest research score (98.6), followed by Caltech and Oxford.
- The rankings cover different numbers of universities: Times 401, Shanghai 500, CWUR 1,000.

## How to run

```bash
pip install pandas numpy matplotlib jupyter
jupyter notebook
```

Open the notebook and run all cells. Change `path` in the first cell if the CSVs are not in the Kaggle input folder.

## Author

Manisha Mali
