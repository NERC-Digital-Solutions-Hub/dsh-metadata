# Soil Gas Flux Dataset with Biochar Treatment – Data Dictionary

## Purpose and Scope
- Defines the variables for a soil gas flux study, including CO2, CH4, and N2O flux measurements, chamber metadata, soil properties, and treatment information.
- Captures timepoints, sampling details, and treatment combinations (biochar and wetted conditions) across multiple sites.

## Key Variables and Structure
- Sample and time identifiers
  - soilcoreno: Individual number for the soil sample/core
  - timepoint: Timepoint of measurements
  - dayfromstart: Days from the start of measurements
  - dayfromstartstring: Day from start as a string
  - datetime: Date and time of the gas flux measurement
- Treatments
  - biochartreatment: Indicates if biochar is amended or not
  - fulltreatname: Full name of the soil treatment (biochar and wetted)
  - temperaturetreatment: Soil temperature treatment
  - nitrogentreatment: 15N-labeled nitrogen treatment (NH4 or NO3)
  - wettingtreatment: Periodic wetting to high water content or not
- Gas flux measurements (gas flux units and derived logs)
  - mgCO2-Cfluxm2h1: CO2 flux (mg CO2-C per m2 per h)
  - log10co2: Log10 of (CO2 flux + 1); negative flux handling via magnitude of negative flux
  - ugCH4-Cfluxm2h1: CH4 flux (mg CH4-C per m2 per h)
  - log10ch4: Log10 of (CH4 flux + 1); negative flux handling via magnitude of negative flux
  - ugN2O-Nfluxm2h1: N2O flux (mg N2O-N per m2 per h)
  - log10n2o: Log10 of (N2O flux + 1); negative flux handling via magnitude of negative flux
- Static chamber headspace at start (t0)
  - CO2ppmt0: CO2 ppm in headspace at t0
  - CH4ppmt0: CH4 ppm in headspace at t0
  - N2Oppmt0: N2O ppm in headspace at t0
- Environmental and soil measurements
  - tempair: Temperature of the soil at measurement time
  - gravwatercontentproportion: Gravimetric water content as a proportion
  - bulkdensitygcm3: Soil bulk density
  - postmixbulkdensity: Bulk density after mixing
  - particledensitygcm3: Soil particle density
  - totalporosity: Total porosity = 1 - (bulk density / particle density)
  - wfpsproportion: Water-filled pore space
- Geometry and sample context
  - chambaream2: Soil area within the static chamber (m2)
  - headvolm3: Volume of the static chamber headspace (m3)
  - drysoilweightg: Dry soil weight in grams
- Biochar specifics and general soil parameters
  - biocharweight: Dry biochar weight added to the soil
  - biocharfraction: Biochar fraction of dry soil weight
- Temporal and site metadata
  - site: Site identifier
  - midpointday: Time in the middle of this and the previous timepoint
  - timeinterval: Duration between the last and current timepoint
  - timeintervalstring: Length of time between timepoints as a string
- Additional soil chemical and temperature context
  - temperaturetreatment: Soil temperature context for treatments
  - wetted? (implicit in wettingtreatment)
  - nitrogentreatment: 15N-labeled nitrogen treatment (NH4 or NO3)

## Data Transformations and Calculations
- Log transformations applied to flux values:
  - log10co2, log10ch4, log10n2o represent log10(flux + 1)
- Negative flux handling for logs:
  - If a flux value is negative prior to logging, the magnitude of the negative flux is added to the flux value before computing the log.

## Metadata and Documentation
- Each variable includes a description and units, facilitating data discoverability and reuse.
- Rich metadata covers sample identity, timepoints, treatments, gas flux measurements (and their transformations), chamber geometry, soil properties, and site information.
- Supported by explicit definitions for porosity, densities, and measurement contexts (datetime, day counts, and interval descriptions).

## Data Quality and Governance Considerations for Data Leaders
- The dataset combines multiple data types (physical measurements, gas fluxs, treatments, and soil properties) requiring consistent metadata standards.
- Key quality aspects:
  - Clarity and consistency of units across all fields
  - Clear documentation of derived fields and transformations (especially log transformations and negative flux handling)
  - Provenance and versioning to track updates to measurements and treatments
  - Standardized naming for treatments to enable cross-study comparability
- Potential data challenges to anticipate:
  - Fragmented or scattered data sources across timepoints and sites
  - Variability in data granularity (e.g., differences in sampling intervals or site-specific methods)
  - Incomplete metadata for some samples or timepoints
  - Need for consistent metadata about treatment combinations and measurement conditions to enable cross-site analyses

## Practical Implications for Data Leaders
- Use this data dictionary as a reference schema to harmonize related datasets and improve discoverability.
- Establish validation rules to ensure unit consistency, valid ranges for flux measurements, and correct application of log transformations.
- Maintain metadata richness (sample IDs, timepoint context, treatment details, site information) to support reusability across projects and networks.
- Promote data integration strategies that align sample IDs, timepoints, and treatment nomenclature across partners and platforms.