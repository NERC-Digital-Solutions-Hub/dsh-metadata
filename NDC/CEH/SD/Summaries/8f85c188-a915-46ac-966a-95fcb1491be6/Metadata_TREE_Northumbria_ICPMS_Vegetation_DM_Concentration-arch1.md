# TREE_Northumbria_ICPMS_Vegetation_DM_Concentration

## Overview
- Data dictionary for concentrations of multiple elements in vegetation samples (dry mass, DM) from Northumbria.
- Includes both biological metadata (species) and sampling metadata (site, date, sample identifiers) plus a comprehensive set of elemental concentrations.

## Key variables and structure
- Biological metadata
  - Latin_Species_Name
  - Common_Species_Name
- Sampling metadata
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Identifier (UKCEH sample identifier)
  - CEH_Sample_Description
- Data conventions and units
  - All concentration values are on a mg/kg dry mass basis (I_mg_kg_DM, Li_mg_kg_DM, Mg_mg_kg_DM, etc.)
  - Some columns use a “<” marker to indicate concentrations below the detection limit (e.g., <I, <Li, <Be, etc.)
  - Several elements have paired or enhanced notations (e.g., Se_mg_kg_DM with Se_mg_kg_DM_1 and Se_mg_kg_DM_2, Mo_mg_kg_DM with 1 and 2, Tl_mg_kg_DM_ with 1 and 2)
- Elemental concentrations included
  - I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U
  - Each element appears as a separate concentration column (e.g., Al_mg_kg_DM, Fe_mg_kg_DM)
- Data quality and annotation
  - Some fields include explanatory text clarifying units and interpretation (e.g., “dry mass” basis, “< marker” meaning below detection)
  - n/a placeholders indicate missing information in metadata fields

## Data quality and interpretation notes
- Detection limits: < markers denote concentrations below detection thresholds for specific elements.
- Dual or multiple entries for certain elements (e.g., Se, Mo, Tl) suggest censored or status-based reporting (1/2 or similar suffixes).
- Dry mass basis: all concentrations are standardized to mg/kg DM, enabling cross-sample comparisons.
- Metadata depth: UKCEH sampling identifiers and descriptions enable traceability and reproducibility.

## Potential analyses and use cases
- Correlation studies between species and elemental uptake across sites.
- Spatial patterns of elemental accumulation by site and by tree species.
- Comparative analyses of foliar/vegetation concentrations to environmental exposure data.
- Data integration with other UKCEH or environmental datasets for broader ecological or toxicological assessments.
- Model development to predict element concentrations based on species, site, and sampling date.

## Challenges and considerations for analysts
- Handling censored data due to detection limits (values with "<" and paired Se/Mo/Tl entries).
- Harmonizing multiple versions or representations of element columns (e.g., Se_mg_kg_DM_1 vs Se_mg_kg_DM_2).
- Dealing with potential gaps or incomplete metadata (n/a fields) and ensuring accurate interpretation of each column.
- Ensuring consistent unit usage and correctly applying the dry mass (DM) basis across analyses.

## Provenance and metadata context
- Sample identifiers and descriptions are provided by UKCEH (CEH_Sample_Identifier, CEH_Sample_Description), facilitating traceability and reproducibility of analyses.