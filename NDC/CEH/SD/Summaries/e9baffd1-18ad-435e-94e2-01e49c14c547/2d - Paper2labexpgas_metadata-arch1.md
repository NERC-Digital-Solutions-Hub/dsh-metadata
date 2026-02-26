# Soil Gas Flux Data under Biochar and Wetting Treatments

- Purpose and scope
  - A dataset of soil gas flux measurements (CO2, CH4, N2O) from soil cores/samples under controlled treatments.
  - Aimed at identifying treatment effects, relationships with soil properties, and building predictive insights.

- Core identifiers and timing
  - soilcoreno: unique soil sample/core identifier.
  - timepoint: measurement occasion index.
  - dayfromstart: days since the start of measurements for this gas analysis.
  - daysfromwettingevent: days since the last wetting event for this analysis.
  - datetime: exact date and time of the soil gas flux measurement.
  - tempair and temperaturetreatment: ambient air temperature and its treatment context.
  - fulltreatname: full name of the soil treatment (biochar and wetted).

- Treatments and experimental design
  - biochartreatment: whether biochar was amended or not.
  - wettingtreatment: whether the sample was periodically wetted to a high water content.
  - These variables enable comparisons across biochar presence and moisture regime.

- Gas flux measurements (primary outcomes)
  - mgCO2-Cfluxm2h1: CO2 flux (mg CO2-C per m2 per hour).
  - log10co2: log10 of (CO2 flux + 1), with a special rule for negative flux values during logging.
  - ugCH4-Cfluxm2h1: CH4 flux (µg CH4-C per m2 per hour).
  - log10ch4: log10 of (CH4 flux + 1) with the same handling for negative fluxes.
  - ugN2O-Nfluxm2h1: N2O flux (µg N2O-N per m2 per hour).
  - log10n2o: log10 of (N2O flux + 1), with the negative-flux handling rule.

- Initial chamber and soil context
  - CO2ppmt0, CH4ppmt0, N2Oppmt0: initial gas concentrations in the static chamber headspace at t0 (ppm).
  - headvolm3: headspace volume of the static chamber.
  - chambaream2: soil area covered by the chamber.
  - tempair: air temperature at measurement time.
  - datetime: timestamp of the measurement (redundant with timepoint/date but provides exact record).

- Soil properties and material inputs
  - gravwatercontentproportion: gravimetric soil water content as a proportion.
  - drysoilweightg: dry soil mass in the core (g).
  - biocharweightg: mass of added biochar (g).
  - biocharfraction: biochar as a fraction of dry soil weight.
  - particledensitygcm3: particle density of the soil.
  - totalporosity: (1 - (bulk density / particle density)).
  - wfpsproportion: water-filled pore space (gravimetric water content × (bulk density / total porosity)).

- Data processing notes
  - log10 columns are computed as log10(flux + 1).
  - If a flux is negative, the absolute magnitude of that negative flux is added to all flux values prior to logging to avoid taking log of negative numbers.

- Analytical opportunities for researchers
  - Assess how biochar amendment and wetting regimes influence CO2, CH4, and N2O fluxes.
  - Explore relationships between fluxes and soil moisture (grav water content, WFPS), temperature treatments, and soil properties.
  - Develop predictive models of gas flux using time since wetting, treatment variables, and soil characteristics.
  - Use both raw flux values and log-transformed fluxes for robust statistical analyses.

- Quality, provenance, and usability considerations
  - Rich metadata accompanies measurements (treatment names, timing, soil properties, chamber geometry) to support reproducibility.
  - Availability of both raw flux values and log-transformed derivatives facilitates a range of analytical approaches.
  - Data are suited to local-scale analyses and integration with related datasets, with attention to standardization and documentation due to potential scale and format differences.