# Topsoil carbon model estimates [Countryside Survey]

## Overview
- Provides modeled estimates of topsoil carbon (0–15 cm) for Great Britain, based on loss-on-ignition (LOI %), carbon concentration (g kg-1), and carbon density (t ha-1).
- Derived from 2614 soil cores across 591 1 km × 1 km squares, analyzed in 2007 (with historical context from 1978 and 1998).
- Means are estimated for selected habitat–parent material combinations using a mixed-model approach, linking to Land Cover Map 2007 and a Soil Parent Material Model (2009).
- Some areas are not sampled (e.g., urban and littoral rock) and some habitat/parent material combinations have insufficient data to estimate means.

## Data scope and outputs
- Variables include:
  - Loss-on-ignition (LOI) values for 1978, 1998, 2007 (LOI_78, LOI_98, LOI_07) with standard errors (LOI_78SE, LOI_98SE, LOI_07SE).
  - Soil carbon concentration (CCONC_78, CCONC_98, CCONC_07) with SEs (CCONC_78SE, etc.).
  - Soil carbon density (CDENS_78, CDENS_98, CDENS_07) with SEs (CDENS_78SE, etc.).
- Attributes are mapped to dominant habitat characteristics from Land Cover Map 2007 and dominant soil material characteristics from the Soil PMM, with coding (e.g., DOM_GRAIN, CACO3_RANK, SOIL_GROUP).
- Spatial reference: OSGB 1936 / British National Grid (EPSG: 27700).

## Sampling design and collection
- LOI values determined from:
  - 1978: 1197 plots within 256 squares
  - 1998: 1098 plots within 256 squares
  - 2007: 2614 plots within 591 squares
- Field collection used 15 cm long × 5 cm diameter cores following Emmett et al. 2008 protocol.

## Analytical methods and modelling approach
- LOI methodology: 10 g sub-sample dried at 105°C, combusted at 375°C, to determine moisture loss and LOI percentage.
- Carbon concentration measured with a total elemental analyser (CEH Lancaster UKAS SOP3102).
- Topsoil carbon density derived by combining LOI/CC data with bulk density measurements.
- Means by habitat–parent material combinations modelled using:
  - Dominant habitat characteristics (from LCM2007)
  - Dominant parent material characteristics (from PMM 2009)
  - Model selection based on minimising AIC
- Some habitat/parent material combinations are not estimated due to insufficient data.

## Data attributes and structure
- Key fields include:
  - LCM_CLASS, LCM_NUMBER (habitat classification)
  - DOM_GRAIN (dominant grain size)
  - SOIL_GROUP (soil texture category)
  - CACO3_RANK (carbonate content ranking)
  - LOI_78, LOI_98, LOI_07 and their SEs
  - CCONC_78, CCONC_98, CCONC_07 and their SEs
  - CDENS_78, CDENS_98, CDENS_07 and their SEs
- Data are aligned to 1 km square units where applicable, with model-derived means rather than direct sampling for all areas.

## Geographic and temporal coverage
- Spatial: Great Britain (land cover and soil material characteristics integrated with 1 km square framework for modelling).
- Temporal: Historical observations from 1978 and 1998 used to model 2007 values; three time points (1978, 1998, 2007) are represented for LOI, CCONC, and CDENS.

## Quality control, provenance, and supporting documents
- Quality control consistent with Defra/NERC Joint Codes of Practice (Emmett et al. 2008, 2010; related technical reports).
- Key references:
  - Emmett et al. (2008, 2010): Soils Manual and Soils Report
  - Scott (2008): Statistical Report
  - Morton et al. (2011): Land Cover Map 2007 data
  - Additional notes on the Soil PMM and related data sources

## Implications for monitoring and governance
- Provides a standardized, model-based set of topsoil carbon indicators across GB to support policy scrutiny, evaluation, and decision-making.
- Facilitates tracking of soil carbon status over time by habitat and parent material categories.
- Useful for informing land management and soil carbon policies, with clear caveats about areas not sampled and the dependence on model structure and underlying metadata.
- Highlights data governance considerations (metadata completeness, data sharing, and the need to manage openness versus data sensitivity).