# Topsoil moisture model estimates [Countryside Survey]

## Overview
- Dataset provides topsoil moisture estimates for 0–15 cm depth across Great Britain.
- Based on 2614 soil moisture cores from 591 1 km × 1 km squares collected in 2007.
- Uses a mixed-model approach to estimate mean moisture for habitat × parent material combinations, integrating 1998 and 2007 data.
- Model inputs derive dominant habitat and parent material characteristics from Land Cover Map 2007 and the 2009 Parent Material Model.

## Data scope and limitations
- Estimates are available for dominant habitat and parent material combinations; urban and littoral rock areas are not sampled and have no data.
- Some habitat/parent material combinations had insufficient samples to estimate means.
- Outputs are model-based estimates with associated standard errors (MOIST98_SE, MOIST07_SE).

## Data attributes and structure
- Spatial reference: OSGB 1936 / British National Grid (EPSG:27700)
- Key attributes:
  - LCM_CLASS: Derived from Land Cover Map 2007; describes broad habitat class.
  - LCM_NUMBER: Integer code (1–23) corresponding to LCM_CLASS.
  - DOM_GRAIN: Qualitative dominant grain size from the BGS Soil Parent Material Model.
  - SOIL_GROUP: General soil texture category (Heavy, Medium, Light).
  - CACO3_RANK: Carbonate content class (none, low, medium, high).
  - MOIST98: Mean gravimetric moisture content modeled for 1998 (percentage).
  - MOIST98_SE: Standard error for MOIST98.
  - MOIST07: Mean gravimetric moisture content modeled for 2007 (percentage).
  - MOIST07_SE: Standard error for MOIST07.

## Sampling design and collection
- Soil moisture measured from 2614 plots in 2007, drawn from the Main Plots within 591 1 km squares.
- Collection method used a 15 cm long by 5 cm diameter black plastic core following a standardized field protocol.

## Analytical methods and quality control
- Initial gravimetric moisture content estimated from moisture loss during processing; subsequently used to compute initial dry weight.
- Detailed quality control procedures described in Emmett et al. (2008, 2010).

## Related documentation and references
- Emmett et al. (2008, 2010): CS Technical Report No. 03/07 (Soils Manual) and No. 9/07 (Soils Report from 2007)
- Scott (2008): CS Technical Report No. 4/07 (Statistical Report)
- Griffiths et al. (2011): The bacterial biogeography of British soils
- Morton et al. (2011): Land Cover Map 2007 (1 km raster dominant Target Class, GB)
- British Geological Survey: Soil Parent Material Model

## Usage considerations
- The dataset enables estimation of mean soil moisture by habitat and parent material across GB, suitable for regional analyses and cross-habitat comparisons.
- Users should note the absence of data for urban and littoral rock areas and potential gaps due to small sample sizes in certain habitat/parent material combinations.
- Model-based nature implies reliance on the 1998 and 2007 inputs and the Land Cover / Parent Material models for interpretation.