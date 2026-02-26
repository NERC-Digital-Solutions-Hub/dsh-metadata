# Topsoil pH and bulk density model estimates [Countryside Survey]

## Overview
- Topsoil pH and bulk density data pertain to 0-15 cm soil depth.
- 2614 cores from 591 1km x 1km squares across Great Britain were collected and analysed in 2007 (see Emmett et al. 2010 for details).
- Mean values for habitat and parent material characteristics across GB were estimated using data from 1978, 1998, and 2007 with a mixed-model approach (Scott 2008).
- Habitat/parent material means are modelled using dominant habitat and parent material characteristics derived from Land Cover Map 2007 (LCM2007) and the British Geological Survey’s Parent Material Model 2009; the parent material characteristic used is the one that minimises AIC in each model (Table 1).
- Areas such as urban and littoral rock are not sampled by Countryside Survey and have no associated data; some habitat/parent material combinations had insufficient sample sizes to estimate means.

## Data scope and variables
- Spatial reference: OSGB 1936 / British National Grid (EPSG:27700).
- Data attributes include:
  - LCM_CLASS, LCM_NUMBER (derived from LCM2007)
  - DOM_GRAIN (dominant grain size from the Soil Parent Material Model)
  - SOIL_GROUP (soil texture description: Heavy, Medium, or Light)
  - CACO3_RANK (carbonate content ranking from the Soil Parent Material Model)
  - PH_78, PH_78SE (mean pH and SE for 1978)
  - PH_98, PH_98SE (mean pH and SE for 1998)
  - PH_07, PH_07SE (mean pH and SE for 2007)
  - BULKD_98, BULKD_98SE (bulk density mean and SE for 1998)
  - BULKD_07, BULKD_07SE (bulk density mean and SE for 2007)

## Experimental design and sampling
- Soil pH and bulk density measured in 2614 plots in 2007.
- Plots are Main Plots within 591 1km x 1km squares.

## Collection methods
- Samples collected using a 15 cm long by 5 cm diameter black plastic core following the field protocol described in Emmett et al. (2008).

## Analytical methods
- Topsoil pH measured with 10 g of field-moist soil and 25 ml de-ionised water (soil:water ratio 1:2.5 by weight).
- Bulk density estimated through detailed weight measurements during sample processing.
- See Emmett et al. (2008, 2010) for full methodology.

## Quality control
- Methods and analyses followed the Defra/NERC Joint Codes of Practice.
- See Emmett et al. (2008, 2010) for additional quality control details.

## Notes on limitations and usage
- Urban and littoral rock areas are not represented in the data.
- Some habitat/parent material combinations have insufficient sample sizes to reliably estimate means.
- Data are suitable for exploring GB-wide soil pH and bulk density patterns by habitat and dominant parent material characteristics, with associated standard errors, using the modeled estimates across 1978, 1998, and 2007 time points.

## References / supporting documents
- Emmett, B.A. et al. (2008). Countryside Survey Technical Report No.03/07: Soils Manual. CEH.
- Emmett, B.A. et al. (2010). CS Technical Report No. 9/07: Soils Report from 2007. CEH.
- Scott, W.A. (2008). CS Technical Report No.4/07: Statistical Report. CEH.
- Morton, R.D. et al. (2011). Land Cover Map 2007 (1km raster dominant Target Class, GB). NERC-EDI.
- Countryside Survey references to Soil Parent Material Model and related datasets.