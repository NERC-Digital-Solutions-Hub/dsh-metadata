# Topsoil invertebrate model estimates [Countryside Survey]

- A dataset describing modeled topsoil invertebrate metrics (0–8 cm depth) across Great Britain, based on Countryside Survey data.
- Core measurements: 947 soil cores from 256 1km x 1km squares, collected in 2007; supporting data from 1978 and 1998 for modelling.
- Outputs are mean values for habitat and parent material combinations, derived from dominant habitat and dominant parent material characteristics.

## Data scope, design, and modelling

- Objective: produce habitat/parent material group estimates (Total Catch, Mite:Springtail ratio, Number of broad taxa, Shannon diversity) across GB.
- Modelling approach: mixed models using:
  - Dominant habitat from Land Cover Map 2007 (LCM2007)
  - Dominant parent material from the British Geological Survey Parent Material Model (2009)
- Parent material characteristic chosen per model to minimize AIC.
- Limitations:
  - Urban and littoral rock areas are not sampled and have no data.
  - Some habitat/parent material combinations have insufficient data to estimate means.
- Output years: model estimates for 1998 and 2007 (and references to 1978 data for modelling context).

## Data attributes and variables

- Core dataset attributes:
  - LCM_CLASS and LCM_NUMBER: derived from Land Cover Map 2007; broad habitat classification.
  - DOM_GRAIN: dominant grain size from the parent material model.
  - SOIL_GROUP: general soil texture category (Heavy/Medium/Light).
  - CACO3_RANK: carbonate content classification of parent material.
- Modelled summary variables (mean values and standard errors):
  - CATCH_98 and CATCH_07; CATCH_98SE and CATCH_07SE: mean total invertebrate catch (per core) for 1998 and 2007.
  - TAXA_98 and TAXA_07; TAXA_98SE and TAXA_07SE: mean number of broad taxa for 1998 and 2007.
  - RATIO_98 and RATIO_07; RATIO_98SE and RATIO_07SE: mean mite:springtail ratio for 1998 and 2007.
  - SHAN_98 and SHAN_07; SHAN_98SE and SHAN_07SE: mean Shannon diversity index for 1998 and 2007.
- Data are spatially referenced and model-derived, not raw counts for all grid cells.

## Spatial reference

- Coordinate System: OSGB 1936 / British National Grid (EPSG: 27700).

## Methods: collection, analysis, and quality control

- Collection:
  - Sampling with 4 cm diameter by 8 cm long cores; surface vegetation removed; litter left in place.
  - Cores pushed into ground and later processed; intact cores mailed to lab.
  - Soil invertebrates extracted using a dry Tullgren method.
- Analytical methods:
  - Identification to major taxa (taxonomic level 1) with broad taxa categories enumerated (comprehensive list provided).
- Quality control:
  - Regular reassembly, re-identification, and counting by a second staff member.
  - Cross-checks to identify and resolve counting discrepancies; changes documented on record sheets.
  
## Data usage notes and caveats

- Areas not sampled (e.g., urban, littoral rock) have no associated data.
- Some habitat/parent material combinations had insufficient sample sizes to estimate means.
- Outputs represent modeled estimates rather than direct observations for all GB areas.

## References and supporting documents

- Emmett et al. 2008, 2010; Countryside Survey Technical Reports (Soils Manual, Statistical Report, Soils Report from 2007).
- Morton et al. 2011: Land Cover Map 2007 dataset.
- British Geological Survey: Soil Parent Material Model documentation.