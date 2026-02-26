# Topsoil invertebrate model estimates [Countryside Survey]

## Overview
- Reports model-based estimates of topsoil invertebrates (0–8 cm) from the Countryside Survey (CS).
- Data derived from 947 soil cores across 256 1 km × 1 km squares in Great Britain, collected in 2007.
- Aims to estimate mean values for habitat/parent material combinations using data from 1978, 1998, and 2007 via mixed-model approaches.

## Data scope and sampling
- Spatial scope: Great Britain; areas such as urban and littoral rock are not sampled and have no data.
- Temporal scope: primary data from 2007; uses historical CS data (1978, 1998) for modelled means.
- Some habitat/parent material combinations have insufficient sample sizes to estimate means.

## Model and variables
- Dependent variables: total catch, mite:springtail ratio, number of broad taxa, Shannon diversity index.
- Predictor/structural variables: dominant land cover (LCM_CLASS) and dominant grain/soil properties (DOM_GRAIN, SOIL_GROUP) derived from Land Cover Map 2007 and Soil Parent Material Model 2009.
- Model selection based on minimizing AIC for each combination; areas without appropriate predictors excluded.
- Data are modelled means (not raw counts) by specified habitat/parent material classes.

## Data attributes
- Core fields include:
  - LCM_CLASS (derived from LCM2007)
  - DOM_GRAIN (dominant grain size)
  - SOIL_GROUP (soil texture category)
  - CATCH_98, CATCH_07 (mean total invertebrate catch for 1998 and 2007)
  - CATCH_98SE, CATCH_07SE (standard errors)
  - TAXA_98, TAXA_07 (mean number of broad taxa)
  - TAXA_98SE, TAXA_07SE (standard errors)
  - RATIO_98, RATIO_07 (mites to springtails ratio)
  - RATIO_98SE, RATIO_07SE (standard errors)
  - SHAN_98, SHAN_07 (Shannon diversity index)
  - SHAN_98SE, SHAN_07SE (standard errors)
  - CACO3_RANK (carbonate content ranking)
- Spatial reference: OSGB 1936/British National Grid (EPSG:27700).

## Collection and analytical methods
- Sampling: 4 cm diameter by 8 cm long cores; surface vegetation removed; litter layer not removed.
- Extraction: dry Tullgren extraction to obtain soil invertebrates.
- Identification: organisms identified to major taxa (broad taxa level 1); extensive taxa list provided.
- Quality control: duplicate identifications by a second technician; cross-checks to resolve discrepancies; recording of any changes.

## Practical considerations for analysts
- Data are presented as model-estimated means with associated standard errors, enabling habitat-material comparisons and predictive insights at the 1 km × 1 km scale.
- Useful for linking invertebrate metrics to habitat and soil characteristics, with explicit caveats about missing data in certain areas and potential uncertainties from model-based estimates.
- Underpinning sources include CS Technical Reports (Emmett et al.) and Land Cover Map 2007 data; recommended to consult original references for full methodological details.