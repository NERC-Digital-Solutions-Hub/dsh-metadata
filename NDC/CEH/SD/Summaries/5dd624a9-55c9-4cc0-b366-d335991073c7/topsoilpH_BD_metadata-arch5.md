# Topsoil pH and bulk density model estimates [Countryside Survey]

## Overview
- Represents topsoil (0-15 cm) pH and bulk density data for Great Britain.
- Based on 2614 soil cores from 591 1km x 1km squares collected in 2007; sampling and methods detailed in Emmett et al. (2008, 2010).
- Means within habitat and parent material combinations are modelled across GB using data from 1978, 1998, and 2007 with a mixed-model approach (see Scott 2008 for related methods).
- Model estimates are linked to dominant habitat and parent material characteristics from Land Cover Map 2007 and the 2009 Parent Material Model.
- Some areas have no data (e.g., urban and littoral rock) and some habitat/parent material combinations have insufficient sample sizes.

## Data scope and content
- Variables modelled: pH and bulk density with habitat/parent material context.
- Model inputs include: Land Cover Map 2007 class (LCM_CLASS, LCM_NUMBER), Dominant grain (DOM_GRAIN), and carbonate content ranking (CACO3_RANK).
- Derived data attributes (as in Table 1): 
  - LCM_CLASS, LCM_NUMBER: Land Cover Map 2007 classification
  - DOM_GRAIN: Dominant grain in soil material
  - SOIL_GROUP: Texture category (Heavy/Medium/Light)
  - CACO3_RANK: Carbonate content ranking (none/low/medium/high)
  - PH_78, PH_78SE: Mean soil pH and standard error for 1978 model
  - PH_98, PH_98SE: Mean soil pH and standard error for 1998 model
  - PH_07, PH_07SE: Mean soil pH and standard error for 2007 model
  - BULKD_98, BULKD_98SE: Mean bulk density and standard error for 1998 model
  - BULKD_07, BULKD_07SE: Mean bulk density and standard error for 2007 model
- Spatial reference: OSGB 1936 / British National Grid (EPSG:27700)

## Data attributes and metadata
- Each record includes dominant habitat/parent material context and derived soil properties.
- Data attributes are derived from the BGS Soil Parent Material Model and the Land Cover Map 2007.
- The dataset provides model-based estimates with associated standard errors to indicate uncertainty (e.g., PH_78SE, PH_98SE, PH_07SE; BULKD_98SE, BULKD_07SE).

## Spatial reference
- Coordinate system: OSGB 1936 / British National Grid (EPSG: 27700).

## Experimental design and collection methods
- Field sampling in 2007 across 591 main plots within 1km x 1km squares; 2614 plots total sampled for pH and bulk density.
- Sampling apparatus: 15 cm long, 5 cm diameter black plastic cores.
- See Emmett et al. (2008, 2010) for full sampling protocol and calibration details.

## Data processing, calibration and quality control
- Topsoil pH: measured using 10 g of field-moist soil with 25 ml deionised water (soil:water ratio 1:2.5 by weight).
- Bulk density: determined via detailed weight measurements throughout the soil processing procedure.
- Calibration and processing steps aligned with the Defra/NERC Joint Codes of Practice.
- Quality control and methodological details documented in Emmett et al. (2008, 2010).

## Limitations and caveats
- Urban and littoral rock areas are not sampled and have no corresponding data.
- Some habitat/parent material combinations have insufficient sample sizes to robustly estimate mean values.
- Model-based estimates rely on dominant habitat and parent material characteristics; uncertainties are reflected in standard error fields (SE).

## References and supporting documents
- Emmett, B.A. et al. (2008). Countryside Survey Technical Report No.03/07: Soils Manual. CEH.
- Scott, W.A. (2008). CS Technical Report No.4/07: Statistical Report. CEH.
- Emmett, B.A. et al. (2010). CS Technical Report No. 9/07: Soils Report from 2007. CEH.
- Morton, R.D. et al. (2011). Land Cover Map 2007 (1km raster dominant Target Class, GB). NERC-EDI.
- Reynolds, B.A. et al. (2013). Vadose Zone Journal article on Soil Change 1978-2007 for GB topsoils. doi:10.2136/vzj2012.0114
- British Geological Survey (Soil Parent Material Model).