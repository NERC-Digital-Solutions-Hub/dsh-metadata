# Soil respiration under Miscanthus x giganteus and an adjacent barley crop

- Citation: Keane, B.; Ineson, P. (2017). Soil respiration under Miscanthus x giganteus and an adjacent barley crop. NERC Environmental Information Data Centre. https://doi.org/10.5285/c397d6f4-96f4-4967-a0df-c64ef35ea572

- Aim and scope
  - Provide a standardized dataset to monitor and compare soil respiration (Rs) under a Miscanthus x giganteus stand and an adjacent spring barley crop.
  - Data intended for long-term environmental monitoring, with clear formats for scrutiny of ecosystem carbon fluxes and policy-relevant performance.

- Study site and experimental design
  - Location: Farm in the east of the United Kingdom; full site description linked to Drewer et al. (2012).
  - Crops: Miscanthus x giganteus and April-sown spring barley in adjacent fields.
  - Replication and layout: Six chambers deployed across the two fields, placed at random within separate plots at least 1.5 m apart; treated as independent replicates.
  - Chamber setup: Chambers seated over PVC collars (diameter 20 cm, height 10 cm) inserted ~2 cm into soil to minimize root-cutting effects; collars remained in place throughout the study.
  - Measurement protocol: Chambers closed for two minutes with a 30-second dead band for gas mixing; cycle repeated across chambers.
  - Environmental measurements: Soil temperature and moisture at 5 cm depth measured near each chamber every 15 minutes; hourly meteorological data (solar radiation, air temperature) recorded on site.

- Data collection details
  - Timeframe: May to August 2013.
  - Equipment: Automated chambers and infrared gas analysers (IRGA, Licor LI-8100-101A) with multiplexers.
  - Data captured: Soil respiration (Rs) fluxes, chamber air temperature, chamber location/identification, area covered by chamber, soil temperature and moisture at 5 cm, and time stamps.

- Data processing and analyses
  - Rs computation: Linear regression of CO2 concentration against time, corrected for chamber volume and temperature using manufacturer software.
  - Statistical analysis: Conducted in SAS 9.3.

- Datasets included
  - Dataset 1: Flux_and_soil_data
    - Key fields: DATE, CROP (ARAB = barley, MISC = Miscanthus), DTHOUR, DTQUART, TIME, Rs_Umol (µmol m^-2 s^-1), Rs_mg (mg m^-2 h^-1), Rs_r2, CHAMBERTEMP (°C), AREA (cm^2), ST_C (soil temperature 5 cm, °C), SM_M3M3 (volumetric soil moisture), etc.
  - Dataset 2: Met_data
    - Key fields: Datetime, AIRTEMP_C (air temperature, °C), RAD_WMSQ (solar radiation, W m^-2)

- References and background
  - Drewer, J. et al. (2012) on soil emissions from perennial bioenergy crops vs. arable crops.
  - Heinemeyer, A. et al. (2011) on measurement and modeling considerations for soil respiration and collar-insertion depth.

- Data management and access considerations for analysts
  - Data are stored and accessible via the NERC Environmental Information Data Centre (EIDC) with a formal data citation.
  - Includes both process-level (Rs) and environmental covariates, enabling integration with other environmental datasets.
  - Standardized formats and clear metadata support reproducibility and cross-study comparability.