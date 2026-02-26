# TREE_Northumbria_ICPMS_Vegetation_FM_Concentration

## Overview
- Dataset of vegetation sample concentrations for numerous elements, measured as milligrams per kilogram fresh mass (mg/kg FM).
- Associated with specific sampling sites and plant species, including both Latin and common names.
- Includes sample identifiers, collection date, and descriptive metadata to support GIS-based visualization and analysis.

## Key fields and data model
- Biological identifiers and context
  - Latin_Species_Name: Latin name of species
  - Common_Species_Name: Common name of species
  - Site: Sampling site
  - Date_Sample_Collected: Date of sampling
  - CEH_Sample_Identifier: UKCEH sample identifier
  - CEH_Sample_Description: UKCEH sample description
  - CEH_Sample_Description (repeated in header with explanation)
  - Fresh_Mass_Dry_Mass_Ratio: Ratio of fresh mass to dry mass
  
- Data values (elemental concentrations in mg/kg FM)
  - I_mg_kg_FM, Li_mg_kg_FM, Be_mg_kg_FM, Na_mg_kg_FM, Mg_mg_kg_FM, Al_mg_kg_FM, P_mg_kg_FM, K_mg_kg_FM, Ca_mg_kg_FM, Ti_mg_kg_FM, V_mg_kg_FM, Cr_mg_kg_FM, Mn_mg_kg_FM, Fe_mg_kg_FM, Co_mg_kg_FM, Ni_mg_kg_FM, Cu_mg_kg_FM, Zn_mg_kg_FM, As_mg_kg_FM, Se_mg_kg_FM, Rb_mg_kg_FM, Sr_mg_kg_FM, Mo_mg_kg_FM, Ag_mg_kg_FM, Cd_mg_kg_FM, Cs_mg_kg_FM, Ba_mg_kg_FM, Tl_mg_kg_FM, Pb_mg_kg_FM, U_mg_kg_FM
  - Each column corresponds to a specific element’s concentration in mg/kg fresh mass (FM)
  - Some columns include “<” markers indicating a concentration value is reported as a “less than” value (e.g., <I, <Li, etc.)
  
- Data quality/metadata notes
  - Units: mg/kg FM for most elements
  - Some header entries indicate when information is not applicable (n/a) or provide explanations for each column

## Special values and data handling
- “<” markers in element columns denote reported concentrations are below a threshold and should be treated as left-censored values in analyses.
- Date, site, and species fields enable spatial aggregation, temporal trends, and species-specific pattern analysis in GIS workflows.

## How this supports GIS tasks
- Enables spatial mapping of elemental concentrations across sampling sites to show geographic patterns.
- Supports layer creation: point features (sites) with attribute tables carrying species metadata and multiple element concentrations.
- Facilitates longitudinal and comparative analyses by linking Date_Sample_Collected with concentrations and site metadata.
- Integrates with other GIS data (site boundaries, habitat types, species distributions) for enriched visualization.

## Data quality and integration considerations for GIS
- Data may have missing values or censored (<) values; plan for handling left-censored data in rasters or thematic maps.
- Variation in data availability by site or species; account for uneven sampling resolution.
- Ensure consistent alignment of site identifiers with GIS layers (e.g., sampling sites shapefile) for accurate mapping.
- Metadata provides context essential for interpretation (sample descriptions, species, and collection details).

## Potential use cases
- Visualizing spatial distribution of iodine, lithium, and other elements in vegetation across Northumbria.
- Comparing element concentrations across species or sites to identify spatial or taxonomic patterns.
- Informing environmental assessments, pollution source investigations, or ecological risk analyses using map-based data products.