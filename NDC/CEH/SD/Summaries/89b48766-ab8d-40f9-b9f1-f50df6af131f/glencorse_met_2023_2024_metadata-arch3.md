# Meteorological data from Glencorse ammonia enhancement site near UKCEH, Edinburgh (2023-2024)

- Overview
  - Long-term meteorological and soil measurements at a forest site to support ammonia enhancement experiments and related environmental monitoring.
  - Data collected 1 January 2023 to 31 December 2024; GMT time; 70,176 measurements across 41 parameters.
  - Extends the 2021–2022 dataset from the same site; design and methodology aligned with Deshpande et al. (2024a, 2024b).

- Data collection details
  - Site and setup: 16 m mast placed 2 m above the forest canopy at Glencorse woodland, next to the ammonia enhancement manifold (coordinates provided in the report).
  - Measurements and heights:
    - Four heights for air temperature, relative humidity, leaf wetness, and wind speed.
    - Above- and below-canopy measurements for rainfall, wind direction, barometric pressure, photosynthetically active radiation (PAR), and total solar radiation.
    - Soil measurements (volumetric water content, electrical conductivity, temperature) at three depths.
  - Cadence: data collected every 20 seconds and averaged to 15-minute intervals.
  - Focus: wind conditions measured below the canopy drive the ammonia enhancement experiment.

- Quality control and data processing
  - Data quality: visual checks; removal of obvious errors due to instrument malfunction, datalogger issues, and power cuts.
  - Gaps: some data gaps due to time needed to replace faulty sensors.

- Data structure and variables
  - Dataset size: 70,176 measurements of 41 parameters.
  - Format: CSV file with columns including Timestamp, Height, Manufacturer, Instrument, Description, plus numerous sensor-specific fields.
  - Key variables (examples):
    - Rain and Throughfall (above/below canopy), with height and instrument metadata.
    - Leaf Wetness Sensors (LWS1–LWS4) at multiple canopy-related heights.
    - Relative Humidity (RH1–RH4) and Air Temperature (AirT1–AirT4) at corresponding heights.
    - Soil measurements: Soil_VWC1/2/3, Soil_EC1/2/3, Soil_T1/2/3 at near-surface, 10 cm, and 15 cm depths.
    - Wind speeds (WS_Cup1–WS_Cup4) at various layers and wind directions (WXT_WD1/WD2) with corresponding temperatures and humidities (WXT_AirT1/AirT2, WXT_RH1/RH2) and barometric pressures (WXT_BP1/BP2).
    - Light and radiation: PAR (PAR1 Above-canopy, PAR2 Below-canopy), Total_Solar1/Total_Solar2.
    - WXT sensor suite (Vaisala WXT536) measurements for below- and above-canopy conditions (wind speed, wind direction, temperature, humidity, barometer).
  - Data lineage: designed to support analysis of ammonia deposition and related environmental processes; data described in detail in the accompanying Deshpande et al. publications.

- Temporal and spatial coverage
  - Temporal coverage: 01-01-2023 to 31-12-2024 (GMT).
  - Spatio-physical context: measurements taken at four heights on the mast, with separate below- and above-canopy data streams; soil measurements at three depths.

- Metadata, access, and governance
  - Metadata: extensive instrument, height, and sensor details included in the CSV structure (manufacturer, instrument, description, height, etc. for each variable).
  - Data sharing and openness: datasets are documented with metadata and linked publications; underlying data sharing practices referenced but not exhaustively specified in this summary—notes mention collaboration with dataset originators for metadata and data gaps.
  - Data provenance: extension of prior 2021–2022 dataset; linked to the methods and findings described in Deshpande et al. (2024a, 2024b).

- Funding and references
  - Funding: UKRI GCRF South Asian Nitrogen Hub (NE/S009019/1) and UKCEH National Capability for UK Challenges Programme NE/Y006208/1.
  - References: 
    - Deshpande, A. G., et al. Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments, Atmos. Environ., 2024a.
    - Deshpande, A. G., et al. Meteorological data and ammonia concentration and deposition rates from an ammonia enhancement experiment site, Glencorse, UK, 2021-2022, NERC EDS Environmental Information Data Centre, 2024b.