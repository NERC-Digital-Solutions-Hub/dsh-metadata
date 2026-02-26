# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) surface sediment chlorophyll concentrations in saltmarsh and mudflat habitats

## Overview
- Dataset of chlorophyll concentrations (chlorophyll a, chlorophyll b, and chlorophyll c1+c2) in surface sediments (top 2 mm) from saltmarsh and mudflat habitats.
- Measured values in micrograms per gram of sediment (µg g-1).
- Seasonal sampling: winter and summer 2013 as part of the CBESS field campaign.
- Sampling design includes 22 randomly allocated 1x1 m quadrats per site across contrasting habitat types.

## Location and site characteristics
- Essex sites: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
- Morecambe Bay sites: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
- Habitat contrasts:
  - Saltmarsh: two contrasting soil types (clay in Essex; sandy in Morecambe Bay); differing inundation frequency, creek structure, and dominant vegetation.
  - Mudflat: Essex sites with cohesive clays/mud/silt; Morecambe sites with coarse, mobile sediments.

## Sampling design and monitoring framework
- Sampling frequency: winter and summer 2013; no planned repeat sampling beyond this campaign.
- Quadrats: twenty-two 1x1 m quadrats per mudflat and per saltmarsh site, randomly allocated using R.
- Spatial scales: four scales (A–D) to capture different extents (e.g., A = single quadrat; D = broader area up to upper limit), enabling multi-scale analyses.

## Field and laboratory procedures
- Field sampling: surface sediment collected using a contact corer (top 2 mm) and flash-frozen with liquid nitrogen; samples stored in darkness below -80°C.
- Laboratory processing: samples freeze-dried (Edwards EF4 Modulyo); chlorophyll extracted from sub-samples (~100 mg) using acetone.
- Measurement: chlorophyll quantification via Cecil CE3021 spectrophotometer at wavelengths 630, 647, 664, and 750 nm.
- Data derived: concentrations of chlorophyll a, chlorophyll b, and chlorophyll c1+c2 calculated from absorption readings using standard equations.

## Data handling and quality control
- Calibration: laboratory protocols followed; spectrophotometer accuracy checked with standard chlorophyll solutions.
- Data capture: readings entered into spreadsheets; spectrophotometer software (Cecil Datastream) used to record absorption figures.
- File formats: CSV (comma-separated values) for data export.
- Metadata and structure: detailed dataset fields describing season, location, site, habitat, quadrat number, spatial scale, chlorophyll metrics (a, b, c1+c2) and their standard deviations, with notes on missing data where applicable.

## Dataset structure and variables
- Season: Winter (W) or Summer (S).
- Location: Essex (E) or Morecambe (M).
- Site: specific site codes (e.g., AH, FW, TM, CS, WS, WP).
- Habitat: Mudflat (MF) or Saltmarsh (SM).
- Quadrat Number: 1–22.
- Scale: A–D (defining spatial extent categories).
- Chlorophyll metrics:
  - Chl a (µg g-1) with corresponding standard deviation.
  - Chl b (µg g-1) with corresponding standard deviation.
  - Chl c1+c2 (µg g-1) with corresponding standard deviation.
- Additional notes: some fields indicate missing data due to inaccessibility of quadrats; header and row number conventions documented.

## Purpose and use
- Provides a standardized, QA/qC-checked dataset to assess coastal phytobenthos (MPB) chlorophyll levels across contrasting habitats and soil types.
- Facilitates temporal (seasonal) and spatial (site and scale) comparisons to monitor environmental health and inform policy-relevant analyses.
- Data storage and sharing are aligned with CBESS practices, ensuring availability through appropriate data portals.