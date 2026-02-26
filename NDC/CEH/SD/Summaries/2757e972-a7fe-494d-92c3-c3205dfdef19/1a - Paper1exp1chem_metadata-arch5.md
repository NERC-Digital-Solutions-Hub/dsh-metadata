# Soil Sample Core and Treatment Dataset: Variable Descriptions

## Overview
- Describes a set of soil sample variables and their metadata for a treatment study (including biochar amendments).
- Intended for Data Stewards to ensure data quality, interoperability, and discoverability; supports proper governance, sharing, and cataloguing of the dataset.
- Captures identifiers, treatment designations, measured properties, and derived calculations.

## Key variables and data structure
- Identifiers and treatments
  - soilcorenumber: Individual number for each soil sample/core.
  - treatmentfullname: Full name of the soil treatment (biochar and wetted).
  - treatmentnamenowet: Full name of the soil treatment (biochar only).
  - shorttreatmentname: Shortened treatment name.
  - biocharamendment: Indicates whether the sample is un-amended or amended with biochar.
- Environmental measurement
  - temperature: Soil temperature of the sample.
  - pH.water: pH of the soil in water (1:2.5 ratio).
- Soil chemical composition
  - total.C.percent: Total carbon content as a percentage.
  - total.N.percent: Total nitrogen content as a percentage.
  - CN ratio: Ratio of total carbon to nitrogen content.
  - extract.nh4-n.mgkg: Extractable ammonium (NH4-N) in mg/kg.
  - extract.no3-n.mgkg: Extractable nitrate (NO3-N) after the start of incubation (mg/kg).
- Physical properties
  - bulkdens.after.mix.gcm3: Bulk density immediately after mixing (g/cm3).
  - bulkdens.fortydays.after.mix.gcm3: Bulk density 40 days after mixing (g/cm3).
  - WFPS.field.moist.proportion: Water-filled pore space under field-moist conditions, calculated as gravimetric water content × (bulk density / total porosity).
  - WFPS.after.wetting.proportion: Water-filled pore space immediately after wetting, calculated similarly.
- Notes on calculations
  - WFPS values are derived calculations that depend on gravimetric water content, bulk density, and total porosity; explicit porosity parameters are implied in the descriptions.

## Data governance considerations for Data Stewards
- Data quality and consistency
  - Ensure accurate, consistent units across all fields (e.g., percent, mg/kg, g/cm3).
  - Validate derived fields (WFPS calculations) against raw measurements and document the calculation method.
- Metadata and documentation
  - Maintain a complete data dictionary with clear definitions, units, and any derivation steps (especially for WFPS).
  - Document data provenance, collection methods, and any data transformations (e.g., cleaning or normalization).
- Data intake and coordination
  - Data creators should provide complete metadata and timely data delivery; establish processes to chase missing items.
  - Support multiple systems/formats by adopting interoperable standards and clear field mappings.
- Data availability and sharing
  - Respect any sharing limitations or embargoes; record data access restrictions.
  - Upload and catalogue datasets in relevant portals; maintain versioning and update mechanisms.

## Practical actions for data stewardship
- Establish a data dictionary and data schema aligned with the dataset variables and units.
- Assign data owners and maintain provenance, including collection date, methods, and treatment details.
- Implement data validation rules to check for missing values, incorrect units, and outliers.
- Ensure clear documentation of derived fields (e.g., WFPS) and their calculation inputs.
- Integrate the dataset into data portals/catalogues and maintain metadata updates over time.
- Plan for updated data releases and version control to reflect any reprocessing or corrections.

## Challenges and considerations
- Incomplete understanding of user needs and priorities related to specific variables or derived metrics.
- Timely acquisition of data from creators and alignment across multiple systems and formats.
- Ensuring standardized metadata and formats across a dataset that includes both raw measurements and derived calculations.
- Handling large datasets and potentially outdated underlying databases requiring bespoke, non-interoperable solutions.

## Endnotes
- The dataset centers on soil core identifiers, treatment designations (including biochar presence), basic environmental and chemical properties, physical properties, and derived soil moisture metrics, forming a coherent basis for data discovery, governance, and reuse.