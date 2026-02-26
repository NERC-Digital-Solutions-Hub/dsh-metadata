# Topsoil invertebrate model estimates [Countryside Survey]

- Represents 0–8 cm soil depth for Great Britain.
- Based on 947 soil cores from 256 1 km × 1 km squares collected in 2007; sampling and methods detailed in Emmett et al. 2010.
- Estimation of mean values across habitat and parent material combinations using data from 1978, 1998, and 2007 with a mixed-model approach (Scott 2008; Emmett et al. 2008, 2010).
- Model inputs linked to dominant habitat/land cover and parent material characteristics from Land Cover Map 2007 (LCM2007) and the British Geological Survey Soil Parent Material Model (PMM 2009); areas like urban and littoral rock are not sampled and have no data.

- Key variables modeled (Table 1):
  - Total Catch (CATCH) and its mean values by year (CATCH_98, CATCH_07) with standard errors (CATCH_98SE, CATCH_07SE)
  - Mite:springtail ratio (RATIO_98, RATIO_07) with SE (RATIO_98SE, RATIO_07SE)
  - Number of broad taxa (TAXA_98, TAXA_07) with SE (TAXA_98SE, TAXA_07SE)
  - Shannon diversity index (SHAN_98, SHAN_07) with SE (SHAN_98SE, SHAN_07SE)
  - Dominant land cover class (LCM_CLASS; code LCM_NUMBER) and dominant parent material characteristics (DOM_GRAIN, SOIL_GROUP)
  - Carbonate content ranking (CACO3_RANK)
- Spatial reference: OSGB 1936 / British National Grid (EPSG:27700).

- Data attributes and schema
  - LCM_CLASS and LCM_NUMBER describe dominant land cover (derived from LCM2007)
  - DOM_GRAIN and SOIL_GROUP describe dominant grain size and soil texture
  - CATCH_98, CATCH_07 and SE fields provide mean invertebrate counts and uncertainty for 1998 and 2007
  - TAXA_98, TAXA_07 and SE fields for number of broad taxa
  - RATIO_98, RATIO_07 and SE fields for mite:springtail ratio
  - SHAN_98, SHAN_07 and SE fields for Shannon diversity index
- Sampling and collection methods
  - 4 cm diameter × 8 cm long white plastic core; vegetation removed; litter layer retained
  - Cores extracted to soil surface, then shipped to lab
  - Dry Tullgren extraction used to recover soil invertebrates
  - Identification to major taxa (taxonomic level 1) with broad taxa categories
- Analytical methods and quality control
  - Invertebrates counted within broad taxa and groups; analyses model mean values by habitat and DOM_GRAIN/SOIL_GROUP
  - Regular cross-checks: second identifications by different staff compared to original counts
  - Discrepancies resolved and documented; ensures consistency and reduces operator error
- Experimental design and limitations
  - Spatial coverage excludes urban and littoral rock areas; not all habitat/parent material combinations have sufficient samples
  - Some data subsets limited by sample size; model uses AIC to select dominant land/soil characteristics
- Data governance considerations for data leaders
  - Data provenance linked to major national datasets (LCM2007, PMM)
  - Metadata includes spatial reference, variable definitions, unit and year of measurements
  - Suitable for cross-year trend analysis (1998 vs 2007) with explicit standard errors
  - Data support materials and methodology detailed in accompanying technical reports
- References and supporting documents
  - Emmett et al. 2008; Emmett et al. 2010; Scott 2008; Morton et al. 2011
  - Land Cover Map 2007 and British Geological Survey Soil PMM documentation

- Implications for data strategy
  - Provides a model-based, GB-wide, soil invertebrate baseline with explicit metadata and uncertainty measures
  - Useful for assessing soil biodiversity in relation to habitat and soil material categories
  - Highlights need for comprehensive coverage in under-sampled areas and for standardized metadata to improve discoverability and reuse