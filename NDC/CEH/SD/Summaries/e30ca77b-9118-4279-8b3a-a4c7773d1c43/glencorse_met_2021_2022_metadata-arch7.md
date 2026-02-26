# Meteorological data from Glencorse ammonia enhancement site near UKCEH, Edinburgh (2021-2022)

## Overview
- Point meteorological dataset from a 16 m mast located in Glencorse woodland (near UKCEH, Edinburgh) at coordinates 55.8539 N, -3.2151 W, altitude 200 m.
- Timeframe: 28 May 2021 to 5 January 2023 (GMT).
- 56,154 measurements covering 41 parameters.
- Data designed to inform ammonia enhancement experiments; wind conditions below the canopy drive the experiment.

## Data collection
- Measurements taken from a single mast with sensors at multiple heights (four heights for many variables).
- Variables include:
  - Air temperature and relative humidity (AirT1–AirT4; RH1–RH4)
  - Leaf wetness sensors (LWS1–LWS4)
  - Rainfall (Rain) and below-canopy throughfall (Throughfall)
  - Soil water content (Soil_VWC1–3), soil electrical conductivity (Soil_EC1–3), soil temperature (Soil_T1–3)
  - Wind speeds at various layers (WS_Cup1–4) and wind-related parameters (WXT_WS1/2; WXT_WD1/2)
  - Photosynthetically active radiation (PAR1) and total solar radiation (Total_Solar1–2)
  - Additional meteorological context (barometric pressure, wind direction)
- Sampling rate: data recorded every 20 seconds, averaged to 15-minute intervals.
- All data are recorded in GMT.
- The documentation references a detailed description of experimental design, methodology, and findings in a 2024 publication by Deshpande et al.

## Quality Control
- Visual checks to identify and remove obvious instrument errors, datalogger issues, and power-cut artifacts.
- Gaps primarily due to sensor replacement; some data gaps remain.

## Data structure and variables
- Data format: CSV with 56,154 rows and 41 parameters.
- Core fields (examples):
  - Timestamp (15-minute intervals in dd/mm/yyyy hh:mm)
  - Height (m)
  - Manufacturer
  - Instrument
  - Description
  - Sensor measurements: Rain, Throughfall, Leaf Wetness (LWS1–LWS4), AirT1–AirT4, RH1–RH4, Soil_VWC1–3, Soil_EC1–3, Soil_T1–3, WS_Cup1–4, PAR1, Total_Solar1–2, WXT_WS1–2, WXT_WD1–2, WXT_AirT1–2, WXT_RH1–2, WXT_BP1–2
- Each sensor row includes units and height context, with notes indicating what each measurement represents (e.g., below-canopy vs. above-canopy, proximity to forest floor vs. canopy layers).
- The data provide a multi-height, multi-parameter view of microclimate conditions relevant to ammonia enhancement experiments.

## Temporal and spatial context
- Spatial context: single fixed mast at a defined location in Glencorse woodland; not a gridded dataset but suitable for site-scale GIS analysis and temporal visualization around a fixed point.
- Temporal context: 20-second raw data, aggregated to 15-minute means; time window spans nearly 20 months.
- Can be used to analyze spatially inferred processes (e.g., ammonia deposition in relation to near-ground vs. canopy microclimates) by associating measurements with their height and canopy layer.

## GIS and data visualization considerations
- Ideal uses:
  - Time-series visualization of selected variables at different heights to examine vertical microclimate structure.
  - Spatially anchored analyses around a fixed point for modeling ammonia enhancement effects (e.g., dependency on wind direction/speed, canopy temperature and humidity).
  - Integration with external spatial layers (topography, vegetation, land cover) to contextualize meteorological conditions.
- Data integration notes:
  - Units and height context must be harmonized when combining with other datasets.
  - Some fields show formatting inconsistencies in the documentation; verify field mappings and sensor labels in the CSV.
  - The multi-height structure requires careful handling to produce layer-specific maps or vertical profiles.
- Data quality considerations for GIS:
  - Gaps from sensor maintenance; account for missing intervals in analyses.
  - Ensure consistent time zone handling (GMT) and alignment across variables.
  - Validate sensor cross-references (Manufacturer, Instrument) to avoid misclassification when merging datasets.

## Related references and funding
- Primary reference: Deshpande AG, Jones MR, van Dijk N, Mullinger NJ, Harvey D, Nicoll R, et al. Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments. Atmos Environ. 2024.
- Funding: UKRI GCRF South Asian Nitrogen Hub.