# Column heading explanations for 5_Fuel_particle_dissolution.csv

- This document defines the column headings and their meanings for the 5_Fuel_particle_dissolution.csv dataset, focusing on 90Sr and 85Sr in soil in exchangeable forms and the activity of fuel particle-associated forms. It includes data structure guidance, measurement timing, and uncertainty reporting to support standardized environmental monitoring and analysis.

## Data columns and definitions

- Code: Database serial number – a unique identifier for each row.
- Identifier: UIAR unique label; samples with the same number come from the same site.
- Date_of_90Sr_measurement: Date of measurement in the format dd-mmm-yy.
- 90Sr_exchangeable_form_in_soil_%: Percentage of 90Sr present in soil in an exchangeable form.
- Relative_uncertainty_of_90Sr_exchangeable_form_portion_in_soil_%: Relative uncertainty of the 90Sr exchangeable soil portion, at 95% confidence.
- 85Sr_exchangeable_form_in_soil_%: Percentage of 85Sr present in soil in an exchangeable form.
- Relative_uncertainty_of_85Sr_exchangeable_form_portion_in_soil_%: Relative uncertainty of the 85Sr exchangeable soil portion, at 95% confidence.
- 90Sr_activity_in_the_FP-associated_form_%: Percentage activity of 90Sr in the fuel-particle-associated form; may contain negative values due to measurement characteristics.
- Relative_uncertainty_of_90Sr_activity_in_the_FP-associated_form_%: Relative uncertainty of the 90Sr activity in the FP-associated form, at 95% confidence.
- Units: Indicates the measurement units for each column (e.g., % or n/a where not applicable).
- Notes: Additional information or caveats; for example, the 90Sr activity in FP-associated form may be negative and should be treated as zero by users.

## Data quality and interpretation notes

- Negative values in 90Sr_activity_in_the_FP-associated_form_% may arise from low exchangeable 90Sr percentages combined with high error; users should assume these values are zero.
- The dataset uses standardized dating and uncertainty reporting (95% confidence intervals) to support consistent temporal analyses.
- Grouping by Identifier allows tracking samples from the same site, facilitating site-level comparisons over time.

## References

- Kashparov, V. A., Oughton, D. H., Zvarich, S. I., Protsak, V. P., and Levchuk, S. E.: Kinetics of fuel particle weathering and 90Sr mobility in the Chernobyl 30-km exclusion zone. Health Physics, 76(3), 251-259, 1999.
- Kashparov, V. A.: Hot Particles at Chernobyl. Environmental Science and Pollution Research, 10(1), 21-30, 2003.
- Kashparov, V. A., Ahamdach, N., Zvarich, S. I., Yoschenko, V. I., Maloshtan, I. M., and Dewiere, L.: Kinetics of dissolution of Chernobyl fuel particles in soil in natural conditions. Journal of Environmental Radioactivity, 72, 335-353, 2004.