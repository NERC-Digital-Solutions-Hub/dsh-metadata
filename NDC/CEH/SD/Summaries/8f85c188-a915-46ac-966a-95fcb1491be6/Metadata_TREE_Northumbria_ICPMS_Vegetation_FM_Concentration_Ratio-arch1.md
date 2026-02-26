# TREE_Northumbria_ICPMS_Vegetation_FM_Concentration_Ratio

## Purpose and scope
- Dataset of concentration ratios calculated as Fresh Mass Vegetation divided by Dry Mass Soil.
- Applies to vegetation samples collected from multiple sites with associated soil samples.
- Includes species information, sampling details, and related metadata to support analyses of element uptake by vegetation.

## Dataset structure and key fields
- Taxonomy and identification
  - Latin_Species_Name
  - Common_Species_Name
- Sampling and site information
  - Site
  - Date_Sample_Collected
- Sample identifiers and descriptions
  - CEH_Sample_Identifier
  - CEH_Sample_Description
  - Notes (preparation of vegetation)
- Co-located soil context
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio
- Concentration ratio data
  - I_Concentration_Ratio: I Concentration Ratio (Fresh Mass Vegetation divided By Dry Mass Soil)
  - For many elements, two related columns exist per element (suffixes ", 1" and ", 2"):
    - Element_Concentration_Ratio, 1
    - Element_Concentration_Ratio, 2
  - Elements covered include Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Mo, Ag, Cd, Cs, Tl, Pb, U, and others
  - Some entries use a less-than marker to indicate censored (<) concentration ratios (e.g., <I, <Li, etc.), which are noted in the corresponding <marker explanations
- Units and interpretation
  - Concentration ratio columns are n/a for units (dimensionless ratios)

## Data quality and handling notes
- Ratios are dimensionless, representing the transfer from soil to vegetation.
- Less-than markers indicate censored data requiring special handling in analyses.
- Metadata (CEH identifiers and sample descriptions) supports traceability and reproducibility.
- Data are organized to allow unification of vegetation and co-located soil samples for ratio calculation, with notes on vegetation preparation.

## Potential analyses and uses
- Investigate species- and site-specific uptake patterns by comparing concentration ratios across elements.
- Explore correlations between soil concentrations and vegetation uptake using the ratio data.
- Develop predictive models of element transfer from soil to vegetation; identify which species show higher accumulation for particular elements.
- Use metadata (sampling date, site, and sample descriptions) to assess temporal or spatial trends and data quality.

## Access, provenance, and metadata considerations
- Data tied to Northumbria sampling programs with CEH sample identifiers and descriptions to facilitate data discovery and provenance.
- Rich metadata supports reproducibility and integration with other datasets, including soil measurements and site characteristics.