COSMOS-UK (2019). Daily and sub-daily hydrometeorological and soil data (2013-2017) [COSMOS-UK]. NERC Environmental Information Data Centre.

## Overview
- A multi-site dataset (46 COSMOS-UK sites) covering hydrometeorological and soil moisture data from 2013 to 2017.
- Provided as five files:
  - Sub-hourly hydrometeorological and soil data
  - Sub-hourly QC flags
  - Daily potential evapotranspiration (PET)
  - Hourly volumetric water content (VWC) from a cosmic-ray sensor
  - Daily VWC from the cosmic-ray sensor
- Missing values are coded as -9999.
- Data are processed and quality-controlled at CEH Wallingford; QC flags are designed to trace which tests failed.

## Data structure and content
- Time resolution and scope:
  - Sub-hourly data at 30-minute resolution (except where noted) for 46 sites; period Oct 2013–Dec 2017.
  - PET and VWC datasets accompany the hydrometeorological data.
- Data processing and QC:
  - Automated QC tests applied on ingest; failing data are flagged and removed.
  - A separate QC flag dataset (COSMOS-UK_Hydrometeorological&Soil_2013-2017_QC_Flags.csv) records aggregated flag values per data point.
  - A daily visual QC review complements automated QC.
  - Flags are additive to yield a unique final QC value for each data point.
- Variable metadata:
  - The main hydrometeorological/soil file includes a comprehensive list of variables with units, aggregation method, and notes.
  - Snow depth is measured at a subset of sites; some wind components are not available at certain sites; Wytham Woods data end in 2016 due to decommissioning.
- File-specific notes:
  - 3.3 COSMOS-UK_Hydrometeorological&Soil_2013-2017.csv:
    - Variables include radiation components (incoming/outgoing longwave/shortwave), precipitation, atmospheric pressure, air temperature, humidity, wind (speed and direction), net radiation, specific soil and soil moisture measurements, and CRNS-related data.
  - 4.1–4.4 COSMOS-UK_PotentialEvapotranspiration_2013-2017.csv:
    - Daily PET calculated via Penman-Monteith using RN, G (mean of G1 and G2), TA, Q, WS, PA.
  - 5.1–5.4 COSMOS-UK_VolumetricWaterContent_Hourly_2013-2017.csv:
    - VWC derived from cosmic-ray neutron sensor (CRNS) counts; corrected for altitude, atmospheric pressure, and humidity; site-specific calibration (N0), universal/hmf, or transport-model methods; 2018 adjustment introduces a site-specific gamma factor to remove spurious trends.
    - 30-minute counts telemetered, summed to hourly, then converted to VWC; D86 depth data included.
  - 6.1–6.4 COSMOS-UK_VolumetricWaterContent_Daily_2013-2017.csv:
    - Daily VWC produced from daily average of hourly corrected counts; D86 depth derived similarly to hourly data.
- Timelines and timestamps:
  - Sub-hourly data timestamps refer to the end of the 30-minute period (e.g., 12:30 represents 12:00–12:30).
  - PET and daily VWC timestamps refer to the start of the day (00:00) for the daily aggregate period.

## Completeness and data quality
- Completeness:
  - A completeness table (Met and Soil groups combined; VWC completeness separate) documents data coverage per site for the study period.
- Data availability caveats:
  - Snow data availability varies by site.
  - Certain instrument types are not installed at every site (see instrumentation section).
  - Wytham Woods data end in 2016 due to decommissioning.
- Quality control specifics:
  - QC tests include: missing data, zero data, too few samples, low power, sensor faults, diagnostic flags, out-of-range, secondary variable checks, spikes, and error codes.
  - QC flags are recorded per data point, enabling traceability of which tests were triggered.

## Instrumentation and site variability
- Core instrument types:
  - Cosmic-Ray Neutron Sensor (CRNS) for VWC
  - Rain gauge (OTT Pluvio²)
  - Time-domain transmissometry soil moisture sensors (TDT)
  - Two soil heat flux plates (0.03 m)
  - Multi-depth soil temperature sensors (STP)
  - Radiometer for net, shortwave, and longwave radiation components
  - Automatic weather station (air temperature, humidity, barometric pressure)
  - Barometric pressure sensor
  - Humidity and temperature sensors
  - 3D and integrated 2D sonic anemometers for wind
  - Snow depth sensor (selected sites)
  - Snow water equivalent sensor (SnowFox)
  - Campbell MicroLogger (CR3000)
- Site variation:
  - Instrumentation is not uniform across all sites; a dedicated table lists which sites lack specific instruments.
  - Some sites have multiple or upgraded sensors over time.
  - Wytham Woods decommissioned in 2016.

## Data provenance and usage
- Data management and governance:
  - CEH maintains QA/QC procedures; data are archived in the NERC Environmental Information Data Centre.
- Methods and references:
  - PET uses FAO56 Penman-Monteith (FAO, 1998).
  - VWC retrieval from CRNS follows established calibration and correction protocols (Zreda/Franz et al.; Evans et al., 2016).
  - 2018 reprocessing introduced site-specific gamma corrections to remove spurious trends in VWC.
- Documentation and metadata:
  - The primary dataset documentation references instrument manuals and methodological papers for calibration and data processing.
  - Metadata includes site descriptions, land cover, soil types, and instrument specifics.

## Access, reuse, and outputs
- Data access:
  - Hosted as part of COSMOS-UK data products within the NERC Environmental Information Data Centre.
- Potential outputs and data products for a Data Support perspective:
  - Multi-site time-series dashboards or self-serve data portals combining met data, PET, and CRNS-derived VWC.
  - Cross-site comparative analyses of soil moisture dynamics and evapotranspiration.
  - Data quality flags integrated into data products to help end users filter reliable observations.
  - Provenance-aware datasets linking raw instrument outputs to QC flags and processed variables.
- Use considerations:
  - Account for missing data and site-specific instrumentation differences.
  - Apply QC flags to assess data reliability; be aware of timestamp conventions across files.
  - For VWC, consider the method used (N0, hmF, or transport modelling) and the post-2018 gamma correction when interpreting trends.