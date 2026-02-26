# Topsoil moisture model estimates [Countryside Survey]

## What this dataset is
- A dataset of topsoil moisture estimates for 0–15 cm depth across Great Britain.
- Based on 2614 soil moisture cores from 591 1 km × 1 km squares collected in 2007.
- Mean moisture values within selected habitat/parent material combinations estimated using a mixed-model approach from data in 1998 and 2007.
- Model inputs include dominant habitat and parent material characteristics derived from Land Cover Map 2007 and the Soil Parent Material Model (2009).

## Coverage and scale
- Spatial coverage: Great Britain (areas such as urban and littoral rock are not sampled).
- Spatial reference: OSGB 1936 / British National Grid (EPSG: 27700).
- Resolution: Model estimates at 1 km × 1 km grid units based on sampled plots.

## Variables and attributes
- Moisture estimates: MOIST98 (mean gravimetric moisture content for 1998), MOIST07 (mean gravimetric moisture content for 2007), with corresponding SEs (MOIST98_SE, MOIST07_SE).
- Habitat/land cover and soil context: 
  - LCM_CLASS: Land Cover Map 2007 broad habitat class.
  - LCM_NUMBER: Integer code for LCM class (1–23).
  - DOM_GRAIN: Dominant grain size from the BGS Soil Parent Material Model (qualitative).
  - SOIL_GROUP: General soil texture category (Heavy/Medium/Light).
  - CACO3_RANK: Calcite/dolomite/siderite carbonate content ranking (none, low, medium, high; with variable/unknown for some units).
- Other model inputs: Information derived from LCM2007 and the Soil Parent Material Model used to generate predictions (e.g., minerals and textures linked to moisture estimates).

## Methods and modelling
- Sampling design: Soils measured in 2614 plots across 591 main plots.
- Collection method: 15 cm long, 5 cm diameter soil cores following the Emmett et al. field protocol.
- Analytical approach: Initial gravimetric moisture content estimated from moisture loss; used to derive initial dry weight for moisture calculations.
- Modelling approach: Estimated mean moisture values for habitat/parent material combinations using a mixed-model framework; parent material characteristics selected to minimize AIC.
- Data provenance: Estimates built from 1998 and 2007 data; linkage to 2007 Land Cover Map and 2009 Soil Parent Material Model.

## Spatial reference and data format
- Coordinate system: OSGB 1936 / British National Grid (EPSG: 27700).
- Data attributes: Clearly defined codes and descriptions for LCM_CLASS, LCM_NUMBER, DOM_GRAIN, SOIL_GROUP, and CACO3_RANK; moisture values with associated standard errors.

## Data quality, limitations, and quality control
- Quality control and detailed processing steps described in Emmett et al. (2008, 2010); full QA procedures available in those references.
- Limitations:
  - Urban and littoral rock areas are not represented in the data.
  - Some habitat/parent material combinations have insufficient sample sizes to reliably estimate means.
  - Data availability is contingent on the sampled plots and derived model inputs; some metadata (e.g., metadata completeness) depends on the Land Cover Map and Soil Parent Material Model versions.

## Data provenance and references
- Core references and supporting documents include:
  - Emmett et al. 2008; 2010 CS Technical Reports: Soils Manual and Soils Report from 2007.
  - Scott 2008: CS Statistical Report.
  - Morton et al. 2011: Land Cover Map 2007 (GB) dataset.
  - BGS: Soil Parent Material Model.
  - Related microbial and soil studies cited for context.

## Practical implications for data strategy and use
- Provides a harmonized national-scale moisture sensitive dataset aligned with land cover and parent material context, useful for cross-domain analyses (ecology, agriculture, hydrology, climate impact).
- Useful for identifying data gaps and prioritizing data collection, particularly in under-sampled habitat/parent material combinations and in urban/littoral zones.
- Metadata-rich with clear variable definitions and provenance, supporting data discoverability, integration into broader data systems, and reproducible analyses.
- Can inform policy and planning needs by offering baseline soil moisture estimates tied to habitat and material characteristics.