# TREE_Northumbria_ICPMS_Earthworm_FM_Concentration

## What this dataset is
- A dataset of element concentrations in earthworms measured by ICP-MS, based on fresh mass (FM).
- Records include species information, sampling site, collection date, and UKCEH sample codes/descriptions.

## Content and structure
- Covers organism identifiers:
  - Latin_Species_Name
  - Common_Species_Name
- Sampling context:
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes
  - CEH_Sample_Description
  - Notes
- Core measurements (all in mg/kg FM):
  - I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U
- Each metal has a corresponding explanation field, though some explanations appear garbled in places.

## Measurements and units
- All metal concentrations are reported as mg/kg fresh mass (FM).
- Variables include a broad suite of trace to major elements, enabling multi-element analyses.

## Potential uses for analysis
- Detect correlations between metal burdens and site, species, or sampling time.
- Compare concentrations across metals to identify pollution signals or bioaccumulation patterns.
- Build predictive or explanatory models of metal accumulation in earthworms for environmental monitoring.
- Support biomonitoring and ecological risk assessments using earthworms as bioindicators.

## Data quality and caveats
- Metadata explanations are inconsistently labeled in places (e.g., repeated references to “Concentration of Fe” across different metals), indicating potential documentation errors.
- Some fields (e.g., Tl, Pb, U) exhibit formatting irregularities that may require data cleaning.
- Cross-dataset harmonization may be needed for scale, boundaries, or standardization of site identifiers.

## Access, provenance, and integration
- Linked to Northumbria and UKCEH sample coding (CEH_Sample_Codes, CEH_Sample_Description).
- Suitable for integration with other environmental datasets, provided careful metadata validation and standardization are performed.
- advisable to verify data quality, ranges, and missing values before rigorous statistical analysis.