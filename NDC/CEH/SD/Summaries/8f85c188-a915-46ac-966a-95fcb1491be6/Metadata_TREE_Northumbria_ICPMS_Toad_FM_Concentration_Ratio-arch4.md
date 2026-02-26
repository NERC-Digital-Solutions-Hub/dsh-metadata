# TREE_Northumbria_ICPMS_Toad_FM_Concentration_Ratio

- Overview
  - Metadata schema for a dataset of ICP-MS concentration ratios in toad tissue relative to soil.
  - Includes species identity, sampling site, collection date, sample identifiers, preparation notes, and a suite of element concentration ratios.

- Key Fields and Purpose
  - Latin_Species_Name, Common_Species_Name: species identification.
  - Site: sampling location.
  - Date_Sample_Collected: date of collection.
  - CEH_Sample_Code, CEH_Sample_Description: laboratory sample identifiers and descriptions.
  - Notes: preparation notes for toads.
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio: description of the soil sample used to compute the ratio.
  - I_Concentration_Ratio, Li_Concentration_Ratio, Be_Concentration_Ratio, Na_Concentration_Ratio, Mg_Concentration_Ratio, Al_Concentration_Ratio, P_Concentration_Ratio, K_Concentration_Ratio, Ca_Concentration_Ratio, Ti_Concentration_Ratio, V_Concentration_Ratio, Cr_Concentration_Ratio, Mn_Concentration_Ratio, Fe_Concentration_Ratio, Co_Concentration_Ratio, Ni_Concentration_Ratio, Cu_Concentration_Ratio, Zn_Concentration_Ratio, As_Concentration_Ratio, Se_Concentration_Ratio, Rb_Concentration_Ratio, Sr_Concentration_Ratio, Mo_Concentration_Ratio, Ag_Concentration_Ratio, Cd_Concentration_Ratio, Cs_Concentration_Ratio, Ba_Concentration_Ratio, Tl_Concentration_Ratio, Pb_Concentration_Ratio, U_Concentration_Ratio: for each element, the Concentration Ratio defined as Fresh Mass Toad (whole body) divided By Dry Mass Soil.
  - Units: indicated as n/a (ratios).
  - Explanation: clarifies that each concentration ratio is the ratio described above.

- Semantics, Provenance, and Context
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio ties the toad ratio to a specific soil sample.
  - Explanations accompany each field to aid interpretation and reproducibility.

- Data Quality and Governance Considerations
  - Structure supports data discoverability and traceability through explicit codes and descriptions (CEH codes, sample descriptions).
  - Potential inconsistencies in field naming (typos/spacing) suggest need for normalization to improve data quality.
  - Ratios rely on correct matching of fresh toad mass and dry soil mass, underscoring importance of consistent preparation notes and metadata.

- Relevance to Data Leaders (Data Strategy Perspective)
  - Demonstrates a clear, structured data asset with metadata that aids discovery, provenance, and reuse.
  - Provides a comprehensive view of sampling and measurement context, supporting assessment of data gaps and data product readiness.
  - Highlights the importance of linking data assets to wider data ecosystems (soil context, lab codes) for collaborative data stewardship.

- Recommendations for Improvement (Data Leadership lens)
  - Standardize field names and ensure consistent metadata vocabulary to reduce ambiguity.
  - Add explicit data types, valid value ranges, and controlled vocabularies (e.g., species names, site identifiers).
  - Enhance metadata for units where applicable and ensure complete documentation of preparation steps.
  - Implement data quality checks and cross-linking to external data systems (e.g., soil sample records) to improve discoverability and reuse.