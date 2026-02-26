# Topsoil moisture model estimates [Countryside Survey]

## Overview
- Represents mean soil moisture for topsoil (0–15 cm) using data from 2614 cores across 591 one-kilometre square sites in Great Britain, collected in 2007.
- Sampling and methods are detailed in Emmett et al. (2008, 2010) and related technical reports.

## Modelling approach
- Means of habitat–parent material combinations estimated using a mixed-model approach, with habitat defined by the dominant land cover and parent material characteristics from the Land Cover Map 2007 and the British Geological Survey Parent Material Model 2009.
- Model selection uses the parent material characteristics CACO3_RANK (calcium carbonate content) and DOM_GRAIN (dominant grain size) to minimise AIC.
- Some areas are not sampled (e.g., urban and littoral rock) and certain habitat/parent material combinations have insufficient sample sizes to estimate means.

## Data attributes and variables
- LCM_CLASS and LCM_NUMBER: derived from Land Cover Map 2007; describe dominant habitat class.
- DOM_GRAIN: qualitative dominant grain size from PMM.
- SOIL_GROUP: general soil texture from PMM.
- CACO3_RANK: carbonate content classification from PMM (none/low/medium/high).
- MOIST98, MOIST07: mean gravimetric moisture content modeled for 1998 and 2007, respectively.
- MOIST98_SE, MOIST07_SE: standard errors for the 1998 and 2007 moisture estimates.
- Spatial reference: OSGB 1936 / British National Grid (EPSG:27700).

## Spatial reference
- Coordinate System: OSGB 1936 / British National Grid (EPSG: 27700).

## Sampling design and collection
- Soil moisture measured in 2614 plots located within 591 Main Plots across 1 km squares.
- Sampling method: 15 cm long by 5 cm diameter black plastic cores, following the field protocol described in Emmett et al. (2008).

## Analytical methods
- Moisture loss during sample processing used to estimate the initial gravimetric moisture content and the initial dry weight of the soil.

## Quality control
- Detailed quality control procedures are described in Emmett et al. (2008, 2010).

## References / Supporting documents
- Emmett, B.A. et al. (2008). Countryside Survey Technical Report No. 03/07: Soils Manual. CEH.
- Emmett, B.A. et al. (2010). CS Technical Report No. 9/07: Soils Report from 2007. CEH.
- Scott, W.A. (2008). CS Technical Report No. 4/07: Statistical Report. CEH.
- Griffiths, R.I. et al. (2011). The bacterial biogeography of British soils. Environmental Microbiology.
- Morton, R.D. et al. (2011). Land Cover Map 2007 (1 km raster dominant Target Class, GB). NERC Data Centre.
- British Geological Survey. Soil Parent Material Model.