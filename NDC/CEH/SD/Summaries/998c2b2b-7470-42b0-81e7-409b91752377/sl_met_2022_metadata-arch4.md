# Meteorological data from Queensberry ammonia enhancement site in Sri Lanka (2022)

- Overview
  - A comprehensive meteorological dataset collected to support an ammonia enhancement experiment near the Queensberry Estate, Sri Lanka, including multi-height atmospheric measurements and soil parameters over 2022.
  - Purpose tied to estimating ammonia deposition and understanding wind-controlled NH3 enhancement effects.

- Data collection details
  - Site setup: 12 m mast extending 5 m above the forest canopy at Queensberry Estate (coordinates 6.9693 N, 80.5911 E; altitude 1645 m).
  - Measurements and layers:
    - Air temperature, relative humidity, and leaf wetness at four heights.
    - Wind speed, wind direction, barometric pressure, photosynthetically active radiation (PAR), and total solar radiation above and below the canopy.
    - Soil volumetric water content (VWC), electrical conductivity (EC), and temperature at three depths.
  - Temporal resolution: instruments sample every 20 seconds; data averaged to 15-minute intervals.
  - Timeframe and time zone: 17 March 2022 to 31 December 2022, Sri Lanka Standard Time (SLST).
  - Experimental relevance: wind conditions measured below the canopy direct the ammonia enhancement experiment.

- Quality control
  - Visual checks performed; obvious instrument malfunctions, datalogger programming issues, and power cuts corrected or removed.
  - Some data gaps occurred during sensor replacement.

- Data structure and format
  - Dataset contains 27,812 measurements across 37 parameters.
  - Provided as a CSV file with columns including: Timestamp, Height, Manufacturer, Instrument, Description, followed by hundreds of sensor-specific fields (e.g., leaf wetness sensors LWS1–LWS4; air temperature and humidity sensors AirT1–AirT4, RH1–RH4; soil sensors Soil_VWC1–3, Soil_EC1–3, Soil_T1–3; wind, PAR, solar radiation sensors; below- and above-canopy sensors).
  - Measurements span multiple canopy layers:
    - Ground flora layer
    - Below-canopy (ground and understory)
    - Above-canopy (tree canopy)
  - Units and metadata are included for each parameter to support data discoverability and reuse.

- Key variables (categories)
  - Atmospheric: AirT1–AirT4, RH1–RH4; wind speed and direction (below and above canopy); barometric pressure; below- and above-canopy air temperatures and humidities; wind-related sensors (WXT series).
  - Surface and radiation: PAR1–PAR2; Total_Solar1–Total_Solar2.
  - Biological and microclimate: Leaf Wetness Sensors LWS1–LWS4.
  - Soil: Soil_VWC1–3, Soil_EC1–3, Soil_T1–3 at surface and depths of 10 cm and 15 cm (as described).
  - Instrumentation and housekeeping: detailed Manufacturer and Instrument fields for each measurement.

- Temporal coverage and access
  - Coverage: 17 March 2022 – 31 December 2022.
  - Format: CSV with time-stamped records at 15-minute intervals (derived from 20-second sampling).
  - Documentation and methods: complete details of experimental design, methodology, analysis, and findings are published in Deshpande et al. (2024).

- Relevance for data leadership
  - Demonstrates end-to-end data lifecycle: from instrument setup, multi-parameter data collection across vertical forest structure, to quality control and structured metadata suitable for integration with other data systems.
  - Supports data governance practices such as data provenance (instrument metadata), data quality notes (gaps, instrument issues), and data discoverability (standardized CSV with descriptive fields).
  - Provides a model for collaborative, data-driven environmental experiments and data sharing within a research community.

- Funding and references
  - Funding: UKRI GCRF South Asian Nitrogen Hub.
  - Reference: Deshpande AG, Jones MR, van Dijk N, Mullinger NJ, Harvey D, Nicoll R, et al. Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments. Atmos Environ. 2024 Jan; doi:10.1016/j.atmosenv.2023.120325.