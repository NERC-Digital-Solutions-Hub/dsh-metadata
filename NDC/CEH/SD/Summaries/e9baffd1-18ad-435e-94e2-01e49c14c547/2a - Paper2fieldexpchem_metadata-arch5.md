# Soil Core Sample Dataset: Variable Descriptions

## Overview
- A collection of field names and descriptions for a soil core sample dataset used in soil gas flux analysis.
- Documents key identifiers, site/context, treatment status, and a suite of soil chemical and physical measurements.
- Designed to support discovery, understanding, and reuse by data users; aligns with data governance practices for large datasets.

## Dataset Fields (Variables and Descriptions)
- soilcorenumber: Unique identifier for the soil sample/core.
- site: The field site where the sample is located.
- biocharamendment: Indicates whether the sample is unamended or amended with biochar.
- depth: The depth of the soil sample from the soil surface.
- treatmentfullname: The full name of the soil treatment (e.g., biochar and wetted).
- dayfromstart: Day count from the start of measurements.
- date: The date on which the soil gas flux analysis was performed.
- pH.water: The pH of the soil in water at a 1:2.5 ratio.
- total.C.percent: Total carbon content of the soil as a percentage.
- total.N.percent: Total nitrogen content of the soil as a percentage.
- CN ratio: The ratio of total carbon to nitrogen content in the soil.
- extract.nh4-n.mgkg: The extractable ammonium concentration (mg/kg).
- extract.no3-n.mgkg: The extractable nitrate concentration (mg/kg) after the start of incubation.
- drysoilweightg: The dry weight of the soil in the core (grams).
- gravwatercontproportion: The gravimetric water content expressed as a proportion.
- bulkdensitygcm3: The bulk density of the soil (g/cm^3).
- bulkdensitygcm3SE: Standard error of the bulk density measurement (g/cm^3).

## Data Quality and Standards Considerations
- Units and formats: Ensure consistent units across datasets (e.g., percent for C/N, mg/kg for extractables, g/cm^3 for density, grams for weight, etc.).
- Metadata completeness: Each field provides essential context for discovery and reuse (sample identity, location, treatment, measurement timing, and key soil properties).
- Data types and validation: Numeric fields (depth, dayfromstart, pH, percentages, mg/kg, g, SE) should be validated for appropriate ranges and data types; categorical fields (biocharamendment) should use consistent categories.
- Provenance and methods: Include measurement date and treatment details to support interpretation and comparability across studies.
- Handling of limitations: Identify data availability, potential embargoes, or proprietary constraints that could affect sharing or reuse.

## Data Sharing, Cataloguing, and Stewardship
- Upload and catalogue: Prepare for publication in relevant data portals and data holdings to enhance discoverability.
- Documentation: Record and communicate work performed on datasets (curation, cleaning, transformations) to support transparency and reuse.
- Update and governance: Establish processes for updating datasets and communicating any sharing limitations or changes in metadata.

## Challenges and Considerations for Data Stewards
- Incomplete understanding of user needs and priorities for the dataset.
- Timely receipt of data from creators and ensuring adherence to metadata and format standards.
- Interoperability across diverse systems and formats, including potentially non-standard or legacy datasets.
- Managing large datasets and data transfers; handling outdated databases that require bespoke solutions.