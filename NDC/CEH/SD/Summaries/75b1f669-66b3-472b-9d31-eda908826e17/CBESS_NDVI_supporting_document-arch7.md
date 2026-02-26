# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) Normalised Difference Vegetation Index (NDVI) in saltmarsh and mudflat habitats

- Overview
  - NDVI dataset measuring surface reflectance as Normalised Difference Vegetation Index (NDVI) within CBESS coastal habitats (saltmarsh and mudflat).
  - Part of the CBESS field campaign conducted in winter and summer 2013; intended as a one-off data collection with no planned repeats.
  - Staff responsible: Timothy Hill.

- Locations and site design
  - Regions and sites:
    - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
    - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS).
  - Site descriptions:
    - Saltmarsh: contrasts in soil types—clay soils in Essex; sandy soils in Morecambe Bay.
    - Mudflat: Essex mudflats with cohesive clays, mud, silt; Morecambe Bay mudflats with coarse, mobile sediments.
  - Coordinates (approximate):
    - Essex: AH ~ 51.783°N, 0.867°E; FW ~ 51.817°N, 0.967°E; TM ~ 51.683°N, 0.933°E.
    - Morecambe Bay: CS ~ 54.167°N, 3.000°W; WS ~ 54.133°N, 2.800°W.
  - Sampling design:
    - Randomly allocated quadrats at each site to standardize NDVI measurement and comparability across sites.
    - Quadrats: 22 per mudflat and saltmarsh site; four spatial scales defined (A: 1 quadrat; B: 3 quadrats at 1–10 m apart; C: 6 quadrats at 10–100 m apart; D: 12 quadrats at 100–1000 m apart).

- Data collection and processing
  - Instrumentation and measurement:
    - OceanOptics USB2000 spectrometer with 1.5 m fibre optic; measurements taken 1.5 m above ground.
    - Data logging with OOIBase32 (Version 2.0.1.3); NDVI calculated in Matlab using Field Spectroscopy Facility Post Processing Toolbox (FSFPostProcessing1.3.8).
  - Measurement protocol:
    - At each quadrat: adjust integration time so white reference peak is ~75% of max; use spectral averaging for short integration times; record dark and white reference; perform NDVI measurement.
    - If ambient light conditions changed during quadrat measurement, the measurement is repeated; measurements under variable light conditions are discarded.
    - For each quadrat, note the number of OOBase files and percentage of cloud and water cover, plus other relevant context.
  - Data formats:
    - Primary data stored in CSV format; NA entries indicate missing data.

- Dataset contents and structure
  - Key variables observed: NDVI (Normalised Difference Vegetation Index) values.
  - Metadata and field descriptors (as encoded in the dataset):
    - Row Number: unique sort order identifier.
    - Season: Winter (W) or Summer (S).
    - Location: Morecambe (M) or Essex (E).
    - Site: Morecambe—Cartmel Sands (CS) or Warton Sands (WS); Essex—Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
    - Habitat: Mudflat (MF) or Saltmarsh (SM).
    - Quadrat Number: 1–22.
    - Scale: A (1 m), B (1–10 m), C (10–100 m), D (100 m to upper limit).
    - NDVI: numeric NDVI value.
  - Data notes:
    - Some cells may be NA where data are unavailable.

- Quality assurance and provenance
  - QA procedures include standardized quadrat placement, calibration steps, and documentation of sampling conditions (cloud cover, water cover) for each quadrat.
  - Explicitly records conditions that may affect data quality (e.g., variable light conditions leading to discarded measurements).
  - Single-phase data collection with no planned repeat measurements.

- Usage notes for GIS specialists
  - Provides multi-scale NDVI observations across contrasting saltmarsh and mudflat habitats, suitable for map-based visualization and spatial analysis.
  - Contains explicit scale-based grouping (A–D), enabling analysis at finer to broader spatial resolutions.
  - Metadata-rich (season, site, habitat, location, and sampling specifics) supports careful geospatial integration and cross-site comparisons.
  - Ensure proper handling of NA values and interpretation of NDVI values within the context of in situ reflectance measurements.