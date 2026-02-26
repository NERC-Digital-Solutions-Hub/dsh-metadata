# Supporting documentation for Biota_Stable_Element.csv

- Purpose and scope
  - Provides the data dictionary for Biota_Stable_Element.csv, detailing sample identifiers, sample descriptions, RAP classification (ICRP Reference Animals and Plants), collection date format, and the structure of concentration data for a broad suite of elements, along with corresponding detection-limit fields.
  - Notes that some samples (RCN119, RCN120, RCN121) are replicate soil samples.

- Key fields and structure
  - Sample_Code: unique sample identifier.
  - RAP: sample type based on ICRP RAPs.
  - Sample_Description: additional explanation of the sample; includes notes on replicates.
  - Collection_Date: date of soil sample collection, format dd-mmm-yyyy.
  - Element concentration fields (on a fresh mass basis, fw)
    - Examples include I-127_mg_kg_fw, Li_mg_kg_fw, Be_mg_kg_fw, B_mg_kg_fw, Na_mg_kg_fw, Mg_mg_kg_fw, Al_mg_kg_fw, P_mg_kg_fw, S_mg_kg_fw, K_mg_kg_fw, Ca_mg_kg_fw, Ti_mg_kg_fw, V_mg_kg_fw, Cr_mg_kg_fw, Mn_mg_kg_fw, Fe_mg_kg_fw, Co_mg_kg_fw, Ni_mg_kg_fw, Cu_mg_kg_fw, Zn_mg_kg_fw, As_mg_kg_fw, Se_mg_kg_fw, Rb_mg_kg_fw, Sr_mg_kg_fw, Mo_mg_kg_fw, Ag_mg_kg_fw, Cd_mg_kg_fw, Cs_mg_kg_fw, Ba_mg_kg_fw, Tl_mg_kg_fw, Pb_mg_kg_fw, U_mg_kg_fw.
  - Notes for concentration fields: blank indicates concentration below detection limit (see the corresponding Detection_Limit field); many entries explicitly state “on a fresh mass basis” and specify units as mg/kg_fw.

- Detection limit fields and conventions
  - For each element, there is a corresponding Detection_Limit_<element>_mg_kg_fw field, indicating the detection limit on a fresh mass basis.
  - Notes describe how to interpret blanks:
    - If the concentration field is blank, the concentration was below the detection limit (as given in the corresponding Detection_Limit field).
    - If the Detection_Limit field is blank, the concentration was detectable (i.e., above the detection limit).
  - Some elements use slightly varied labeling (e.g., “Detection_Limit_B_mg_kg_fw, 1 = …; 2 = …; 3 = …”) to convey the same information, or use phrases like “given sample” in the field names for context.

- Replicates and sample notes
  - Replicate samples are noted in Sample_Description (e.g., RCN119, 120, 121 are replicate soil samples).
  - Notes column provides context on analyses or how samples were used in estimating whole-organism concentration; a separate Notes field exists for general notes.

- Units and measurement scope
  - Concentrations are reported on a fresh mass basis (fw).
  - Primary units for concentrations and detection limits are milligrams per kilogram (mg/kg_fw).
  - The dataset encompasses a wide range of elements (from iodine to uranium) with extensive detection-limit information to support data quality assessment and preprocessing.

- Date formatting and data usage implications
  - Collection_Date uses a consistent date format (dd-mmm-yyyy) to facilitate parsing and temporal analyses.
  - The inclusion of RAP classification and a comprehensive set of element measurements enables cross-element analysis, comparison across RAP categories, and integration with other data products.
  - The explicit detection-limit fields support careful data cleaning, censoring decisions, and self-serve exploration of which samples exceed detection thresholds for each element.

- How this supports data use
  - Enables transparent data cleaning, transformation, and self-serve analysis by providing clear field definitions, units, and detection-limit semantics.
  - Supports multi-element analyses and RAP-based stratification, with replicate handling and detailed notes for interpretation.
  - Facilitates quality control and reproducibility by documenting measurement basis, detection limits, and sample-specific notes.