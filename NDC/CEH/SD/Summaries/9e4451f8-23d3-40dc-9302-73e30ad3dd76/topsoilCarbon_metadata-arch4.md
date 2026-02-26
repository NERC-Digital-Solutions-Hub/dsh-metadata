# Topsoil carbon model estimates [Countryside Survey]

## Overview
- Dataset provides topsoil carbon data for Great Britain (0–15 cm depth), including loss-on-ignition (%), carbon concentration (g kg-1), and carbon density (t ha-1).
- Based on 2614 cores from 591 1 km × 1 km squares analyzed in 2007.
- Mean values for habitat/parent material combinations estimated across GB using mixed-model approaches from data in 1978, 1998, and 2007.
- Habitat and parent material characteristics derived from Land Cover Map 2007 and the British Geological Survey Soil Parent Material Model (2009).
- Note: Urban and littoral rock areas are not sampled; some habitat/parent material combinations have insufficient sample sizes.

## Data content and structure
- Attributes include: LCM_CLASS, DOM_GRAIN, SOIL_GROUP, CACO3_RANK, LOI_78/LOI_98/LOI_07 (and SE), CCONC_78/CCONC_98/CCONC_07 (and SE), CDENS_78/CDENS_98/CDENS_07 (and SE), among others.
- Spatial reference: OSGB 1936 / British National Grid (EPSG: 27700).
- Units and descriptions are tied to Land Cover Map 2007 classifications and the Soil Parent Material Model.
- Data are organized to support derived topsoil carbon metrics by habitat and dominant parent material characteristics.

## Data collection and methods
- Sampling: 15 cm long by 5 cm diameter cores; field protocol described in Emmett et al. (2008).
- Laboratory analysis:
  - Loss-on-ignition (LOI) measured from 10 g subsamples; LOI% calculated after drying and combustion (CEH Lancaster UKAS SOP3102).
  - Soil carbon concentration determined via elemental analysis; bulk density used to compute carbon density (g cm⁻³ or t ha⁻¹) when combined with LOI/CCONC values.
- Quality control: Followed Defra/NERC Joint Codes of Practice.

## Modeling approach
- Habitat/parent material means are modeled using dominant habitat and dominant parent material characteristics from LCM2007 and PMM2009.
- For each model, the parent material characteristic used was the one that minimized AIC (model selection details in Table 1 references).
- Refer to Emmett et al. (2008, 2010) and Scott (2008) for detailed statistical methodology.

## Spatial and temporal coverage
- Spatial: Great Britain (excluding urban and littoral rock areas in sampling coverage).
- Temporal: Direct measurements from 2007; 1978 and 1998 values are modeled estimates (not measured at all sites) using the same framework.

## Data quality, limitations, and considerations
- Not all habitat/parent material combinations have adequate sample sizes; some areas lack data (urban/littoral exclusions).
- Data gaps due to scattering of available data and reliance on modeled estimates for certain years/habitat-material combos.
- Metadata and detailed methodological notes (sampling design, calibration, and QA) are anchored in the referenced CEH reports (Emmett et al., 2008, 2010) and Scott (2008).

## Access, metadata, and provenance
- Data attributes and relationships grounded in Land Cover Map 2007 (LCM2007) and British Geological Survey Soil PMM.
- Core references:
  - Emmett, B.A. et al. (2008, 2010): Soils Manual and Soils Report (Countryside Survey).
  - Scott, W.A. (2008): Statistical Report.
  - Mortier et al. (2011): Land Cover Map 2007 (1 km raster dominant Target Class, GB).
- Additional related datasets and protocols available through CEH and the Defra/NERC QA framework.