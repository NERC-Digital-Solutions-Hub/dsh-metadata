# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) Meteorological Data for Abbotts Hall, Essex

- Overview and aim
  - Meteorological measurements at the Abbotts Hall site in Essex, intended to support understanding of coastal biodiversity and ecosystem services.
  - Data collected to represent contrasting habitats (saltmarsh, mudflat) and sediment types, with Essex and Morecambe Bay sites included for comparison.
  - Time period: half-hourly mean values from 15/12/2012 to 27/01/2015.

- Location and site descriptions
  - Observation locations: Essex – Abbotts Hall (AH); additional Essex sites Fingringhoe Wick (FW) and Tillingham Marshes (TM); Morecambe – Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
  - Habitat types: Mudflat and Saltmarsh; soil types include clay (Essex) and sandy (Morecambe Bay).
  - Grid/site context includes coordinates for Abbotts Hall and habitat-specific site details.

- Variables observed and measurement specifics
  - Primary meteorological variables: Air temperature (T_air), soil temperatures at 10 cm, 20 cm, 30 cm (T_soil_10cm, T_soil_20cm, T_soil_30cm), Relative Humidity (RH), Net Radiation (Net_rad), Photosynthetically Active Radiation (PAR), Precipitation (Precip), Wind Speed (Wind_Spd), Wind Direction (Wind_Dir), Vapour Pressure Deficit (VPD).
  - Measurement cadence: Wind at 10 Hz; all other variables at 1/60 Hz (one measurement per minute); mean values calculated over half-hour intervals.
  - Time reference: The middle of each half-hour period (e.g., 00:15 for 00:00–00:30).

- Instrumentation and data collection procedures
  - Data logging: Campbell Scientific dataloggers.
  - Wind: CSAT3A anemometer at 4.3 m on a lattice tower; wind data processed with quality flags.
  - Other variables: Vaisala HMP155A for temperature/humidity; EML ARG100 tipping bucket rain gauge for precipitation; Kipp and Zonen NR Lite for net radiation; Skye Instruments SKP215 for PAR; CS 107 thermistors for soil temperatures.
  - Data processing: Mean half-hourly values computed in Matlab; time stamps refer to the mid-point of the half-hour window.

- Data quality and quality control
  - Wind measurements filtered for wind shadowing and data quality flags before averaging to half-hour means.
  - Other variables averaged to half-hourly means; quality control relies on instrument-specific flags (e.g., wind data flags).
  - Data gaps are documented and attributed to sensor malfunction or power loss.
  - NA values indicate measurements not performed.

- Data formats and metadata structure
  - File format: CSV.
  - Dataset field descriptions include:
    - Temporal metadata: Year, Month, Day, Hour, Minute; Season (Winter, Summer).
    - Spatial/locational metadata: Location (Morecambe or Essex), Site (e.g., AH, FW, TM; CS, WS, WP), Habitat (Mudflat or Saltmarsh).
    - Sampling/scale metadata: Quadrat Number, Scale (A–D representing different spatial extents).
    - Measured variables and units: T_air (°C), T_soil_10cm (°C), T_soil_20cm (°C), T_soil_30cm (°C), RH (%), Net_rad (W/m²), PAR (μmol m⁻² s⁻¹), Precip (mm), Wind_Spd (m s⁻¹), Wind_Dir (degrees from North), VPD (kPa).
  - Row numbering serves to preserve original input order.

- Data governance and hosting notes for stewards
  - Data are prepared for sharing via relevant portals and catalogues; documentation should accompany uploads to maintain interpretability across systems.
  - Clear provenance is provided through instrument names, logging routines, and processing steps (e.g., half-hour averaging, wind-shadow filtering, and QC flags).
  - Documentation highlights data limitations, including data gaps and non-performance periods, to support proper discovery and reuse.
  - Because the dataset uses multiple systems and formats and covers several sites/habitats, ensure consistent metadata across datasets to support interoperability and discoverability.