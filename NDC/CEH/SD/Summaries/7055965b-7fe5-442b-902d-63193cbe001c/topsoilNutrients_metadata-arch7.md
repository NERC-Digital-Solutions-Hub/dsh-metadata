# Topsoil nutrient model estimates [Countryside Survey] Topsoil nutrient data - total nitrogen (N) concentration (%), C:N ratio and Olsen-Phosphorus (mg/kg). Data is representative of 0 - 15 cm soil depth.

## Overview
- Provides modelled mean values of soil nutrients (total N concentration, C:N ratio, Olsen-Phosphorus) for GB soils at 0-15 cm depth.
- Based on Countryside Survey data from 1998 and 2007; 256 1km x 1km squares across Great Britain.
- N concentration: 1024 cores (2007); Olsen-P: 1054 cores (2007). 75% of 2007 plots also sampled in 1998; 65% of Olsen-P plots overlap with 1998.

## Spatial coverage and reference
- Spatial reference: OSGB 1936 / British National Grid (EPSG:27700).
- Grid: 1 km x 1 km squares across GB; urban and littoral rock areas are not sampled (no data there).

## Model approach and scope
- Estimation: mean values within habitat/parent material combinations using a mixed-model approach.
- Habitat classification: Dominant habitat derived from Land Cover Map 2007 (LCM2007).
- Parent material: Dominant grain (DOM_GRAIN) derived from the BGS Soil Parent Material Model; the parent material characteristic selected to minimise AIC in each model.
- Limitations: some habitat/parent material combinations have insufficient sample sizes; areas with no sampling data are not modeled.

## Data attributes and units
- Spatial attribute: LCM_CLASS, LCM_NUMBER (derived from LCM2007).
- Parent material attributes: DOM_GRAIN; SOIL_GROUP; CACO3_RANK.
- Nutrient variables (2007 and 1998 modelled means) with standard errors:
  - N concentration: NCONC_98, NCONC_98SE, NCONC_07, TOTN_07SE.
  - C:N ratio: CN_98, CN_98SE, CN_07, CN_07SE.
  - Olsen-Phosphorus: OLSEN_98, OLSEN_98SE, OLSEN_07, OLSEN_07SE.
- Units: total N concentration (%) and Olsen-P (mg/kg); C:N ratio (dimensionless); standard errors provided for each estimate.

## Data collection, methods, and QA
- Sampling: soil cores 15 cm long, 5 cm diameter; collected following Emmett et al. field protocol.
- Analyses:
  - Total N: elemental analyser (CEH Lancaster, UKAS SOP3102).
  - Olsen-P: extraction with 0.5 M NaHCO3, colorimetric molybdenum blue method with dialysis; measured at 880 nm.
- Quality Control: Defra/NERC Joint Codes of Practice followed; additional details in Emmett et al. 2008, 2010; SOPs and QA documented in supporting reports.

## Usage notes and references
- Data derived from Countryside Survey and linked to Land Cover Map 2007 and Soil Parent Material Model 2009.
- Key references: Emmett et al. 2008; Emmett et al. 2010; Scott 2008; Morton et al. 2011 (LCM2007 raster product).
- For full methodological details, consult the cited technical reports and the Countryside Survey datasets.