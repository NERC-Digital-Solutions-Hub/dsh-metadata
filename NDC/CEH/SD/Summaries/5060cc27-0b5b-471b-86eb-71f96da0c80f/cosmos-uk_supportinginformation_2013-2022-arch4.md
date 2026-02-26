# Supporting documentation for COSMOS-UK. Stanley et al. (2023). Daily and sub-daily hydrometeorological and soil data (2013-2022) [COSMOSUK]. NERC Environmental Information Data Centre.

## Overview
- Dataset comprises 51 COSMOS-UK sites with time series of hydrometeorological and soil moisture data from 2013 to 2022 (through 31 Dec 2022).
- Total of 258 files, including site metadata, sub-hourly data and flags, daily data and flags, and related metadata.
- Data are measured with on-site loggers and telemetered hourly to a central system; missing values marked as -9999.
- Includes derived products (e.g., volumetric water content from cosmic-ray neutron sensor, snow water equivalent, potential evapotranspiration, albedo, GCC) and extensive quality-control (QC) and infilling procedures.

## Data products and structure
- File types (example filenames):
  - COSMOS-UK_SiteMetadata_2013-2022.csv (site details)
  - COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2022.csv (sub-hourly data)
  - COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2022_Metadata.csv (sub-hourly metadata)
  - COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2022_QC_Flags.csv (QC flags)
  - COSMOS-UK_<SITE_ID>_HydroSoil_Daily_2013-2022.csv (daily data)
  - COSMOS-UK_<SITE_ID>_HydroSoil_Daily_2013-2022_Metadata.csv (daily metadata)
  - COSMOS-UK_<SITE_ID>_HydroSoil_Daily_2013-2022_Flags.csv (daily data flags)
- Data coverage includes:
  - Sub-hourly hydrometeorological and soil data (30-minute resolution; 2013-2012 end date varies by site)
  - Daily data including VWC (derived from CRNS), potential evapotranspiration (PE), snow water equivalent (SWE), net radiation, and other met/soil variables
  - Derived and auxiliary variables (CRNS-based VWC, SWE, PE, GCC from PhenoCam, albedo)
- Variables are organized with site-specific IDs; sub-hourly and daily data differ in units and aggregation (end-of-interval timestamps).

## Data fields and key variables
- Sub-hourly (30-minute) data fields (selected examples):
  - Radiation: LWIN, LWOUT, SWIN, SWOUT; Net radiation RN (derived)
  - Meteorology: PA, TA, WS, WD, Q (absolute humidity), RH
  - Precipitation: PRECIP (pluvio), PRECIP_TIPPING (tipping bucket), PRECIP_RAINE (RainE)
  - Snow: SNOW_DEPTH; other tect physicals
  - Soil and heat flux: G1, G2, TDT?_TSOIL (soil temperatures), TDT?_VWC (soil moisture), STP_TSOILx/TODO (soil temps at depths)
  - Wind components: UX, UY, UZ (3D components)
  - Derived/ancillary: GCC (Green Colour Content from PhenoCam), albedo, PE (Penman-Monteith)
- Daily data fields:
  - LWIN, LWOUT, SWIN, SWOUT, RN (all as daily totals or equivalents)
  - Precipitation totals (PRECIP, PRECIP_TIPPING, PRECIP_RAINE)
  - PA, TA, WS, WD, Q, RH, G1, G2, TDT and VWC variables (from TDT sensors)
  - SWE, PE, GCC, Albedo, COSMOS_VWC (overall VWC), CTS_MOD_CORR (CRNS-corrected counts), D86_75m (CRNS footprint)
  - SNOW (snow days; 1/0), SNOW_DEPTH (snow depth), SWE (snow water equivalent)
- Flags and quality indicators:
  - QC flags for sub-hourly and daily data (COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2022_QC_Flags.csv; ..._Daily_2013-2022_Flags.csv)
  - Data flags indicating infilling or estimation (Missing, Unchecked, Infilled, Estimated)

## Processing, quality control, and flags
- Quality control (QC):
  - Two-stage QC: automated QC tests (scripted) plus daily visual inspection
  - QC flags indicate which tests failed (e.g., out of range, low power, sensor fault) and are combined if multiple tests fail
  - QC flags explain why data were removed; non-zero QC flags imply infilled/estimated data
  - Net radiation (RN) and absolute humidity (Q) are not QC’d themselves because they derive from QC’d inputs
- Data flags:
  - Separate data flags indicate data quality and infilling status (M = missing, U = unchecked, I = infilled, E = estimated)
  - Data flags provide guidance on data reliability and processing status
- Infilling:
  - Interpolation (linear or polynomial order 2) used for gaps deemed reasonable
  - Gap-size and surrounding data determine method; RMSE-based evaluation selects best method
  - Infilling applied to selected variables for both sub-hourly and daily data as described in sections 5
- Completeness:
  - Completeness summarized per site for the period Oct 2013–Dec 2022
  - Met and Soil groups define overall data completeness; VWC completeness for CRNS-derived data
  - Derived products (e.g., VWC) are included with completeness assessments

## Instrumentation and site setups
- Core instruments (COSMOS-UK network):
  - Cosmic-Ray Neutron Sensor (CRNS) for soil moisture (VWC)
  - OTT Pluvio rain gauge; tipping bucket (TBR) and RainE systems for precipitation
  - Time-domain reflectometry (TDT) soil moisture sensors and soil temperature sensors at various depths
  - Heat-flux plates (Hukseflux HFP01SC)
  - Radiometer (Hukseflux NR01) for net radiation calculations
  - Automatic weather station components (air temperature, humidity, barometric pressure, wind)
  - PhenoCam for GCC (green color content) derived from images
  - Snow sensors (SR50A, SnowFox) for snow depth and SWE estimation
  - Data logger (Micrologger Campbell Scientific CR3000)
- Site variability:
  - Instrumentation and configurations vary by site and over time; detailed site setup and changes are described in Tables 8–9 of the document
  - Some sites decommissioned (e.g., Wytham Woods, Redmere, Cochno, Harwood Forest)
  - PhenoCam and CRNS configurations contribute to site-specific data characteristics and quality considerations

## Changes to data and version history
- Data processing and reprocessing occur as improvements are identified
- Notable changes:
  - Feb 2023: VWC reprocessed at Hollin Hill due to a pressure sensor calibration issue
  - Feb 2023: Removal of all 00:30 and 01:00 heat flux values (spikes linked to midnight calibrations); gaps infilled
  - Feb 2022: Infilling applied to additional variables for gaps < 10 data points
  - 2021–2020: VWC calibration updates; CRNS count corrections; some infilling methods expanded
  - 2019–2019+: SWE addition; daily albedo added; several methodological revisions
- Version notes are detailed in the Changes to data table and associated narrative

## Data provenance and access
- Primary author: S. Stanley; project management and data handling by multiple team members
- Derived data processing methods, calibration details, and methodologies are documented with references to foundational papers (e.g., Evans et al. 2016; Zreda et al. 2012; Wallbank et al. 2020)
- For full dataset access and metadata, refer to the COSMOS-UK data center and supporting documentation

## References (selected)
- Baatz et al. 2014; Bogena et al. 2015; Desilets et al. 2010; Franz 2012; Franz et al. 2013; Köhli et al. 2015
- Evans et al. 2016; Wallbank et al. 2020; FAO 1998; Zreda et al. 2012
- COSMOS-UK specific methodological and calibration literature cited within the document