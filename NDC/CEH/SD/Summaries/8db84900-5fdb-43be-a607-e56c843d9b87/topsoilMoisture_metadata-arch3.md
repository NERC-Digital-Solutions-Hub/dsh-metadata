# Topsoil moisture model estimates [Countryside Survey]

## Overview
- Provides topsoil moisture data representative of 0 – 15 cm depth for Great Britain, based on a 2007 survey.
- Data include 2614 soil cores from 591 1 km x 1 km squares, used to generate mean moisture estimates across habitat and parent material types.
- Mean values are modelled using habitat and parent material characteristics derived from existing land cover and soil models.

## Data sources and modelling approach
- Means of habitat/parent material combinations are modelled using a mixed model approach.
- Habitat and parent material characteristics are derived from Land Cover Map 2007 (LCM2007) and the British Geological Survey Parent Material Model (2009), selecting parent material characteristics that minimised AIC in each model.
- Some areas (e.g., urban and littoral rock) are not sampled and have no data.

## Data attributes and variables
- LCM_CLASS: Broad habitat land cover code derived from LCM2007.
- LCM_NUMBER: Integer code (1–23) for the corresponding habitat class.
- DOM_GRAIN: Dominant grain size classification from the soil parent material model.
- SOIL_GROUP: General soil texture description (Heavy/Medium/Light).
- CACO3_RANK: Carbonate content ranking (none/low/medium/high, with variability for some units).
- MOIST98: Mean gravimetric moisture content for 1998 modelled by CACO3_RANK and DOM_GRAIN.
- MOIST98_SE: Standard error for MOIST98.
- MOIST07: Mean gravimetric moisture content for 2007 modelled by CACO3_RANK and DOM_GRAIN.
- MOIST07_SE: Standard error for MOIST07.
- The spatial reference is OSGB 1936 / British National Grid (EPSG:27700).

## Experimental design and collection methods
- Sampling conducted in 2007: 2614 plots collected from Main Plots within 591 1 km x 1 km squares.
- Soil moisture measured using a 15 cm long by 5 cm diameter core, following the field protocol described in Emmett et al. (2008).

## Analytical methods and quality control
- Initial gravimetric moisture content estimated from moisture loss during soil processing, enabling calculation of initial dry weight.
- Quality control details are provided in related emissions (Emmett et al. 2008; 2010).

## Gaps, limitations, and data governance
- Not all habitat/parent material combinations have sufficient sample sizes to estimate mean moisture values.
- Areas such as urban and littoral rock are not sampled and thus lack data for those contexts.
- Some metadata and data transformation steps may be required for reuse, as indicated by the reliance on model-derived estimates and associated supporting documents.

## References / Supporting documents
- Emmett, B.A. et al. (2008). Countryside Survey Technical Report No.03/07: Soils Manual. CEH.
- Emmett, B.A. et al. (2010). CS Technical Report No. 9/07: Soils Report from 2007. CEH.
- Scott, W.A. (2008). CS Technical Report No.4/07: Statistical Report. CEH.
- Griffiths, R.I. et al. (2011). The bacterial biogeography of British soils. Environmental Microbiology.
- Morton, R.D. et al. (2011). Land Cover Map 2007 (1 km raster dominant Target Class, GB). NERC-EDI.