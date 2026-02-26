# Topsoil moisture model estimates [Countryside Survey]

- Overview
  - Represents topsoil moisture for 0–15 cm depth.
  - Based on 2007 data: 2614 cores from 591 1km × 1km squares across Great Britain.
  - Means estimated for habitat/parent material combinations using data from 1998 and 2007 via mixed-model approaches.

- Data and coverage
  - Spatial reference: OSGB 1936 / British National Grid (EPSG:27700).
  - Habitat and parent material characteristics derived from Land Cover Map 2007 (LCM2007) and Parent Material Model 2009.
  - Urban and littoral rock areas are not sampled and have no data.
  - Some habitat/parent material combinations lack sufficient sample sizes for reliable means.

- Model approach
  - Estimates are modelled on dominant habitat characteristics and dominant parent material characteristics.
  - Parent material characteristics chosen to minimize AIC in each model.
  - Moisture variables tied to parent material characteristics: Calcium carbonate content (CACO3_RANK) and dominant grain size (DOM_GRAIN).

- Data attributes
  - LCM_CLASS: Derived from Land Cover Map 2007 (habitat level).
  - LCM_NUMBER: Integer code (1–23) from LCM2007.
  - DOM_GRAIN: Dominant grain size classification (from PMM).
  - SOIL_GROUP: General soil texture category (Heavy/Medium/Light).
  - CACO3_RANK: Carbonate content ranking (none/low/medium/high).
  - MOIST98: Mean gravimetric moisture content in 1998 (modelled by CACO3_RANK & DOM_GRAIN).
  - MOIST98_SE: Standard error for MOIST98.
  - MOIST07: Mean gravimetric moisture content in 2007 (modelled by CACO3_RANK & DOM_GRAIN).
  - MOIST07_SE: Standard error for MOIST07.

- Experimental design / collection
  - Soil moisture measured in 2614 plots in 2007, drawn from main plots in 591 1km squares.
  - Collection used a 15 cm long by 5 cm diameter black plastic core.

- Analytical methods
  - Moisture loss at processing stages used to estimate initial gravimetric moisture content and initial dry weight.

- Quality control and references
  - Quality control details provided in Emmett et al. (2008, 2010) CS technical reports.
  - Key supporting documents include Land Cover Map 2007 (1 km raster dominant Target Class) and the British Geological Survey Soil PMM.
  - Notable references: Emmett et al. 2008/2010; Scott 2008; Griffiths et al. 2011.