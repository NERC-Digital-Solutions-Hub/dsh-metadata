# TREE_Northumbria_ICPMS_Earthworm_FM_Concentration_Ratio

## Overview
- A dataset of concentration ratios comparing Fresh Mass Earthworm (whole body) to Dry Mass Soil, derived from ICP-MS measurements.
- Covers Northumbria sampling with species metadata, site information, sampling date, and associated soil sample used for ratio calculation.
- Contains concentration ratios for a wide range of elements (I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U).
- Units are largely listed as n/a; ratios are the primary data values.

## Key Fields (Data Model)
- Latin_Species_Name, Common_Species_Name: taxonomic names of earthworm species.
- Site: sampling location identifier.
- Date_Sample_Collected: date of sampling.
- CEH_Sample_Codes, CEH_Sample_Description: internal sample codes and description.
- Co_Located_Soil_Sample_Used_To _Calculate_Concentration_Ratio: description of the soil sample used for the ratio calculation.
- Notes: any supplementary sample-related notes.
- I_Concentration_Ratio, Li_Concentration_Ratio, Be_Concentration_Ratio, Na_Concentration_Ratio, Mg_Concentration_Ratio, Al_Concentration_Ratio, P_Concentration_Ratio, K_Concentration_Ratio, Ca_Concentration_Ratio, Ti_Concentration_Ratio, V_Concentration_Ratio, Cr_Concentration_Ratio, Fe_Concentration_Ratio, Co_Concentration_Ratio, Ni_Concentration_Ratio, Cu_Concentration_Ratio, Zn_Concentration_Ratio, As_Concentration_Ratio, Se_Concentration_Ratio, Rb_Concentration_Ratio, Sr_Concentration_Ratio, Mo_Concentration_Ratio, Ag_Concentration_Ratio, Cd_Concentration_Ratio, Cs_Concentration_Ratio, Ba_Concentration_Ratio, Tl_Concentration_Ratio_, Pb_Concentration_Ratio, U_Concentration_Ratio: computed concentration ratios for each element.
- Note on units: listed as n/a for most fields.
- U_Concentration_Ratio specifics: includes a mapping where 1 = n/a and 2 = U Concentration Ratio (Fresh Mass Earthworm divided by Dry Mass Soil).

## Spatial and Temporal Context
- Data tied to specific sampling sites and collection dates, enabling spatial visualization of earthworm element accumulation over time.
- Co-located soil samples provide the basis for calculating the concentration ratios, linking soil context to earthworm measurements.

## Data Quality and Standards
- The dataset contains inconsistencies and typos in field names and descriptions (e.g., Tl_Concentration_Ratio_ vs Tl_Concentration_Ratio, and repeated MnConcentration references within Fe/Co lines).
- Some fields’ naming and labeling (e.g., Fe_Concentration_Ratio line) appear to have copy-paste errors.
- Units are largely unspecified (n/a), which may require clarification for downstream GIS use.
- Data may originate from multiple sources or formats, necessitating standardization before GIS integration.

## GIS Use: Visualization and Analysis
- Core use: map concentration ratios across sampling sites to show spatial patterns of earthworm metal accumulation.
- Potential visualizations:
  - Thematic maps (choropleth/point) by site for selected elements.
  - Faceted maps or small multiples to compare multiple elements simultaneously.
  - Time-series maps if multiple dates exist.
- Key GIS actions:
  - Join to a spatial base (sites shapefile or geocoded points) using Site or a related key.
  - Validate and harmonize field names (address typos/inconsistencies).
  - Handle missing values and resolve unit ambiguities.
  - Link to CO-located soil sample coordinates to enrich context (soil properties, proximity, etc.).

## Data Preparation Tips for GIS Specialists
- Clean and standardize field names (resolve Tl_Concentration_Ratio_ vs Tl_Concentration_Ratio, unify MnConcentration references).
- Confirm and document the calculation method for each concentration ratio (I, Li, Be, etc.) and ensure consistent application across records.
- Clarify units where applicable; convert to explicit units if needed for analysis.
- Validate Site identifiers against the spatial base to ensure accurate geolocation.
- Flag and document any records with ambiguous or missing Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio or Date_Sample_Collected values.
- Create metadata that notes data origins, QA steps, and any corrections undertaken.

## Challenges and Considerations for GIS Specialists
- Data availability and resolution: ensure sampling sites have precise geolocations and consistent date formats.
- Data standardization: address inconsistent naming and potential duplication across elements.
- Managing large/complex datasets: structure concentration ratios in a scalable schema for efficient queries and visualization.
- Data provenance: maintain clear links between earthworm samples and their co-located soil samples for reproducibility.

## End Note
- The document defines a comprehensive, multi-element concentration-ratio dataset for Northumbria earthworm samples, suitable for spatial analysis and map-based presentation once data quality issues are resolved and fields are standardized.