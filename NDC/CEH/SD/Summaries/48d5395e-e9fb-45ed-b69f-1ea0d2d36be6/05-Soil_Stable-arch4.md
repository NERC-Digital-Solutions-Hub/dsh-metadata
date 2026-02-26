# Supporting documentation for 05-Soil_Stable.csv

- Overview
  - Metadata and field definitions for a soil sample dataset focusing on stable element concentrations.
  - Captures sample identifiers, location, description, collection date, sample size, and concentrations with associated uncertainties and detection limits.

- Key data fields and definitions
  - Sample_Code: Unique sample identifier.
  - Sample_Type: Soil.
  - Location: Name of the collection location.
  - Sample_Description: Additional details; example provided—soil collected at depth 0-10 cm.
  - Collection_Date: Date of sample collection (format: dd-mm-yyyy).
  - Sample_size_g_dm: Amount of sample analyzed (g dry matter).
  - Element concentration fields (all on a dry matter basis where specified):
    - Cs_mg/kg_dm; Unc_Cs_mg/kg_dm; Detection_Limit_Cs_mg/kg_dm
    - Sr_mg/kg_dm; Unc_Sr_mg/kg_dm; Detection_Limit_Sr_mg/kg_dm
    - K_mg/kg_dm; Unc_K_mg/kg_dm; Detection_Limit_K_mg/kg_dm
    - Na_mg/kg_dm; Unc_Na_mg/kg_dm; Detection_Limit_Na_mg/kg_dm
    - Ca_mg/kg_dm; Unc_Ca_mg/kg_dm; Detection_Limit_Ca_mg/kg_dm
    - Mg_mg/kg_dm; Unc_Mg_mg/kg_dm; Detection_Limit_Mg_mg/kg_dm
    - P_mg/kg_dm; Unc_P_mg/kg_dm; Detection_Limit_P_mg/kg_dm
    - Pb_mg/kg_dm; Unc_Pb_mg/kg_dm; Detection_Limit_Pb_mg/kg_dm
    - U_mg/kg_dm; Unc_U_mg/kg_dm; Detection_Limit_U_mg/kg_dm
    - Th_mg/kg_dm (with multiple suffixes in some rows, e.g., 1, 2, 3); Unc_Th_mg/kg_dm; Detection_Limit_Th_mg/kg_dm
  - Notes on data values:
    - Where a concentration or uncertainty field is blank, the value is below the detection limit.
    - Some fields include clarifications such as “on a dry matter basis” or “mass” to denote units.
    - For Th, multiple entries (Th_mg/kg_dm, 1/2/3) suggest multiple related measurements or records within the same dataset.

- Data quality, standards, and handling
  - Units are predominantly mg per kg dry mass (mg/kg_dm) or g dry matter for sample size.
  - Detection limits are provided for most elements to indicate measurement sensitivity.
  - Uncertainties accompany concentrations to quantify measurement precision.
  - Metadata supports discoverability and interpretation (location, collection date, description).
  - Some inconsistencies and formatting issues in the dataset presentation (e.g., varied phrasing like “on a dry matter basis” vs. “mass,” and irregular column labeling for Th) may require cleaning during integration.
  - Missing values are signaled by blanks, typically representing concentrations below detection limits.

- Data governance, usability, and integration
  - This documentation enables understanding of data provenance (sample collection context, location, and date) and analytic readiness (concentration values with uncertainties and detection limits).
  - Supports cross-system data sharing and re-use by standardizing key metadata fields (Sample_Code, Location, Collection_Date, Sample_size_g_dm) and element-specific metadata (concentration, uncertainty, detection limit).
  - Facilitates quality control and decision-making related to data gaps, reliability, and comparability across samples and studies.

- Practical considerations for Data Leaders
  - Assess data completeness by checking for blanks that indicate concentrations below detection limits.
  - Align unit conventions across systems (ensure mg/kg_dm and g dry matter are consistently applied).
  - Plan for data cleaning to harmonize field names and resolve inconsistencies in Th-related fields.
  - Leverage detection limits and uncertainties to evaluate data suitability for policy analysis or reporting.
  - Maintain metadata updates (collection context, location naming, and sample description) to support co-ownership and broader data stewardship across networks.