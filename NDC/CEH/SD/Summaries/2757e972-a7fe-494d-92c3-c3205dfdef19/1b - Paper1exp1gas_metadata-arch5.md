# Soil Gas Flux Measurements Data Dictionary

- A variable-level description set for a soil gas flux dataset collected under biochar and related soil treatments, detailing sample identifiers, timepoints, measurements, treatments, soil properties, and metadata to support governance, discoverability, and reuse.

## What the dataset covers

- Sample identifiers and timing:
  - soilcoreno: unique soil/core sample number
  - timepoint, dayfromstart, dayfromstartstring, datetime, midpointday, timeinterval, timeintervalstring
- Treatments and experimental setup:
  - biochartreatment, fulltreatname
  - biocharweight, biocharfraction
  - temperaturetreatment, nitrogentreatment, wettingtreatment
  - site
- Gas flux measurements and quality
  - mgCO2-Cfluxm2h1 (CO2 flux)
  - log10co2 (log10(CO2 flux + 1) with handling for negative values)
  - ugCH4-Cfluxm2h1 (CH4 flux)
  - log10ch4 (log10(CH4 flux + 1) with handling for negative values)
  - ugN2O-Nfluxm2h1 (N2O flux)
  - log10n2o (log10(N2O flux + 1) with handling for negative values)
  - CO2ppmt0, CH4ppmt0, N2Oppmt0 (gas concentrations in headspace at t0)
- Environmental and chamber context
  - tempair (air temperature at measurement)
  - gravwatercontentproportion (gravimetric soil water content)
  - chambaream2 (soil area within the static chamber)
  - headvolm3 (static chamber headspace volume)
  - drysoilweightg (dry soil mass in the core)
  - biocharweight (dry biochar added)
  - biocharfraction (biochar as a proportion of dry soil weight)
  - bulkdensitygcm3 (soil bulk density)
  - postmixbulkdensity (bulk density after mixing)
  - particledensitygcm3 (particle density)
  - totalporosity (derived porosity from densities)
  - temperaturetreatment (soil temperature condition for the sample)
  - wettingtreatment (whether soil was periodically wetted)
  - wfpsproportion (water-filled pore space)
- Derived and provenance information
  - site (site number)
  - datetime (date and time of measurement)
  - midpointday, timeinterval (temporal context)
  - log10 transformations and accompanying notes on calculation method (offset of +1 and handling of negative flux values)

## Data quality, processing, and stewardship considerations

- Data processing
  - Quality assurance, cleaning, and transformation are performed before sharing.
  - Log-transform fields are defined with a consistent offset rule and special handling when original flux values are negative.
- Metadata and documentation
  - Comprehensive field descriptions, units, and calculation notes should accompany datasets to aid reuse.
  - Documentation of data lineage, processing steps, and any changes between versions.
- Data availability and updates
  - Clearly defined data sharing restrictions, embargoes, and update mechanisms.
  - Systems in place to incorporate updates and to track versioning.
- Data governance and interoperability
  - Use consistent units, formats, and controlled vocabularies to support interoperability across systems and portals.
  - Catalog datasets in relevant portals and ensure discoverability through metadata tagging and proper dataset documentation.

## Key challenges for Data Stewards

- Incomplete understanding of user needs and priorities for this dataset.
- Timely acquisition of data from multiple data creators.
- Ensuring data creators meet standards for metadata, units, and formatting.
- Managing data across diverse systems and formats, including large datasets.
- Maintaining compatibility with older databases requiring bespoke, non-interoperable solutions.

## Practical actions for Data Stewards

- Define and enforce metadata requirements for all contributing data creators.
- Provide templates and validation tools for units, field names, and calculations (e.g., log transformations with offset rules).
- Establish submission workflows and follow-up processes to obtain missing metadata or samples.
- Create and maintain data sharing policies, including embargoes and access controls.
- Maintain and curate a portal or catalog for discoverability, with clear versioning and provenance records.