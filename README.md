# Transition-matrix-shad-growth
Code and results for reconstructing seasonal growth of juvenile American shad from length-frequency data using transition matrices.

## Repository contents (REVISE!!)

- `data.xlsx` – Dataset used throughout the analyses.
- `Growth_abundaunce_temperature.ipynb`
- `Transition_matrix.ipynb`
- `Bootstrap_uncertainty.ipynb`
- `LICENSE`
- `README.md`

## Software requirements
The analyses were developed using Python 3 and Jupyter Notebook (Anaconda distribution).

Required Python packages:

- matplotlib
- NumPy
- openpyxl
- pandas
- scikit-posthoc
- SciPy
- seaborn
- statsmodels

  
## Data description (REVISE)
The repository contains the Excel workbook `data.xlsx`, which includes the datasets used throughout the analyses. The data are based on long-term monitoring of female American shad conducted by the Connecticut Department of Energy and Environmental Protection (CT DEEP). For the purposes of this project, data were organized into worksheets corresponding to the analyses performed in the notebooks.

## Reproducing the content
Each notebook is independent and can be run separately.
Open the desired notebook in Jupyter Notebook or JupyterLab and execute all cells from top to bottom.

## Notebook descriptions. 
(The notebooks are listed in the order in which the analyses are performed.)

### `Growth_abundaunce_temperature.ipynb`
Estimates annual juvenile American shad growth, abundance indices, and mean summer temperature; compares upper- and lower-river patterns; and evaluates associations between growth, abundance, and temperature.

**Input:** 
- `CTR_Juvenile_ASD_Master.csv` — juvenile abundance counts and temperature by year, month, and site.
- `Juvenile_Master_Length_Data_1978_2021.csv` — individual fish lengths by date and sampling site.

**Outputs:** 
- Data tables of annual abundance, mean temperature, and growth estimates.
- Statistical comparisons and regression summaries.
- Figures showing regional patterns, growth–environment relationships, and model diagnostics.

### `Site_level_growth.ipynb`
Estimates site-level juvenile American shad growth and evaluates its relationship with abundance, temperature, and sampling site using regression, the Kruskal–Wallis test, and post hoc pairwise comparisons.

**Input:** 
- `CTR_Juvenile_ASD_Master.csv` 
- `Juvenile_Master_Length_Data_1978_2021.csv`
  
**Outputs:** 
- Site-year summaries of growth, abundance, and temperature.
- Regression and site-comparison results.
- Figures showing growth distributions across sampling sites.
  
### `Transition_matrix.ipynb`
Reconstructs juvenile American shad growth-transition matrices from monthly length-frequency distributions, estimates conditional growth and apparent
retention, and compares direct and composed seasonal transitions.

**Input:** `Juvenile_Master_Length_Data_1978_2021.csv`

**Outputs:** ## Outputs

- CSV tables of transition diagnostics, growth, and apparent retention.
- Excel workbook containing annual and mean transition matrices.
- Figures showing length distributions, transition matrices, annual growth and retention, and direct-versus-composed comparisons.

### `Bootstrap_uncertainty.ipynb`
This notebook quantifies sampling uncertainty in apparent retention, conditional mean growth, and prediction residuals derived from a direct July-to-September transition matrix for a selected year. Fish are resampled with replacement within each month and river region, thereby preserving the observed upper- and lower-river sample sizes in every bootstrap
replicate. The selected year can be changed using the `BOOT_YEAR` setting.

**Input:** `Juvenile_Master_Length_Data_1978_2021.csv`

**Outputs:** 
- CSV tables containing individual bootstrap results and summary statistics.
- Figures showing bootstrap distributions of conditional mean growth, apparent retention, and prediction residuals, together with the relationship between retention and growth.

