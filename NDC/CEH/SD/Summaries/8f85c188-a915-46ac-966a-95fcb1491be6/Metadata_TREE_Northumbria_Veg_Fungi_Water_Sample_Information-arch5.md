# TREE_Northumbria_Veg_Fungi_Water_Sample_Information

- Purpose and scope
  - Data dictionary for sample information related to vegetation, fungi, and water samples, detailing field names, units, and explanations to support data quality and interoperability.

- Key metadata fields (name – Units – Explanation)
  - Latin_Species_Name – Units: n/a – Explanation: Latin name of species.
  - Common_Species_Name – Units: n/a – Explanation: Common name of species.
  - Site – Units: n/a – Explanation: Sampling site.
  - Date_Sample_Collected – Units: n/a – Explanation: Date sample collected.
  - Sampling_Location_Or_National_Grid_Reference – Units: n/a – Explanation: Sampling location or national grid reference (NGR).
  - CEH_Sample_Code – Units: n/a – Explanation: CEH sample code associated with sample.
  - CEH_Sample_Description – Units: n/a – Explanation: CEH sample description.
  - Sample_Fresh_Mass_kg – Units: kg – Explanation: Fresh mass of sample in kilograms.
  - Sample_Dried_Mass_kg – Units: kg – Explanation: Dry mass of sample in kilograms; Not applicable for water samples.
  - General_Notes – Units: n/a – Explanation: General notes.
  - Sample_Preparation_And_Analysis_Performed – Units: n/a – Explanation: Sample preparation of sample and analysis performed.

- Data quality and governance considerations for Data Stewards
  - Ensure fields contain accurate and consistent taxonomy, metadata, and units.
  - Validate alignment between Latin_Species_Name and Common_Species_Name.
  - Enforce standardized location references (NGR) and format of sampling locations.
  - Track any notes about sample state (e.g., mass measurements) and applicability (e.g., dried mass not applicable for water samples).

- Data lifecycle and sharing
  - Data are received (with follow-ups as needed), quality assured, cleaned, and transformed for sharing.
  - Datasets are uploaded to relevant portals and catalogued for discoverability.
  - Work done on datasets may be documented for governance and provenance.

- Practical notes and edge cases
  - Not applicable: Sample_Dried_Mass_kg is not applicable for water samples.
  - NGR (National Grid Reference) should be used consistently for geographic localization.
  - CEH_Sample_Code and CEH_Sample_Description provide sponsor/collection context that aids traceability. 

- Challenges to address (from arc perspective)
  - Incomplete understanding of user needs and priorities for metadata.
  - Timely receipt of data from data creators.
  - Getting data creators to meet metadata standards (including metadata completeness).
  - Handling multiple systems/formats and large datasets with potential interoperability issues.
  - Dealing with outdated databases requiring bespoke solutions.