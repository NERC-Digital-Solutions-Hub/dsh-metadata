# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) Meteorological Data for Cartmel Sands, Morecambe

- Purpose and scope
  - Meteorological measurements at Cartmel Sands, Morecambe, intended to support environmental monitoring and interpretation of coastal biodiversity and ecosystem service sustainability.
  - Contextual comparison across Essex and Morecambe Bay habitats described to represent contrasting sediment types and inundation regimes, aiding interpretation of site-specific climate impacts.

- Study sites and sampling design
  - Primary site: Cartmel Sands (CS), Morecambe.
  - Additional context: Essex and Morecambe Bay saltmarsh and mudflat sites used to illustrate habitat contrasts (soil types, inundation, vegetation).
  - Monitoring period: 31 May 2013 to 26 January 2015.
  - Sampling frequency: Half-hourly mean values for most variables; select variables recorded at 15-minute intervals.

- Measurements and equipment
  - Variables observed: Air temperature (T_air), Soil temperature at 5 cm (T_soil_5cm), Soil temperature at 10 cm (T_soil_10cm), Relative humidity (RH), Net radiation (Net_rad), Photosynthetically active radiation (PAR), Precipitation (Precip), Wind speed (Wind_Spd), Wind direction (Wind_Dir), Vapour Pressure Deficit (VPD).
  - Instrumentation:
    - Data logger: Campbell Scientific CR5000.
    - Wind: CSAT3 anemometer at 4.3 m on a lattice tower (10 Hz measurements).
    - Air temperature and humidity: Vaisala MP103A (converted to VPD).
    - Precipitation: EML ARG100 tipping bucket rain gauge.
    - Net radiation: Kipp and Zonen NR Lite.
    - PAR: Skye Instruments SKP215.
    - Soil temperatures: Type T thermocouples.
  - Data processing: mean values computed in Matlab; time stamps reference the middle of the half-hour period (e.g., 00:15 for 00:00–00:30).

- Data processing and quality control
  - Calibration and data quality:
    - 10 Hz wind data filtered for wind shadowing and quality flags before averaging to half-hour means.
    - Other meteorological measurements averaged to half-hourly means; data quality flags used to filter problematic wind data.
  - Data checking: wind measurements screened using data quality flags from CSCSATA and considerations of wind shadowing.
  - Data gaps: gaps indicate sensor malfunctions or power loss; NA values denote non-performed measurements.

- Data structure and metadata
  - File format: CSV.
  - Dataset fields (examples): Row Number, Season (Winter/W), Location (Morecambe/Essex), Site (CS, WS, WP; AH, FW, TM for Essex), Habitat (Mudflat, Saltmarsh), Quadrat Number, Scale (A-D with defined meters), Year, Month, Day, Hour, Minute, T_air, T_soil_5cm, T_soil_10cm, RH, Net_rad, PAR, Precip, Wind_Spd, Wind_Dir, VPD.
  - Description of data lineage and measurement details included to support reproducibility and verification.

- Data availability and governance considerations (relevant to monitoring frameworks)
  - Metadata and field definitions are provided to facilitate data integration, verification, and reuse in monitoring frameworks.
  - Emphasizes need for data openness, provenance (origin of sensors and processing steps), and clear documentation of data handling and quality checks.
  - Highlights typical challenges for monitoring bodies: data gaps, metadata adequacy, data transformation needs, and the importance of transparent data governance and sharing practices.