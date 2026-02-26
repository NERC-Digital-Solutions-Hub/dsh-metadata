# Stable oxygen and hydrogen isotope composition of precipitation, river water and lake water in the Five Lakes of Mikata catchment, 2011-2012 and 2020-2022 - SUPPORTING DOCUMENTATION

## Overview
- Dataset of stable isotope composition (δ18O, δ2H) and d-excess for waters in the Five Lakes of Mikata catchment.
- Sampling spans March 2011–January 2012 and July 2020–July 2022.
- Includes event-based precipitation isotopes, weekly river water, and weekly lake water samples.
- Accompanied by total precipitation and average temperature data for subsampling periods.
- Lake Suigetsu water-column data (temperature and salinity vs depth) on six dates within 2020–2022.
- Purpose: assess whether catchment water composition reflects East Asian Monsoon variability.

## Data and Variables
- Isotope data: δ18O, δ2H, and derived d-excess for surface waters (lakes and river) and precipitation.
- Additional context: precipitation totals and mean temperatures during each sampling period.
- Lake Suigetsu profiling: depth-dependent water temperature and salinity on six dates.
- Output format: structured to enable comparison across periods and with climatic drivers (monsoon variability).

## Collection / Sampling Methods
- Total samples: 463 water samples (Hasu River, Lake Mikata, Lake Suigetsu).
- Timeline:
  - 2011/2012: weekly sampling from 01 Mar 2011 to 03 Jan 2012.
  - 2020/2022: weekly sampling from 15 Jul 2020 to 29 Jul 2022.
- Sampling details:
  - Water samples collected from top ~50 cm; minor checklist of location changes between periods (within same depth range; designed to reflect average surface conditions).
  - Algal filtrations applied when visible (50 µm PET filter).
  - Precipitation samples (n=120) collected 13 Jul 2020–29 Jul 2022 using a 3D-printed funnel and glass bottle; silicone oil added to prevent evaporation; event-based sampling for rain, with snow samples melted under silicone oil.
  - Rainfall and temperature data supported by Netatmo weather station.
- Lake water-column sampling (Lake Suigetsu): approximately quarterly measurements at the lake center; sampling depths from surface to 34 m with varying intervals; van Dorn sampler used to avoid depth cross-contamination; Hydrolab DS5 used for temperature and salinity profiling.

## Laboratory Methods
- δ18O: Isoprime 100 mass spectrometer with CO2 equilibration; samples equilibrated 12–37 h; standards calibrated to VSMOW2; typical precision < 0.05 ‰.
- δ2H: TC-EA-IRMS with continuous flow; five measurements per sample; corrected using CA-HI and CA-LO standards relative to VSMOW; typical precision < 0.5 ‰.
- d-excess: calculated as δ2H − 8 × δ18O (reflects deviation from the Global Meteoric Water Line due to evaporation processes).
- Data corrections: laboratory standards used for QA/QC; acknowledged influences include precipitation composition, transit times, ocean–lake interactions, and minor evaporation within lakes.

## Data Structure and Access
- Two CSV files:
  - mikatagoko_modernisotopes_results.csv: isotope data plus total precipitation and average temperature for each subsampling period. Key fields include sample type (LakeRiver/Rainwater/Column), location, sampling depth (where applicable), dates, δ18O, δ2H, d-excess, and precipitation/temperature metadata.
  - lakesuigetsu_tempsalinity_results.csv: lake water-column data across six dates, including sampling date, depth, water temperature, and water salinity.
- Data fields include detailed metadata on sampling positions, locations, and batch analysis to support traceability and reproducibility.

## Quality Control and Limitations
- QC: corrections applied against laboratory standards; standard references anchored to international materials (VSMOW2, SLAP2, GISP).
- Limitations:
  - 2011–2012 surface-period data lack accompanying precipitation and water-column data due to the pilot study design.
  - Sampling locations changed between periods but remained within comparable depth ranges and away from lake inputs to minimize bias.
  - Data interpretation may be affected by catchment transit times, lake–sea interactions (Sea of Japan), and small-scale evaporation effects.

## Relevance for Monitoring Environmental Health and Policy
- Provides standardized, time-series isotopic evidence of hydrological and climatic influences (notably East Asian Monsoon variability) on catchment water composition.
- Facilitates trend analysis, cross-period comparisons, and integration with other environmental datasets for monitoring environmental health and policy performance over time.
- The explicit data structure and QA/QC measures support reuse, data integration, and broad accessibility for researchers and decision-makers.