# TREE_Northumbria_ICPMS_Toad_AM_Concentration

## Overview
- A dataset containing concentrations of multiple elements measured in ash mass per kilogram (mg/kg) for toad samples, using ICPMS (Inductively Coupled Plasma Mass Spectrometry).
- Focuses on UK Centre for Ecology & Hydrology (UKCEH) sample codes and descriptions, with accompanying metadata to support data discovery and reuse.

## Dataset contents and structure
- Biological and sampling metadata:
  - Latin_Species_Name
  - Common_Species_Name
  - Site
  - Date_Sample_Collected
- Sample identifiers and descriptions:
  - CEH_Sample_Code
  - CEH_Sample_Description
- Preparation and notes:
  - Fresh_Mass_Ash_Mass_Ratio
  - Notes
- Measured concentrations (all in mg/kg as ash mass, AM):
  - I_mg_kg_AM, Li_mg_kg_AM, Be_mg_kg_AM, Na_mg_kg_AM, Mg_mg_kg_AM, Al_mg_kg_AM, P_mg_kg_AM, K_mg_kg_AM, Ca_mg_kg_AM, Ti_mg_kg_AM, V_mg_kg_AM, Cr_mg_kg_AM, Mn_mg_kg_AM, Fe_mg_kg_AM, Co_mg_kg_AM, Ni_mg_kg_AM, Cu_mg_kg_AM, Zn_mg_kg_AM, As_mg_kg_AM, Se_mg_kg_AM, Rb_mg_kg_AM, Sr_mg_kg_AM, Mo_mg_kg_AM, Ag_mg_kg_AM, Cd_mg_kg_AM, Cs_mg_kg_AM, Ba_mg_kg_AM, Tl_mg_kg_AM, Pb_mg_kg_AM, U_mg_kg_AM.
- Column-level remarks (as provided in the data dictionary) describe that each element’s value is the concentration of that element in milligrams per kilogram of ash mass, with occasional formatting inconsistencies in the source text.

## Variables and units
- Primary concentration variables: Element concentrations in mg/kg_AM (e.g., I_mg_kg_AM, Li_mg_kg_AM, …, U_mg_kg_AM).
- Metadata fields: Latin_Species_Name, Common_Species_Name, Site, Date_Sample_Collected, CEH_Sample_Code, CEH_Sample_Description, Fresh_Mass_Ash_Mass_Ratio, Notes.
- All concentration fields are described as “Concentration of [Element] in milligram per kilogram ash mass” (mg/kg_AM).

## Sample provenance and metadata provenance
- CEH sample identifiers link observations to UKCEH sample codes and descriptions.
- Date and site fields enable temporal and spatial traceability.
- Fresh_Mass_Ash_Mass_Ratio provides context on sample preparation and mass balance.

## Data quality, governance, and sharing
- Data quality focus for Data Stewards:
  - Ensure accuracy and consistency of species and site names, sample codes, and descriptions.
  - Validate that concentration values are recorded in the correct mg/kg_AM units.
  - Maintain complete metadata for each field (units, explanations) to support re-use.
- Metadata and interoperability:
  - Preserve and standardize key metadata (species, site, date, sample code, preparation ratio) to enhance discoverability and interoperability across datasets.
- Availability and updates:
  - Track data availability, any embargoes, and update cycles; ensure mechanisms exist to publish updated measurements or corrected values.
  - Upload datasets to relevant portals and catalogue data holdings as part of ongoing publishing practices.
- Documentation:
  - Maintain clear documentation for data columns (meanings of abbreviations, handling of missing values like n/a) to support downstream users.

## Key challenges for data stewards
- Incomplete picture of user needs and priorities, affecting dataset curation and metadata depth.
- Timely receipt of data from collaborators or data creators.
- Ensuring data creators provide complete metadata and adhere to standards (aliases, formats, units).
- Heterogeneous data systems and formats across different datasets or departments.
- Handling large datasets with numerous element concentrations and associated metadata.
- Dealing with outdated or bespoke databases that are not interoperable with modern data platforms.

## Implications for stewardship actions
- Implement and enforce a standard metadata template for ICPMS datasets, including explicit units and element explanations.
- Establish data validation rules to confirm mg/kg_AM units and plausible concentration ranges for each sample.
- Create mapping and harmonization practices for species names, site identifiers, and CEH sample codes.
- Develop procedures for updating Fresh_Mass_Ash_Mass_Ratio and Notes as preparation methods evolve.
- Plan for regular data transfers and versioning to maintain a living, discoverable dataset repository.