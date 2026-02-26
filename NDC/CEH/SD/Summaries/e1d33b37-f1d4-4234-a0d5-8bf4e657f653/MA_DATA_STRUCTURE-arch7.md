# UK Environmental Change Network (ECN) meteorology data: 1992-2012

- Overview
  - Hourly meteorology summaries derived from 5-second Automatic Weather Station (AWS) data, collected across ECN sites from 1992 to 2012.
  - Data are suitable for GIS map-based visualisations and analysis, with site coordinates and multi-AWS at the same location.

- Data origin and governance
  - Originator: ECN Data Centre, Centre for Ecology and Hydrology.
  - Owners: UK ECN programme, sponsored by a consortium of government departments/agencies (e.g., DEFRA, Natural England, NERC, and others).
  - Usage acknowledgement requested; please send one reprint of any publication citing the data.

- Data content and structure
  - Primary content: hourly summaries computed from high-frequency AWS measurements.
  - Site and deployment details:
    - Multiple AWS at many sites; AWS replacements flagged by AWSNo; awareness of concurrent AWS is important.
    - Site codes (T01–T12) with coordinates and AWS1/AWS2 active date ranges.
  - Example variables and units (from the Fields/table definitions):
    - Albedo and radiation: ALBGRD (Albedo Ground) W m-2, NETRAD (Net Radiation) W m-2, SOLAR (Solar Radiation) W m-2.
    - Temperature: DRYTMP (Dry bulb temperature) °C, STMP10/STMP30 (Soil temperature at 10 cm/30 cm) °C, WETTMP (Wet bulb temperature) °C.
    - Humidity and moisture: RH (%) relative humidity, SWATER (Soil moisture - gypsum block), SWATER_T (theta probe at 20 cm) %, WC (volumetric soil moisture) m3/m3, STMP10/30 as above.
    - Precipitation and surface: RAIN (Rainfall total) m, SURWET (Surface wetness) minutes in hour, RAIN-related notes.
    - Radiation and energy balance: NETRAD (Net Radiation) W m-2, SOLAR (Solar Radiation) W m-2.
    - Air and wind: DRYTMP_R (temperature sensor context), WDIR (Wind direction) degrees, WSPEED (Wind speed) m/s, WETTMP (Wet bulb temperature) °C.
  - Data organization: structured tables defining Field names, descriptions, units, and data types; separate site code mappings with coordinates and active date ranges.

- Spatial and temporal coverage
  - Spatial: 12 ECN sites with precise geographic coordinates provided.
  - Temporal: data cover 1992–2012, with hourly summaries and periods when AWS units were replaced or operated concurrently at sites.

- Data quality and usage guidance
  - Always consult accompanying quality information; quality flags accompany measurements.
  - When aggregating across sites or multiple AWS at a site, account for AWSNo to avoid mixing concurrent sensors.
  - Protocol MA.pdf (in the ECN data documentation) provides reuse guidance and methodological details.

- Access and documentation
  - Access via the ECN Data Centre (ECN) and the EIDC Hub data holdings page.
  - Documentation and protocol references included; please acknowledge data use and consult the Protocol MA.pdf for reuse details.

- Practical GIS considerations
  - For map-based products, join meteorological variables to site coordinates and (where relevant) to AWSNo to distinguish sensors at the same location.
  - Use time-structured data to create temporal maps or time-series visualisations (hourly resolution).
  - Leverage site-specific date ranges to filter data for consistent spatial-temporal analysis.
  - Incorporate data quality filters to improve reliability of map outputs and analyses.