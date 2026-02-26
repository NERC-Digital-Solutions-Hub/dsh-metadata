# Historic Standardized Groundwater level Index (SGI) for 54 UK boreholes (1891-2015)

- A cross-disciplinary groundwater drought dataset within the Historic Droughts Inventory, produced to understand past drought episodes in the UK and support future drought management.
- SGI time series (1891–2015) are standardized groundwater levels from reconstructed data across 54 boreholes on Principal Aquifers, mainly Chalk, with records extended back to the 19th century.

## What the dataset contains

- Standardised groundwater level Index (SGI) monthly time series for 54 UK boreholes.
- Time period: 1891 to 2015.
- For each site: SGI values plus probability estimates of SGI being less than 0, -1, -1.5, and -2.
- Data provided as separate CSV files per site; one additional metadata CSV lists sites and basic metadata (location, aquifer, MORECS cell, etc.).
- File naming follows a detailed convention indicating project, model, run, variable, catchment/borehole ID, and version.

## How SGI is calculated

- SGI is derived from reconstructed groundwater level time series using a non-parametric normal scores transform for each calendar month.
- Probability estimates are produced by the GLUE methodology, using behavioural parameter sets (Nash-Sutcliffe Efficiency > 0.5).

## Data structure and format

- Each site CSV has headers:
  - Date (Year-Month-Day, with day as the first of the month)
  - SGI (standardised groundwater level)
  - Prob0 (probability SGI < 0)
  - Prob1 (probability SGI < -1)
  - Prob15 (probability SGI < -1.5)
  - Prob2 (probability SGI < -2)
- Example file naming: HistoricDroughts_BGSAquiMod_Output_Feb2018_SGI_Rockleyver1
- Metadata file: Metadata_forGWLandSGI_reconstructions.csv with Site_name, Easting, Northing, BGS_WellMaster_ID, Full_BGS_site_name, Aquifer, MORECS_ID, etc.

## Context and purpose

- Part of the Historic Droughts project (2014–2018), funded by UK Research Councils.
- aims to develop a cross-disciplinary understanding of droughts by integrating hydro-meteorological, environmental, agricultural, regulatory, social, and cultural information.
- SGI provides a standardized, comparable measure of groundwater drought to align with meteorological drought indices (e.g., SPI) and hydrological drought indices (e.g., SSI).

## Usage and potential data products

- Create dashboards or self-serve tools enabling end-users to explore groundwater drought status by site or region.
- Compare groundwater drought signals (SGI) with meteorological drought indices to study drivers and impacts.
- Support drought management planning by providing historical context on groundwater drought frequency, duration, and severity.
- Integrate with policy, regulatory, or utility planning outputs (e.g., reference droughts for management plans).

## Data quality, limitations, and considerations

- Data are reconstructed groundwater levels, with inherent uncertainties quantified via GLUE; early records are sparse, and records are patchy across sites.
- Majority of sites are in southern/eastern England on Chalk aquifers; results are most robust where long, continuous reconstructions exist.
- SGI thresholds align with drought severity definitions: SGI ≤ -1 (drought), -1.5 (severe), ≤ -2 (extreme).

## Acknowledgements and references

- Funded by the Natural Environment Research Council (Historic Droughts project; NE/L010151/1).
- Key references: McKee et al. 1993; WMO 2012; Beven & Freer 2001; Bloomfield et al. 2018; Bloomfield & Marchant 2013.