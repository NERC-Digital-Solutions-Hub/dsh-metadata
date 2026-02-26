# TREE_Northumbria_ICPMS_Deer_mg_per_tissue_FM_Concentration

## Purpose and Scope
- Data dictionary for ICP-MS measured concentrations of multiple elements in deer tissue from Northumbria, expressed as milligrams per total deer tissue fresh mass.
- Captures per-sample metadata to enable traceability and context for analysis (species names, sampling site, collection date, UKCEH sample codes and descriptions, tissue sampled).
- Intended to support analyses of correlations, patterns, and potential ecological or environmental impacts based on elemental concentrations.

## Data Columns and Units
- Core metadata fields:
  - Latin_Species_Name, Common_Species_Name (species identifiers)
  - Site (sampling location)
  - Date_Sample_Collected (collection date)
  - CEH_Sample_Codes, CEH_Sample_Description (UKCEH identifiers and descriptions)
  - Tissue (type of tissue sampled)
- Concentration fields (all in mg per total deer tissue fresh mass, FM):
  - I_mg_per_tissue_FM
  - Li_mg_per_tissue_FM
  - Be_mg_per_tissue_FM
  - Na_mg_per_tissue_FM
  - Mg_mg_per_tissue_FM
  - Al_mg_per_tissue_FM
  - P_mg_per_tissue_FM
  - K_mg_per_tissue_FM
  - Ca_mg_per_tissue_FM
  - Ti_mg_per_tissue_FM
  - V_mg_per_tissue_FM
  - Cr_mg_per_tissue_FM
  - Mn_mg_per_tissue_FM
  - Fe_mg_per_tissue_FM
  - Co_mg_per_tissue_FM
  - Ni_mg_per_tissue_FM
  - Cu_mg_per_tissue_FM
  - Zn_mg_per_tissue_FM
  - As_mg_per_tissue_FM
  - Se_mg_per_tissue_FM
  - Rb_mg_per_tissue_FM
  - Sr_mg_per_tissue_FM
  - Mo_mg_per_tissue_FM
  - Ag_mg_per_tissue_FM
  - Cd_mg_per_tissue_FM
  - Cs_mg_per_tissue_FM
  - Ba_mg_per_tissue_FM
  - Tl_mg_per_tissue_FM
  - Pb_mg_per_tissue_FM
  - U_mg_per_tissue_FM
- Special notations observed in headers:
  - Some "<X" prefixes indicate concentrations reported as less-than values (censored data).
  - For certain entries, headers reference thyroid-specific measurements (e.g., "... thyroid"), indicating tissue-specific reporting in some rows (not uniformly present across all elements).

## Data Quality Flags, Gaps, and Notable Details
- Recurrent note: “No data for Roe deer 4 thyroid” for multiple elements, indicating missing thyroid tissue data for Roe deer 4 in those fields.
- Presence of censored values indicated by "<" markers in several element columns (e.g., <Be, <Al, <V, etc.), requiring special handling in analysis (e.g., left-censoring).
- Some columns show “Units = n/a” for non-concentration metadata fields, while concentration fields are in mg per tissue FM.
- Data provenance ties to UKCEH sample codes/descriptions, emphasizing the need to cross-reference with the CEH metadata for full context.

## Challenges and Considerations for Analysts
- Local-scale data availability may be limited by partial data gaps (e.g., missing Roe deer thyroid data).
- Handling censored (<) values appropriately to avoid bias in summaries and models.
- Ensuring consistent tissue type interpretation when comparing across samples (some entries mention thyroid-specific measurements).
- Managing potential variability in sample documentation across sites, dates, and descriptions (requires careful data cleaning and harmonization).

## Potential Analyses and Use Cases
- Correlation analyses between elemental concentrations and sampling sites or temporal trends.
- Comparative assessments across species or tissue types where data exist.
- Exploratory modeling to predict environmental exposure or contamination risk based on ICP-MS profiles.
- Data quality checks and traceability workflows leveraging CEH sample codes and metadata.

## Provenance and Metadata Notes
- Dataset appears to be a Northumbria/CEH ICP-MS concentration dataset, with sample-level identifiers and descriptive metadata to support reproducibility and data sharing.
- Emphasizes the need to consult accompanying metadata portals for complete definitions of sites, tissue types, and CEH sample descriptions to complement the concentration matrix.