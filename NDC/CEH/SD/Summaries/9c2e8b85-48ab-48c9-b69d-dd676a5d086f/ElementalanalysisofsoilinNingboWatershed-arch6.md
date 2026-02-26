# ElementalanalysisofsoilinNingboWatershed_metadata

## Overview
- Metadata for a soil elemental survey in Ningbo, eastern China. Topsoil (0–20 cm) from peri-urban catchment analyzed for multiple elements and Pb isotopes to identify anthropogenic inputs.
- Samples: 80 total (40 cropland, 11 orchard, 29 forest) collected March 2016; each sample composed of five sub-samples within a 2 m² grid.
- Data purpose: Support source identification of trace elements and enable multivariate analyses (correlation, regression, PCA) and isotopic tracing.

## What was recorded and why
- Elements and isotopes:
  - ICP-MS measurements: Ag, As, Ba, Cd, Co, Cr, Cs, Cu, Fe, Mn, Mo, Ni, P, Pb, Rb, Sr, Tl, Zr (units: mg/kg).
  - XRF measurements: Al, As, Ba, Ca, Cu, Fe, Ga, K, Mn, Nb, P, Pb, Rb, Si, Sr, Ti (units: mg/kg).
  - Lead isotopic ratios: 206/207, 206/208, 207/208 (unitless).
- Location data: Latitude, longitude, and altitude recorded for each sample.
- Sample collection and prep: 0–20 cm soil samples; dried, sieved, and milled; analyses via ICP-MS (BDH acids for digestion) and XRF (Rigaku Nex CG); internal standards used; calibration with blanks and standards; quality control with certified reference materials (CRMs).
- Data processing and QC:
  - CRM recoveries and LODs provided for all samples; below-LOD values replaced by half-LOD for analysis purposes.
  - Pb isotopic data corrected using bracketing certified Pb standards.
  - Altitude missing for one sample (AMCS040).
- Why: to explore sources of trace elements in peri-urban soils and differentiate anthropogenic inputs from natural background using multivariate analyses and isotopic tracers.
- Provenance: Samples collected by Inst. for Urban Environment, Chinese Academy of Sciences; analyses performed by Queen's University Belfast. Publication: Sun et al. 2018, Exposure & Health; DOI: https://doi.org/10.1007/s12403-018-0290-1.

## Data content and structure
- Sample scope: 80 samples with associated metadata and measurements.
- Variables included:
  - Spatial: latitude, longitude, altitude.
  - Sample description: land-use type (cropland, orchard, forest).
  - Analytical data: ICP-MS concentrations (As, Cd, Cr, Cu, Ni, Pb, Zn, and others), XRF concentrations (Al, Ca, K, Si, Ti, etc.), Pb isotope ratios.
  - Units: all elemental concentrations in mg/kg soil dry weight; Pb isotopic ratios unitless.
- Data quality and limits:
  - Specific recovery percentages and LOD values are provided per element (ICP-MS and XRF) in the metadata.
  - One missing altitude value identified (AMCS040).

## How to use the data
- Ideal for:
  - Combining ICP-MS and XRF data to create unified contaminant profiles (mg/kg).
  - Isotopic tracing of Pb sources via 206/207, 206/208, and 207/208 ratios.
  - Multivariate analyses to identify relationships between land use, element associations, and potential anthropogenic input.
- Data processing considerations:
  - Handle below-LOD values by substituting half-LOD as documented.
  - Ensure Pb isotopic data are treated as unitless ratios.
  - Address the single missing altitude value during integration with GIS or spatial analyses.

## Particular notes for Data Support practitioners
- Data coverage: 80 samples across three land-use types provide a broad peri-urban context.
- Data integrity: QC procedures and CRM-based recoveries are documented; bracketing standards used for Pb isotopes ensure comparability.
- Limitations: minor missing data (altitude for AMCS040); integration of ICP-MS and XRF results requires careful unit alignment and cross-calibration.
- Source and access: dataset described in the referenced Exposure & Health paper; DOI provided for access to the publication and accompanying dataset references.