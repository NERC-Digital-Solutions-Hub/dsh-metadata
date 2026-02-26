# TREE_Northumbria_ICPMS_Frog_and_Frogspawn_DM_Concentration

## Overview
- A dataset containing ICP-MS-derived concentrations of numerous elements in frog tissue or frogspawn, measured as milligrams per kilogram of dry mass (mg/kg DM).
- Metadata and concentration data are organized for samples from the Northumbria area, with UK Centre for Ecology & Hydrology (CEH) sample identifiers.

## Data Structure and Fields
- Species and sample metadata:
  - Latin_Species_Name, Common_Species_Name
  - Site, Date_Sample_Collected
  - CEH_Sample_Codes, CEH_Sample_Description
  - Tissue (tissue sampled: frog or frogspawn)
  - Fresh_Mass_Dry_Mass_Ratio (as a quality/weight indicator)
- Concentration measurements (mg/kg DM) for a wide suite of elements:
  - I, Li, Be, B, Na, Mg, Al, P, S, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U (plus additional notes on < indicators)
- Data quality indicators:
  - Some entries include a less-than symbol (<) to denote concentrations below detection limits (e.g., <Be, <Al, <Ni, <Se, <Ag, <Ba, <U).

## Spatial and Temporal Context
- Site and Date_Sample_Collected enable spatial mapping and temporal analysis of contaminant concentrations across sampling locations and times.
- CSV-like structure implies joinable tabular data for integration with GIS point data (sites) and time-series analyses.

## Data Quality, Standards, and Preparation Needs
- Concentrations are reported per dry mass, requiring consistent mass basis handling when linking to GIS layers (e.g., site coordinates and tissue type).
- Several fields show units as mg/kg_DM and explanations; some metadata fields indicate "n/a" for applicability, signaling potential gaps or placeholders to address during data cleaning.
- Presence of "<" values for nondetects requires handling decisions in GIS analyses (e.g., censoring, substitution rules).

## GIS Applications and Visualizations
- Map-based visualization of multi-element concentrations across sampling sites to identify spatial patterns of contamination.
- Create choropleth/ Graduated symbol maps for selected elements (e.g., heavy metals) by site.
- Time-enabled maps to observe trends if Date_Sample_Collected is used with time-aware layers.
- Integrate with site geometry to enable spatial joins, buffering, or proximity analyses relative to pollution sources.

## Data Cleaning and Preparation Considerations
- Standardize field names and units across datasets if integrating with other data sources.
- Decide on treatment of nondetects (< values) in analyses and visualizations.
- Validate Site entries with corresponding spatial coordinates; ensure consistent dating formats.
- Consider converting wide format (one column per element) to long format if required by GIS workflows or statistical analyses.

## Limitations and Gaps
- Data availability and resolution may vary, with potential inconsistencies in metadata completeness.
- Some fields may be incomplete or marked as not applicable (n/a), requiring curation before GIS deployment.
- Large, multidimensional dataset may require careful data management to maintain performance in map rendering and analysis.