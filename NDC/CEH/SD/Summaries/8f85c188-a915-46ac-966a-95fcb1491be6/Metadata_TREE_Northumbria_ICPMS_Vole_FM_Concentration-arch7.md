# TREE_Northumbria_ICPMS_Vole_FM_Fresh_Mass_Concentration

## Overview
- A dataset of ICP-MS measured concentrations of multiple elements in vole tissue (fresh mass basis) from Northumbria.
- Includes biological, sampling, and analytical metadata to support map-based data visualization and spatial analyses.
- Concentrations reported for numerous elements (e.g., I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U) with units mg/kg_fresh_mass.
- Some concentration fields use “<” to indicate values below a detectable threshold.
- Key sample descriptors: Latin and Common species names, sampling site, date collected, UKCEH sample codes, sample preparation details, tissue notes, and the ratio of fresh mass to ash mass.

## Key fields (structure and purpose)
- Biological identifiers:
  - Latin_Species_Name (Latin name of species)
  - Common_Species_Name (Common name of species)
  - Tissue (notes on vole preparation)
- Sampling metadata:
  - Site (sampling site)
  - Date_Sample_Collected (collection date)
  - CEH_Sample_Codes (UKCEH sample codes)
  - Sample_Details (sample preparation details)
  - CEH_Sample_Description (UKCEH sample description)
  - Fresh_Mass_Ash_Mass_Ratio (ratio of whole animal fresh mass to ash mass)
- Concentration measurements (mg/kg_fresh_mass) for:
  - I_mg_kg_FM, Li_mg_kg_FM, Be_mg_kg_FM (and <Be), Na_mg_kg_FM, Mg_mg_kg_FM, Al_mg_kg_FM, P_mg_kg_FM, K_mg_kg_FM, Ca_mg_kg_FM, Ti_mg_kg_FM, V_mg_kg_FM, Cr_mg_kg_FM, Mn_mg_kg_FM, Fe_mg_kg_FM, Co_mg_kg_FM, Ni_mg_kg_FM, Cu_mg_kg_FM, Zn_mg_kg_FM, As_mg_kg_FM, Se_mg_kg_FM, Rb_mg_kg_FM, Sr_mg_kg_FM, Mo_mg_kg_FM, Ag_mg_kg_FM (and <Ag), Cd_mg_kg_FM, Cs_mg_kg_FM, Ba_mg_kg_FM, Tl_mg_kg_FM, Pb_mg_kg_FM, U_mg_kg_FM (and <U)
- Notation:
  - < preceding a value indicates a “less than” concentration (threshold reporting)

## Data quality and structure considerations
- Units: Most concentration fields are in mg/kg_fresh_mass; some fields use a threshold indicator (<).
- Some fields are marked n/a or have notes explaining meaning (e.g., organismal and sampling details).
- Data may be distributed across multiple sources or records; requires integration for GIS use.
- Consistency of field names and definitions is essential for reliable joins and visualizations (e.g., matching Site codes to geolocations).

## GIS applications
- Spatial mapping of element concentrations across sampling sites to identify spatial patterns or hotspots.
- Time-enabled mapping by Date_Sample_Collected to observe temporal trends.
- Multivariate visualization (e.g., choropleth maps, graduated symbol maps) for individual elements or composite contamination indices.
- Data joins with geographic boundaries or shapefiles using Site (requires georeferencing of Site identifiers).
- Potential integration with habitat, land-use, or population data to explore ecological drivers.

## Practical considerations for analysis
- Data integration:
  - Georeference Site identifiers to obtain spatial coordinates for mapping.
  - Align Date_Sample_Collected formats for temporal analyses.
  - Ensure consistency of species-level fields if comparing across datasets.
- Data cleaning:
  - Handle “<” values as censored data; decide on imputation or plotting policies.
  - Resolve any n/a fields prior to visualization to avoid misleading interpretations.
- Data transformation:
  - Use Fresh_Mass_Ash_Mass_Ratio to contextualize concentrations if ash mass corrections are needed in advanced analyses.
- Quality control:
  - Verify UKCEH sample codes (CEH_Sample_Codes) against metadata records.
  - Cross-check tissue notes (Tissue) for comparability across samples.

## End-user considerations
- Clear legends and units are essential for map interpretability (mg/kg_fresh_mass).
- Documentation of thresholds and data limitations should accompany maps and dashboards.
- When communicating findings, distinguish between measured concentrations and censored (<) values.