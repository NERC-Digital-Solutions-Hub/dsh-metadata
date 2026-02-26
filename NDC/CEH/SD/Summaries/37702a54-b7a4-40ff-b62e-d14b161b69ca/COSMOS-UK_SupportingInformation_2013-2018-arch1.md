# COSMOS-UK. Stanley et al. (2020). Daily and sub-daily hydrometeorological and soil data (2013-2018) [COSMOSUK]. NERC Environmental Information Data Centre.

- The dataset provides 50 COSMOS-UK sites with time-series of hydrometeorological and soil-moisture data from 2013 to 2018, organized into 201 files covering site metadata, sub-hourly, hourly, and daily data, plus QC flags.
- Access and context: CERH COSMOS-UK network overview at cosmo s.ceh.ac.uk; data are described in detail in the COSMOS-UK User Guide and this supporting documentation.

## Data structure and content

- 201 files in total, including:
  - COSMOS-UK SiteMetadata_2013-2018.csv (site locations, soil type, land cover, start/end dates, coordinates, bulk density, soil organic carbon).
  - COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2018.csv (sub-hourly data at ~30 min resolution; multiple meteorological and soil variables; some site-specific missing measurements).
  - COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2018_QC_Flags.csv (QC flags for sub-hourly data).
  - COSMOS-UK_<SITE_ID>_HydroSoil_Hourly_2013-2018.csv (hourly data including VWC from CRNS; includes radiometric, meteorological, soil variables).
  - COSMOS-UK_<SITE_ID>_HydroSoil_Daily_2013-2018.csv (daily data including COSMOS_VWC, D86_75m, PE, SWE, SNOW, ALBEDO).
- Derived and key variables:
  - Volumetric water content (VWC) from CRNS (COSMOS_VWC at hourly; VWC estimates from sub-hourly data; D86 depth info).
  - Net radiation (RN), incoming/outgoing shortwave (SWIN/SWOUT) and longwave (LWIN/LWOUT) radiation.
  - Precipitation (PRECIP), atmospheric pressure (PA), air temperature (TA), relative humidity (RH), wind speed (WS) and direction (WD), humidity (Q and RH), snow depth (SNOWD_DISTANCE_COR).
  - Soil surface and profile measurements: soil temperatures (TDT sensors), VWC at various depths (TDT_VWC, STP_TSOIL2/5/10/50, STP_TSOIL*), soil heat flux (G1, G2).
  - Derived daily metrics: potential evapotranspiration (PE), snow water equivalent (SWE), daily albedo (ALBEDO), and daily snow day indicator (SNOW).
- Spatial and temporal notes:
  - 30-minute sub-hourly measurements with end-of-interval timestamps (e.g., 12:30 refers to 12:00–12:30).
  - Hourly VWC derived from corrected cosmic-ray neutron counts; 2018 introduced site-specific ɣ corrections for cosmic-ray counts.
  - Daily data timestamps refer to the preceding 24-hour period, except SWE and albedo calculations have their own time references.

## Methodology and data processing

- Data collection: on-site instruments feed loggers; data telemetered hourly to CEH Wallingford; two-stage QC applied.
- Quality control:
  - Automatic QC tests applied per variable; flagged data removed; QC flags stored in corresponding QC files with a mechanism to sum flags when multiple tests fail.
  - QC tests cover zero data, too few samples, low power, sensor faults, diagnostic flags, out-of-range values, secondary-variable dependencies, spikes, and error codes.
- QC flags:
  - Final QC flag values are stored in per-site per-variable QC files (with _QCFLAG suffix) to trace which tests led to data removal.
- VWC processing and calibration:
  - VWC derivation from corrected neutron counts involves background cosmic-ray correction, altitude, atmospheric pressure, humidity adjustments, and one of three methods (site-specific N0 calibration, universal hydrogen molar fraction method, or neutron transport modelling). COSMOS-UK uses site-specific N0 calibration with corrections for lattice/bound water and soil organic carbon.
  - A 2018 revision applied an empirical site-specific gamma factor to remove trends; counts are summed hourly and then converted to VWC (hourly) and D86 depths.
- Snow and albedo:
  - Snow days identified using albedo thresholds (10:00–14:00 GMT values); SWE estimated from differences in snow-free and observed neutron counts.
- Derived daily metrics:
  - PE computed via Penman-Monteith; SWE derived through above method; daily albedo calculated from SWOUT/SWIN between 10:00–14:00 for daily albedo.

## Data quality, completeness, and limitations

- Completeness:
  - A site-by-site completeness table (Met, Soil, and VWC) summarizes overall data coverage (noting that VWC completeness depends on CRNS data and processing).
- Data gaps and site differences:
  - Not all instruments are installed at every site; snow depth sensors are present only at a subset of sites; some sites (e.g., Wytham Woods) decommissioned in 2016.
  - Specific sensor components (e.g., certain wind components, SNOW sensors) may be missing at various sites.
- Data corrections and reprocessing:
  - Data reprocessed when improvements are made; 2020 updates include VWC calibration adjustments, infilling from secondary CRNS tubes, NMDB data infilling, updated 30-minute precipitation, and revisions to PE calculations.
- Documentation and provenance:
  - All data are accompanied by detailed method notes and references (Evans et al., Zreda et al., Franz et al., etc.).

## Instrumentation

- Cosmic-Ray Neutron Sensor (CRNS) for VWC (Hy droinnova CRS-2000/CRS-1000/B); counts corrected for atmospheric pressure, humidity, and cosmic ray intensity.
- Rain gauge: OTT Pluvio 1 (with corrections for funnel area and installation context).
- Point soil moisture sensors (TDT) for soil moisture and temperature at multiple depths; not site-calibrated to individual soil types, using generic calibration data.
- Soil heat flux plates: Hukseflux HFP01SC (0.03 m depth).
- Soil temperature sensors: Hukseflux STP01 at multiple depths.
- Radiometer: four-component radiometer (shortwave and longwave components) and net radiation calculation.
- Automatic weather station: Rotronic HC2A-S3 + Gill MetPak base station for air temperature, humidity, and barometric pressure; Vaisala PTB110 for pressure; HUMICAP HMP155 for humidity; thermocouples for soil temperature.
- Wind measurement: 3D sonic anemometer and integrated 2D sonic anemometer (Gill WindMaster / WindSonic).
- Snow depth: Campbell Scientific SR50A; SWE via SnowFox cosmic-ray measurement.
- Data logging: Campbell Scientific CR3000 micrologger.

- Note: The 7.2 section outlines site-specific instrument configurations; some sites lack certain instruments or have substitutions.

## Changes to data and versions

- Jul 2020:
  - VWC calibration values updated; CRNS counts infilled from secondary tube where available; NMDB data infilled; 30-minute precipitation re-aggregated from non-real-time data; PE recalculated with updated method.
- Dec 2019:
  - SWE added; snow days calculated from albedo and SWE method implemented.
- Apr 2020:
  - PE method revised; 30-minute values calculated and aggregated to hourly and daily (previously only daily calculations).
- Ongoing data processing: full time series retrievable when updates occur.

## Access, authorship, and references

- Data stewardship: COSMOS-UK project (CEH); data managed and presented by a dedicated team; primary contact is S. Stanley; data managers include H. M. Cooper, O. Hitt, M. Fry, O. Swain.
- Author contributions, site metadata curation, instrumentation maintenance, and data presentation are described in the document.
- References include COSMOS-UK methodological papers (Zreda et al., Desilets et al., Franz et al., Evans et al., Koehli et al., etc.) and related data products.

- For access: NERC Environmental Information Data Centre; COSMOS-UK data portal and user guide referenced in the documentation.