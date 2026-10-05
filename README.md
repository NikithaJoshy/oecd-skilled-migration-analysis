# Skilled Migration, Labor-Market Integration & Innovation in the OECD

An analysis of how the skill mix of migrants changed from 2000 to 2020 in **Australia, Greece, and Norway**, how well immigrants integrated into labor markets, and whether high-skill migration tracks national R&D investment.

*Texas A&M University, DAEN 400, Case Study 6, Fall 2025. Two-person team project.*

## Data
- OECD **Database on Immigrants in OECD Countries (DIOC)** for 2000-01, 2005-06, 2010-11, and 2015-16. Each vintage has different file structures and variable definitions.
- OECD labor-market indicators
- OECD gross domestic expenditure on R&D

## Approach
- **Harmonized four inconsistent DIOC vintages** into one country-year panel, and standardized education levels into low, medium, and high skill.
- Calculated immigrant vs. native **employment and unemployment rates** using OECD/ILO definitions.
- Merged high-skill migrant shares with R&D expenditure and ran **Pearson correlation tests** (SciPy).
- Visualized skill-mix trends with stacked bars and line plots.

## Key Results
- High-skill migration increased in all three countries, most in Australia. Greece's inflows remain mostly low and medium skill.
- In Australia and Norway, immigrants became more educated than natives, and immigrant employment gaps narrowed over time.
- High-skill migration vs. R&D investment:

| Country | Pearson r | Significance |
|---|---|---|
| Greece | **0.951** | p < 0.05 |
| Norway | 0.917 | borderline (p = 0.083) |
| Australia | 0.757 | not significant |

## Recommendations
Simplify high-skill visa and credential pathways, expand integration support (language training, job matching), align migration and innovation policy, and improve consistency of OECD migration data.

## Tech Stack
Python, pandas, NumPy, SciPy, matplotlib, seaborn, Google Colab

## Repository Contents
- `notebooks/oecd_skilled_migration.ipynb`: data loading and harmonization, analysis, figures
- `reports/OECD_Skilled_Migration_Report.pdf`: technical report

> The notebook was run in Google Colab with the DIOC files on Google Drive. Download them from the [OECD DIOC page](https://www.oecd.org/en/data/datasets/database-on-immigrants-in-oecd-and-non-oecd-countries.html) and update the paths to run it locally.
