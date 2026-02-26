# Supporting documentation for 19-Transfer_Parameter_Animal_Stable.csv

## Purpose and scope
- Provides a data dictionary for the dataset 19-Transfer_Parameter_Animal_Stable.csv.
- Describes sample metadata and the set of concentration (CR) parameters for stable elements in milk.
- Outlines how each field should be interpreted, including units, notes, and handling of below-detection-limit values.

## Key data fields and structure
- Top-level sample metadata
  - Sample_Code: Unique sample identifier.
  - Sample_Type: General description of the sample (e.g., foodstuff group).
  - Location: Location where the sample was collected.
  - Sample_Description: Part of the organism analyzed (e.g., where the whole organism was divided and analyzed).
  - Collection_Date: Date of collection (format: dd-mm-yyyy).
- For each element/parameter (Cs, Sr, K, Na, Ca, Mg, P, Pb, U, Th)
  - CR: The concentration value for the stable element (unit varies by element; generally unitless or per kg dry matter per L for milk in certain cases).
  - Unc_CR: Uncertainty associated with the CR value (same units as CR).
  - Detection_Limit_CR: Detection limit for the CR value (same units as CR).
  - Notes: Indicates that, where blank, the value is below the detection limit (where applicable).
- Units and compatibility
  - Some fields specify units as unitless or kg dry matter per liter for milk.
  - Unc_CR, Detection_Limit_CR, and other related fields use the same units as their corresponding CR field.
- Example field naming pattern
  - Cs_CR, Unc_Cs_CR, Detection_Limit_Cs_CR
  - Sr_CR, Unc_Sr_CR, Detection_Limit_Sr_CR
  - K_CR, Unc_K_CR, Detection_Limit_K_CR
  - Na_CR, Unc_Na_CR, Detection_Limit_Na_CR
  - Ca_CR, Unc_Ca_CR, Detection_Limit_Ca_CR
  - Mg_CR, Unc_Mg_CR, Detection_Limit_Mg_CR
  - P_CR, Unc_P_CR, Detection_Limit_P_CR
  - Pb_CR, Unc_Pb_CR, Detection_Limit_Pb_CR
  - U_CR, Unc_U_CR, Detection_Limit_U_CR
  - Th_CR, Unc_Th_CR, Detection_Limit_Th_CR

## Metadata and data quality considerations
- The documentation emphasizes clear definitions for each field, including when values are below detection limits.
- Notes and some field descriptions indicate blank entries imply below-detection-limit values (where applicable).
- There are some formatting inconsistencies in the source text (e.g., truncated notes). Users should verify field completeness and consistency during data ingestion.
- The data dictionary supports cross-element comparability by standardizing field names, units (where stated), and the handling of uncertainties and detection limits.

## Practical use for data strategy (Data Leaders perspective)
- Supports governance of a dataset that combines multiple chemical transfer parameters in milk, enabling end-to-end data management from collection to analysis.
- Facilitates discovery and reuse by providing explicit metadata for each field, aiding requirement gathering from policy colleagues or downstream analysts.
- Enables data product co-ownership by outlining header fields, units, and uncertainty information, helping teams prioritize data quality improvements and metadata enhancements.
- Assists in assessing data readiness for analytical workflows, by clarifying where data gaps exist (e.g., missing detection limits or uncertain values) and how to interpret blank entries.
- Supports consistency across datasets by aligning on naming conventions (e.g., element_CR fields, corresponding uncertainty and detection limit fields) and unit expectations.

## Key considerations and potential challenges
- Data standardization: Ensure uniform units and metadata conventions across all CR parameters.
- Handling missing and below-detection-limit values: Implement clear rules based on the notes (blank equals below detection limit) in downstream analyses.
- Data quality improvements: Address formatting inconsistencies and complete any truncated notes to improve clarity and usability.
- Data discoverability: Maintain comprehensive metadata, including collection date formats and location details, to improve findability for users across networks.