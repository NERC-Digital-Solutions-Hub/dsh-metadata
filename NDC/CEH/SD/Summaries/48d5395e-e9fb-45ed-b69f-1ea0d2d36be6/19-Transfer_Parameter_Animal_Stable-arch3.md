# Supporting documentation for 19-Transfer_Parameter_Animal_Stable.csv

## Purpose and scope
- Provides a data dictionary for the 19-Transfer_Parameter_Animal_Stable.csv dataset.
- Describes sample metadata and measurement fields used to report transfer-related concentrations (critical elements) in milk.
- Establishes how data should be recorded, including handling of detection limits and uncertainties to support transparency and reproducibility in monitoring.

## Data fields and structure

- Sample metadata
  - Sample_Code: Unique sample identifier.
  - Sample_Type: General description of the sample (e.g., foodstuff group).
  - Location: Location where the sample was collected.
  - Sample_Description: Part of the organism analysed (e.g., where the whole organism was divided and analysed).
  - Collection_Date: Date of sample collection (dd-mm-yyyy).

- Element-specific transfer parameters (CR = concentration or transfer value)
  - Cs_CR, Sr_CR, K_CR, Na_CR, Ca_CR, Mg_CR, P_CR, Pb_CR, U_CR, Th_CR: CR values for stable elements (specific units vary by element and matrix, e.g., unitless or kg dry matter per L for milk).
  - Unc_Cs_CR, Unc_Sr_CR, Unc_K_CR, Unc_Na_CR, Unc_Ca_CR, Unc_Mg_CR, Unc_P_CR, Unc_Pb_CR, Unc_U_CR, Unc_Th_CR: Uncertainty associated with the corresponding CR value.
  - Detection_Limit_Cs_CR, Detection_Limit_Sr_CR, Detection_Limit_K_CR, Detection_Limit_Na_CR, Detection_Limit_Ca_CR, Detection_Limit_Mg_CR, Detection_Limit_P_CR, Detection_Limit_Pb_CR, Detection_Limit_U_CR, Detection_Limit_Th_CR: Detection limits for the corresponding CR value.
  - Notes: In many fields, if the value is blank, it indicates the result is below the detection limit.

- Units and interpretation
  - Several CR fields are described as Unitless or kg dry matter per L for milk, with similar guidance applying to uncertainty and detection-limit fields.
  - The document consistently uses field-specific units and explicitly notes when values are below detection limits.

## Data quality, metadata and governance considerations
- The dictionary specifies that data should be accompanied by clear metadata (e.g., units, interpretation) to ensure usability and comparability.
- It documents how missing values are treated (blank entries typically indicate results below the detection limit).
- Emphasizes the need for clear definitions for each field (e.g., what constitutes a Sample_Description) to support auditability and transparency.

## How this supports monitoring frameworks
- Standardizes data collection and reporting for environmental health monitoring related to transfer parameters in milk.
- Facilitates data quality assurance by defining uncertainties and detection limits alongside core CR values.
- Promotes openness and reproducibility by detailing field meanings, units, and handling of below-detection data, aligning with governance and data-sharing practices.