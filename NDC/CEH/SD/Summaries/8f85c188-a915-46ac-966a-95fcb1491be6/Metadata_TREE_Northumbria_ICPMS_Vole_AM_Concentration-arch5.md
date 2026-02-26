# TREE_Northumbria_ICPMS_Vole_AM_Concentration

## Overview
- A data schema/dataset describing ICP-MS concentrations of multiple elements in vole ash mass (AM) samples.
- Includes taxonomic names, site, collection date, sample identifiers, preparation details, and notes on vole preparation.
- Concentrations are reported as milligrams per kilogram of ash mass (mg/kg AM). Some fields indicate non-detects with “less than” markers.

## Key Metadata and Variables
- Taxonomy and naming
  - Latin_Species_Name
  - Common_Species_Name
- Sampling context
  - Site (sampling location)
  - Date_Sample_Collected
- Sample identification and description
  - CEH_Sample_Codes (UKCEH sample codes)
  - Sample_Details (sample preparation details)
  - CEH_Sample_Description (UKCEH sample description)
  - Notes (notes on vole preparation; e.g., separate tissues were not prepared)
- Mass and ratio
  - Fresh_Mass_Ash_Mass_Ratio (ratio of whole organism fresh mass to ash mass)
- Elemental concentrations (in mg/kg AM)
  - I_mg_kg_AM
  - Li_mg_kg_AM
  - Be_mg_kg_AM (with < marker indicating a less-than value)
  - Na_mg_kg_AM
  - Mg_mg_kg_AM
  - Al_mg_kg_AM
  - P_mg_kg_AM
  - K_mg_kg_AM
  - Ti_mg_kg_AM
  - V_mg_kg_AM
  - Cr_mg_kg_AM
  - Mn_mg_kg_AM
  - Fe_mg_kg_AM
  - Co_mg_kg_AM
  - Ni_mg_kg_AM
  - Cu_mg_kg_AM
  - Zn_mg_kg_AM
  - As_mg_kg_AM
  - Se_mg_kg_AM
  - Rb_mg_kg_AM
  - Sr_mg_kg_AM
  - Mo_mg_kg_AM
  - Ag_mg_kg_AM (with separate subfields for value markers, e.g., Ag_mg_kg_AM,1 and Ag_mg_kg_AM,2)
  - Cd_mg_kg_AM
  - Cs_mg_kg_AM
  - Ba_mg_kg_AM
  - Tl_mg_kg_AM
  - Pb_mg_kg_AM
  - U_mg_kg_AM
- Data formatting notes
  - Some elements have paired fields (e.g., Ag_mg_kg_AM,1 and Ag_mg_kg_AM,2) to capture value and description.
  - “<” markers denote concentrations below detection limits.
  - Some lines show apparent labeling inconsistencies (e.g., Ti_mg_kg_AM associated with “Concentration of Ca” in the explanation), which may require data cleaning.

## Data Quality, Standards, and Governance Implications
- Metadata richness supports discoverability and reuse for data stewards and end users.
- Standards to enforce
  - Consistent units: mg/kg AM across all elemental concentrations.
  - Clear handling of non-detects: explicit < markers and associated fields.
  - Clear, accurate sample metadata: species names, site, date, sampling codes, and preparation notes.
- Data quality considerations for stewardship
  - Validate that field names and explanations align (resolve potential mislabeling like Ca vs Ti explanations).
  - Ensure consistent handling and documentation of non-detects and two-part concentration fields.
  - Confirm CEH_Sample_Codes mapping to UKCEH systems and ensure traceability from collection to data output.
- Sharing and governance
  - This dataset is prepared for upload to relevant portals and catalogues; ensure governance around data availability, updates, and disclosure limitations.
  - Document any embargoes, proprietary considerations, or data-use restrictions.

## Data Availability, Updates, and Reuse
- The dataset is structured to be uploaded to data portals and catalogued for discoverability.
- Possible embargoes or limitations should be identified and documented (as per governance practices).
- Updates should maintain compatibility with existing metadata fields and ensure backward compatibility for users reusing historical data.

## Practical Use and Value for Data Stewards
- Enables standardized discovery and reuse of vole contaminant data across organizations.
- Facilitates cross-study comparisons by providing a common framework: species, site, collection date, preparation details, and multi-element ash-mass concentrations.
- Supports quality assurance workflows by highlighting metadata requirements (e.g., preparation notes, detection limits, and data structure).

## Key Considerations and Potential Challenges
- Handling large multi-element datasets with a mix of detect/non-detect values and paired fields for certain elements.
- Ensuring interoperability across systems with potentially conflicting or mislabelled metadata (e.g., incorrect explanatory notes).
- Managing timeliness of data delivery from data creators/sharers to meet user needs.
- Aligning terminology and units when integrating with other datasets (e.g., other studies using fresh mass or different mass bases for concentration).