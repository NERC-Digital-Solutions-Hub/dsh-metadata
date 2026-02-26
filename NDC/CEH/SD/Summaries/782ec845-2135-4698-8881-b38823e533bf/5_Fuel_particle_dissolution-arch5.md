# Column heading explanations for 5_Fuel_particle_dissolution.csv

## Overview
- Provides explanations for the column headers in the 5_Fuel_particle_dissolution.csv dataset.
- Covers identifiers, measurement dates, and key radionuclide data related to 90Sr and 85Sr in soil exchangeable forms, in the context of fuel particle dissolution studies (e.g., Chernobyl-related work).
- Indicates how samples are labeled (e.g., 1a, 1b) to show samples from the same site.
- Includes references that underpin the data interpretation and methods.

## Dataset schema and key fields
- Code: Database serial number; a unique identifier for each row.
- Identifier: UIAR unique label or chemical analysis number; samples with the same number (e.g., 1a, 1b) come from the same site.
- Date_of_90Sr_measurement: Date of measurement in the format dd-mmm-yy.
- 90Sr_exchangeable_form_in_soil_%: Percentage of 90Sr present in the soil in an exchangeable form.
- Relative_uncertainty_of_90Sr_exchangeable_form_portion_in_soil_%: Relative uncertainty of the 90Sr exchangeable portion (at 95% confidence interval).
- 85Sr_exchangeable_form_in_soil_%: Percentage of 85Sr present in the soil in an exchangeable form.
- Relative_uncertainty_of_85Sr_exchangeable_form_portion_in_soil_%: Relative uncertainty of the 85Sr exchangeable portion (at 95% confidence interval).
- 90Sr_activity_in_the_FP-associated_form_%: Percentage activity of 90Sr in the fuel particle (FP)-associated form (value may be negative in some cases).
- Relative_uncertainty_of_90Sr_activity_in_the_FP-associated_form_%: Relative uncertainty of the 90Sr activity in the FP-associated form (at 95% confidence interval).
- Notes: Some 90Sr FP-associated form values may be negative due to low exchangeable-form percentages coupled with high error; users should treat these as zero.

## Data quality and interpretation considerations
- Units and formats vary by field (e.g., some are percentages, others are “n/a” for certain codes); consistency in a data dictionary is important.
- Uncertainty fields are provided at 95% confidence intervals, enabling quality assessment and weighting in analyses.
- Negative values in 90Sr activity for FP-associated form are an expected artefact of measurement constraints; recommended practice is to treat such values as zero during downstream analysis.
- Sample naming conventions (1a, 1b, etc.) indicate spatial or site grouping, which is important for aggregations and comparisons across sites.
- Metadata should document the measurement context, method references, and any data transformations applied.

## Provenance and references
- Kashparov, V. A., Oughton, D. H., Zvarich, S. I., Protsak, V. P., and Levchuk, S. E.: Kinetics of fuel particle weathering and 90Sr mobility in the Chernobyl 30-km exclusion zone. Health Physics, 1999.
- Kashparov, V. A.: Hot Particles at Chernobyl. Environmental Science and Pollution Research, 2003.
- Kashparov, V. A., Ahamdach, N., Zvarich, S. I., Yoschenko, V. I., Maloshtan, I. M., and Dewiere, L.: Kinetics of dissolution of Chernobyl fuel particles in soil in natural conditions. Journal of Environmental Radioactivity, 2004.
- These references provide context for the measurement approach and interpretation of 90Sr/85Sr in soil and FP-associated forms.

## Data stewardship considerations and actions
- Ensure a complete data dictionary accompanies the dataset, clarifying units, field names, and allowable value ranges.
- Enforce standardized field names and consistent formatting (e.g., date formats, percentage domains).
- Preserve sample grouping indicators (e.g., 1a, 1b) to enable site-based analyses and reproducibility.
- Capture data provenance, including references to underlying methodologies and any data processing steps.
- Clarify data availability and any potential disclosure or embargo conditions; document any limitations or caveats in data sharing.
- Implement quality checks to flag unusual values (e.g., negative FP-associated 90Sr activity) and confirm they are treated appropriately in analyses.
- Maintain versioning and an audit trail for updates or corrections to measurements, uncertainties, or metadata.