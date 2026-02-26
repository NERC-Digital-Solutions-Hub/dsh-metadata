# Topsoil pH and bulk density model estimates [Countryside Survey]

## Overview
- Dataset provides modelled estimates of topsoil pH and bulk density (0-15 cm depth) for Great Britain, based on 2007 field data.
- Estimates are produced by linking soil measurements to habitat and parent material characteristics using a mixed-model approach.
- Includes uncertainty measures (standard errors) and is tied to land cover and parent material classifications.

## Data Coverage and Sampling
- 2614 soil cores collected in 2007 from Main Plots across 591 one-kilometre squares (GB).
- Mean values estimated within selected habitats and parent material characteristics across GB using data from 1978, 1998, and 2007.

## Modelling Approach and Data Derivation
- Habitat and parent material characteristics derived from:
  - Land Cover Map 2007 (LCM2007)
  - Parent Material Model 2009
- Dominant habitat/parent material characteristics used in models; the parent material characteristic that minimised AIC was selected per model.
- Areas such as urban and littoral rock are not sampled and have no data.
- Some habitat/parent material combinations had insufficient sample sizes to estimate means.

## Data Content and Attributes
- Key variables (derived from LCM2007 and the Soil Parent Material Model):
  - LCM_CLASS, Description (dominant land cover, e.g., Coniferous woodland)
  - LCM_NUMBER (integer code 1-23)
  - DOM_GRAIN (dominant grain size; qualitative)
  - SOIL_GROUP (soil texture descriptor: Heavy/Medium/Light)
  - CACO3_RANK (carbonate content: none/low/medium/high)
  - PH_78, PH_78SE (mean topsoil pH and SE for 1978)
  - PH_98, PH_98SE (mean topsoil pH and SE for 1998)
  - PH_07, PH_07SE (mean soil nitrogen concentration? model label; provided as pH-related in table context)
  - BULKD_98, BULKD_98SE (bulk density 1998 and SE)
  - BULKD_07, BULKD_07SE (bulk density 2007 and SE)

## Spatial Reference
- Coordinate System: OSGB 1936 / British National Grid (EPSG:27700)

## Collection Methods
- Soil pH and bulk density measured in samples from 2614 plots (Main Plots in 591 squares).
- Sampling method: 15 cm long by 5 cm diameter cores.
- Field protocol described in Emmett et al. (2008).

## Analytical Methods and Calibration
- Topsoil pH measured using 10 g field-moist soil with 25 ml deionised water (soil:water ratio 1:2.5 by weight).
- Bulk density estimated through detailed weight measurements during processing.
- Calibration and detailed methods documented in Emmett et al. (2008, 2010).

## Quality Control
- Followed Defra/NERC Joint Codes of Practice throughout.
- Full QA details available in Emmett et al. (2008, 2010).

## Experimental Design and Sampling Regime
- Soil pH and bulk density measured across 2614 plots in 2007, from Main Plots within 591 1km squares.

## Data Use and Limitations for GIS
- Suitable for map-based representations of soil pH and bulk density by habitat and dominant parent material characteristics.
- Notable limitations:
  - No data for urban and littoral rock areas.
  - Some habitat/parent material combinations lack sufficient samples.
  - Data are modelled estimates with associated standard errors (uncertainty).
  Data require integration with Land Cover Map 2007 and Soil Parent Material Model outputs; not all areas have high-resolution local data, and cleaning/transformation may be needed for complex datasets.

## References and Supporting Documents
- Emmett, B.A. et al. (2008). Countryside Survey Technical Report No.03/07: Soils Manual. CEH.
- Scott, W.A. (2008). CS Technical Report No.4/07: Statistical Report. CEH.
- Emmett, B.A. et al. (2010). CS Technical Report No. 9/07: Soils Report from 2007. CEH.
- Morton, R.D. et al. (2011). Land Cover Map 2007 (1km raster dominant Target Class, GB). NERC-EDC.
- Reynolds, B.A. et al. (2013). Vadose Zone Journal: Soil Change 1978-2007 for Topsoils in Great Britain. doi:10.2136/vzj2012.0114
- British Geological Survey. Soil Parent Material Model.