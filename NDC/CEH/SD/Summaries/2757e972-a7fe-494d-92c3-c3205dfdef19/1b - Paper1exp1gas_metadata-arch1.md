# Soil Gas Flux Dataset with Biochar and Wetted Treatments - Data Dictionary

- Purpose and scope
  - A dataset of soil gas flux measurements (CO2, CH4, N2O) from soil cores with biochar amendments and moisture/wetting treatments.
  - Captures multiple timepoints per sample, along with environmental and soil property data to support correlations, models, and predictions of gas flux responses to treatments.

- Key variables and data types
  - Sample and timing
    - soilcoreno: Individual soil core/sampler number.
    - timepoint: Timepoint of measurements.
    - dayfromstart / dayfromstartstring: Day from start of measurements (numeric and string forms).
    - datetime: Date and time of measurement.
    - midpointday: Time midway between this and the previous timepoint.
    - timeinterval / timeintervalstring: Length of interval since last timepoint (numeric and string forms).
  - Treatments and site metadata
    - biochartreatment: Whether sample is un-amended or amended with biochar.
    - fulltreatname: Full name of the soil treatment (biochar and wetted, etc.).
    - biocharweight: Dry biochar weight added to soil (g).
    - biocharfraction: Proportion of biochar relative to dry soil weight.
    - wettingtreatment: Whether the sample is periodically wetted to high water content.
    - temperaturetreatment: Soil temperature treatment at the time of gas measurement.
    - nitrogentreatment: 15N-labeled molecule used (NH4+ or NO3−) or related label.
    - site: Site identifier for the soil source.
  - Gas flux measurements (flux units and conversions)
    - mgCO2-Cfluxm2h1: CO2 flux (mg C per m2 per hour).
    - log10co2: log10(flux + 1) for CO2 (special handling if prior flux was negative).
    - ugCH4-Cfluxm2h1: CH4 flux (mg C per m2 per hour).
    - log10ch4: log10(flux + 1) for CH4 (same logging rule as CO2).
    - ugN2O-Nfluxm2h1: N2O flux (mg N per m2 per hour).
    - log10n2o: log10(flux + 1) for N2O (same logging rule as CO2/CH4).
  - Chamber and measurement context
    - CO2ppmt0 / CH4ppmt0 / N2Oppmt0: Static chamber gas concentrations at t0 (ppm).
    - tempair: Air temperature during gas measurement.
    - gravwatercontentproportion: Soil gravimetric water content (as a proportion).
    - chambaream2: Ground area of the static chamber (m2).
    - headvolm3: Volume of the static chamber headspace (m3).
    - drysoilweightg: Dry soil weight in grams per core.
    - bulkdensitygcm3: Soil bulk density (g/cm3).
    - postmixbulkdensity: Bulk density after mixing (g/cm3).
    - particledensitygcm3: Particle density of soil (g/cm3).
    - totalporosity: Derived porosity = 1 - (bulk density / particle density).
  - Additional contextual data
    - wfpsproportion: Water-filled pore space (derived from gravimetric water content, bulk density, and total porosity).

- Transformations and derived quantities
  - log10co2, log10ch4, log10n2o are computed as log10(flux + 1), with a special rule: if a previous flux value is negative, the absolute magnitude of that negative flux is added to every flux value before logging.
  - totalporosity is computed as 1 - (bulkdensitygcm3 / particledensitygcm3).

- Data structure and relationships
  - Each row represents a specific soil core, treatment, timepoint, and measurement context, enabling analysis of treatment effects over time.
  - Measurements include both raw flux values (mg C or mg N per m2 per hour) and log-transformed values to support statistical modeling.
  - Contains both static measurements (e.g., site, soil properties) and dynamic measurements (gas fluxes, chamber conditions) across timepoints.

- Practical considerations for analysts
  - Data may require handling of log transformations with the described special rule for negative prior flux values.
  - Derived quantities (e.g., totalporosity) rely on other properties (bulk and particle densities) that may be post-mixing values.
  - Potential scale and data accessibility challenges highlighted in the archetype (e.g., integration of diverse datasets and metadata) are addressed by including clear metadata fields (units, descriptions, and relationships).