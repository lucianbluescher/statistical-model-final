# Snow and Irradiance Effects on PV Performance

![pv-winter](images/clipboard-841556536.png)  
_Image credit: [Revision Energy](https://www.revisionenergy.com/solar-information/solar-resources/10-reasons-go-solar/works-in-winter)_

### Beta regression of PV performance ratio (PR) on snow, irradiance, and age using the OEDI PV dataset

Author: Lucian Scher

This repository contains a Quarto analysis of how cumulative snow depth, low irradiance, plant age, and region relate to daily photovoltaic performance ratio (PR). It builds on Jackson & Gunda (2021), who showed extreme weather—especially snow—can reduce utility-scale PV output.

## Data
Dataset: OEDI PV dataset (bundled here as `oedi_data.xlsx`, with `README`, `data`, and `data_dictionary` sheets)
- [Gunda, T., & Jackson, N. (2021, April). Dataset for Evaluation of Extreme Weather Impacts on Utility-Scale Photovoltaic Plant Performance in the United States. OpenEI.](https://data.openei.org/submissions/4055)

O&M and production records (PVROM): Sandia National Laboratories. PV Reliability, Operations, and Maintenance (PVROM) database (50,000+ O&M tickets, 837 sites, 5.1 GWDC). Accessible via the [OEDI release](https://data.openei.org/submissions/4055): 
(See also Sandia [PVROM overview](https://www.osti.gov/servlets/purl/1337988).

Weather augmentation (2008–2020): [NOAA Storm Events Database](https://www.ncdc.noaa.gov/stormevents/), [PRISM Climate Group data](https://prism.oregonstate.edu), and [Global Historical Climatology Network (GHCN)](https://www.ncei.noaa.gov/data/global-historical-climatology-network-daily/), as curated in Jackson & Gunda.
‌

## Repository Structure

```
├── beta_blog.qmd             # Beta regression analysis notebook
├── oedi_data.xlsx            # OEDI PV data (README, data, data_dictionary)
├── extreme_weather.pdf/txt   # Reference paper (Jackson & Gunda, 2021)
├── images/                   # Figures
└── README.md
```

## How to Run

1. Install R and Quarto. Ensure these R packages are installed: `tidyverse`, `readxl`, `janitor`, `betareg`, `broom`, `kableExtra`, `dagitty`.
2. Render the notebook:
   `quarto render beta_blog.qmd`
3. Open the generated HTML to view results (coefficients, plots, discussion).

### Acknowledgments
This project was part of EDS 222 *Statistics for Environmental Data Science*, a course in the Master of Environmental Data Science (MEDS) program at the Bren School at UC Santa Barbara.
I would like to thank Max Czapanskiy for his masterful patience and pedagogical ability, Nathan Grimes for his deeply insightful and constructive feedback and them both for the wonderful instruction of this course and guidance through this final project.
