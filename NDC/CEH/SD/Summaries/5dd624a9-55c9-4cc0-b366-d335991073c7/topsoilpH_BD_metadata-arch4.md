# Topsoil pH and bulk density model estimates [Countryside Survey]

## Overview
- Represents topsoil properties for 0-15 cm depth in Great Britain.
- Based on 2614 cores from 591 1km x 1km squares, collected in 2007.
- Uses model-estimated means for habitat and parent material combinations, derived from Land Cover Map 2007 and a Soil/Parent Material Model.
- Some areas (e.g., urban and littoral rock) are not sampled and have no associated data.

## Data scope and sampling
- Sampling regime: 2614 plots within 591 1km x 1km squares (2007).
- Collection method: 15 cm long, 5 cm diameter cores following standard field protocol.
- Analytical targets: topsoil pH and bulk density.
- Fragmentation and coverage: some habitat/parent material combinations have insufficient sample sizes to estimate mean values.
- Data depth and context: estimates integrate habitat/parent material characteristics to model mean values.

## Modelling approach
- Mean values are modelled for selected habitat and parent material combinations.
- Dominant habitat characteristics derived from Land Cover Map 2007 (LCM2007).
- Dominant parent material characteristics derived from the BGS Soil Parent Material Model (PMM 2009); the parent material used is the one that minimises AIC in each model.
- Models built to support broader soil property interpretation, not just direct measurements.

## Data attributes and structure
- Core attributes include:
  - LCM_CLASS: Derived from Land Cover Map 2007 (habitat level).
  - LCM_NUMBER: Integer code from LCM2007 (1-23).
  - DOM_GRAIN: Dominant grain size from the Soil Parent Material Model.
  - SOIL_GROUP: Broad soil texture category (Heavy/Medium/Light) per PMM guidance.
  - CACO3_RANK: Carbonate content ranking (none, low, medium, high) per PMM.
  - PH_78, PH_98, PH_07: Mean soil pH values for 1978, 1998, and 2007 models by LCM_CLASS and CACO3_RANK.
  - PH_78SE, PH_98SE, PH_07SE: Standard errors for corresponding pH values.
  - BULKD_98, BULKD_07: Mean soil bulk density for 1998 and 2007 modeled by LCM_CLASS and DOM_GRAIN.
  - BULKD_98SE, BULKD_07SE: Standard errors for bulk density estimates.
- Spatial reference: OSGB 1936 / British National Grid (EPSG:27700).
- Data sources linked: Land Cover Map 2007; Soil Parent Material Model; related technical reports and datasets.

## Spatial reference and data sources
- Primary spatial framework: OSGB 1936 / British National Grid.
- Land cover linkage: Land Cover Map 2007 for dominant habitat coding.
- Soil context: British Geological Survey Soil Parent Material Model for dominant material characteristics.
- References for methodology and modelling: Emmett et al. (2008, 2010) for soils and sampling; Scott (2008) for statistical analysis; related technical reports and DB entries.

## Methods, calibration, and quality control
- Calibration and analytical steps detailed in Emmett et al. publications.
- pH measured using 10 g field-moist soil with 25 ml deionised water (1:2.5 lab ratio).
- Bulk density determined from detailed weight measurements during soil processing.
- Quality control aligned with Defra/NERC Joint Codes of Practice.

## Limitations and caveats
- Areas not sampled by Countryside Survey (e.g., urban, littoral rock) have no data.
- Some habitat/parent material combinations have insufficient sample size to estimate means.
- Model estimates depend on dominant habitat and dominant material characteristics, which may not capture all local variability.
- Data presented are model estimates for comparison and integration with broader soil datasets, not universal direct measurements for all sites.

## Access and references
- Key references: 
  - Emmett et al. 2008, 2010 (Soils manuals and reports).
  - Scott 2008 (Statistical report).
  - Morton et al. 2011 (Land Cover Map 2007 data paper).
  - Related CS technical reports and PMM documentation.
- Data provenance includes links to LCM2007 and PMM resources; further methodological details available in cited reports.