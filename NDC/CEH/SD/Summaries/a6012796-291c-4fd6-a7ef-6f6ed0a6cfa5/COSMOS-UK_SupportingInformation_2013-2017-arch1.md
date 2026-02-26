# COSMOS-UK (2019). Daily and sub-daily hydrometeorological and soil data (2013-2017) [COSMOS-UK]. NERC Environmental Information Data Centre.

- Purpose and scope
  - Provides daily and sub-daily time series of hydrometeorological and soil moisture data from 46 COSMOS-UK sites spanning 2013–2017.
  - Aims to enable analysis of soil moisture, rainfall, evapotranspiration, and related processes across diverse UK sites.

- Data content and structure
  - Five files included:
    - Sub-hourly hydrometeorological and soil data (COSMOS-UK_Hydrometeorological&Soil_2013-2017.csv)
    - Sub-hourly QC flags (COSMOS-UK_Hydrometeorological&Soil_2013-2017_QC_Flags.csv)
    - Daily potential evapotranspiration (COSMOS-UK_PotentialEvapotranspiration_2013-2017.csv)
    - Hourly soil volumetric water content (VWC) from cosmic-ray sensor (COSMOS-UK_VolumetricWaterContent_Hourly_2013-2017.csv)
    - Daily soil volumetric water content (VWC) from cosmic-ray sensor (COSMOS-UK_VolumetricWaterContent_Daily_2013-2017.csv)
  - Time resolution and interpretation
    - Sub-hourly data at 30-minute intervals; timestamps refer to end of the 30-minute period.
    - Daily PET and daily VWC timestamps refer to the start of the day (00:00 GMT) and cover the preceding 24 hours or daily period.
    - Data values may be missing and are encoded as -9999.

- Quality control and data provenance
  - Dual QC process:
    - Automated QC tests applied on ingest; data failing tests are flagged and removed; flags are stored in a dedicated QC file with *_QCFLAG suffix.
    - Daily visual inspection using plots for 1- and 10-day windows.
  - QC flags are additive to reflect multiple failures; flags are traceable to specific tests per variable.
  - The QC framework is designed to enable full traceability of data quality and the exact tests failed.

- Sub-hourly data details
  - Variables include: incoming/outgoing longwave and shortwave radiation, net radiation, precipitation, atmospheric pressure, air temperature, wind speed and direction, humidity, snowfall, cosmic-ray neutron counts, VWC (from CRNS), soil temperatures at multiple profiles, soil heat flux, etc.
  - Processing and corrections
    - CRNS-derived VWC requires corrections for background cosmic-ray intensity, altitude, atmospheric pressure, and absolute humidity.
    - VWC calculations use one of three methods (site-specific N0 calibration, universal hydrogen molar fraction hmF, or neutron transport models); COSMOS-UK uses site-specific N0 calibration.
    - A 2018 correction factor was applied to address spurious trends in corrected counts, with site-specific gamma values derived empirically.
  - Instrumentation note
    - Not all instruments are installed at every site; some sites lack certain sensors or have decommissioned sites (e.g., Wytham Woods ended 2016).

- Daily potential evapotranspiration (PET)
  - Calculated with Penman-Monteith (FAO 56, 1998) using RN, mean soil heat flux (G1 and G2), TA, absolute humidity (Q), wind speed (WS), and atmospheric pressure (PA).
  - PET values presented as daily totals (mm) at each site.

- Hourly and daily volumetric water content (VWC) from CRNS
  - Hourly VWC (COSMOS_VWC) derived from corrected neutron counts; hourly counts aggregated from 30-minute measurements and corrected for reference intensity, altitude, PA, and Q.
  - Depth-related parameter D86_75m provided for ancillary context.
  - Daily VWC computed as daily average of hourly corrected counts and converted to VWC; D86 depth value derived for daily times.

- Completeness and site instrumentation
  - Completeness metrics cover Met (meteorological) and Soil groups; VWC completeness tracked separately.
  - Instrumentation summary lists: CRNS sensors, rain gauge, point soil moisture sensors (TDT), soil heat flux plates, soil temperature sensors (multiple depths), radiometer, automatic weather station, barometric pressure sensor, temperature and humidity sensor, wind sensors (3D and integrated sonic), snow depth sensor, snow water equivalent sensor, and Campbell Scientific data logger.
  - Instrumentation varies by site; some sites lack certain sensors; Wytham Woods decommissioned in 2016.
  - Comprehensive site details (46 sites) are documented in the accompanying site table and figure.

- Access, authorship, and references
  - Primary author: S. Stanley; data managers and instrument calibration/maintenance credited.
  - Data are hosted and described per CEH/NERC data-centre guidelines; metadata and instrument histories are provided to support reproducibility and re-use.

- References and methodology sources
  - Key methodological references for CRNS, calibration, and PET calculations (e.g., Desilets et al., Zreda et al., Franz 2012/2013, Köhli et al., Evans et al., FAO 56) are cited to support data processing and interpretation.