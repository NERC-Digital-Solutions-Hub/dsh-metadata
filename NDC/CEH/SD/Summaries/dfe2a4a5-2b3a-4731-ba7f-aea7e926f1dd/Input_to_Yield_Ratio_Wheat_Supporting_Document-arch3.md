# Input to Yield Ratio (IYR) values for wheat farming in England, 2010-2017 Dataset Documentation

## Overview
- A dataset documenting the methodology and metadata for mapping Input to Yield Ratio (IYR) values for winter wheat farming in England from 2010 to 2017.
- IYR expresses the ratio of agrochemical inputs (fertilisers and pesticides) to agricultural reward (yield), calculated at 1 km resolution across England.
- Produces four mapped products: IYR for Nitrogen fertilisers, IYR for Phosphorus fertilisers, IYR for pesticide risk to earthworms, and IYR for pesticide risk to honeybees.
- Values are scaled so the maximum in each input/yield dataset is 1, enabling relative comparisons of input harm to yield.
- Intended to support evaluating trade-offs between yields and agrochemical inputs and to guide sustainability-focused farming or land-use decisions.

## What is measured and why it matters for monitoring policy
- Measures four environmental-harm-to-yield indicators:
  - Nitrogen fertilisers
  - Phosphorus fertilisers
  - Pesticide risk to earthworms
  - Pesticide risk to honeybees
- Enables policy-relevant monitoring of where higher environmental harms occur relative to yields, supporting targeted interventions, practice change, or land-use planning (e.g., ecosystem restoration).

## Data sources and harmonization
- Inputs and targets:
  - Yields: Defra June Survey of Agriculture and Horticulture (2018 methodology references used for averaging)
  - Fertiliser usage: Defra Fertiliser Practice data (2022)
  - Pesticide usage: FERA Pesticide Usage Surveys (2022)
  - Wheat-cropping areas: UKCEH Land Cover® plus: Crops map (2017)
  - Toxicity data: Pesticide Properties Database (PPDB, 2022)
- Spatial and temporal scope:
  - England, 1 km resolution, 2010–2017 (annual data averaged across years to expand data availability)
  - Some cells may lack data where winter wheat was not grown
- Outputs are four single-layer TIFF rasters, aligned to British National Grid.

## Methodology and metadata
- Calculation:
  - Compare estimated fertiliser/pesticide applications to estimated wheat yields to derive IYR for four harms.
  - Convert pesticide toxicity information to risk values for honeybees and earthworms.
  - Normalize each product by scaling to a maximum value of 1 within its dataset.
- Outputs:
  - input_to_yield_ratio_honeybees.tif
  - input_to_yield_ratio_nitrogen_fertilisers.tif
  - input_to_yield_ratio_phosphorus_fertilisers.tif
  - input_to_yield_ratio_earthworms.tif
- Documentation includes a detailed methodology figure and references to Bullock et al. (2023) for in-depth processes.

## Outputs and interpretation
- Maps and frequency distributions illustrate the distribution of IYR values across England; higher values indicate greater potential harm relative to yield.
- White areas indicate no winter wheat grown.
- Useful for identifying regions where policy actions could reduce environmental harms while maintaining yields, and for exploring land-use options or crop diversification.

## Data access, citation, and governance
- Citation: Fincham et al. (2023). Input to Yield Ratio (IYR) values for wheat farming in England, 2010-2017. NERC Environmental Information Data Centre. DOI to be inserted.
- Access: Environmental Information Data Centre (eidc.ceh.ac.uk).
- Version: 1.0; 11/07/2023.
- Acknowledgements to funding programs (ASSIST, AgZero+), data providers (FERA, Defra, PPDB), and data licensing support.

## Limitations and challenges for monitoring frameworks
- Temporal alignment: different data sources have varying collection periods; averaging across years mitigates but does not eliminate misalignment.
- Data gaps: some 1 km cells lack data where winter wheat was not grown.
- Normalization: scaling to a maximum of 1 can obscure absolute magnitudes of inputs or yields.
- Dependence on multiple external datasets with their own uncertainties (surveys, toxicity databases).
- Data sharing and provenance considerations; underlying data licensing and accessibility need ongoing governance.