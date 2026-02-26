# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) Normalised Difference Vegetation Index (NDVI) in saltmarsh and mudflat habitats

## Overview
- NDVI surface reflectance dataset for saltmarsh and mudflat habitats as part of the CBESS project.
- Measured using an OceanOptics USB2000 spectrometer to capture surface reflectance; NDVI calculated in Matlab.
- Collected during CBESS field campaigns in winter and summer 2013; no planned repeat sampling.
- Staff responsible: Timothy Hill.
- Two contrasting geographic regions: Essex (saltmarsh/mudflat) and Morecambe Bay (saltmarsh/mudflat), chosen to represent different soil types, inundation regimes, creek structures, and vegetation.

## Data collection and methods
- Locations and habitats:
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM) – saltmarsh and mudflat sites with clay soils.
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS) – saltmarsh and mudflat sites with sandy soils and distinct hydrology.
- Quadrat-based sampling:
  - Randomly allocated 22 quadrats of size 1 x 1 m at each site.
  - Four spatial scales: A = 1 quadrat; B = 3 quadrats (1–10 m apart); C = 6 quadrats (10–100 m apart); D = 12 quadrats (100–1000 m apart).
  - Quadrats are common to all CBESS quadrat data; NDVI measured before any destructive sampling.
- Instrumentation and procedure:
  - Reflectance measured with OceanOptics USB2000 spectrometer, 1.5 m above ground.
  - Data logging via OOBase32 Version 2.0.1.3 on a laptop.
  - Measurement steps per quadrat: adjust integration time for white reference ~75% of max; spectral averaging for short integration times; record dark and white references; perform NDVI measurement; repeat if ambient light changed during steps.
  - Measurements under variable light conditions discarded.
  - For each quadrat: record associated OOBase file numbers and percentage cloud/water cover; capture additional relevant notes.
- NDVI calculation and processing:
  - NDVI calculated in Matlab using the Field Spectroscopy Facility Post Processing Toolbox (FSFPostProcessing1.3.8).
  - Data stored in CSV format; “NA” cells indicate missing data.

## Dataset structure and content
- Dataset fields (examples):
  - Row Number: Sorting index (numeric).
  - Season: Winter (W) or Summer (S).
  - Location: Morecambe (M) or Essex (E).
  - Site: Morecambe – Cartmel Sands (CS), Warton Sands (WS); Essex – Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
  - Habitat: Mudflat (MF) or Saltmarsh (SM).
  - Quadrat Number: 1–22.
  - Scale: A (1 m), B (1–10 m), C (10–100 m), D (100–upper limit).
  - NDVI: NDVI value (numeric).
- File format: CSV.
- Data completeness: Some missing data indicated by NA cells.

## Quality, provenance, and governance
- Data quality controls:
  - NDVI calculated after standardized collection procedures; measurements discarded if light conditions were unsuitable.
  - White reference targeted at ~75% of spectrometer maximum; calibration and dark/white references captured for each quadrat.
  - Random quadrats and standardized spatial scales support comparability across sites and habitats.
- Provenance:
  - Sampling designed to reflect contrasting sediment types and inundation regimes across Essex and Morecambe Bay.
  - Documentation includes site descriptions, habitat types, and sampling design to enable reproducibility and re-use.
- Metadata and discoverability:
  - Detailed description of procedures, instruments, and processing steps.
  - Structured field descriptions and explicit data fields to facilitate understanding and integration with other CBESS data.

## Access, use, and reuse considerations
- Data format and documentation support reuse in cross-site analyses of NDVI across saltmarsh and mudflat habitats.
- Clear metadata on sampling design, instrumentation, processing, and quality decisions (e.g., discarding data under variable light).
- No repeats planned within this dataset, which informs its suitability for snapshot analyses rather than temporal trend assessment.
- Timothy Hill is the point of contact for dataset details and stewardship.

## Alignment with Data Leaders’ aims and challenges
- Addresses the system-wide view of data collection by detailing sites, habitats, and sampling design, enabling cross-site data integration.
- Supports user needs through explicit metadata, methodological transparency, and data quality controls.
- Mitigates data fragmentation by providing a cohesive dataset with standardized quadrat sampling and clear NDVI computation procedures.
- Highlights governance aspects relevant to data standards and metadata (e.g., CSV format, explicit field definitions, and quality notes), though the absence of repeated measurements may limit longitudinal analyses.
- Illustrates practical handling of access barriers and data discoverability through thorough documentation and structured data formats.