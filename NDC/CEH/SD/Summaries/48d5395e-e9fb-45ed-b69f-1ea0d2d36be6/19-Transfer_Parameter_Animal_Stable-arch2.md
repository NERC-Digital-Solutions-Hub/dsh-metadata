# Supporting documentation for 19-Transfer_Parameter_Animal_Stable.csv

## Purpose
- Provide the field definitions and data conventions used in the 19-Transfer_Parameter_Animal_Stable.csv dataset.
- Support consistent monitoring of transfer parameters for stable elements in animals, enabling environmental health assessment over time.

## Scope of the dataset
- Captures sample-level metadata and measured transfer parameters for stable elements in animal-related samples.
- Focuses on Cs, Sr, K, Na, Ca, Mg, P, Pb, U, and Th transfer values (CR) with associated uncertainty and detection limits.
- Emphasizes standardized data handling to support comparability and policy performance evaluation.

## Key fields and definitions
- Sample_Code: Unique sample identifier.
- Sample_Type: General description of sample (e.g., foodstuff group).
- Location: Name of the collection location.
- Sample_Description: Part of the organism analysed (e.g., tissue/location within the organism).
- Collection_Date: Date of sample collection (dd-mm-yyyy).
- Cs_CR, Sr_CR, K_CR, Na_CR, Ca_CR, Mg_CR, P_CR, Pb_CR, U_CR, Th_CR: CR value (transfer parameter) for the respective stable element.
- Unc_Cs_CR, Unc_Sr_CR, Unc_K_CR, Unc_Na_CR, Unc_Ca_CR, Unc_Mg_CR, Unc_P_CR, Unc_Pb_CR, Unc_U_CR, Unc_Th_CR: Uncertainty of the CR value for the respective element.
- Detection_Limit_Cs_CR, Detection_Limit_Sr_CR, Detection_Limit_K_CR, Detection_Limit_Na_CR, Detection_Limit_Ca_CR, Detection_Limit_Mg_CR, Detection_Limit_P_CR, Detection_Limit_Pb_CR, Detection_Limit_U_CR, Detection_Limit_Th_CR: Detection limit for the respective CR value.
- Units: Specifies units for each field where applicable (e.g., Cs_CR and others described as unitless or kg dry matter per L for milk; some fields note per L for milk or unitless).
- Notes: Indicates that if a field is blank, the value is below the detection limit.

## Measurement and data handling conventions
- Data are verified, quality assured, cleaned, and transformed as part of standardised analysis.
- CR values represent stable element transfer results; associated uncertainties and detection limits accompany each value.
- Blank values indicate non-detects (below detection limit) for the corresponding measurement.
- Documentation clarifies units and context (e.g., milk-related units for some CR fields).

## Data quality and storage
- Outputs are prepared to be presented in clear formats (reports, maps, charts) and stored/uploaded to appropriate data portals.
- Emphasises standardised methods and consistent formatting to enable scrutiny of environmental health and policy performance over time.

## Practical use for Analysts Monitoring the Environment
- Enables consistent monitoring of transfer parameters across samples, locations, and time.
- Supports trend analysis, comparisons against standards, and reporting for environmental health assessments.
- Facilitates integration with other datasets while maintaining standardized metadata.

## Challenges and considerations
- Increasing the value of datasets by combining them with other relevant data (beyond single-use analyses).
- Ensuring open access or broad accessibility to underlying data used to create final outputs.