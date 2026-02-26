# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) Normalised Difference Vegetation Index (NDVI) in saltmarsh and mudflat habitats

## Overview
- NDVI dataset from CBESS measuring surface reflectance to quantify vegetation health and cover in saltmarsh and mudflat habitats.
- Data collected during CBESS field campaign in winter and summer 2013.
- No repeat sampling planned for the same quadrats.

## Dataset scope and aim
- Observations focused on NDVI as a proxy for vegetation condition across contrasting habitat types and sediment characteristics.
- Intended to support analyses of coastal biodiversity and ecosystem service sustainability.

## Locations and habitat context
- Essex locations: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
- Morecambe Bay locations: Cartmel Sands (CS), Warton Sands (WS).
- Habitat contrasts:
  - Saltmarsh: two soil types in Essex (clay) and Morecambe Bay (sandy).
  - Mudflat: Essex (cohesive clays, mud, silt) vs Morecambe Bay (coarse, mobile sediments).
- Coordinates provided for each site to indicate precise observation points.

## Sampling design
- Randomly allocated quadrats at each site: twenty-two 1 m x 1 m quadrats per mudflat and saltmarsh site.
- Four spatial scales (A–D) for quadrat placement:
  - A: 1 quadrat
  - B: 3 quadrats (1 m to 10 m apart)
  - C: 6 quadrats (10 m to 100 m apart)
  - D: 12 quadrats (100 m to 1000 m apart)
- Quadrats shared across CBESS quadrat datasets.
- NDVI measurements taken before any destructive harvesting.

## Measurement protocol and instruments
- Instrumentation: OceanOptics USB2000 spectrometer with 1.5 m fiber; data logged with OOIBase32 (v2.0.1.3).
- Measurement setup: 1.5 m above ground; ensure white reference peak around 75% of spectrometer max; for short integration times use spectral averaging; record dark and white references; NDVI measurement performed; repeat if ambient light changed.
- Logging: note number of OOBase files per quadrat and percentage cloud/water cover; capture additional relevant information.
- NDVI calculation: performed in Matlab using Field Spectroscopy Facility Post Processing Toolbox (FSFPostProcessing1.3.8).

## Data formats and fields
- Primary data format: CSV.
- Handling of missing data: NA cells indicate no data.
- Key fields (sampled per record):
  - Row Number (sorting identifier)
  - Season: Winter (W) or Summer (S)
  - Location: Morecambe (M) or Essex (E)
  - Site: Morecambe – Cartmel Sands (CS) or Warton Sands (WS); Essex – Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
  - Habitat: Mudflat (MF) or Saltmarsh (SM)
  - Quadrat Number: 1–22
  - Scale: A (1 m), B (1–10 m), C (10–100 m), D (100–upper limit)
  - NDVI: numeric NDVI value

## Data quality, provenance, and QC
- Thorough calibration steps outlined (white reference, dark measurement, ambient conditions handling).
- Measurements repeated if lighting conditions changed; records include cloud and water cover details.
- NDVI computed with established toolbox to ensure consistency across quadrats and scales.
- Site selection designed to capture contrasts in sediment type, inundation frequency, creek structure, and vegetation.

## Access, stewardship, and lineage
- Staff responsible: Timothy Hill.
- Data collection integrated with broader CBESS field campaign practices; quadrats and sampling scales align with other CBESS datasets for cross-dataset analyses.

## Considerations for analysts
- Rich, multi-scale NDVI data enabling scale-dependent analyses and comparisons across contrasting coastal habitats.
- Opportunities to integrate with other CBESS datasets for ecosystem service and biodiversity assessments.
- Pay attention to local context (soil type, inundation, sediment characteristics) when modeling NDVI variation between sites.