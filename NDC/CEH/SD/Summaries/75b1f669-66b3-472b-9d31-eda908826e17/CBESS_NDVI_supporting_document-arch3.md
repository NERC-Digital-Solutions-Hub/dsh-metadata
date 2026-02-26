# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) Normalised Difference Vegetation Index (NDVI) in saltmarsh and mudflat habitats

## Purpose and scope
- NDVI dataset measuring surface reflectance to indicate vegetation health/status in saltmarsh and mudflat habitats.
- Part of the CBESS field campaign; intended for environmental monitoring with potential use in policy evaluation and future decision-making.

## Study sites and habitats
- Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM) representing saltmarsh with clay soils and higher inundation frequency.
- Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS) representing saltmarsh with sandy soils and distinct inundation characteristics.
- Mudflat sites: Essex (cohesive clays, mud, silt) and Morecambe Bay (coarse, mobile sediments).

## Sampling design and timeframe
- Field campaign conducted in winter and summer 2013; no planned repeats.
- For each mudflat and saltmarsh site: 22 randomly allocated 1 x 1 m quadrats.
- Four spatial scales (A–D) defined to structure quadrat placement:
  - A: 1 quadrat
  - B: 3 quadrats at 1 m to 10 m apart
  - C: 6 quadrats at 10 m to 100 m apart
  - D: 12 quadrats at 100 m to 1000 m (or site maximum)
- Quadrats are common across all CBESS quadrat data.
- NDVI measurements taken before any destructive harvesting of quadrats.

## Measurements, instrumentation, and procedures
- Observed variable: Normalised Difference Vegetation Index (NDVI).
- Instrumentation: OceanOptics USB2000 spectrometer with 1.5 m fibre optic; data logged with OOIBase32.
- Measurement protocol at each quadrat:
  - Spectral integration time adjusted so white reference peak ≈ 75% of detector maximum.
  - Spectral averaging for short integration times to reduce noise.
  - Dark, white reference, then reflectance measurement.
  - Repeat measurements if ambient light conditions changed; measurements under variable light discarded.
  - Record linkage: number of OOIBase files, percentage cloud and water cover, and other relevant notes.
- NDVI calculation performed in Matlab using Field Spectroscopy Facility Post Processing Toolbox (FSFPostProcessing1.3.8).

## Data formats and metadata
- Data format: CSV files.
- NA indicates no data.
- Dataset fields (example descriptors):
  - Row Number: sortable by original input order.
  - Season: Winter (W) or Summer (S).
  - Location: Morecambe (M) or Essex (E).
  - Site: Morecambe: Cartmel Sands (CS), Warton Sands (WS); Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
  - Habitat: Mudflat (MF) or Saltmarsh (SM).
  - Quadrat Number: 1–22.
  - Scale: A–D corresponding to predefined spatial scales.
  - NDVI: NDVI value (numerical).
- Data collection and site descriptions emphasize contrasting soil types and inundation regimes to enable cross-habitat comparisons.

## Data quality and governance considerations
- Quality control embedded in measurement protocol (calibration, dark/white references, exclusion of data collected under unsuitable light).
- Detailed metadata to support traceability, site comparability, and replication.
- Clear documentation of sampling design (quadrats and spatial scales) to support robust analyses and policy-relevant insights.

## Relevance for monitoring frameworks and decision-making
- Demonstrates an end-to-end monitoring approach: site selection, randomized quadrat design, standardized NDVI measurements, data processing, and rich metadata.
- Enables cross-site and cross-habitat comparisons to inform coastal environmental health, biodiversity status, and ecosystem service assessments.
- Highlights practical considerations for data sharing, metadata completeness, and governance—key factors for scalable monitoring frameworks used in policy evaluation and future planning.