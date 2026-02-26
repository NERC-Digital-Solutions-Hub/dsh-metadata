# Meteorological data from Glencorse ammonia enhancement site near UKCEH, Edinburgh (2021-2022)

- Purpose: Provides meteorological data to support the Glencorse ammonia enhancement experiment and subsequent analyses of ammonia deposition to forest ecosystems; data underpin wind-controlled NH3 enhancement studies (Deshpande et al. 2024).

## Study site and data collection

- Location: Glencorse woodland, near UKCEH, Edinburgh (coordinates 55.8539 N, -3.2151 W; altitude 200 m).
- Instrumentation: 16 m tall mast installed next to the ammonia enhancement manifold; measurements extend from near the forest floor to above the canopy.
- Height and variables:
  - Air temperature, relative humidity, leaf wetness, and wind speed measured at four heights.
  - Rainfall, wind direction, barometric pressure, photosynthetically active radiation (PAR), and total solar radiation recorded above- and below-canopy.
  - Soil volumetric water content (VWC), electrical conductivity (EC), and temperature measured at three depths.
- Temporal resolution: Data collected every 20 seconds; 15-minute averages derived for analysis.
- Timeframe: 28 May 2021 to 5 January 2023; all data in GMT.

## Quality control and data handling

- Quality control: Visual checks; removal of obvious errors due to instrument malfunction, datalogger programming issues, and power cuts.
- Gaps: Occasional gaps arising from sensor replacement or maintenance.

## Dataset structure and contents

- Size and scope: 56,154 measurements across 41 parameters.
- Format: CSV file with detailed column structure, including:
  - Timestamp, Height, Instrument, Description, and per-measurement metadata.
  - Variables such as Rain, Throughfall, leaf wetness sensors (LWS1–LWS4) at multiple heights; AirT and RH at several canopy layers; Soil_VWC, Soil_EC, Soil_T at multiple depths; wind speed and direction at various layers; PAR and total solar radiation at multiple positions; and a range of WXT (weather) variables.
- Layer and height descriptors: Column names encode measurement height and canopy layer (ground floor, ground flora, tree canopy, top of canopy, etc.).

## Funding and provenance

- Funding: UKRI GCRF South Asian Nitrogen Hub.
- References for methodology and context: Deshpande AG, Jones MR, van Dijk N, Mullinger NJ, Harvey D, Nicoll R, et al. Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments. Atmos Environ. 2024 Jan; doi:10.1016/j.atmosenv.2023.120325.