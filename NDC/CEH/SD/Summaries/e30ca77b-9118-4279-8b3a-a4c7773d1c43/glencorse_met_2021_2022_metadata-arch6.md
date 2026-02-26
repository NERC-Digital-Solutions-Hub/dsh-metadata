# Meteorological data from Glencorse ammonia enhancement site near UKCEH, Edinburgh (2021-2022) Deshpande, A.G., Jones, M.R., Mullinger, N. J., Harvey, D., Simmons, I. and Nicoll, R.

## Overview
- Purpose: Meteorological data collection to support the ammonia enhancement experiment; wind conditions below the forest canopy control the experiment.
- Timeframe: 28 May 2021 to 5 January 2023; all times in GMT.
- Location: Glencorse woodland, near Edinburgh (coordinates 55.8539°, -3.2151°, altitude 200 m); 16 m mast extending 2 m above canopy.

## Data collection and sensors
- Measurements include: air temperature, relative humidity, leaf wetness, wind speed (at four heights); rainfall, wind direction, barometric pressure, photosynthetically active radiation (PAR), total solar radiation (above and below canopy); soil volumetric water content (VWC), soil electrical conductivity (EC), soil temperature (T) at three depths.
- Cadence: data recorded every 20 seconds; 15-minute averages computed.
- Outputs are tied to canopy position (below/above) and multiple heights/depths; instrument metadata includes timestamp, height, manufacturer, instrument, and description.
- Typical instruments and sensor families referenced include Vaisala (HMP60), METER Environment leaf sensors, EML rainfall/throughfall, Skye Instruments, Vector Instruments, and Campbell Scientific components.

## Quality control
- Visual checks performed to remove obvious instrument/recording errors due to instrument malfunction, datalogger issues, or power cuts.
- Some data gaps occurred during sensor replacement periods.

## Data structure and format
- Dataset size: 56,154 measurements across 41 parameters.
- Format: CSV file with columns such as Timestamp, Height, Manufacturer, Instrument, Description, and parameter-specific fields (e.g., Rain, Throughfall, LWS1–LWS4, AirT1–AirT4, RH2–RH4, Soil_VWC1–VWC3, Soil_EC1–EC3, Soil_T1–T3, WS_Cup1–WS_Cup4, PAR1, Total_Solar1–Total_Solar2, WXT_WS1–WXT_BP1, etc.).
- Sample column semantics include measurements at various heights (near forest floor, ground flora, canopy layers, top of canopy), and depths (0.5 m, 10 cm, 15 cm) with corresponding units and descriptions.

## Temporal and spatial coverage
- Height levels: near floor (0.5 m), ground flora (~2.0 m), tree canopy (~7.1 m), top canopy (~11.6 m); wind speeds recorded at multiple heights; air temperature and humidity captured at several elevations.
- Soil measurements: VWC, EC, T at surface (~0.5 m), 10 cm, 15 cm depths.
- Radiation and meteorology: below- and above-canopy PAR and total solar radiation; below-canopy wind speeds and directions; barometric pressure.
- All data are logged in GMT and packaged in a single CSV dataset for ease of integration.

## Deliverables for data use
- Cleaned, self-serve-ready data products such as time-series dashboards and pivotable summaries for environmental conditions and potential drivers of ammonia enhancement effects.
- Metadata availability through instrument and sensor descriptors to enable reproducibility and provenance tracking.
- Dataset suitable for analyses related to ammonia deposition estimates and wind-controlled exposure, as described in the associated methodology.

## Funding and references
- Funding: UKRI GCRF South Asian Nitrogen Hub.
- Key reference: Deshpande AG, Jones MR, van Dijk N, Mullinger NJ, Harvey D, Nicoll R, et al. Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments. Atmos Environ. 2024 Jan; doi:10.1016/j.atmosenv.2023.120325.