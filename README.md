# CIS635 Final Project

## Overview
This repository contains our final project for CIS 635: Knowledge Discovery and Data Mining. The project looks at whether socioeconomic factors from U.S. Census ACS data are related to K-12 dropout outcomes from NCES data.

## Repository Contents
This repository contains:
- Source code for data cleaning, fusion, analysis, and visualization
- Project data used in the analysis
- Report materials
- Instructions needed to reproduce the project workflow

## Project Structure
```text
CIS635-Final-Project/
|-- Code/
|   |-- CIS635_Project.ipynb
|-- Data/
|   |-- NCES_2022-2023/
|   |-- S1501_Educational_Attainment_2010-2024/
|   |-- B14006_Poverty_Status_in_the_Past_12_Month_by_School_Enrollment_by_Level_of_School_for_the_Populuation_3_Years_and_Over/
|   |-- B17003_Poverty_Status_in_the_Past_12_Months_of_Individuals_by_Sex_by_Education_Attainemnt/
|-- Images/
|   |-- correlation_heatmap.png
|   |-- scatter_plots.png
|-- Report/
|   |-- Final Project Report CIS 635.docx
|-- README.md
```

## Main Source Code
The main project file is:
- `Code/CIS635_Project.ipynb`

This notebook performs the full preprocessing and analysis pipeline:
- Pulls ACS socioeconomic data from the Census API
- Loads NCES district-level datasets
- Cleans and aggregates NCES records to one row per district
- Aggregates both datasets to the state level
- Merges the fused data on state FIPS
- Runs correlation analysis, linear regression, and visualizations

## Requirements
This project uses Python 3 and the following packages:
- `pandas`
- `scikit-learn`
- `matplotlib`
- `seaborn`

Install the required packages with:

```bash
pip install pandas scikit-learn matplotlib seaborn
```

## Reproducibility
To reproduce the analysis:
1. Clone the repository:

```bash
git clone https://github.com/coolingj-gvsu/CIS635-Final-Project.git
cd CIS635-Final-Project
```

2. Install the required Python packages:

```bash
pip install pandas scikit-learn matplotlib seaborn
```

3. Open `Code/CIS635_Project.ipynb` in Jupyter Notebook.
4. Run all cells from top to bottom.
