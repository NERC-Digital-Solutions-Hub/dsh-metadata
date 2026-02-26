# TREE_Northumbria_ICPMS_Vegetation_DM_Concentration

## Overview
- A dataset describing concentrations of multiple elements in vegetation samples, measured by ICP-MS, with concentrations reported on a dry mass basis.
- Key identifiers include species (Latin and common names), sampling site, date of sample collection, and UKCEH sample identifiers and descriptions.
- Designed to support assessment of data availability, provenance, and suitability for analyses across vegetation samples collected at Northumbria sites.

## Data structure and key fields
- Taxonomic and site identifiers:
  - Latin_Species_Name (and explanation)
  - Common_Species_Name
  - Site (sampling location)
- Sampling and provenance metadata:
  - Date_Sample_Collected
  - CEH_Sample_Identifier
  - CEH_Sample_Description
- Measurement fields (concentrations in mg/kg dry mass):
  - I_mg_kg_DM, Li_mg_kg_DM, Be_mg_kg_DM, Na_mg_kg_DM, Mg_mg_kg_DM, Al_mg_kg_DM, P_mg_kg_DM, K_mg_kg_DM (dry mass variant), Ca_mg_kg_DM, Ti_mg_kg_DM, V_mg_kg_DM
  - Cr_mg_kg_DM, Mn_mg_kg_DM, Fe_mg_kg_DM, Co_mg_kg_DM, Ni_mg_kg_DM, Cu_mg_kg_DM, Zn_mg_kg_DM
  - As_mg_kg_DM, Se_mg_kg_DM (with supporting indicators), Rb_mg_kg_DM, Sr_mg_kg_DM
  - Mo_mg_kg_DM, Ag_mg_kg_DM, Cd_mg_kg_DM, Cs_mg_kg_DM, Ba_mg_kg_DM, Tl_mg_kg_DM, Pb_mg_kg_DM, U_mg_kg_DM
- Special value handling indicators:
  - Markers such as "<I" or "<Li" indicate concentrations reported as below the detection/quantification limit for the corresponding column (e.g., <I implies I is reported as a "<" value in I_mg_kg_DM)
  - Similar "<" markers appear for other elements (e.g., <Be, <Cr, <As, <Se, etc.)
  - Several columns include notes about dual-value representations (e.g., Se_mg_kg_DM_1 and Se_mg_kg_DM_2) to capture below-limit scenarios

## Measurement details and units
- All concentration measurements are in mg/kg dry mass (DM).
- Some columns explicitly denote a “dry mass” variant for interpretation (e.g., K_mg_kg_DM, dry mass).
- Below-detection-limit values are represented with designated markers (<) in the respective concentration columns.

## Metadata, provenance, and documentation
- CEH_Sample_Identifier and CEH_Sample_Description provide UKCEH-related provenance.
- Date_Sample_Collected and Site capture spatial-temporal context of the samples.
- Latin_Species_Name and Common_Species_Name enable cross-referencing with taxonomic information.
- The dataset appears to be organized as a data dictionary or schema for vegetation ICP-MS concentration data, supporting data discovery and reuse.

## Data quality considerations and governance
- Handling of below-detection-limit values requires clear rules (represented by < markers or dual-value fields).
- Metadata richness (species names, site, date, sample identifiers) supports traceability and data integration across networks.
- Potential gaps may arise from inconsistent metadata around certain columns or the need to interpret dual-value fields for detection-limit cases.
- As a data asset, this dataset would benefit from clear metadata standards for detection-limit handling, units consistency, and explicit data quality indicators to support cross-site analyses and data sharing with partners.