# Topsoil carbon model estimates [Countryside Survey]

## Overview
- Provides topsoil carbon estimates for 0–15 cm depth, including loss-on-ignition (% LOI), carbon concentration (g kg-1), and carbon density (t ha-1).
- Based on 2614 soil cores from 591 1 km × 1 km squares across Great Britain, collected in 2007.
- Estimates of mean values for selected habitats and parent material characteristics across GB are produced using data from 1978, 1998, and 2007 via a mixed-model approach.
- Habitat/parent material means are modelled using dominant habitat and parent material characteristics derived from the Land Cover Map 2007 (LCM2007) and the British Geological Survey’s Parent Material Model (2009). Areas not sampled by Countryside Survey (e.g., urban, littoral rock) have no data.
- Some habitat/parent material combinations have insufficient sample sizes to estimate means.

## Data and variables
- Spatial reference: OSGB 1936 / British National Grid (EPSG: 27700).
- Key data attributes include:
  - LCM_CLASS and LCM_NUMBER (derived from LCM2007)
  - DOM_GRAIN (dominant grain size from PMM)
  - SOIL_GROUP (soil texture category)
  - CACO3_RANK (carbonate content ranking)
  - LOI_78, LOI_98, LOI_07 and their standard errors (LOI by year)
  - CCONC_78, CCONC_98, CCONC_07 and their SEs (carbon concentration by year)
  - CDENS_78, CDENS_98, CDENS_07 and their SEs (carbon density by year)
- The dataset aggregates LOI, C concentration, and carbon density by habitat and dominant material characteristics.

## Methods and modelling
- Sampling regime:
  - LOI values determined for 1197 plots within 256 1 km squares (1978), 1098 plots within 256 squares (1998), and 2614 plots within 591 squares (2007).
  - Field protocol used: 15 cm long by 5 cm diameter cores (Emmett et al. 2008).
- Laboratory analysis:
  - LOI measured on a 10 g air-dried sub-sample; drying and combustion steps followed; LOI calculated from weight loss.
  - Soil carbon concentration measured with a total elemental analyser (CEH Lancaster UKAS SOP3102).
  - Topsoil carbon density calculated by combining LOI, C concentration, and bulk density to convert to t ha−1.
- Modelling approach:
  - Mean values for habitat/parent material combinations modelled using dominant habitat (LCM) and dominant grain/ carbonate characteristics derived from the PMM.
  - Model selection used AIC to choose the dominant grain (DOM_GRAIN) and other parent material attributes.
  - Referenced datasets: Land Cover Map 2007 and Soil Parent Material Model.
- Quality control:
  - Adherence to Defra/NERC Joint Codes of Practice (Emmett et al. 2008, 2010).

## Output format and usefulness
- Produces estimated means for habitat × parent material combinations across GB for each time point (1978, 1998, 2007).
- Outputs are designed to be used in environmental monitoring formats (e.g., reports, maps, charts) to assess soil carbon status and trends.
- Data support monitoring environmental health and policy performance over time by providing standardised, comparable metrics.

## Data limitations and gaps
- Areas not sampled by Countryside Survey (e.g., urban areas, littoral rock) have no associated data.
- Some habitat/parent material combinations have insufficient sample sizes to reliably estimate means.
- LOI-based measurements and subsequent carbon density calculations depend on bulk density estimates and modelled relationships, which introduce uncertainty.

## Data management and accessibility
- Data are stored and prepared for upload to appropriate data portals as part of standard monitoring outputs.
- Datasets are linked to related outputs such as LCM2007 and the Soil Parent Material Model, enabling integrated analysis.

## References and supporting documents
- Emmett et al. (2008, 2010): Soils Manual and Soils Report from 2007; methodological details.
- Scott (2008): Statistical Report.
- Morton et al. (2011): Land Cover Map 2007 product details.
- Additional project reports and standard operating procedures cited for methods and QA.