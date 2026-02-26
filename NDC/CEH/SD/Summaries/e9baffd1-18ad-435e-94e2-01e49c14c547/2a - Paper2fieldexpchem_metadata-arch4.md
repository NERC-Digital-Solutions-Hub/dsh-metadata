# Soil Gas Flux Analysis Data Dictionary

## Overview
- A field-ready data dictionary describing the variables collected in a soil core/gas flux analysis study.
- Each row corresponds to a soil core sample with associated site, treatment, depth, and time measurements, plus chemical and physical soil properties.

## Key Data Fields and What They Capture
- soilcorenumber: Unique identifier for the soil core/sample.
- site: Field location of the sample.
- biocharamendment: Indicates whether the sample is un-amended or amended with biochar.
- depth: Depth of the soil sample from the soil surface.
- treatmentfullname: Full description of the soil treatment (e.g., biochar and wetted).
- dayfromstart: Day count from the start of measurements.
- date: Date of the soil gas flux analysis.
- pH.water: Soil pH measured in a water suspension (ratio 1:2.5).
- total.C.percent: Total carbon content as a percentage.
- total.N.percent: Total nitrogen content as a percentage.
- CN ratio: Carbon-to-nitrogen ratio.
- extract.nh4-n.mgkg: Extractable ammonium (NH4-N) concentration (mg/kg).
- extract.no3-n.mgkg: Extractable nitrate (NO3-N) concentration (mg/kg) after incubation starts.
- drysoilweightg: Dry soil weight of the core (grams).
- gravwatercontproportion: Gravimetric soil water content as a proportion.
- bulkdensitygcm3: Soil bulk density (g/cm³).
- bulkdensitygcm3SE: Standard error of the soil bulk density (g/cm³).

## Metadata and Data Quality
- Descriptions provide clear definitions for each variable, including units and measurement context.
- Some fields include measurement uncertainty (e.g., bulkdensitygcm3SE).
- Time-series positioning via dayfromstart and date supports tracking changes over the measurement period.
- The mix of chemical and physical soil properties enables integrated analyses related to soil respiration and gas flux experiments.

## Governance, Access, and Usage Considerations
- Metadata explicitly documents variable meanings and units, supporting data discoverability and reuse.
- Clear treatment and site identifiers facilitate cross-site comparisons and assessment of biochar impact.
- Ensure data consistency across samples (e.g., units, naming conventions) to maintain data quality and enable reliable analyses.
- Potential needs: data validation rules, handling of missing values, and alignment of dates with dayfromstart for time-series analyses.

## Implications for Data Leaders
- Establish and enforce standard metadata practices to maintain coherence across datasets and studies.
- Promote data discoverability by maintaining comprehensive variable descriptions and consistent units.
- Coordinate with field teams on data collection standards (treatment naming, depth measurement, timing) to minimize variability.
- Plan for data quality checks (units, calibration consistency, and reporting of uncertainty) to support robust analyses of soil gas flux and treatment effects.