# CO2 efflux and hydraulic data for two Scottish and four Amazonian streams 2011-13

- Field sites cover six locations with varying catchment characteristics (Scotland: River Kelvin RK and Drumtee Water DW; Amazon: Main Trail MT, New Colpita NC, La Torre LT, Tambopata TP).
- Sampling span and seasonality: RK and DW sampled regularly from June 2012 to December 2013 (weekly to every ~3 weeks); MT, NC, LT and TP sampled during three field campaigns between Feb 2011 and May 2012 to capture wet and dry seasons.
- Site details: RK is semi-urban with agriculture nearby; DW is peat-dominated headwater; MT and NC are small tropical rainforest streams; LT and TP are larger Amazonian rivers near the Tambopata area.

- Data collected
  - CO2 efflux (mean and SD) from floating chamber measurements
  - Hydraulic parameters: flow velocity, water depth, calculated mean depth-averaged velocity, Fr (Froude number), Re (Reynolds number)
  - Water chemistry: pCO2, [DIC], pH, water temperature
  - Metadata: Date, Region, Site

- CO2 efflux measurements
  - Method: Floating chamber (volume 0.0029 m3) with closed-loop LICOR LI-840A CO2/H2O analyzer; bubbles circulated with Schego pump
  - Protocol: CO2 accumulation tracked over 4 minutes, three repeats
  - Flux calculation: FCO2 = (δCO2/δt) × (V / (R × T × S)); where δCO2/δt is slope (μatm s^-1), V is chamber volume, S is chamber surface area
  - Field notes: For Amazon sites MT/NC, near-surface velocity taken as mean of three replicates under the chamber; Fr and Re not computed from these sites due to unavailable data

- Hydraulic measurements
  - UK sites: velocity measured with Valeport flow meter (50 mm impeller), 60 s averaging, at 20% and 80% of depth plus at least three other depths
  - Calculated parameters: mean velocity ū (m s^-1), Froude number Fr, Reynolds number Re
  - Purpose: Fr as indicator of surface disturbance and gas exchange potential; Re as indicator of turbulence and mixing affecting CO2 transport

- Water chemistry and calibration
  - pH measurements: 
    - DW: continuous in-situ logging (MP TROLL 9000)
    - MT/NC/LT/TP: pH logged with Troll 9500 (15 min resolution)
    - RK: pH calculated from discharge-pH relationship due to equipment issues
  - Temperature and conductivity: logged at several sites; TZ-specific methods noted
  - [DIC] measurements: collected within 15 minutes of flux measurement; triplicate samples acidified and stored in exetainers; analyzed later with Gas Bench/Delta V Plus
  - pCO2 calculation: derived from [DIC], pH, and temperature

- Equipment calibration and data quality
  - Troll 9000 calibrations ~every 5 weeks; Troll 9500 calibrations ~monthly
  - Two-point pH calibrations (pH 4 and 7) using lab-prepared buffers
  - QA notes: missing data occurred due to equipment failure, high flow impeding access, or seasonal drying (MT); 2012-2013 period lacked some DIC/pCO2 data at DW and RK
  - All recorded values within detection limits; quality control performed where possible

- Data structure and file format
  - One spreadsheet: CO2 efflux and hydraulic data for two Scottish and four Amazonian streams 2011-13
  - Columns (11): 
    1) Date (dd/mm/yyyy)
    2) Region (Amazon Basin or Scotland)
    3) Site (stream name)
    4) Mean CO2 efflux (μmol CO2 m^-2 s^-1)
    5) SD of mean CO2 efflux
    6) Flow (m s^-1) – mean at measurement point
    7) Water depth (m)
    8) pCO2 (μatm) – calculated from [DIC] with pH and temperature
    9) [DIC] (mM C)
    10) pH
    11) Water temperature (°C)
  - Missing values indicated as NA
  - File naming: CO2 efflux and hydraulic data for two Scottish and four Amazonian streams 2011-13.csv (note: document shows a minor filename inconsistency with .cvs)

- Data provenance and use considerations for governance
  - Data span multiple regions and campaigns; consistent measurement approaches and units established to support cross-site comparability
  - Documentation includes measurement protocols, calibration routines, and data processing steps to support reproducibility
  - Some site-specific deviations exist (e.g., RK pH derived from discharge relationship; MT/NC/LT/TP velocity data not used to compute Fr/Re at Amazon sites)
  - Gaps exist in data coverage (e.g., 2012-2013 DIC/pCO2 gaps for DW and RK; MT dried up in dry season; some data lost to equipment failures)
  - Suitability for meta-analyses and cross-site modeling is enhanced by explicit QA notes, standardized units, and comprehensive metadata
  - Guidance needed for updating and extending the dataset, including explicit data provenance and versioning if shared through portals

- Practical implications for data stewardship
  - Ensure consistent metadata, units, and naming conventions across sites if expanding the dataset
  - Maintain traces of calibration, QA events, and any data imputation or exclusion decisions
  - Clearly document any deviations from standard methodology to preserve interpretability
  - Facilitate data access via a standardized portal, with notes on missing periods and site-specific caveats