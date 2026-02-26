# ElementalanalysisofsoilinNingboWatershed_metadata

## Overview
- Elemental analysis of soils from the Ningbo peri-urban watershed in eastern China. 
- Topsoil (0–20 cm) analyzed for multiple elements using ICP-MS and XRF; Pb isotopes also measured.
- Includes 80 samples across land-use types: 40 cropland, 11 orchards, 29 forests; data used for source identification of trace elements in peri-urban soils.
- Pb isotopes (206/207, 206/208, 207/208) are unitless; all other element concentrations are in mg/kg soil dry weight (except Pb isotope ratios).
- Data published in Sun et al. 2018 (Exposure & Health); DOI provided in metadata.
- CRM recoveries and LODs provided to support interpretation of measurements.

## What was recorded and why
- Records:
  - ICP-MS: Ag, As, Ba, Cd, Co, Cr, Cs, Cu, Fe, Mn, Mo, Ni, P, Pb, Rb, Sr, Tl, Zr (units: mg/kg).
  - XRF: Al, As, Ba, Ca, Cu, Fe, Ga, K, Mn, Nb, P, Pb, Rb, Si, Sr, Ti (units not explicitly stated here; typically mg/kg or wt% in XRF analyses).
  - Pb isotopes: 206/207, 206/208, 207/208 (unitless).
  - Coordinates: latitude, longitude, and altitude recorded for each sample.
- Purpose:
  - Characterize elemental composition and Pb sources in peri-urban soils.
  - Enable multivariate analyses and isotopic tracers for source attribution.

## Where and when data were collected
- Location: Ningbo, eastern China (peri-urban catchment).
- Time: Sampling conducted in March 2016.
- Sample scope: 80 soil samples (40 cropland, 11 orchard, 29 forest).
- Sample composition: Each soil sample comprised a mixture of five sub-samples randomly collected within a 2 m2 grid.

## How data were collected and processed
- Sample collection:
  - Soil collected with a stainless hand auger; stored in snap-sealed polypropylene bags.
  - Sub-samples combined into a single 0–20 cm soil sample per site.
- Sample preparation:
  - Drying (freeze-drying), sieving, and milling to a fine powder (except for pH and texture tests).
- Analytical methods:
  - ICP-MS (Thermo Scientific iCAP Q) for As, Cd, Cr, Cu, Ni, P, Pb, Ag, Mn, Mo, Tl, Sr, Zn, and Pb isotopes; direct solution acquisition mode with auto-sampler.
  - XRF (Rigaku Nex CG benchtop) for Al, Ca, Ga, K, Nb, P, Si, Ti, Zn, etc.
  - Digestion: nitric acid with H2O2 for ICP-MS; specific reagent sets and internal standards used.
  - Pb isotopes measured with dwell times of 300 ms per isotope; results averaged over 10 replicates and corrected using bracketing standards.
- Quality control:
  - Certified reference materials (CRMs) used for QA/QA (e.g., ISE-921 river clay for ICP-MS, VHGLISPB1-50 for Pb isotopes) and blanks.
  - Recovery analyses and calibration performed; results used to assess accuracy.
  - XRF QA included batches with certified reference materials and blanks.
  
## Data structure and metadata for GIS use
- Data fields include:
  - Geographic coordinates (latitude, longitude) and altitude for each sample.
  - Element concentrations from ICP-MS (mg/kg) and XRF (units consistent with XRF reporting).
  - Pb isotope ratios (206/207, 206/208, 207/208) as unitless values.
  - Sample type/land-use category (cropland, orchard, forest).
- Data quality notes:
  - One altitude value missing (sample AMCS040); all other samples have coordinates and altitude.
  - CRM recovery and LOD metadata provided to support interpretation and data integration.
- Potential GIS applications:
  - Mapping spatial distributions of elemental concentrations and Pb isotopes.
  - Integrating with land-use, soil type, and pollution-source layers to identify anthropogenic inputs.
  - Using isotope data for source attribution analyses in conjunction with multivariate results.

## Source and publication
- Collected by the Inst. for Urban Environment, Chinese Academy of Sciences; analyses conducted by Queen's University Belfast.
- Data accompany a study on source identification of trace elements in peri-urban soils of eastern China (Sun et al., 2018) in Exposure & Health.