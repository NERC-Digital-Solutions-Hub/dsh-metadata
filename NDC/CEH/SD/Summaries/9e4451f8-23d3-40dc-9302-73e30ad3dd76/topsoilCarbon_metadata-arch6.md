# Topsoil carbon model estimates [Countryside Survey]

## Overview
- Topsoil data represent 0-15 cm depth, including loss-on-ignition (% LOI), carbon concentration (g/kg), and carbon density (t/ha).
- Based on 2614 cores from 591 1km x 1km squares across Great Britain, collected in 2007 (sampling details in Emmett et al. 2010).
- Mean values for habitat and parent material combinations estimated across GB using data from 1978, 1998, and 2007 via a mixed-model approach (see Scott, 2008).
- Habitat/parent material–specific estimates are modelled using dominant habitat from Land Cover Map 2007 and a Parent Material Model (2009); areas such as urban and littoral rock are not sampled and thus have no data; some habitat/parent material combinations have insufficient sample sizes.

## Data content and structure
- Data attributes include:
  - LCM_CLASS, LCM_NUMBER: derived from Land Cover Map 2007 (habitat level, numeric code)
  - DOM_GRAIN: dominant grain size (from BGS Soil Parent Material Model)
  - SOIL_GROUP: general soil texture category (Heavy/Medium/Light)
  - CACO3_RANK: carbonate content ranking (none/low/medium/high)
  - LOI_78, LOI_98, LOI_07 with standard errors LOI_78SE, LOI_98SE, LOI_07SE
  - CCONC_78, CCONC_98, CCONC_07 with SEs CCONC_78SE, CCONC_98SE, CCONC_07SE
  - CDENS_78, CDENS_98, CDENS_07 with SEs CDENS_78SE, CDENS_98SE, CDENS_07SE
- Units are specified for each attribute (e.g., LOI in %, CCONC in g/kg, CDENS in t/ha).
- Spatial reference: OSGB 1936/British National Grid (EPSG:27700).

## Spatial reference and coverage
- Geographic scope: Great Britain
- Spatial framework: 1km x 1km squares; data tied to dominant habitat and dominant soil parent material characteristics.
- Some areas are not represented (e.g., urban and littoral rock) because they were not sampled by Countryside Survey.

## Experimental design and sampling
- Loss-on-ignition (LOI) values measured for:
  - 1197 plots in 1978 across 256 squares
  - 1098 plots in 1998 across 256 squares
  - 2614 plots in 2007 across 591 squares
- Field sampling used a 15 cm long by 5 cm diameter core following the protocol in Emmett et al. (2008).

## Analytical methods and calibration
- LOI measurement: 10 g air-dried sub-sample, dried at 105°C (16 h), combusted at 375°C (16 h), LOI calculated from weight loss.
- Carbon concentration (C concentration) measured with a total elemental analyser (CEH Lancaster UKAS accredited SOP3102).
- Topsoil carbon density derived by combining C concentration with bulk density (requires C per unit volume; LOI and C concentration together produce density estimates).
- Calibration and methodological details are provided in Emmett et al. (2008, 2010).

## Quality control
- Followed Defra/NERC Joint Codes of Practice throughout.
- Additional methodological details available in Emmett et al. (2008, 2010).

## Limitations and considerations for use
- Model estimates rely on dominant habitat and dominant parent material characteristics; some habitat/parent material combinations have limited sample sizes.
- Urban and littoral rock areas are not represented in the sample, limiting extrapolation to those areas.
- Some years’ model components (e.g., the 2007 measurements and historical data) are modelled rather than directly observed for all habitat/material combinations.

## References and supporting documents
- Emmett et al. 2008, 2010: Countryside Survey technical reports (Soils Manual; Statistical Report; Soils Report from 2007)
- Scott 2008: CS Technical Report No. 4/07: Statistical Report
- Morton et al. 2011: Land Cover Map 2007 (1km raster dominant Target Class, GB)
- Related: Countryside Survey publications on soil change and soil models (e.g., Vadose Zone Journal 2013) and the British Geological Survey Soil Parent Material Model
- Links and DOIs provided for Land Cover Map 2007 and related datasets