# TREE_Northumbria_ICPMS_Bee_FM_Concentration

## Overview
- Dataset describing ICP-MS concentration measurements in bee samples from Northumbria.
- Records include species identification (Latin and common names), sampling site, collection date, UKCEH sample codes and descriptions, along with general sample details and notes.
- Concentrations reported as mg/kg fresh mass (FM) for a wide range of elements.

## Key Data Elements
- Taxonomy and identifiers:
  - Latin_Species_Name
  - Common_Species_Name
- Sampling and context:
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes
  - CEH_Sample_Description
  - Sample_Details
  - Notes
- Measurements (mg/kg_FM):
  - I_mg_kg_FM, Li_mg_kg_FM, Be_mg_kg_FM, Na_mg_kg_FM, Mg_mg_kg_FM, Al_mg_kg_FM, P_mg_kg_FM, K_mg_kg_FM, Ca_mg_kg_FM, Ti_mg_kg_FM, V_mg_kg_FM
  - Cr_mg_kg_FM, Mn_mg_kg_FM, Fe_mg_kg_FM, Co_mg_kg_FM, Ni_mg_kg_FM, Cu_mg_kg_FM, Zn_mg_kg_FM, As_mg_kg_FM, Se_mg_kg_FM, Rb_mg_kg_FM, Sr_mg_kg_FM
  - Mo_mg_kg_FM, Ag_mg_kg_FM, Cd_mg_kg_FM, Cs_mg_kg_FM, Ba_mg_kg_FM, Tl_mg_kg_FM, Pb_mg_kg_FM, U_mg_kg_FM
- Notes on data values:
  - Some concentrations are marked as less-than (<) values (e.g., <Be, <Se, <U) indicating non-detects or censored values.
  - Several field descriptions contain minor typographical inconsistencies (e.g., “A Concentration of l”); metadata should be standardized during curation.
- Data normalization:
  - Units consistently reflect mg/kg fresh mass for all elemental concentrations.
  - Explanations accompany many fields to define purpose and units.

## Metadata, Provenance, and Governance
- CEH_Sample_Codes and CEH_Sample_Description provide UKCEH-linked identifiers for traceability.
- Notes and Sample_Details supply contextual information to assist data reuse and interpretation.
- Metadata structure is oriented toward uploading to relevant data portals and catalogues; emphasis on documenting work and enabling updates while respecting sharing limitations.

## Data Quality and Handling Considerations
- Ensure consistency between Latin_Species_Name and Common_Species_Name across records.
- Validate date formats and site naming for cross-dataset interoperability.
- Address lower-bound values (<) by recording detection limits or censoring approach used.
- Review and standardize field descriptions to remove typographical inconsistencies (e.g., “A Concentration of l”).
- Verify UKCEH codes and sample descriptions align with laboratory records and data provenance.

## Sharing, Access, and Updates
- Designed for publication and discovery through appropriate portals; alignment with data governance and sharing limitations.
- Recommend establishing a clear data update workflow to incorporate new samples, re-analyses, or corrections.
- Maintain traceability from sample codes to measurements and notes to support reproducibility and reuse.

## Recommendations for Data Stewards
- Apply standard ontologies and controlled vocabularies for species names, site identifiers, and sample descriptions.
- Create a concise data dictionary capturing:
  - Field purpose, data type, allowed values, and units for each column.
  - Handling rules for < values and non-detects.
  - Provenance chain from sampling to final concentration fields.
- Implement data validation rules:
  - Consistency checks between taxonomic fields.
  - Date validation and plausible site-date relationships.
  - Range checks for element concentrations with documented detection limits.
- Document any data processing steps (e.g., calibration, data cleaning, unit conversions).
- Plan for periodic review and update of UKCEH codes and sample descriptions to maintain interoperability with external portals.