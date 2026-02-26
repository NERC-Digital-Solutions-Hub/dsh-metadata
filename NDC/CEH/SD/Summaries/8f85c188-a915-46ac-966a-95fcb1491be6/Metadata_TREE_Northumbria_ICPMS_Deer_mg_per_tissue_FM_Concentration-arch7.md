# TREE_Northumbria_ICPMS_Deer_mg_per_tissue_FM_Concentration

## Overview
- A dataset detailing concentrations of multiple elements in deer tissue, measured as milligrams per total deer tissue fresh mass (mg per tissue_FM).
- Associated with UK Centre for Ecology & Hydrology (UKCEH) sampling codes and descriptions.
- Includes basic metadata per sample: species names, sampling site, date collected, and tissue sampled.
- Some entries indicate data limitations (e.g., "No data for Roe deer 4 thyroid") and detection-limit indicators.

## Data Structure
- Core metadata fields:
  - Latin_Species_Name
  - Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes
  - CEH_Sample_Description
  - Tissue
- Concentration fields (example fields shown among many):
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
  - Cs_mg_per_t tissue_FM
  - Ba_mg_per_tissue_FM
  - Tl_mg_per_tissue_FM
  - Pb_mg_per_tissue_FM
  - U_mg_per_tissue_FM
- Some columns indicate special markers:
  - "<Be" and similar tokens denote concentration values provided as a "less than" detection limit.
  - Notes such as "No data for Roe deer 4 thyroid" appear for several metals.
  - Some entries include multi-part coding (e.g., "1 = mg. 2 = ...") related to how values are stored or interpreted.

## Key Fields and Units
- Units: All listed concentrations are in mg per total deer tissue fresh mass (mg per_tissue_FM).
- Metadata fields help locate and identify samples:
  - Site and Date_Sample_Collected enable temporal and spatial analysis.
  - CEH_Sample_Codes and CEH_Sample_Description provide traceability to UKCEH records.
  - Tissue indicates the anatomical part sampled (e.g., thyroid, blood-related tissues implied by context).
- Species information:
  - Latin_Species_Name and Common_Species_Name for species-specific analyses.
- Data limits:
  - Detection-limit indicators ("<" markers) require careful handling in GIS analyses (e.g., censored data).
  - Gaps noted as "No data for Roe deer 4 thyroid" for multiple elements.

## Data Quality, Gaps, and Considerations for GIS
- Missing data: Notably "No data for Roe deer 4 thyroid" for several elements, which can affect spatial or species-specific summarizations.
- Data provenance: Tied to UKCEH sampling, with explicit sample codes and descriptions aiding data lineage.
- Inconsistent reporting cues: Presence of "<" values and mixed encoding across elements; requires consistent treatment when joining with GIS layers or performing statistical mapping.
- Resolution and standardization needs:
  - Harmonize species naming and tissue identifiers.
  - Standardize handling of censored data (values below detection limit).
  - Align sample sites with a geospatial layer to enable mapping.

## GIS and Mapping Considerations
- How to map:
  - Use Site as a join key to a spatial layer of sampling locations (points or polygons).
  - Create choropleth maps or graduated symbol maps of individual element concentrations (per sample or aggregated by site/species).
  - Build multi-layer dashboards showing spatial distribution across elements of interest.
- Data integration:
  - Combine with environmental layers (habitat type, pollution sources) or wildlife management zones.
  - Link to species-specific GIS attributes using Latin_Species_Name and Common_Species_Name.
- Handling data limitations:
  - Represent detections below limit as censored data (e.g., with special symbology or separate fields).
  - Exclude or separately tag samples with missing data for Roe deer 4 thyroid where necessary.

## Data Preparation and Best Practices
- Clean and standardize:
  - Normalize species names and tissue identifiers.
  - Tag and document all "<" values and their corresponding detection limits.
- Documentation:
  - Capture provenance in metadata (sampling date, site codes, sample descriptions).
  - Record any known data gaps (e.g., Roe deer 4 thyroid data absence) in data quality notes.
- Analysis-ready steps:
  - Create a master table with consistent units and ambient data quality flags.
  - Generate derived fields if needed (e.g., log-transformed concentrations for visualization).

## Usage Scenarios for GIS Specialists
- Spatial distribution of trace element concentrations in deer tissue across sampling sites.
- Comparative maps by species (Latin/Common names) and tissue types.
- Temporal analysis if dates are extended across multiple campaigns or seasons.
- Integration into policy or public-facing dashboards illustrating environmental exposure markers in wildlife.