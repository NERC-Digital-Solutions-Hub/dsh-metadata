# TREE_Northumbria_ICPMS_Bee_DM_Concentration

## Purpose and scope
- Metadata/schema for a dataset of ICP-MS concentrations in bee samples from Northumbria.
- Supports data governance, standardization, discoverability, and sharing across organisations with large datasets.

## Core identifiers and sample metadata
- Latin_Species_Name: Latin name of species (Units = n/a; Explanation provided).
- Common_Species_Name: Common name of species (Units = n/a; Explanation provided).
- Site: Sampling site (Units = n/a; Explanation provided).
- Date_Samples_Collected: Date the sample was collected (Units = n/a; Explanation provided).
- CEH_Sample_Codes: UKCEH sample codes (Units = n/a; Explanation provided).
- CEH_Sample_Description: UKCEH sample description (Units = n/a; Explanation provided).
- Sample_Details: Sample preparation details (Units = n/a; Explanation provided).
- UKCEH sample-related fields imply linkage to UKCEH catalogues and sample histories.

## Analytical measurements and units
- I_mg_kg_DM: Concentration of I in mg/kg dry mass.
- Li_mg_kg_DM: Concentration of Li in mg/kg dry mass.
- Be_mg_kg_DM and <Be_mg_kg_DM: Concentration of Be (with potential "less than" value indicator).
- Na_mg_kg_DM, Mg_mg_kg_DM, Al_mg_kg_DM, P_mg_kg_DM, K_mg_kg_DM, Ca_mg_kg_DM, Ti_mg_kg_DM, V_mg_kg_DM, Cr_mg_kg_DM, Mn_mg_kg_DM, Fe_mg_kg_DM, Co_mg_kg_DM, Ni_mg_kg_DM, Cu_mg_kg_DM, Zn_mg_kg_DM, As_mg_kg_DM, Se_mg_kg_DM and <Se_mg_kg_DM, Rb_mg_kg_DM, Sr_mg_kg_DM, Mo_mg_kg_DM, Ag_mg_kg_DM, Cd_mg_kg_DM, Cs_mg_kg_DM, Ba_mg_kg_DM, Tl_mg_kg_DM, and U_mg_kg_DM (each with Units = mg/kg; Explanation note specifies concentration in milligram per kilogram dry mass).
- U_mg_kg_DM: Uranium concentration (mg/kg DM).
- < markers (e.g., <Be_mg_kg_DM, <Se_mg_kg_DM, <U_mg_kg_DM): indicate a concentration given as a "less than" value (detection limit context).

## Data quality and metadata details
- Each concentration field includes an Explanation describing the concentration in mg/kg dry mass.
- All elements are measured as mg/kg dry mass (DM), with some fields representing non-detects or censored values (indicated by "<" fields).
- n/a placeholders indicate non-applicable categories for certain metadata fields.

## Data governance implications for data stewards
- Ensure consistent naming and unit conventions across datasets (mg/kg DM).
- Maintain linkage between sample identifiers (CEH UKCEH codes, sample descriptions) and concentration data.
- Properly handle and document non-detects or censored values using the designated "<" fields.
- Document sample preparation details and site/date information to support reproducibility.
- Prepare data for ingestion into portals and catalogs with clear metadata for discoverability.

## Practical considerations and challenges
- Potential for incomplete metadata (e.g., species details or sample context) requiring careful curation.
- Handling of diverse elements across many samples and potential semi-structured descriptions.
- Ensuring compatibility with data-sharing standards and embargo conditions, if applicable.