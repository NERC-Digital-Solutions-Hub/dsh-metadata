# Topsoil pH and bulk density model estimates [Countryside Survey]

- Overview
  - British dataset representing topsoil (0–15 cm) across Great Britain.
  - Based on 2614 cores from 591 1km × 1km squares collected in 2007.
  - Estimates mean values within habitat/parent material combinations using mixed-models; linked to Land Cover Map 2007 and a Soil Parent Material Model (2009).
  - Some areas (urban, littoral rock) are not sampled and some habitat/parent material combinations lack sufficient data.

- Data collection and sampling
  - Soil pH and bulk density measured in 2614 plots in 2007 (Main Plots within 591 squares).
  - Sampling used a 15 cm long, 5 cm diameter core following the Emmett et al. field protocol.

- Modelling approach and variables
  - Means modelled for habitat × parent material combinations.
  - pH modeled using dominant grain characteristic from the parent material (CACO3_RANK).
  - Bulk density modeled using dominant grain size (DOM_GRAIN).
  - Model selection for parent material characteristics based on minimizing AIC (see Table 1).

- Spatial and data attributes
  - Spatial reference: OSGB 1936/British National Grid (EPSG:27700).
  - Key data attributes include: LCM_CLASS, LCM_NUMBER, DOM_GRAIN, SOIL_GROUP, CACO3_RANK; pH values for 1978, 1998, 2007 (PH_78, PH_98, PH_07) with corresponding standard errors; bulk density values for 1998 and 2007 (BULKD_98, BULKD_07) with standard errors.

- Experimental design and sampling regime
  - Samples collected from 2614 plots in 2007, using the 591 main plots within 1km squares.

- Collection methods and calibration
  - pH measured with 10 g field-moist soil and 25 ml deionised water (ratio 1:2.5 by weight).
  - Bulk density estimated via detailed weight measurements throughout processing.
  - Calibration and detailed methodology described in Emmett et al. (2008, 2010).

- Analytical methods and quality control
  - Analyses and processing follow Defra/NERC Joint Codes of Practice.
  - Supporting methodological details provided in CS Technical Reports (Emmett et al. 2008/2010).

- Data provenance and supporting references
  - Countryside Survey technical reports:
    - Soils Manual (Emmett et al. 2008)
    - Statistical Report (Scott 2008)
    - Soils Report from 2007 (Emmett et al. 2010)
  - Land Cover Map 2007 (Morton et al., 2011)
  - Soil Parent Material Model (British Geological Survey)
  - Related CS outputs on Soil Change (Vadose Zone Journal, 2013)

- Considerations for use
  - Model estimates depend on dominant habitat/parent material characteristics; direct measurements are not available for all combinations.
  - Areas with urban or littoral rock are not represented in the dataset.