# Topsoil nutrient model estimates [Countryside Survey]

## Overview
- Provides model estimates of topsoil nutrient status (0–15 cm depth) across Great Britain from the Countryside Survey.
- Variables: total nitrogen concentration (N, %), C:N ratio, and Olsen-P (mg/kg).
- Based on 2007 data, with supporting data from 1998; representative across 256 1km × 1km squares.
- Uses mixed-model estimates for habitat and parent material combinations derived from Land Cover Map 2007 (LCM2007) and a Soil Parent Material Model (2009); Dominant grain (DOM_GRAIN) used as the parent material characteristic.
- Some areas are not sampled (urban and littoral rock) and some habitat/parent material combinations have insufficient samples to estimate means.

## Data content and structure
- Data attributes include:
  - Totals and year-specific values with standard errors: TOTN_07, TOTN_07SE; CN_07, CN_07SE; OLSEN_07, OLSEN_07SE.
  - Historical values for 1998: NCONC_98, NCONC_98SE; CN_98, CN_98SE; OLSEN_98, OLSEN_98SE.
  - Habitat and material descriptors: LCM_CLASS, LCM_NUMBER, DOM_GRAIN, SOIL_GROUP, CACO3_RANK.
  - Sample and model context: numerous model-derived mean values by habitat/DOM_GRAIN combination; sample sizes noted (e.g., 1024 plots for TOTN in 2007, 1110 plots in 1998 for TOTN; 1068 plots for Olsen-P in 2007).
- Spatial reference: OSGB 1936 / British National Grid (EPSG:27700).
- Collection domain: 256 main squares; data collected from core samples using standardized field and lab methods.

## Methods and provenance
- Sampling design: total N measured in 1024 plots (2007) and 1110 plots (1998); Olsen-P measured in 1068 plots (2007); 75% of 1998 plots overlap with 2007.
- Field collection: 15 cm long, 5 cm diameter cores following Emmett et al. protocols.
- Laboratory analyses:
  - Total N: CEH Lancaster UKAS-accredited method SOP3102 (elemental analyzer) on air-dried, sieved samples (<2 mm).
  - Olsen-P: extraction with 0.5 M NaHCO3 (pH 8.5), colorimetric determination via molybdenum blue on a continuous flow analyser with dialysis step.
- Calibration and quality control: described in Emmett et al. (2008, 2010); Defra/NERC Joint Codes of Practice followed.

## Data quality, limitations, and governance
- Strength: well-documented metadata, standardized units and codes, and traceable methodology linking field sampling, lab analysis, and modeling.
- Limitations:
  - Urban and littoral rock areas are not sampled; no associated data for these areas.
  - Some habitat/parent material combinations have insufficient samples to estimate means.
  - Model-based estimates reflect dominant habitat and dominant grain characteristics, which may not capture fine-grained variability.
- Data lineage and references: Emmett et al. (2008, 2010) soils reports; Scott (2008) statistical report; Morton et al. (2011) Land Cover Map 2007; Countryside Survey data and related technical reports.

## Relevance and implications for data strategy
- Demonstrates integration of field measurements, historical data, and model-based estimates to produce spatially extensive soil nutrient indicators.
- Emphasizes the importance of linking soil data with land cover and parent material models to enable landscape-scale analyses.
- Highlights need for clear metadata on sampling design, data gaps, and limitations to support responsible use and interpretation.
- Supports data discoverability and interoperability through standardized attributes, units, and spatial reference systems, facilitating reuse across networks and partner initiatives.