# Soil Gas Flux Measurements Dataset with Biochar Treatment: Variable Descriptions

## Overview
- A dataset describing soil gas flux measurements and related soil properties for cores with potential biochar amendments.
- Includes timepoint-specific gas flux data (CO2, CH4, N2O, CO), gas concentrations at start, environmental context, and soil/chamber characteristics.
- Designed to support analysis of treatment effects (biochar) and gas production under defined measurement conditions.

## What this dataset contains
- Sample and timing identifiers
  - soilcoreno: Individual soil sample/core number
  - timepoint: Timepoint of measurements
  - dayfromstart: Days from start of measurements
  - hourfromstart: Hours from start of measurements
  - datetimefirst: Date and time of the first soil gas flux measurement
- Treatment information
  - biochartreatment: Indicates whether the sample is un-amended or amended with biochar
  - biocharweight: Dry weight of biochar added to the soil
  - biocharfraction: Proportion of dry soil weight that is biochar
- Gas flux measurements (cumulative)
  - ugCO2-Cfluxg-1cumu: CO2 cumulative gas production (ug CO2-C flux g-1 dry soil)
  - ngCH4-Cfluxg-1cumu: CH4 cumulative gas production (ng CH4-C flux g-1 dry soil)
  - ngN2O-Nfluxg-1cumu: N2O cumulative gas production (ng N2O-N flux g-1 dry soil)
  - ugCO-Cfluxg-1cumu: CO cumulative gas production (ug CO-C flux g-1 dry soil)
- Gas concentrations at t0 (static chamber headspace)
  - CO2ppmt0, CH4ppmt0, N2Oppmt0, COppmt0: ppm of respective gases at t0
- Environmental and soil context
  - tempair: Temperature of the soil at the time of gas measurement
  - gravwatercontentproportion: Gravimetric soil water content (proportion)
  - bulkdensitygcm3: Soil bulk density (g/cm3)
  - wfpsproportion: Water-filled pore space (calculated from gravimetric water content and bulk density)
  - maximumwhc: Maximum water holding capacity of the soil
  - proportionofwhc: Proportion of maximum WHC at time of gas sampling
- Chamber context
  - chambaream2: Soil area within the static chamber (m2)
  - headvolm3: Volume of the static chamber headspace (m3)
- Sample mass
  - drysoilweightg: Dry soil weight in the soil core (g)
- Additional context
  - datetimefirst (relevant for time alignment with gas measurements)

## Data quality and metadata considerations for Data Stewards
- Attribute clarity
  - Ensure consistent units across records (e.g., ug, ng, ppm, g, m2, m3).
  - Maintain explicit definitions for derived fields (e.g., how wfpsproportion is calculated).
- Metadata completeness
  - Document data collection protocol, measurement intervals, and any calibration or instrument details.
  - Record data provenance: who collected data, data entry procedures, and any transformations.
- Data governance and sharing
  - Define data ownership, access rights, and embargoes if applicable.
  - Establish versioning, update cadence, and avenues for re-use (catalogue visibility).
- Interoperability
  - Use standardized vocabularies for treatment descriptors and measurement methods where possible.
  - Maintain consistent naming conventions to facilitate cross-dataset integration.
- Data quality assurance
  - Implement checks for outliers, missing values, and unit consistency during ingestion.
  - Document QA steps and any data cleaning or transformation applied.

## Ingestion, curation, and sharing workflow (Data Steward perspective)
- Receive data from data creators/sharers.
- Quality assure: verify accuracy, consistency of units, and alignment of timepoints.
- Clean and transform: resolve discrepancies, standardize metadata fields, and compute derived indicators if needed.
- Upload: deposit into appropriate data portals and catalogues; attach comprehensive metadata and lineage.
- Documentation: maintain notes on methods, data quality, and any deviations; provide user-facing data dictionaries.

## Challenges and considerations to mitigate (aligned with common Data Steward issues)
- Incomplete picture of user needs and priorities
  - Engage potential data users early to determine essential metadata and accessibility requirements.
- Timeliness of data delivery
  - Establish clear data submission windows and SLAs with data providers.
- Heterogeneous data formats and systems
  - Promote and enforce standardized templates and controlled vocabularies.
- Large dataset size and transfer logistics
  - Plan for scalable storage, efficient transfer methods, and partial data access where needed.
- Working with complex measurement setups and legacy data
  - Provide detailed documentation of chamber geometry, measurement protocols, and any legacy definitions.

## Recommendations for further documentation
- Develop a concise data dictionary outlining every variable, its units, permissible values, and derivation (where applicable).
- Provide method details for gas flux calculations, air temperature measurements, and WHC calculations.
- Include data provenance and a changelog to support reproducibility and governance.