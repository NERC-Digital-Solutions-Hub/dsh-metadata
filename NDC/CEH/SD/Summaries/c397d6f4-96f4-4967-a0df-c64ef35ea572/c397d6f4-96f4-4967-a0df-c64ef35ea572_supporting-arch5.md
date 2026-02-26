# Soil respiration under Miscanthus x giganteus and an adjacent barley crop

- Purpose and scope
  - Dataset collection to measure soil respiration (Rs) under Miscanthus x giganteus and adjacent spring barley.
  - Location: farm in eastern United Kingdom; study conducted May–August 2013.
  - Experimental design: automated chambers with infrared gas analysers (IRGA) deployed in each crop; six chambers placed randomly within plots treated as independent replicates; collars inserted 2 cm into soil; no above-ground vegetation included.
  - Environmental context: hourly soil temperature (5 cm depth) and soil moisture, plus hourly meteorological data (solar radiation, air temperature) recorded on site.

- Data collection methods
  - Instrumentation: IRGA (Licor LI-8100-101A) with multiplexers; chambers closed for 2 minutes per measurement cycle with a 30-second dead band.
  - Replicates: 6 chambers per crop, with random placement at least 1.5 m apart.
  - Data capture cadence: measurements processed to compute Rs from CO2 concentration vs. time; results corrected for chamber volume and temperature using manufacturer software.
  - Data processing: subsequent analyses conducted with SAS 9.3.

- Datasets and schema
  - Dataset 1: Flux_and_soil_data
    - Key fields include: DATE, DTHOUR, DTQUART, TIME, CROP (ARAB = barley, MISC = Miscanthus), Rs_Umol (µmol m^-2 s^-1), Rs_mg (mg m^-2 h^-1), Rs_r2, CHAMBERTEMP (°C), CHANNEL, Rs_cv, AREA (cm^2), ST_C (°C), SM_M3M3 (volumetric soil moisture), plus additional metadata like DATES and time stamps.
    - Units and formats are explicitly defined (e.g., Rs_Umol in µmol m^-2 s^-1, TIME in hh:mm:ss, etc.).
  - Dataset 2: Met_data
    - Key fields: Datetime, AIRTEMP_C (°C), RAD_WMSQ (W m^-2).
    - Temporal resolution aligns with observational timing.

- Provenance and citation
  - Data citation: Keane, B.; Ineson, P. (2017). Soil respiration under Miscanthus x giganteus and an adjacent barley crop. NERC Environmental Information Data Centre. DOI: 10.5285/c397d6f4-96f4-4967-a0df-c64ef35ea572.
  - Standards for referencing the dataset are provided to ensure proper attribution.

- Data quality, governance, and usability considerations
  - Metadata richness supports discoverability and reuse (detailed column definitions, units, and formats).
  - Clear documentation of study design and data processing steps (Rs calculated from CO2 vs. time; corrections applied using manufacturer software; SAS 9.3 for analyses) aids reproducibility.
  - Potential governance considerations for data stewards:
    - Ensure ongoing discoverability through the provided DOI and repository (NERC Environmental Information Data Centre).
    - Maintain compatibility of data formats and column naming across related datasets.
    - Provide guidance on data reuse and citation, including crop identifiers, timestamps, and measurement units.
    - Note that data collection occurred in a specific time window and site, which may affect longitudinal integration or meta-analyses.

- References and context
  - Drewer, J. et al. (2012). How do soil emissions of N2O, CH4 and CO2 from perennial bioenergy crops differ from arable annual crops?
  - Heinemeyer, A. et al. (2011). Soil respiration: implications of the plant-soil continuum and respiration chamber collar-insertion depth on measurement and modelling of soil CO2 efflux rates in three ecosystems.