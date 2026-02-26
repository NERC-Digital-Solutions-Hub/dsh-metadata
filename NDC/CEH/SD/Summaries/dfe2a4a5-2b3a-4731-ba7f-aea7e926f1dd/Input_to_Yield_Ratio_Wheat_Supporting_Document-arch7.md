# Input to Yield Ratio (IYR) values for wheat farming in England, 2010-2017 Dataset Documentation

## Overview
- Dossier detailing the methodology and metadata for the IYR dataset for winter wheat in England (2010–2017).
- IYR is a ratio of agrochemical inputs to agricultural reward (yield); calculated at 1 km resolution.
- Four mapped products: IYR for nitrogen fertilisers, phosphorus fertilisers, pesticide risk to earthworms, and pesticide risk to honeybees.
- Values are scaled so the maximum in each dataset is 1, enabling proportional comparison across inputs and harms.
- Aims to help evaluate trade-offs between yields and agrochemical inputs at large spatial scales and inform sustainability actions or land-use decisions.

## Data structure and products
- Four single-layer TIFF rasters at 1 km resolution (British National Grid):
  - input_to_yield_ratio_honeybees.tif
  - input_to_yield_ratio_nitrogen_fertilisers.tif
  - input_to_yield_ratio_phosphorus_fertilisers.tif
  - input_to_yield_ratio_earthworms.tif
- No-data areas occur where winter wheat was not grown (white areas in outputs).

## Purpose and use cases
- Enables assessment of sustainability trade-offs between wheat yields and agrochemical inputs across England.
- Supports targeting of actions to improve arable farming sustainability or guide land-use changes (e.g., ecosystem restoration).

## Methodology highlights
- Data period: 2010–2017; maps produced for each year but values averaged across years to increase data availability.
- Yield data: average wheat yield map for England derived from the Defra June Survey data (2018 reference) and other sources.
- Input data:
  - Fertiliser usage mapped from FERA Pesticide Usage Survey (2022) and Defra Fertiliser Usage data (2022) for nitrogen and phosphorus.
  - Pesticide risk mapped using toxicity information from the Pesticide Properties Database (PPDB, 2022) to derive risks to honeybees and earthworms.
  - Winter wheat area identified from UKCEH Land Cover Plus: Crops map (2017).
- Normalisation: all inputs and yields scaled to a maximum value of 1 within each dataset.

## Data sources and references
- FERA Pesticide Usage Surveys (2022)
- Defra Fertiliser Usage data (2022)
- UKCEH Land Cover Plus: Crops (2017)
- Defra June Survey of Agriculture and Horticulture methodology (2018)
- PPDB – Pesticide Properties DataBase (2022)
- Bullock et al. (2023) for methodology context

## Access, citation, and versioning
- Citation: Fincham, W.N.W.; Risser, H.A.; Jarvis, S.G.; Schultz, C.; Spurgeon, D.J.; Redhead, J.W.; Storkey, J.; Pywell, R.F.; Bullock, J.M. (2023). Input to Yield Ratio (IYR) values for wheat farming in England, 2010-2017. NERC Environmental Information Data Centre. DOI to be inserted.
- Access: Environmental Information Data Centre (eidc.ceh.ac.uk).

## Outputs and visualization
- Example outputs include maps and frequency distributions of IYR across England (1 km resolution), with figure descriptions aligning map colors to histograms and noting areas with no wheat.

## Practical notes for GIS specialists
- Use as comparative, relative indicators rather than absolute risk values due to scaling.
- Mask or exclude non-wheat areas where data are NA for accurate analyses.
- Compatible with GIS workflows for overlay analyses, spatial prioritization, and landscape-scale sustainability assessments.