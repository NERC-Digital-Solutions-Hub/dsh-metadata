# Supporting documentation for: Daily and sub-daily hydrometeorological and soil data (2013-2023) [COSMOS-UK]

- Scope
  - COSMOS-UK network: 51 sites with daily and sub-hourly hydrometeorological and soil moisture data from 2013 to 2023 (end of 2023).
  - Data products: sub-hourly (30-minute) time series and daily derivatives, plus extensive metadata and quality control information.
  - File set: 258 files in total, including site metadata, sub-hourly data and QC/data flags, sub-hourly metadata, daily data and flags, and daily metadata.

- Data holdings and structure
  - Metadata and data files
    - 1 x COSMOS-UK_SiteMetadata_2013-2023.csv (site metadata for 51 sites)
    - 51 x Sub-hourly Hydrometeorological and Soil data files (COSMOS-UK_<SITE ID>_HydroSoil_SH_<YEAR SITE OPENED>-2023.csv)
    - 51 x Sub-hourly QC flags files (COSMOS-UK_<SITE ID>_HydroSoil_SH_<YEAR SITE OPENED>-2023_QC_Flags.csv)
    - 51 x Sub-hourly data flags files (COSMOS-UK_<SITE ID>_HydroSoil_SH_<YEAR SITE OPENED>--2023_Flags.csv)
    - 1 x COSMOS-UK_HydroSoil_SH_2013-2023_Metadata.csv
    - 51 x Daily Hydrometeorological and Soil data files (COSMOS-UK_<SITE ID>_HydroSoil_Daily_<YEAR SITE OPENED>-2023.csv)
    - 51 x Daily data flags files (COSMOS-UK_<SITE ID>_HydroSoil_Daily_<YEAR SITE OPENED>--2023_Flags.csv)
    - 1 x COSMOS-UK_HydroSoil_Daily_2013-2023_Metadata.csv
  - Coverage and format
    - Timeframe: October 2013 – December 2023
    - Sub-hourly data: 30-minute resolution; timestamps end of each 30-minute period (e.g., 12:30 end corresponds to 12:00:01–12:30:00)
    - Daily data: derived metrics (e.g., VWC, SWE, PE) at daily resolution
    - Missing values indicated as -9999
    - Weapons of truth: site IDs in filenames map to network sites; QC and data flags provide provenance on data handling

- Sub-hourly data details (Section 3)
  - Variables (examples)
    - Radiation and energetics: LWIN, LWOUT, SWIN, SWOUT, RN, Q (absolute humidity), RH, PA, TA, WS, WD, UX, UY, UZ, G1, G2
    - Precipitation types: PRECIP (pluvio), PRECIP_TIPPING (tipping bucket), PRECIP_RAINE (rain[e])
    - Soil and moisture: TDT-based soil temperature and volumetric water content at multiple depths (10 cm, 5 cm, 15 cm, 25 cm, 50 cm, 5/10/15/25/50 cm, etc.)
    - Snow and albedo related: SNOW_DEPTH, COSMOS_VWC (CRNS-based VWC), SWE, ALBEDO, PE, GCC (green colour content from PhenoCam)
  - Quality control
    - Two-stage QC: automatic QC tests (flag values) and daily visual inspection
    - QC flags file mirrors data file; QC flags explained in Table 3.1–3.4; non-zero flags indicate tests failed
    - Derived data (e.g., RN and Q) are not QC-tested if they are derived from QC’d inputs
  - Data flags
    - Data flags file indicates data point status: M = Missing (not infilled), U = Unchecked, I = Infilled, E = Estimated
    - Flags provide context on data values beyond QC flags

- Daily data details (Section 4)
  - Derived daily products
    - Volumetric water content (VWC) derived from CRNS
    - Snow water equivalent (SWE)
    - Potential evapotranspiration (PE) via Penman-Monteith
    - GCC (Green Colour Content) from PhenoCam imagery
  - Derived units and aggregation
    - LWIN, LWOUT, SWIN, SWOUT: MJ m-2 day-1
    - RN, PRECIP, PRECIP_TIPPING, PRECIP_RAINE: daily totals
    - PA: daily mean pressure; TA: daily mean air temperature; WS and WD: daily mean wind speed and direction
    - Q, RH, G1, G2, TDT-based soil metrics: daily means
    - GCC: daily maximum value across PhenoCam images for the day
  - PhenoCam GCC notes
    - GCC data derived from masks focusing on surrounding fields
    - GCC data not subjected to formal quality control
  - Completeness
    - Daily data are derived from sub-hourly inputs and inherit QC; completeness indicators available per site

