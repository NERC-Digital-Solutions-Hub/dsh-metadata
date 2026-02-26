# Column heading explanations for 5_Fuel_particle_dissolution.csv

## Overview
- Defines the metadata and meaning of each column in the 5_Fuel_particle_dissolution.csv dataset.
- Focuses on measurements related to 90Sr and 85Sr in soil, including exchangeable forms and activities associated with fuel particles.
- Clarifies sample labeling, measurement timing, data units, and uncertainty information to support consistent interpretation and reuse.

## Column definitions

- Code: Database serial number - unique ID. Units: n/a. Notes: .
- Identifier: UIAR unique label - chemical analysis number. Samples with the same identifier suffix (e.g., 1a, 1b) originate from the same site. Units: n/a. Notes: .
- Date_of_90Sr_measurement: Date of measurement (dd-mmm-yy). Units: n/a. Notes: .
- 90Sr_exchangeable_form_in_soil_%: Percentage of 90Sr present in an exchangeable form in soil. Units: percentage. Notes: .
- Relative_uncertainty_of_90Sr_exchangeable_form_portion_in_soil_%: Relative uncertainty of the 90Sr exchangeable-form proportion at 95% confidence interval. Units: percentage. Notes: .
- 85Sr_exchangeable_form_in_soil_%: Percentage of 85Sr present in an exchangeable form in soil. Units: percentage. Notes: .
- Relative_uncertainty_of_85Sr_exchangeable_form_portion_in_soil_%: Relative uncertainty of the 85Sr exchangeable-form proportion at 95% confidence interval. Units: percentage. Notes: .
- 90Sr_activity_in_the_FP-associated_form_%: Percentage of 90Sr activity in the fuel particle (FP)–associated form. Units: percentage. Notes: May contain negative values; these occur when a small exchangeable portion combines with a large error. Users should treat such values as zero. 
- Relative_uncertainty_of_90Sr_activity_in_the_FP-associated_form_%: Relative uncertainty of the 90Sr activity in the FP-associated form at 95% confidence interval. Units: percentage. Notes: .

- Notes: Various fields show Notes = . (i.e., no additional notes provided).

## Data quality, interpretation and governance implications

- Measurement uncertainty is explicitly recorded (95% CI), supporting transparent uncertainty analysis in monitoring frameworks.
- Possible negative values for 90Sr activity in FP-associated form are not physically meaningful; guidance is to interpret these as zero when using the data for policy or health assessments.
- Sample labeling (e.g., 1a, 1b) enables site-based traceability, which is important for spatial monitoring and comparative analyses.
- Many fields have blank notes, indicating opportunities to enrich metadata for better data governance and reuse.

## References

- Kashparov, V. A., Oughton, D. H., Zvarich, S. I., Protsak, V. P., and Levchuk, S. E.: Kinetics of fuel particle weathering and 90Sr mobility in the Chernobyl 30-km exclusion zone. Health Physics, 1999.
- Kashparov, V. A.: Hot Particles at Chernobyl. Environmental Science and Pollution Research, 2003.
- Kashparov, V. A., Ahamdach, N., Zvarich, S. I., Yoschenko, V. I., Maloshtan, I. M., and Dewiere, L.: Kinetics of dissolution of Chernobyl fuel particles in soil in natural conditions. Journal of Environmental Radioactivity, 2004.