# Topsoil nutrient model estimates [Countryside Survey]

## Overview
- Dataset of topsoil nutrients (0–15 cm): total nitrogen concentration (%), C:N ratio, and Olsen-Phosphorus (mg/kg) across Great Britain.
- Primary measurements from 256 1km × 1km squares in 2007; 1024 plots for total N, 1054 plots for Olsen-P.
- Additional modeled means for habitat/parent material combinations using Land Cover Map 2007 and Soil Parent Material Model 2009, with dominant habitat/parent material characteristics.
- Data scope excludes areas not sampled by Countryside Survey (e.g., urban and littoral rock).

## Data content and structure
- Attributes include:
  - LCM_CLASS, LCM_NUMBER (Land Cover Map 2007 class codes)
  - DOM_GRAIN (dominant grain size of parent material)
  - SOIL_GROUP, CACO3_RANK (soil texture and carbonate content)
  - NCONC_98, NCONC_07; CN_98, CN_07; OLSEN_98, OLSEN_07 (means by year)
  - TOTN_07, TOTN_07SE; CN_07SE; OLSEN_07SE (standard errors)
- Model estimates are built by combining habitat class (LCM) and dominant grain (DOM_GRAIN) using selection based on AIC.
- Spatial reference: OSGB 1936 / British National Grid (EPSG:27700).

## Methods and provenance
- Experimental design: 256 main plots (1km × 1km squares); 1024 total plots for N, 1068 for Olsen-P (1998/2007 data with overlap).
- Collection method: soil cores (15 cm length, 5 cm diameter) following standard field protocol.
- Analytical methods:
  - Total N via CEH Lancaster UKAS SOP3102 elemental analyser.
  - Olsen-P via 5 g soil extraction with 0.5M NaHCO3; colorimetric molybdenum blue detection (880 nm) with dialysis step.
- Calibration and QA: Defra/NERC Joint Codes of Practice followed; detailed calibration/QA described in Emmett et al. (2008, 2010) and related reports.

## Spatial scope and coverage
- Coverage derived from Countryside Survey data, with data modeled across habitat × DOM_GRAIN.
- Urban and littoral rock areas are not sampled; no data available for these areas.

## Data quality and limitations
- Some habitat/parent material combinations have insufficient sample sizes to estimate mean values.
- Data patchiness and the need to integrate across multiple formats/systems may affect direct comparability.
- Model reliance on dominant grain and habitat classification may simplify complex parent material characteristics.

## Usage and potential applications
- Enables self-serve insights into soil nutrient status across GB and across habitat/parent material categories.
- Facilitates regional comparisons, trend assessment (1988–2007 data points), and policy-relevant soil health interpretation.
- Supports integration with other Countryside Survey outputs and Land Cover data for broader environmental analyses.

## Access and references
- Primary sources and supporting documents available via Countryside Survey publications and the NERC Environmental Information Data Centre.
- Key references: Emmett et al. (2008, 2010) soil manuals and reports; Scott (2008) statistical report; related Land Cover Map 2007 dataset.