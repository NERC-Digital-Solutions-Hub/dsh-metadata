# Meteorological and atmospheric dust data from Kangerlussuaq, southwest Greenland, 20172019

- Purpose and scope
  - A multi-file data collection of meteorological, atmospheric dust, and dust-deposition measurements from two primary sites in southwest Greenland (Ridge and SS85) and five deposition traps across several locations.
  - Data designed for map-based visualization and spatial analysis of dust, weather conditions, and deposition patterns.

- Datasets and key variables
  - DUSTY_DustTrak.csv
    - Dust concentration measurements (PM1, PM2.5, RESP, PM10, Total)
    - Sites: Ridge and SS85
    - Instrument: TSI DustTrak DRX Environmental Monitor (inlet ~2.5 m above ground)
    - Temporal resolution: average per 1 minute, data aggregated every 5 minutes
  - DUSTY_Weather_Station_Temperature_and_Humidity_Data.csv
    - Air temperature, relative humidity, absolute humidity, dew point
    - Sites: Ridge and SS85
    - Instrument: Omega OMYL-RH20 (~1 m above ground)
    - Temporal resolution: 1 reading every 10 minutes
  - DUSTY_Weather_Station_Wind_Data.csv
    - Wind speed (mean, max, min) and wind direction
    - Sites: Ridge and SS85
    - Instrument: RMYoung 5013 (2.5 m above ground)
    - Temporal resolution: 1 reading every 5 minutes
  - HDT_Deposition_Data.csv
    - Dust deposition measurements (final areal dust deposition in gm^-2 day^-1)
    - Locations: five sites (SS906, Ridge, SS17b, SS1590, SS85)
    - Trap setup: Hall Deposition Trap, head height 1.5–1.8 m
    - Seasonal operational windows (Spring to Autumn/Winter 2017–2019)
    - Processing details: LOI and mass-based deposition with trap-specific protocols
  - 1 = Particle-size data for deposited dust (data files PSA906_DUST_HDT.csv, PSAR_DUST_HDT.csv, PSA17b_DUST_HDT.csv, PSA1590_DUST.csv, PSA85_DUST_HDT.csv)
    - Particle-size distribution (0.375–2000 µm) analyzed with a laser sizer
    - Locations: five sites (SS906, Ridge, SS17b, SS1590, SS85)
    - Seasonal sampling windows as above
    - Data structure: size (µm) and trap-specific values for HDT1–HDT4/5
    - Units: areal deposition per season (gm^-2 day^-1) for aggregated distributions

- Locations and spatial context
  - Ridge: 67°3'36.0432"N, 50°26'9.5208"W
  - SS85: 67°0'9.522"N, 51°0'39.114"W
  - Other deposition sites include SS906, SS17b, SS1590
  - Spatially distributed to enable mapping of dust concentration, deposition, and meteorological gradients

- Temporal coverage and sampling
  - Dust concentration and weather data span multiple periods in 2018 and 2019 (specific start/end dates per site and sensor)
  - Deposition and particle-size data organized by seasonal blocks (Spring, Summer, Autumn/Winter) from Spring 2017 through Autumn 2018 and into 2019
  - Deposition traps deployed per location with 4–5 traps per site; some missing data due to traps not recovered or damage

- Data quality, gaps, and limitations
  - Missing data: high proportions of missing measurements per sampling period due to power loss, auto-zero malfunctions, or equipment faults
  - Wind, temperature, humidity, and dust data exhibit intermittent gaps; deposition data may have traps unavailable or damaged
  - Particle-size data are aggregated across multiple traps to produce site-level distributions where individual trap data may be incomplete
  - Data standards and harmonization considerations needed when integrating across sites, resolutions, and seasons

- Data structure and formats
  - CSV/Excel-based data files with clear column definitions
  - Common fields across datasets: Date/Time, Site (Ridge, SS85, etc.)
  - Specific variable columns per dataset (e.g., PM1, PM2.5, RESP, PM10, Total; Temperature, Humidity, Absolute Humidity, Dew Point; Wind speeds and direction)
  - Particle-size data organized by Size (µm) and trap numbers; seasonal context embedded in dataset headings
  - Units
    - Dust concentrations: mg/m^3
    - Temperature: degrees Celsius
    - Humidity: %
    - Absolute humidity: g/m^3
    - Dew point: degrees C
    - Wind: m/s and degrees
    - Deposition: g/m^2/day

- GIS-oriented considerations and potential uses
  - Create multi-layer maps showing spatial distribution of dust concentrations, wind fields, and deposition intensities
  - Integrate meteorological fields with deposition data to explore drivers of dust deposition
  - Use time-enabled GIS visualization to compare seasonal patterns across sites
  - Join with site polygons or point locations to assess exposure or impact over time
  - Combine particle-size distributions with deposition and location to analyze particle-size spatial trends

- Notes on practical use and integration
  - Ensure temporal alignment when joining datasets (e.g., match 5-minute dust/wind data with 10-minute temperature/humidity data)
  - Account for missing data in analyses and use appropriate imputation or masking strategies for GIS visualizations
  - Confirm site identifiers and coordinates consistency across files for accurate spatial joins
  - The dataset provides robust spatial coverage and seasonal context suitable for policy-relevant mapping and communications

- Data availability and provenance
  - Data files are organized with explicit naming conventions indicating site, sensor type, and deposition data
  - Presentation of measurement protocols (sampling, retrieval, LOI processing) supports transparency and reproducibility for GIS analyses