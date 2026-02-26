# Meteorological data from Glencorse ammonia enhancement site near UKCEH, Edinburgh (2023-2024)

## Overview
- Meteorological and environmental data collected at the Glencorse ammonia enhancement site, near UKCEH, Edinburgh (latitude 55.8539, longitude -3.2151, altitude 200 m).
- Study context: ammonia enhancement experiment; wind conditions below the forest canopy influence the experimental setup.
- Time period: 1 January 2023 to 31 December 2024; all data are recorded in GMT.
- This dataset extends the earlier 2021-2022 dataset from the same site.

## Dataset scope and content
- Data volume: 70,176 measurements across 41 parameters.
- Data captured at a 16 m mast (extending 2 m above the canopy) with measurements at four heights, plus above- and below-canopy measurements for several parameters.
- Measured variables include:
  - Atmospheric: air temperature (multiple heights), relative humidity, wind speed and direction, rainfall, barometric pressure, leaf wetness (multiple layers), photosynthetically active radiation (PAR), total solar radiation.
  - Soil: volumetric water content, electrical conductivity, and temperature at three depths.
  - Canopy-related: leaf wetness at various canopy layers, below- and above-canopy radiation and wind metrics.
- Data structure: stored as a CSV with 15-minute averaged records derived from 20-second raw measurements.
- File contents include detailed per-row metadata such as timestamp, height, instrument maker, instrument type, and a description for each parameter.

## Data collection and timing
- Sampling cadence: instrument readings every 20 seconds, averaged to 15-minute intervals.
- Sensor setup covers multiple heights and regions (below canopy, ground flora layer, tree canopy, top of canopy) to capture vertical variation.
- Data collected using a range of manufacturers and instruments (e.g., Vaisala, Campbell Scientific, METER Environment, EML, Skye Instruments).

## Quality control and data processing
- Quality assurance performed via visual checks to identify and remove obvious instrument malfunctions, misprogramming, and power-cut related errors.
- Gaps encountered due to sensor replacement and related downtime; some data omissions are acknowledged.
- Data have been cleaned for obvious errors prior to release; still reflect typical field collection limitations.

## Data structure and metadata
- 41 parameters are documented with extensive header details in the CSV, including:
  - Timestamp fields (with 15-minute timestamps)
  - Height (m), Manufacturer, Instrument, Description
  - Parameter-specific columns (e.g., Rain, Throughfall, LWS1–LWS4, AirT1–AirT4, RH1–RH4, Soil_VWC1–VWC3, Soil_EC1–EC3, Soil_T1–T3, WS_Cup1–Cup4, PAR1–PAR2, Total_Solar1–2, WXT_WS1–2, WXT_WD1–2, WXT_AirT1–2, WXT_RH1–2, WXT_BP1–2)
- Units and height associations are detailed for each parameter, aiding data standardization and interoperability.

## Provenance and related work
- This dataset is an extension of the 2021-2022 Glencorse study (Deshpande et al., 2024b) and is linked to related analyses (Deshpande et al., 2024a) on ammonia deposition and concentrations.
- Funding for facility establishment provided by UKRI GCRF South Asian Nitrogen Hub and UKCEH National Capability for UK Challenges Programme.

## Access, usage, and governance notes
- Primary references for methodology and experimental design: Deshpande et al. (2024a) and Deshpande et al. (2024b).
- Data is provided as a CSV file; detailed metadata and context are described in the accompanying publications.
- For data governance: the dataset exemplifies standard data stewardship practices—clear instrumentation metadata, multi-height and multi-sensor data, explicit quality control steps, and documentation of data gaps due to operational factors. Ensures traceability to instrumentation, locations, timestamps, and data processing steps.
- Suggestion for stewardship: ensure continued alignment with metadata standards (e.g., instrument provenance, height, sensor type, units, data quality flags) and maintain notes on any future reprocessing or gap-filling to support discoverability and reuse.