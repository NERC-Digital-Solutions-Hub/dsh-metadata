# Topsoil invertebrate model estimates [Countryside Survey]

## Overview
- Purpose: Model-based estimates of topsoil invertebrate metrics to monitor environmental health and policy performance over time.
- Scope: Data representing 0–8 cm soil depth across Great Britain (GB) using Countryside Survey.
- Samples: 947 cores from 256 1 km × 1 km squares analyzed in 2007; historical data from 1978 and 1998 used in a mixed-model framework.
- Outputs: Means of invertebrate measures by habitat/parent material combinations, derived from Land Cover Map 2007 and Soil Parent Material Model 2009.

## Data and Outputs
- Key variables modeled: Total Catch, Mite:springtail ratio, Number of broad taxa, Shannon diversity index.
- Parent material and habitat predictors: Dominant grain (DOM_GRAIN) and Soil Group (SOIL_GROUP); linked to LCM2007 and Soil PMM.
- Spatial reference: OSGB 1936 / British National Grid (EPSG:27700).
- Data coverage caveats: Areas not sampled by Countryside Survey (e.g., urban, littoral rock) have no data; some habitat/parent-material combos had insufficient sample sizes to estimate means.

## Methods
- Experimental design: Sampling of all Main Plots; includes revisit of 256 original CS squares (1978) as part of the 2007 dataset; details in Emmett et al. 2008, 2010.
- Collection: 4 cm diameter × 8 cm long white plastic cores; surface vegetation removed; dry Tullgren extraction used to obtain invertebrates.
- Analytical methods: Identification to major taxa (broad taxa categories listed) and counting; taxa include Acari, Collembola, Diptera, Lepidoptera, Isopoda, and many others.
- Quality control: Independent re-identification and counting by a second staff member; discrepancies resolved and documented; cross-checks logged on sample records.

## Data Attributes
- Derived attributes from LCM2007 and PMM: LCM_CLASS, LCM_NUMBER; DOM_GRAIN; SOIL_GROUP; CACO3_RANK; and year-specific metrics.
- Year-specific outputs: CATCH_98, CATCH_07 and SE (standard errors); TAXA_98, TAXA_07 and SE; RATIO_98, RATIO_07 and SE; SHAN_98, SHAN_07 and SE.
- Documentation references for data definitions and modeling details are provided (Emmett et al. 2008, 2010; Scott 2008).

## Data Availability, Assumptions, and Limitations
- Model-based estimates rely on historical data (1978, 1998) to inform 2007 estimates via mixed models.
- Some combinations lack sufficient samples; hence not all habitat/parent-material pairs have mean estimates.
- Urban and littoral rock areas are outside CS sampling and lack associated data.
- Data are suitable for standardized reporting and cross-time comparisons within the modeled framework.

## Validation and References
- Quality assurance procedures described in the dataset documentation.
- Supporting and methodological references:
  - Emmett et al. (2008) Soils Manual; Countryside Survey Technical Report No. 03/07
  - Scott (2008) CS Technical Report No. 4/07: Statistical Report
  - Emmett et al. (2010) CS Technical Report No. 9/07: Soils Report from 2007
  - Morton et al. (2011): Land Cover Map 2007
  - British Geological Survey: Soil Parent Material Model
- Spatial data and methods linked to Land Cover Map 2007 and Soil PMM sources.