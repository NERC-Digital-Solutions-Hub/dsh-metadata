# Supporting documentation for 19-Transfer_Parameter_Animal_Stable.csv

## Purpose and scope
- Data dictionary for the dataset 19-Transfer_Parameter_Animal_Stable.csv.
- Documents field definitions, units, and data quality conventions used for stable element transfer parameters (CR values) in milk-related samples.

## Core sample metadata
- Sample_Code: Unique sample identifier.
- Sample_Type: General description of the sample (e.g., foodstuff group).
- Location: Name of the collection location.
- Sample_Description: Part of the organism analysed (e.g., specific tissue or organ portion).
- Collection_Date: Date of sample collection (format: dd-mm-yyyy).

## Transfer parameter variables (CR values) and quality fields
- Cs_CR: CR value for stable Cesium; Units: unitless or kg dry matter per L for milk.
  - Unc_Cs_CR: Uncertainty of Cs_CR.
  - Detection_Limit_Cs_CR: Detection limit for Cs_CR.
- Sr_CR: CR value for stable Strontium; Units: unitless or kg dry matter per L for milk.
  - Unc_Sr_CR: Uncertainty of Sr_CR.
  - Detection_Limit_Sr_CR: Detection limit for Sr_CR.
- K_CR: CR value for stable Potassium; Units: unitless or kg dry matter per L for milk.
  - Unc_K_CR: Uncertainty of K_CR.
  - Detection_Limit_K_CR: Detection limit for K_CR.
- Na_CR: CR value for stable Sodium; Units: unitless or kg dry matter per L for milk.
  - Unc_Na_CR: Uncertainty of Na_CR.
  - Detection_Limit_Na_CR: Detection limit for Na_CR.
- Ca_CR: CR value for stable Calcium; Units and notes indicate unitless or kg dry matter per L for milk.
  - Unc_Ca_CR: Uncertainty of Ca_CR.
  - Detection_Limit_Ca_CR: Detection limit for Ca_CR.
- Mg_CR: CR value for stable Magnesium; Units and notes indicate unitless or kg dry matter per L for milk.
  - Unc_Mg_CR: Uncertainty of Mg_CR.
  - Detection_Limit_Mg_CR: Detection limit for Mg_CR.
- P_CR: CR value for stable Phosphorus; Units and notes indicate unitless or kg dry matter per L for milk.
  - Unc_P_CR: Uncertainty of P_CR.
  - Detection_Limit_P_CR: Detection limit for P_CR.
- Pb_CR: CR value for stable Lead; Units and notes indicate unitless or kg dry matter per L for milk.
  - Unc_Pb_CR: Uncertainty of Pb_CR.
  - Detection_Limit_Pb_CR: Detection limit for Pb_CR.
- U_CR: CR value for stable Uranium; Units and notes indicate unitless or kg dry matter per L for milk.
  - Unc_U_CR: Uncertainty of U_CR.
  - Detection_Limit_U_CR: Detection limit for U_CR.
- Th_CR: CR value for stable Thorium; Units and notes indicate unitless or kg dry matter per L for milk.
  - Unc_Th_CR: Uncertainty of Th_CR.
  - Detection_Limit_Th_CR: Detection limit for Th_CR.

## Data quality conventions and notes
- For each CR value, an accompanying Unc_ field provides the measurement uncertainty.
- Detection_Limit_ fields indicate the detection threshold; blank values imply the CR is below the detection limit.
- Collection_Date uses the format dd-mm-yyyy.
- Units vary by element but commonly indicate either unitless or kg dry matter per L for milk, as specified per element.

## How to use
- Use the metadata to correctly interpret CR values and their uncertainties across samples.
- Treat blank detection-limit fields as censored data (below detection limit).
- Align sample descriptions and collection dates when aggregating across studies or performing comparative analyses on transfer parameters for stable elements in milk.