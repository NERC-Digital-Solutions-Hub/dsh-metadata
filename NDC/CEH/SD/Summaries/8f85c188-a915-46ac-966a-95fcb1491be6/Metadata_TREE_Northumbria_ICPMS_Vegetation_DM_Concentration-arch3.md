# TREE_Northumbria_ICPMS_Vegetation_DM_Concentration

- Purpose and scope
  - A dataset describing ICP-MS measured concentrations of multiple elements in vegetation from Northumbria, UK, expressed on a dry mass basis (mg/kg DM).
  - Enables environmental health monitoring, policy scrutiny, and informing future decisions by providing site- and species-specific contaminant data.

- Key identification fields
  - Latin_Species_Name and Common_Species_Name: scientific and common names of sampled vegetation.
  - Site: sampling location.
  - Date_Sample_Collected: date of sampling.
  - CEH_Sample_Identifier and CEH_Sample_Description: UKCEH sample identifier and description for traceability.
  - Any accompanying metadata placeholder values (e.g., n/a) indicating missing or unavailable information in parts of the header.

- Concentration data (elements and units)
  - Concentrations for a broad suite of elements, reported as mg/kg on a dry mass (DM) basis. Elements include I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U.
  - For some elements, less-than values are indicated with a preceding "<" marker (e.g., <I_mg_kg_DM, <Li_mg_kg_DM), representing censored data at detection/quantification limits.
  - Certain elements have dual columns to separately capture censored values (e.g., Se_mg_kg_DM_1 and Se_mg_kg_DM_2; Mo_mg_kg_DM_1 and Mo_mg_kg_DM_2; Tl_mg_kg_DM_1 and Tl_mg_kg_DM_2; Pb_mg_kg_DM_1 and Pb_mg_kg_DM_2; U_mg_kg_DM_1 and U_mg_kg_DM_2). This reflects handling of detection limits or value ranges.

- Data structure and metadata notes
  - Units consistently mg/kg with dry mass basis, ensuring comparability across samples.
  - Some columns use placeholders or markers (e.g., n/a) to indicate missing information or not applicable descriptions in the header.
  - The presence of less-than markers and dual-value columns highlights the need for careful data governance, handling of censored data, and transparent reporting for monitoring frameworks.

- Relevance for monitoring frameworks
  - Provides a comprehensive, structured template for reporting vegetation contaminant concentrations, suitable for evaluating environmental policies and informing decisions.
  - Demonstrates practical data governance considerations: traceability through sample identifiers, explicit metadata, data quality notes, handling of non-detects, and consistent units.
  - Illustrates common challenges in data sharing and metadata completeness that authors of monitoring frameworks must anticipate and address (e.g., data availability, metadata quality, and transparency of underlying datasets).