# Soil Core Sample Data Dictionary

## Overview
- Describes field-level metadata for a dataset of soil core samples, including identifiers, treatment, and key soil properties.

## Key Data Fields
- soilcorenumber: Unique identifier for the soil core
- soilcorename: Name of the individual soil sample
- treatmentfullname: Full name of the soil treatment (biochar and wetted)
- pH.water: pH of the soil in water at a 1:2.5 ratio
- total.C.percent: Total carbon content of the soil (percent)
- total.N.percent: Total nitrogen content of the soil (percent)
- CN ratio: Ratio of total carbon to nitrogen content (C/N)
- extract.nh4-n.mgkg: Extractable ammonium (mg/kg)
- extract.no3-n.mgkg: Extractable nitrate after incubation (mg/kg)
- bulkdensitygcm3: Bulk density of the soil (g/cm3)
- wfpsproportion: Water filled pore space (gravimetric water content × (bulk density / total porosity))
- whcproportion: Proportion of maximum water holding capacity at the time of gas sampling
- . (and additional fields with missing descriptions in the source dataset)

## Data Quality & Metadata Gaps
- Several fields have missing or placeholder descriptions (Description = .), indicating incomplete metadata.
- Need for consistent units, definitions, and provenance notes to improve usability and interoperability.

## Data Governance Considerations for Data Leaders
- Metadata completeness: fill in missing descriptions and ensure consistent naming and units.
- Discoverability: document data lineage, collection methods, and update cadence; link related datasets (treatment details, porosity, WHC).
- Data quality: verify measurement methods (e.g., incubation conditions, sampling timing) and ensure metadata covers these specifics.
- Access and sharing: assess any data access constraints and ensure appropriate documentation for users across teams and partner networks.

## Potential Uses and Next Steps
- Analytical use: compare soil chemical properties across cores and treatments; study carbon and nitrogen dynamics.
- Policy and practice: inform soil health assessments and nutrient management strategies for stakeholders.
- Actionable improvements: standardize field names and units, complete missing descriptions, and integrate with broader soil data assets.