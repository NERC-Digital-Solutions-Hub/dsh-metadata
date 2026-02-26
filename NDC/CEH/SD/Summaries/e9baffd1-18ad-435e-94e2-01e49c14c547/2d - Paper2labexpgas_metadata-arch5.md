# Soil Gas Flux Measurements Data Dictionary

## Purpose and scope
- Defines the data fields and metadata for soil gas flux measurements, including CO2, CH4, and N2O fluxes, associated treatments, and environmental context.
- Supports data governance by clarifying data elements, units, transformations, and provenance for reuse and sharing.

## Core data model and field groups
- Sample and time identifiers
  - soilcoreno: Unique identifier for the soil sample/core
  - timepoint: Timepoint of measurements
  - dayfromstart: Days from the start of measurements
  - daysfromwettingevent: Days since last wetting event
  - datetime: Date and time of the soil gas flux analysis
- Treatments and naming
  - temperaturetreatment: Soil temperature condition
  - biochartreatment: Biochar amendment status (un-amended or amended)
  - wettingtreatment: Periodic wetting status
  - fulltreatname: Full name of the soil treatment (e.g., biochar and wetted)
  - biocharweightg: Dry biochar weight added to the soil
  - biocharfraction: Biochar proportion relative to dry soil weight
- Gas flux measurements and derived metrics
  - mgCO2-Cfluxm2h1: CO2 flux (mg C per m2 per h)
  - log10co2: Base-10 log of (CO2 flux + 1); negative flux handling described below
  - ugCH4-Cfluxm2h1: CH4 flux (µg C per m2 per h)
  - log10ch4: Base-10 log of (CH4 flux + 1); negative flux handling described below
  - ugN2O-Nfluxm2h1: N2O flux (µg N per m2 per h)
  - log10n2o: Base-10 log of (N2O flux + 1); negative flux handling described below
- Chamber and ambient conditions
  - CO2ppmt0, CH4ppmt0, N2Oppmt0: Gas concentrations in ppm in the static chamber headspace at t0
  - tempair: Temperature of the soil air at measurement
  - chambaream2: Soil area within the static chamber (m2)
  - headvolm3: Headspace volume of the static chamber (m3)
- Soil physical properties and moisture
  - gravwatercontentproportion: Gravimetric water content (as a proportion)
  - drysoilweightg: Dry weight of soil in the core (g)
  - totalporosity: Total soil porosity
  - particledensitygcm3: Particle density (g/cm3)
  - wfpsproportion: Water-filled pore space (WFPS) as a proportion
- Temporal and measurement context
  - datetime: Date and time of the measurement (aligned with flux data)
  - dayfromstart and daysfromwettingevent help contextualize longitudinal measurements

## Data quality, units, and transformations
- Units
  - CO2 flux: mg CO2-C flux m-2 h-1
  - CH4 flux: ug CH4-C flux m-2 h-1
  - N2O flux: ug N2O-N flux m-2 h-1
  - Concentrations: ppm in headspace
  - Other quantities: g, m2, m3, proportions as specified
- Derived fields and transformation rules
  - log10co2, log10ch4, log10n2o are log10(flux + 1)
  - If the flux in the previous column is negative, the magnitude of that negative flux is added to every flux value before logging (to enable log transformation of negative values)
- Metadata and provenance
  - Each field includes a description clarifying purpose and unit
  - Data may be subject to quality assurance, cleaning, and transformation before sharing
- Data availability and updates
  - Clear understanding of updates, embargoes, or redistribution rights as part of sharing

## Governance, sharing, and provenance practices
- Data handling workflow
  - Receive datasets from data creators
  - Apply quality assurance and cleaning
  - Transform and prepare for publication or portal upload
  - Document work performed on datasets
  - Upload to relevant portals and catalogue data holdings
- Compliance and standards
  - Ensure consistency of field definitions, units, and metadata
  - Maintain traceability of changes and versions for reproducibility

## Challenges relevant to Data Stewards
- Incomplete picture of user needs and priorities
- Timely accessibility of data from creators
- Getting data creators to meet standards (metadata completeness, consistent formats)
- Handling multiple systems and formats, including difficult or non-interoperable ones
- Managing large datasets and transfer logistics
- Dealing with outdated databases necessitating bespoke solutions

## Practical implications for data stewardship
- Promote standardized submission templates and validation checks for metadata and units
- Enforce consistent data formats and clear field definitions
- Capture and preserve provenance, including processing steps (QC, cleaning, transformations)
- Support versioning, access controls, and, where applicable, embargo policies
- Provide clear documentation on the log transformation approach and special handling of negative flux values

## Summary takeaway
- This dataset provides a structured, well-documented data dictionary for soil gas flux measurements under various treatments, with explicit unit conventions, derived log-transform rules, and comprehensive metadata to support discoverability, reuse, and governance by data stewards.