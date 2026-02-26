# Input to Yield Ratio (IYR) values for wheat farming in England, 2010-2017 Dataset Documentation

## Overview
- Documentation of the dataset that maps the Input to Yield Ratio (IYR) for wheat farming in England from 2010 to 2017.
- IYR compares agrochemical inputs to agricultural yield, expressed as a scaled measure (values normalized to 1 within each dataset).
- Four mapped products to assess environmental harm: nitrogen fertilisers, phosphorus fertilisers, pesticide risk to earthworms, and pesticide risk to honeybees.
- Purpose: evaluate trade-offs between yields and agrochemical inputs at large spatial scales to inform sustainability actions and potential land-use decisions.

## Data scope and structure
- Spatial resolution: 1 km, British National Grid reference system.
- Format: four single-layer TIFF files at 1 km resolution:
  - input_to_yield_ratio_honeybees.tif
  - input_to_yield_ratio_nitrogen_fertilisers.tif
  - input_to_yield_ratio_phosphorus_fertilisers.tif
  - input_to_yield_ratio_earthworms.tif
- Time period: 2010–2017 (values averaged across years to maximize data availability).
- Coverage: England; areas with no data where winter wheat was not grown show as gaps.

## IYR concept and interpretation
- IYR = ratio of agrochemical inputs to wheat yield (scaled). A higher IYR indicates greater potential harm relative to the yield obtained.
- Scaled values allow comparison across inputs and harms within the dataset.

## Data sources and inputs
- Wheat yield: Defra June Survey of Agriculture and Horticulture (Defra, 2018).
- Fertiliser usage: Defra fertiliser usage data (2022).
- Pesticide usage: FERA Pesticide Usage Surveys (2022).
- Crop presence: UKCEH Land Cover plus: Crops map (2017).
- Harm toxicity mappings:
  - Honeybees and earthworms risk derived from toxicity data in the Pesticide Properties Database (PPDB, 2022).
- Dataset creation uses annual data aggregated to create national-scale estimates of pesticide and fertiliser applications and yields.

## Methodology and workflow
- Spatially-explicit, national-scale estimation of variables for winter wheat and associated harms (four product types).
- Approached by deriving:
  - Estimated pesticide and fertiliser applications (mapped to honeybee and earthworm risk using toxicity data).
  - Average wheat yield map for England (from Defra data).
- Calculation steps:
  - Compute IYR for each harm type by comparing fertiliser/pesticide data to estimated yields.
  - Average across years to enhance data robustness.
- Outputs produced as full-country 1 km maps (and related outputs such as frequency distributions).
- Methodology overview illustrated in Figure 2; full details in Bullock et al. (2023).

## Outputs and how to use
- Four main outputs (IYR products) for assessment of environmental sustainability:
  - IYR for nitrogen fertilisers
  - IYR for phosphorus fertilisers
  - IYR for pesticide risk to earthworms
  - IYR for pesticide risk to honeybees
- Example outputs include maps and frequency distributions of IYR values across England (Figure 1).
- Potential applications:
  - Identify regions with high environmental harm relative to yield.
  - Target actions to improve sustainability of arable farming.
  - Inform land-use decisions, including potential shifts to other farming practices or ecosystem restoration.

## Data access, citation, and versioning
- Citation: Fincham et al. (2023). Input to Yield Ratio (IYR) values for wheat farming in England, 2010-2017. NERC Environmental Information Data Centre. DOI to be inserted.
- Data access: Environmental Information Data Centre (http://eidc.ceh.ac.uk/).
- Version: Version 1.0; 11/07/2023.
- Notes: No data areas correspond to cells where winter wheat was not grown.

## Acknowledgements and references
- Acknowledgements to funding and data providers:
  - ASSIST and AgZero+ projects
  - Fera for Pesticide Usage Survey data
  - Caroline Cowan (UKCEH) for data licensing assistance
- Core references include:
  - Defra (2018) June Survey methodology
  - FERA (2022) Pesticide Usage Surveys
  - Defra (2022) Fertiliser usage data
  - PPDB (2022) Pesticide Properties Database
  - UKCEH Land Cover plus: Crops (2017)
  - Bullock et al. (2023) for in-depth methodology and outputs