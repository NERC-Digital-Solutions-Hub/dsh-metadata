# Soil Core Sample Dataset - Variable Descriptions

- A dataset describing individual soil core samples and their treatments, with a suite of chemical, physical, and moisture measurements collected after mixing and at later incubation. It supports comparison of biochar-amendment effects versus non-amended soils.

## Key variables and what they capture

- soilcorenumber: Identifier for the soil sample/core.
- treatmentfullname: Full name of the soil treatment (biochar and wetted).
- treatmentnamenowet: Full name of the soil treatment (biochar, not wetted).
- shorttreatmentname: Shortened treatment name for concise labeling.
- biocharamendment: Indicates if the sample is un-amended or amended with biochar.
- temperature: Soil temperature of the sample.
- pH.water: Soil pH measured in water at a 1:2.5 ratio.
- total.C.percent: Total carbon content of the soil (percent).
- total.N.percent: Total nitrogen content of the soil (percent).
- CN ratio: Ratio of total carbon to nitrogen content in the soil.
- extract.nh4-n.mgkg: Extractable ammonium (NH4-N) in mg/kg.
- extract.no3-n.mgkg: Extractable nitrate (NO3-N) in mg/kg after the start of incubation.
- bulkdens.after.mix.gcm3: Bulk density immediately after mixing (g/cm3).
- bulkdens.fortydays.after.mix.gcm3: Bulk density 40 days after mixing (g/cm3).
- WFPS.field.moist.proportion: Water-filled pore space at field moisture status, calculated from gravimetric water content, bulk density, and total porosity.
- WFPS.after.wetting.proportion: Water-filled pore space immediately after wetting, calculated similarly.

## Data quality, standards, and governance implications

- Metadata presence: Each variable has a descriptive label, including units where applicable, aiding discoverability and understanding.
- Consistency considerations: Multiple naming fields for treatments (fullname, nowet, short name) suggest a need for harmonized, standardized naming to prevent ambiguity.
- Temporal framing: Measurements cover immediate post-mix conditions and a 40-day interval, with some fields tied to incubation timing (e.g., extractable NO3-N after incubation start).
- Derived metrics: CN ratio and WFPS metrics are derived from other measurements, highlighting the importance of clear calculation methods and provenance.
- Granularity and scope: Focused on soil cores with treatment comparisons, enabling intra- and inter-treatment analyses across chemical, physical, and moisture properties.

## How this dataset supports Data Leaders’ aims

- Whole data system perspective: Captures a cohesive set of core identifiers, treatments, and multi-domain measurements (chemistry, physics, moisture) enabling end-to-end data product development.
- User-centered validation: Descriptions and units facilitate user understanding; the presence of multiple treatment names supports flexible labeling for stakeholders.
- Data availability and gaps: The dataset includes key properties but may require additional metadata on measurement methods, porosity calculation, and data provenance to improve discoverability and reuse.
- Data stewardship: The explicit fields for treatment and amendment status support traceability of experimental design and data lineage.
- Community and collaboration potential: Clear treatment distinctions and granular measurements can be shared across teams working on soil health, carbon cycling, and land management.

## Challenges and considerations for implementation

- Naming consistency: Variations in treatment naming (fullname vs nowet vs short name) may hinder data integration; align to a single, controlled vocabulary.
- Metadata depth: Consider adding measurement methods, instruments used, incubation conditions, sampling timing, and data quality flags to strengthen data quality and reuse.
- Standardization: Ensure uniform units and definitions across all records; document any deviations or exceptions.
- Data discoverability: Provide a public data dictionary, data lineage, and versioning to facilitate discovery by policy colleagues and partner networks.

## Recommendations for action

- Standardize field naming and create a controlled vocabulary for treatments.
- Enrich metadata with measurement methods, instrument details, incubation conditions, and data quality indicators.
- Document data lineage and version history to support reproducibility and accountability.
- Publish a centralized data dictionary and data catalog entry to improve discoverability for internal and external stakeholders.
- Establish data quality checks and validation rules (e.g., plausible ranges for pH, CN ratios, and bulk density) to flag anomalies.