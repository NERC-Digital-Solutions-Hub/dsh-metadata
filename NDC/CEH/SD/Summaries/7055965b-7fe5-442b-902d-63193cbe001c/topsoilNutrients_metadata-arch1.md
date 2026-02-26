# Topsoil nutrient model estimates [Countryside Survey]

## Purpose and scope
- Data describe topsoil nutrient status (0–15 cm depth) for Great Britain, focusing on total nitrogen concentration (%), C:N ratio, and Olsen-P (mg/kg).
- Based on 2007 field data: 1024 cores for total N, 1054 cores for Olsen-P from 256 1 km × 1 km squares.
- Mean values estimated for habitat/parent material combinations using a mixed-model approach, linked to Land Cover Map 2007 (LCM) and a 2009 Parent Material Model.
- Dominant parent material characteristic used: Dominant grain (DOM_GRAIN) for N, CN, and Olsen-P.
- Some areas (urban, littoral rock) are not sampled; some habitat/parent material combinations have insufficient sample sizes to estimate means.

## Variables and attributes
- Core nutrients: TOTN_07, TOTN_07SE; TOTN_98, TOTN_98SE; CN_07, CN_07SE; CN_98, CN_98SE; OLSEN_07, OLSEN_07SE; OLSEN_98, OLSEN_98SE.
- Habitat and material descriptors: LCM_CLASS (land cover map class), LCM_NUMBER (LCM code), DOM_GRAIN (dominant grain size), SOIL_GROUP, CACO3_RANK.
- Modelled means are associated with habitat/DOM_GRAIN combinations; some combinations lack data.
- Spatial reference: OSGB 1936 / British National Grid (EPSG:27700).
- Data columns also include detailed per-plot and per-class summary statistics and model-derived estimates.

## Sampling, collection, and methods
- Sampling regime: 1024 plots for total N (2007), 1110 plots for total N (1998); Olsen-P measured in 1068 plots (2007), with 65% also sampled in 1998.
- Field collection: 15 cm long, 5 cm diameter cores following Emmett et al. protocols.
- Analytical methods: 
  - Total N via CEH Lancaster UKAS-accredited elemental analyzer (SOP3102) on air-dried, sieved samples (<2 mm).
  - Olsen-P via extraction with 0.5 M NaHCO3 (pH 8.5), colorimetric molybdenum blue detection at 880 nm with dialysis step.
- Calibration and quality control: Refer to Emmett et al. (2008, 2010) and Defra/NERC Joint Codes of Practice.

## Modelling approach
- Means calculated by combining dominant habitat characteristics (LCM2007) and dominant parent material (DOM_GRAIN) using mixed-model analyses.
- Model selection for parent material uses AIC to identify the characteristic that minimizes AIC in each model.
- Some habitats/parent material combinations could not be estimated due to insufficient sample sizes.

## Spatial structure and data availability
- Spatial units: 256 original 1 km × 1 km squares; data also linked to a higher-level habitat/class framework.
- Dominant habitat and material context derived from LCM2007 and Parent Material Model 2009; urban and littoral rock areas are not represented in the sample.
- Data are designed to be discoverable with metadata; primary sources and related technical reports are cited for methods and quality control.

## Data quality, limitations, and caveats
- Gaps where data are not available (urban/littoral areas) and where some habitat/parent combinations lack sufficient observations.
- Variation in data sources across years (1998 vs 2007) and the need to interpret time-specific means with caution.
- Potential scale and standardization issues when unifying data from multiple sources and formats; careful attention needed for cross-context comparisons.

## References and supporting documents
- Emmett et al. (2008). Countryside Survey Technical Report No.03/07: Soils Manual.
- Emmett et al. (2010). CS Technical Report No. 9/07: Soils Report from 2007.
- Scott, W.A. (2008). CS Technical Report No.4/07: Statistical Report.
- Morton's Land Cover Map 2007 (1 km raster dominant Target Class, GB).
- Additional related publications and the British Geological Survey Soil Parent Material Model.