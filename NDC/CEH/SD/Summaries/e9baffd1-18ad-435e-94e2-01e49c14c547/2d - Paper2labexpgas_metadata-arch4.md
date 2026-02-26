# Soil Gas Flux Measurements Data Dictionary

## Overview
- A metadata dictionary describing variables for soil gas flux measurements from soil cores/samples across time points and experimental treatments.
- Captures sample identity, timing, environmental conditions, treatments (biochar and moisture), gas flux measurements for CO2, CH4, and N2O, and related derived metrics and soil/chamber properties.

## Data structure and key variables
- Sample and timing
  - soilcoreno: Unique identifier for the soil sample/core.
  - timepoint: Timepoint of measurements.
  - dayfromstart: Days since the start of gas analysis measurements for this sample.
  - daysfromwettingevent: Days since the last wetting event for this gas analysis.
  - datetime: Date and time of the soil gas flux measurement.
- Experimental treatments
  - temperaturetreatment: Soil temperature condition during the measurement.
  - biochartreatment: Indicates whether biochar was added to the sample.
  - wettingtreatment: Indicates whether the sample was periodically wetted to a high water content.
  - fulltreatname: Full descriptive name of the soil treatment (biochar and wetted).
- Gas flux measurements (raw)
  - mgCO2-Cfluxm2h1: CO2 flux (mg CO2-C per m2 per hour).
  - ugCH4-Cfluxm2h1: CH4 flux (μg CH4-C per m2 per hour).
  - ugN2O-Nfluxm2h1: N2O flux (μg N2O-N per m2 per hour).
  - CO2ppmt0, CH4ppmt0, N2Oppmt0: Gas concentrations (ppm) in the static chamber headspace at t0.
  - tempair: Temperature of the air/soil at the time of gas measurement.
- Derived/transform metrics
  - log10co2: Base-10 log of (CO2 flux + 1), used to stabilize variance for CO2 data.
  - log10ch4: Base-10 log of (CH4 flux + 1).
  - log10n2o: Base-10 log of (N2O flux + 1).
  - Note on log transforms: If there is a negative flux in the corresponding raw flux column, the positive magnitude of this negative flux is added to every flux value before logging.
- Environmental and chamber context
  - gravwatercontentproportion: Gravimetric water content as a proportion.
  - chambaream2: Soil area within the static chamber (m2).
  - headvolm3: Volume of the static chamber headspace (m3).
- Soil and amendment properties
  - drysoilweightg: Dry weight of soil in the core (g).
  - biocharweightg: Dry weight of biochar added to the soil (g).
  - biocharfraction: Proportion of biochar by dry soil weight.
  - particledensitygcm3: Particle density of the soil (g/cm3).
  - totalporosity: Total porosity of the soil, calculated as 1 - (bulk density / particle density).
  - wfpsproportion: Water-filled pore space (gravimetric water content × (bulk density / total porosity)).

## Metadata quality and standards
- Each field includes a clear description and defined units (e.g., mg CO2-C flux m-2 h-1, μg CH4-C flux m-2 h-1, ppm for headspace gases).
- Derived logs have explicit calculation rules, including handling of negative flux values to ensure meaningful log values.
- The dataset integrates both raw measurements and derived metrics to support analysis, visualization, and normalization.

## Data governance and usability considerations
- Data discoverability and reuse are aided by explicit field names and detailed descriptions.
- Consistency of units and definitions is critical for cross-study comparability and data integration.
- Potential gaps to monitor (noted from typical Data Leader concerns): data provenance and lineage, presence of missing values, alignment of measurement times, and adherence to standardized metadata conventions.

## Challenges and recommendations for Data Leaders
- Challenges
  - Diverse audiences across partners require clear, standardized metadata and consistent variable naming.
  - Data fragmentation across heterogeneous sources can hinder overview and discovery.
  - Variable data quality and incomplete metadata can impede cross-project reuse.
- Recommendations
  - Maintain strict data standards for variable naming, units, and metadata to improve interoperability.
  - Document data collection protocols and data lineage to support reproducibility.
  - Implement robust data quality checks, especially for derived metrics (log transforms) and handling of negative flux values.
  - Encourage collaboration and shared metadata practices within the data community to reduce duplication of effort and improve discoverability.