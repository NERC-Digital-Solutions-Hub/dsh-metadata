# Topsoil moisture model estimates [Countryside Survey]

## Overview
- Provides GB-wide estimates of topsoil moisture (0–15 cm depth) using data from the Countryside Survey.
- Based on 2614 cores from 591 1 km × 1 km squares collected in 2007; mean values modelled for selected habitats and parent material characteristics from 1998 and 2007.
- Habitat and parent material characteristics are derived from the Land Cover Map 2007 and the 2009 Parent Material Model.
- Notes that some areas (e.g., urban, littoral rock) are not sampled and some habitat/parent material combinations have insufficient sample sizes.

## Data scope and contents
- Spatial reference: OSGB 1936/British National Grid (EPSG: 27700).
- Data attributes include:
  - LCM_CLASS and LCM_NUMBER: habitat class and numeric code from Land Cover Map 2007.
  - DOM_GRAIN: dominant grain size from the BGS Soil Parent Material Model.
  - SOIL_GROUP: broad soil texture category from the Soil Parent Material Model.
  - CACO3_RANK: carbonate content classification (none, low, medium, high).
  - MOIST98 and MOIST07: mean gravimetric moisture content for 1998 and 2007, respectively.
  - MOIST98_SE and MOIST07_SE: standard errors for the respective moisture estimates.
- Purpose: provide model-based moisture estimates by habitat/parent material characteristics, facilitating interpretation and use in soil and biodiversity studies.

## Sampling, collection, and methods
- Experimental design: 2614 plots measured in 2007 from 591 main plots within 1 km × 1 km squares.
- Collection method: soil moisture measured using a 15 cm long by 5 cm diameter plastic core, following a defined field protocol.
- Analytical methods: initial gravimetric moisture content estimated from moisture loss at processing stages, enabling calculation of initial soil dry weight.
- Quality control: detailed quality control procedures provided in Emmett et al. 2008 and 2010.

## Modelling approach
- Mixed-model framework applied to 1998 and 2007 data to estimate mean moisture values for habitat/parent material combinations.
- Models selected using the dominant habitat and parent material characteristics from LCM2007 and Parent Material Model 2009, minimizing AIC.
- Some areas/populations not represented due to sampling gaps (e.g., urban areas, littoral rock).

## Data structure and accessibility
- Data attributes include both descriptive (LCM_CLASS, Description) and quantitative fields (MOIST98, MOIST07, MOIST98_SE, MOIST07_SE) with corresponding units.
- Documentation references primary data sources and supporting statistical analyses (Emmett et al. 2008, 2010; Scott 2008; Morton et al. 2011; related soil and land cover datasets).

## Data quality, provenance, and limitations
- Coverage gaps: urban and littoral rock areas are not covered; certain habitat/parent material combinations have insufficient samples for reliable means.
- Model-based estimates rely on external characterizations (LCM2007, PMM 2009) and may inherit their uncertainties.
- Quality control and methodological details are documented in the referenced technical reports and papers; users should consult Emmett et al. (2008, 2010) for full QC procedures.

## Governance, reuse, and stewardship considerations
- Metadata aligns with standard GB land cover and soil material modeling sources; data governance should ensure consistency with LCM2007 and PMM references.
- Considerations for data stewards:
  - Ensure attribution to Countryside Survey and the cited supporting documents.
  - Note areas lacking data when applying estimates to urban or shoreline regions.
  - Maintain awareness of the model-based nature of moisture estimates and their associated uncertainties (se weights provided).
  - Verify interoperability with GB spatial datasets using OSGB 1936 coordinates.
  - Document any updates or recalibration if newer survey cycles become available.

## References and supporting documents
- Emmett, B.A. et al. 2008. Countryside Survey Technical Report No.03/07: Soils Manual. CEH.
- Emmett, B.A. et al. 2010. CS Technical Report No. 9/07: Soils Report from 2007. CEH.
- Scott, W.A. 2008. CS Technical Report No.4/07: Statistical Report. CEH.
- Griffiths, R.I. et al. 2011. The bacterial biogeography of British soils. Environmental Microbiology.
- Morton, R.D. et al. 2011. Land Cover Map 2007 (1 km raster dominant Target Class, GB). NERC-EDC.
- Soil Parent Material Model documentation (British Geological Survey).