# Mathematically modelled daily water saturation profiles for sites on the Namoi River floodplain in south-east Australia, at different distances from the river.

## Overview
- Model-generated dataset of vertical soil-water saturation along profiles from the surface to 10 m depth, at six sites across two locations near the Namoi River.
- Outputs daily time series with depth-based measurements, intended to align with figures in Evans et al. (2018).

## Data Description
- Sites and locations:
  - Old Mollee: 50 m, 140 m, 320 m from the river
  - Yarral East: 40 m, 110 m, 290 m from the river
- Depth and time:
  - Depth range: surface to 10 m
  - Time series: daily outputs
  - Depth indexing: first row of outputs gives depths; first column gives dates
  - Depth units: metres
  - Saturation units: proportion of pore space, 0.0 to 1.0, reported to 7 decimal places
- Grid details:
  - Model domain uses 944 grid points across 10 m depth with half-grid spacing
  - Outputs initially produced in unformatted files, converted to formatted files for ease of use
- Spatial coordinates:
  - Old Mollee 50m: lat/long -30.254, 149.681; elevation (202.25 m AHD)
  - Old Mollee 140m: -30.254, 149.682; 204.37 m AHD
  - Old Mollee 320m: -30.254, 149.684; 203.82 m AHD
  - Yarral East 40m: -30.237, 149.671; 202.98 m AHD
  - Yarral East 110m: -30.236, 149.671; 202.84 m AHD
  - Yarral East 290m: -30.234, 149.671; 202.02 m AHD

## Acquisition and Modelling
- Modelling tool: HaughFlow (Evans et al., 2018)
- Purpose: predict water movement in vadose and phreatic zones of hydraulically connected floodplains; outputs time series of soil-water profiles
- Mathematical basis:
  - Vertical transport: 1D Richards equation for the vadose zone
  - Lateral flow: 1D Boussinesq equation for the phreatic zone
  - Two-way coupling allows water exchange between vadose and phreatic zones
- Implementation:
  - Fortran90, tri-diagonal solver, predictor-corrector time discretisation
  - Spatial discretisation using centered finite differences
- Inputs used to drive outputs:
  - River stage levels, climate parameters, and soil properties
  - Determine lateral/vertical inputs and water flow speed
- Data handling:
  - Model outputs stored in unformatted files; converted to formatted files in this dataset for usability
- Calibration:
  - Calibrated against 2013 water table levels at Yarral East 290 m
  - Calibrated soil properties: saturated hydraulic conductivity = 5.756 m/day; drainage = 0.01568 m/day

## Time Frame
- Old Mollee sites:
  - 50 m, 140 m, 320 m: 01 July 2011 – 30 June 2015
- Yarral East sites:
  - 40 m, 110 m, 290 m: 01 Jan 2013 – 30 June 2015
- Old Mollee Figure 7 dataset:
  - 01 January 2004 – 31 December 2016 (alternative climate inputs)

## Documentation and Provenance
- Related publication: Evans, C.M., Dritschel, D.G., and Singer, M.B. (2018) Modeling subsurface hydrology in floodplains, Water Resources Research
- Data provenance:
  - Part of a PhD project funded by the Natural Environment Research Council (NERC) and the National Trust
  - Datasets relate to figures presented in Evans et al. (2018)

## Data Stewardship Notes
- Metadata and standards:
  - Clear site identifiers, distances from river, exact coordinates, elevations
  - Depth, time, and saturation units explicitly defined; high-precision saturation values (7 decimals)
  - Comprehensive model description, calibration parameters, and publication linkage for traceability
- Accessibility considerations:
  - Outputs linked to specific figures in the reference paper for context
  - Original outputs were unformatted; reformatted for usability while preserving original content
- Governance considerations:
  - Documented model assumptions (1D vertical and 1D lateral coupling) and calibration basis
  - Clear provenance back to Evans et al. 2018 and funding sources
  - Data licensing and reuse conditions inferred from publication and dataset provenance; ensure citation of Evans et al. 2018 when reused