# Meteorological data from Glencorse ammonia enhancement site near UKCEH, Edinburgh (2023-2024)

- Purpose and scope
  - Meteorological data collected at a 16 m mast near the Glencorse ammonia enhancement manifold in the Glencorse woodland (coordinates 55.8539, -3.2151; altitude 200 m).
  - Extends the 2021-22 dataset from the same site; associated with ammonia enhancement experiments and wind-controlled NH3 deposition studies.

- Data collection details
  - Measurements include air temperature, relative humidity, leaf wetness, wind speed at four heights; rainfall, wind direction, barometric pressure, photosynthetically active radiation (PAR), and total solar radiation above and below the canopy.
  - Soil measurements: volumetric water content (VWC), electrical conductivity (EC), and temperature at three depths.
  - Instrumentation captures data every 20 seconds; results aggregated to 15-minute intervals.
  - All data are recorded in GMT for 2023-01-01 to 2024-12-31.
  - Below-canopy and above-canopy sensors provide context for the ammonia enhancement experiment.

- Data structure and contents
  - CSV dataset with 70,176 measurements across 41 parameters.
  - Columns include: Timestamp, Height (m), Manufacturer, Instrument, Description, plus a wide range of sensor-specific fields (e.g., Rain, Throughfall, LWS1–LWS4, AirT/RH at multiple heights, Soil_VWC/EC/T at multiple depths, WS Cup sensors, PAR, Total_Solar, WXT sensors for wind/pressure/temperature/humidity, etc.).
  - Variable descriptions specify measurement location (near/far from canopy) and the physical quantity (e.g., leaf wetness near the forest floor vs canopy, soil properties at various depths).

- Quality control and data quality
  - Visual quality checks performed; obvious instrument faults, datalogger issues, and power-cut artifacts removed.
  - Some data gaps exist due to sensor replacements.

- Provenance and references
  - Related publications detailing experimental design, methodology, analysis, and findings: Deshpande et al. (2024a) and Deshpande et al. (2024b).
  - Data contribution funded by UKRI GCRF South Asian Nitrogen Hub and UKCEH National Capability for UK Challenges Programme.

- Access, use, and integration notes for data support
  - Dataset suitable for building self-serve data products (dashboards, pivot analyses) to monitor meteorological conditions and their relation to ammonia enhancement experiments.
  - Time series in GMT facilitates synchronization with other environmental datasets.
  - Rich metadata (instrument, height, description) supports data cleaning, harmonisation, and cross-dataset integration.
  - For deeper methodology and dataset context, consult the cited Deshpande et al. publications and the associated Environmental Information Data Centre resources.