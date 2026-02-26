# Input to Yield Ratio (IYR) values for wheat farming in England, 2010-2017 Dataset Documentation

- Purpose: Document the methodology, data sources, and outputs for the Input to Yield Ratio (IYR) dataset, which assesses environmental harm relative to agricultural reward for winter wheat in England (2010–2017) at 1 km resolution.

## What the dataset measures

- IYR = ratio of agrochemical inputs (fertilisers, pesticides) to wheat yield (agricultural reward).
- Four harmonised harms mapped at 1 km:
  - IYR for Nitrogen fertilisers
  - IYR for Phosphorus fertilisers
  - Pesticide risk to earthworms
  - Pesticide risk to honeybees
- Values are scaled within each input-yield pair so the maximum is 1, enabling cross-comparison of relative environmental harm across space.
- Areas with no data correspond to 1 km cells where winter wheat was not grown.

## Data products and format

- Four single-layer TIFF files (1 km resolution, British National Grid):
  - input_to_yield_ratio_honeybees.tif
  - input_to_yield_ratio_nitrogen_fertilisers.tif
  - input_to_yield_ratio_phosphorus_fertilisers.tif
  - input_to_yield_ratio_earthworms.tif

## Key context and aims

- Scope: Map estimated uses of fertilisers and pesticides, relate to yield to identify trade-offs and inform sustainability actions for arable farming across England.
- Intended use: Target actions to improve sustainability, or consider land-use changes such as ecosystem restoration in areas with unfavorable IYR values.
- Scale: Nationally explicit, spatially explicit across England; supports large-scale decision-making.

## Data sources and inputs

- Fertiliser use: Defra (Fertiliser usage data, 2022) and the British Survey of Fertiliser Practice (Defra, 2022).
- Pesticide use: FERA Pesticide Utilisation Survey (FERA, 2022).
- Wheat crop extent: UKCEH Land Cover plus: Crops map (2017).
- Wheat yield: June Survey of Agriculture and Horticulture (Defra, 2018).
- Toxicity/toxicity-based risk: Pesticide Properties Database (PPDB, 2022) to convert applications to risk for honeybees and earthworms.

## Methodology (high-level)

- Spatially explicit, national-extent estimates of yields, fertiliser applications, and pesticide applications for winter wheat (2010–2017; slightly overlapping time windows due to data periodicities).
- Estimation steps:
  - Identify winter wheat areas and map yields.
  - Map estimated pesticide and fertiliser applications.
  - Convert pesticide applications to risk values for honeybees and earthworms using toxicity data.
  - Derive IYR by relating inputs to yields for four harms.
- Data are averaged across years to maximize data availability; maps produced at 1 km resolution.
- Overall workflow summarized in Figure 2; full details available in Bullock et al. (2023).

## Outputs and interpretation

- Example outputs include maps and frequency distributions of IYR values (Figure 1) showing spatial patterns and relative harm-to-yield relationships.
- A higher IYR value indicates greater potential environmental harm per unit of yield for the specified input/harms.

## Access, citation, and reuse

- Citation: Fincham, W.N.W.; Risser, H.A.; Jarvis, S.G.; Schultz, C.; Spurgeon, D.J.; Redhead, J.W.; Storkey, J.; Pywell, R.F.; Bullock, J.M. (2023). Input to Yield Ratio (IYR) values for wheat farming in England, 2010-2017. NERC Environmental Information Data Centre. <insert DOI here>.
- Data access: Environmental Information Data Centre (http://eidc.ceh.ac.uk/).
- Acknowledgments include funding and data providers (ASSIST, AgZero+, Fera, UKCEH, etc.).

## Limitations and considerations

- Gaps where winter wheat is not grown lead to no-data areas.
- Slightly differing time windows due to the periodicity of source datasets; values averaged across years may mask inter-annual variability.
- IYR is a relative, scaled index rather than absolute input or yield values, aiding cross-location comparisons but requiring careful interpretation when inferring absolute impacts.