- Infilling (Section 5)
  - Purpose: fill gaps in time series with estimates where appropriate
  - Methods
    - Linear interpolation or order-2 polynomial interpolation
    - Selection criteria based on gap length and surrounding data points
    - RMSE-based guidance: 5000 artificial gaps used to assess performance and select best method per variable
  - Scope
    - Infilling applied to select sub-hourly and daily variables as described in the tables

- Completeness and data quality (Section 6)
  - Completeness figures outline data coverage for Met (precipitation, temperature, pressure, radiation, wind) and Soil (heat flux, soil temperature, VWC)
  - VWC completeness highlighted (CRNS-derived moisture data)

- Instrumentation and site specifics (Section 7)
  - Core instruments
    - Cosmic-Ray Neutron Sensor (CRNS) for VWC at multiple depths; correction for atmospheric pressure, humidity, and cosmic-ray intensity
    - Pluvio 2 rain gauge; rain[e] and tipping bucket variants
    - Time Domain Transmissometry (TDT) soil moisture sensors
    - Soil heat flux plates
    - Radiometer (upward/downward shortwave and longwave components)
    - Air temperature, humidity, and pressure sensors
    - 3D or integrated 2D sonic anemometers for wind
    - PhenoCam for GCC; SnowFox for snow interaction
    - Campbell Scientific data loggers (CR3000)
  - Variability and site changes
    - Not all instruments installed at every site; instrumentation has evolved
    - Rain[e] height adjustments in 2023 to reduce data loss from vegetation and blockages; raised to 1.0 m at many sites
    - Some sites modified sensor configurations (e.g., wind sensors upgraded, different humidity/pressure setups)
  - Site-specific notes
    - Several sites decommissioned; others upgraded over time
    - Specific dates of rain[e] height changes are provided per site

- Changes to data and reprocessing (Section 8)
  - Ongoing data processing; major changes include:
    - Mar 2024: Daily PE data fix (negative sub-hourly PE not counted in daily sum)
    - Mar 2024: Site altitude metadata updated
    - Mar 2024: VWC calibration gamma values updated; bulk density recalculated; related N0_MOD, N_MIN, N_MAX recalculated
    - Feb 2023: Recalibration and reprocessing at Hollin Hill; pressure sensor calibration issue corrected; VWC calibration updated
    - Feb 2023 onward: 00:30 and 01:00 heat flux values removed; midnight calibration spikes removed and infilled
    - 2020–2021: Various VWC calibration updates; CRNS processing refinements; NMDB data infilled; precipitation processing updates
    - SWE and albedo additions and daily data derivations introduced in earlier updates
  - Implication for users
    - Time series may be reprocessed; use versioned data references and check Change to data table for traceability

- Author contributions and references (Section 9–10)
  - Primary author: R. Smith; network management and data processing teams listed with contributions to data, site metadata, instrumentation, and data processing
  - References provided for methods and calibration approaches (e.g., CRNS processing, SWE derivation, PE computation)

- Access and usage notes (implied)
  - Data are hosted by NERC Environmental Information Data Centre
  - COSMOS-UK website for network information and ongoing updates: https://cosmos.ceh.ac.uk/
  - Data products designed for self-serve analytics and supportive of data combination across topics (consistent with Data Support archetype goals)
  - QC and data flags are essential for understanding data reliability and for informing downstream analyses and dashboard-driven exploration

- Practical takeaways for data support users
  - Expect two-layer QC: automated QC flags and data flags describing infilling or estimation
  - Sub-hourly data are detailed and require careful handling of missing values (-9999) and QC flags to determine usable segments
  - Daily data provide derived metrics (VWC, SWE, PE, GCC) with explicit derivation methods and their own completion status
  - Infilling and reprocessing history should be tracked when using the data; consult Change to data tables for major revisions
  - Instrumentation variability across sites means careful cross-site comparability checks may be needed

- Key links
  - COSMOS-UK project site and user guidance: COSMOS-UK website (cosmos.ceh.ac.uk)
  - NERC Environmental Information Centre hosting of the COSMOS-UK dataset