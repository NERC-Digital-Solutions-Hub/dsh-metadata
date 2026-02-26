# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) Normalised Difference Vegetation Index (NDVI) in saltmarsh and mudflat habitats

## Overview
- NDVI dataset detailing surface reflectance, expressed as Normalised Difference Vegetation Index (NDVI).
- Part of the CBESS project; field campaign conducted in winter and summer 2013.
- No repeat sampling planned; dataset designed for end-user self-service and further product development.

## Scope and locations
- Regions: Essex and Morecambe Bay (UK).
- Sites: Essex – Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM); Morecambe Bay – Cartmel Sands (CS), Warton Sands (WS).
- Habitat contrasts: saltmarsh (two soil types in Essex clays; Morecambe Bay sands) and mudflats (Essex clays vs Morecambe sands) to reflect differing sediment types, inundation, creek structure, and vegetation.
- Spatial and environmental context captured to support comparisons across soil types, inundation regimes, and habitat types.

## Sampling and data collection
- Quadrat design: twenty-two 1 x 1 m quadrats per site; quadrats randomly allocated using R to define four spatial scales (A–D):
  - A: 1 quadrat
  - B: 3 quadrats from 1 m to 10 m apart
  - C: 6 quadrats from 10 m to 100 m apart
  - D: 12 quadrats up to 1000 m apart
- Timing: during CBESS field campaigns (winter and summer 2013); no planned repeats.
- NDVI observations: collected before any destructive sampling.

## Instrumentation and measurement procedures
- Instrument: OceanOptics USB2000 spectrometer with a 1.5 m fiber optic.
- Data logging: OOIBase32 Version 2.0.1.3 on a laptop.
- Measurement protocol per quadrat:
  - Adjust integration time so white reference peak ~75% of maximum.
  - Use spectral averaging for short integration times (<100 ms) to reduce noise.
  - Record dark, white reference, and reflectance measurements.
  - Repeat measurements if ambient light conditions change.
  - Discard measurements taken under variable light conditions.
  - Record metadata: corresponding OOBase file numbers and percentages of cloud/water cover and other relevant notes.
- NDVI processing: calculated in Matlab using Field Spectroscopy Facility Post Processing Toolbox (FSFPostProcessing1.3.8).

## Data formats and structure
- Primary file format: CSV.
- Data integrity: missing data indicated as NA.
- Dataset fields (example structure):
  - Row Number: numeric sorting key
  - Season: Winter (W) or Summer (S)
  - Location: Morecambe (M) or Essex (E)
  - Site: Morecambe – Cartmel Sands (CS) or Warton Sands (WS); Essex – Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
  - Habitat: Mudflat (MF) or Saltmarsh (SM)
  - Quadrat Number: 1–22
  - Scale: A (1 m), B (1–10 m), C (10–100 m), D (100 m to upper limit)
  - NDVI: numerical NDVI value

## Data quality, QA, and metadata
- Data collection includes explicit QA steps for sensor calibration, lighting conditions, and repeat measurements when needed.
- Detailed site descriptions and habitat context accompany the data to support correct interpretation.
- NDVI computation and toolbox version are documented to facilitate reproducibility.

## Intended use and value for end users
- Enables self-serve exploration of NDVI across saltmarsh and mudflat habitats, soil types, and sites.
- Supports comparative analyses of vegetation health/activity under different habitat and sediment conditions.
- Provides metadata-rich dataset suitable for habitat mapping, biodiversity assessments, and ecosystem service evaluations.

## Considerations and limitations
- Snapshot dataset limited to winter and summer 2013; not designed for temporal trend analysis beyond those seasons.
- No planned repetition; users should account for temporality when interpreting results.
- Variation in site characteristics (soil type, inundation, vegetation) is captured to support cross-site comparisons but may require careful normalization when aggregating.

## Access notes
- Data described as CSV with accompanying methodological metadata (calibration, QA steps, and processing details) to support reuse and integration into data products or dashboards.