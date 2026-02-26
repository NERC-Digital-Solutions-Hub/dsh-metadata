# Topsoil moisture model estimates [Countryside Survey]

- Aim
  - Provide modelled mean topsoil (0–15 cm) moisture across Great Britain to support consistent environmental health monitoring and policy assessment.
  - Use data from 1998 and 2007 to compare habitat and parent material moisture characteristics over time.

- Data and sampling
  - 2614 soil cores from 591 1 km × 1 km squares collected in 2007.
  - Sampling consistent with Countryside Survey methods; see Emmett et al. 2008/2010 for details.

- Modelling and outputs
  - Means of moisture for habitat × parent material combinations modelled using dominant habitat and parent material traits from Land Cover Map 2007 (LCM2007) and Parent Material Model 2009.
  - Parent material characteristic used in each model is the one that minimised AIC (Table 1).
  - Outputs are habitat/parent material–specific mean moisture values (MOIST98 and MOIST07 with SE).

- Data attributes and structure
  - Spatial reference: OSGB 1936 / British National Grid (EPSG:27700).
  - Key attributes:
    - LCM_CLASS, LCM_NUMBER (from LCM2007)
    - DOM_GRAIN (dominant grain size)
    - SOIL_GROUP (soil texture description)
    - CACO3_RANK (carbonate content)
    - MOIST98, MOIST98_SE (1998 moisture and standard error)
    - MOIST07, MOIST07_SE (2007 moisture and standard error)

- Experimental design and collection
  - Soil moisture measured in 2614 plots across 591 main plots within 1 km squares in 2007.
  - Collection method used a 15 cm long, 5 cm diameter black plastic core.

- Analytical methods
  - Moisture loss during processing used to estimate the initial gravimetric moisture content and initial dry weight of soil.

- Quality control and references
  - Quality control details provided in Emmett et al. (2008, 2010).
  - Supporting documents include CS technical reports and the Land Cover Map 2007 product.
  - Key references: Emmett et al. 2008/2010; Scott 2008; Morton et al. 2011; and related materials. 

- Limitations and coverage
  - Urban and littoral rock areas are not sampled; no associated data for these areas.
  - Some habitat/parent material combinations had insufficient sample sizes to estimate means.