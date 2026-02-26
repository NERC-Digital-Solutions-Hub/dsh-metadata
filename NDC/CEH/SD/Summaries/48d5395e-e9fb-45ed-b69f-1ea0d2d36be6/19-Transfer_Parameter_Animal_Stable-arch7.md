# Supporting documentation for 19-Transfer_Parameter_Animal_Stable.csv

- Purpose and scope
  - Provides metadata and measurement values for the 19-Transfer_Parameter_Animal_Stable.csv dataset.
  - Focuses on concentrations (CR values) of multiple elements in stable samples (milk), with accompanying uncertainty and detection-limit information.
  - Indicates handling of non-detects (blank fields are treated as below detection limit).

- Key metadata fields
  - Sample_Code: Unique sample identifier.
  - Sample_Type: General description of the sample (e.g., foodstuff group).
  - Location: Name of the collection site.
  - Sample_Description: Part of the organism analysed (e.g., where the organism was divided).
  - Collection_Date: Date of sample collection (format: dd-mm-yyyy).
  - Notes: Various fields are marked as not applicable (n/a) for many columns.

- Measurement data structure
  - For each element (e.g., Cs, Sr, K, Na, Ca, Mg, P, Pb, U, Th):
    - CR (Concentration/CR value): Reported as unitless or per kg dry matter per litre for milk, depending on the element.
    - Unc_CR (Uncertainty of CR): Represents the uncertainty of the CR value.
    - Detection_Limit_CR (Detection limit): The detection limit for the CR value.
    - Where blank: indicates below detection limit (non-detect).
  - Example columns included: Cs_CR, Unc_Cs_CR, Detection_Limit_Cs_CR; Sr_CR, Unc_Sr_CR, Detection_Limit_Sr_CR; K_CR, Unc_K_CR, Detection_Limit_K_CR; Na_CR, Unc_Na_CR, Detection_Limit_Na_CR; Ca_CR, Unc_Ca_CR, Detection_Limit_Ca_CR; Mg_CR, Unc_Mg_CR, Detection_Limit_Mg_CR; P_CR, Unc_P_CR, Detection_Limit_P_CR; Pb_CR, Unc_Pb_CR, Detection_Limit_Pb_CR; U_CR, Unc_U_CR, Detection_Limit_U_CR; Th_CR, Unc_Th_CR, Detection_Limit_Th_CR.
  - Additional notes indicate blanks imply below detection limit; some fields include unit qualifiers such as “per L for milk” or “kg dry matter per L”.

- Temporal and spatial aspects
  - Collection_Date provides temporal context for the samples.
  - Location provides spatial context; may require geocoding to map, as only location names are provided.
  - Data are intended to be used in GIS-enabled analyses and map-based visualizations, with fields ready for joins to spatial features via Sample_Code or Location.

- Data quality and consistency considerations
  - Some fields appear truncated or inconsistently formatted in the documentation (e.g., Ca_CR and related notes), signaling potential documentation or data loading issues.
  - The documentation emphasizes that data standards may be inconsistent across sources ("Lack of consistent data standards" is a general challenge).
  - Large or complex datasets may need packaging into manageable chunks; cleaning and transformation steps are necessary to prepare for GIS use.

- Practical guidance for GIS use
  - Integrate into GIS by linking Sample_Code or Location to spatial features (e.g., milk sampling sites, regions).
  - Use Collection_Date as a time attribute to enable temporal analyses or time-series mapping.
  - Map element CR values as thematic layers or layered attributes, with non-detects represented using censoring information (e.g., separate attribute for Detection_Limit and Unc_CR).
  - Standardize units across elements if integrating with other datasets; explicitly record units per element (noting they vary between “unitless” and “kg dry matter per L” for milk).
  - Handle missing and non-detect values explicitly to avoid misinterpretation in visualizations (non-detects vs. missing data).

- Considerations and caveats
  - Data may originate from multiple sources or locations, requiring harmonization.
  - Ensure careful treatment of below-detection-limit values in analyses and visualizations.
  - Verify and resolve any formatting anomalies in the documentation before loading into GIS workflows.