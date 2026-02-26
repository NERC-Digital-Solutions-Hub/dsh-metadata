# Input to Yield Ratio (IYR) values for wheat farming in England, 2010-2017 Dataset Documentation

## Overview
- Purpose: documents the methodology and metadata for the IYR dataset, which maps the ratio of agrochemical inputs to agricultural reward (yield) for winter wheat in England at 1km resolution over 2010–2017.
- Product scope: four mapped products expressing potential environmental harm relative to yield:
  - IYR for Nitrogen fertilisers
  - IYR for Phosphorus fertilisers
  - IYR for pesticide risk to earthworms
  - IYR for pesticide risk to honeybees
- Key design: values are scaled within each dataset so the maximum value = 1 to enable proportional comparisons across inputs and harms.
- Intended use: supports assessment of trade-offs between yields and agrochemical inputs at large scales and informs where sustainability actions or land-use changes may be appropriate.

## Data assets
- Four single-layer TIFF rasters at 1km resolution using the British National Grid:
  - input_to_yield_ratio_honeybees.tif
  - input_to_yield_ratio_nitrogen_fertilisers.tif
  - input_to_yield_ratio_phosphorus_fertilisers.tif
  - input_to_yield_ratio_earthworms.tif
- Note: data gaps exist in areas where winter wheat was not grown during the study period.

## Data description and methodology
- Spatial and temporal scope: national-extent estimates for England, averaged across 2010–2017 due to differing dataset periodicities (yield, fertilisers, pesticides, crop mapping); maps produced at 1 km resolution.
- Data sources:
  - Pesticide and fertiliser usage data from FERA Pesticide Utilisation Survey (2022) and Defra Fertiliser Practice (2022)
  - Wheat crop areas from UKCEH Land Cover® plus: Crops map (2017)
  - Pesticide toxicity to honeybees and earthworms from the Pesticide Properties Database (PPDB, 2022)
  - Wheat yield maps from Defra (June Survey of Agriculture and Horticulture, 2018)
- IYR calculation: separate comparisons of fertiliser/pesticide data to estimated yields to derive four harm-specific IYR values; methodology overview provided in Figure 2; detailed approach outlined in Bullock et al. (2023).
- Output format and accessibility: TIFF rasters with BNGrid coordinates; example outputs include maps and frequency distributions of IYR values.

## Usage and applications
- Analytical use: evaluate trade-offs between agricultural yields and agrochemical inputs at large spatial scales.
- Decision support: identify locations where action could improve sustainability, including fertilizer/pesticide reduction or land-use change (e.g., ecosystem restoration).

## Access, citation, and licensing
- Data access: Environmental Information Data Centre (EIDC) – http://eidc.ceh.ac.uk/
- Citation: Fincham et al. (2023). Input to Yield Ratio (IYR) values for wheat farming in England, 2010-2017. NERC Environmental Information Data Centre. DOI to be inserted.
- Version/date: Version 1.0; 11/07/2023.
- Acknowledgements: funding from ASSIST and AgZero+; data contributions from FERA, Defra, PPDB, UKCEH, and collaborators.

## Limitations and notes
- Year coverage varies slightly due to differing survey periodicities; values averaged across years.
- Some 1km cells have no data if winter wheat was not grown.
- IYR values are scaled within each input type; they do not represent absolute environmental harm magnitudes.

## References
- Bullock et al. 2023: Mapping the ratio of environmental harm to agricultural reward reveals areas with less sustainable farming.
- Defra (2018, 2022), FERA (2022), PPDB (2022), UKCEH (2017).