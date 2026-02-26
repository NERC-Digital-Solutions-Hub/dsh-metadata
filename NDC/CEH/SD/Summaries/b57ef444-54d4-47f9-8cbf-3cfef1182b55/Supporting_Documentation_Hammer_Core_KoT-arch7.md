# Supporting documentation for data resource Hammer_Cores_KoT.csv

## Overview
- Project: Carbon Storage in Intertidal Environments (C-SIDE)
- Funding: NERC (NE/R010846/1)
- Staff Responsible: Craig Smeaton
- Research Team: Craig Smeaton (St Andrews), Luis Rees-Hughes (Leeds), Natasha L.M. Barlow (Leeds), William E.N. Austin (St Andrews/SAMSI)
- Data resource name: Sedimentological and organic carbon data from the Kyle of Tongue Saltmarsh (Hammer cores)
- Purpose: Provides bulk density, water content, porosity, and organic carbon data for saltmarsh cores to support blue carbon stock and burial estimations; linked to best-practice methodologies

## Data resource details
- Description: 39 soil samples across 4 hammer cores collected from the Kyle of Tongue saltmarsh
- Variables observed:
  - Water Content (%)
  - Wet Bulk Density (g cm^-3)
  - Dry Bulk Density (g cm^-3)
  - Porosity (Φ)
  - Organic Carbon content (% weight)
  - Troels-Smith soil descriptions (simplified)
- Location and boundaries:
  - Site: Kyle of Tongue, Scotland
  - Geographic boundaries provided in decimal degrees (WGS84)
  - Also provided as British National Grid (OSGB 1936) with easting/northing
- Sampling plan:
  - No repeat sampling planned

## Sampling and laboratory procedures
- Core collection:
  - PVC core tubes: 150 cm length, 6.16 cm inner diameter, 0.24 cm wall
  - Inserted to 100 cm depth, sealed, and extracted with a tractor jack
  - Cores split lengthways into working/archive sections
- Field measurements:
  - GPS locations recorded with DGPS
  - Troels-Smith soil descriptions used (simplified to dominant class)
- Physical property measurements:
  - Fixed-volume samples (4 cm^3) collected at 10 cm intervals
  - Wet bulk density derived from mass, samples dried at 60°C for 72 hours to obtain dry bulk density
  - Water content and porosity calculated from wet/dry masses
  - Calculations follow Athy (1930) and Dadey et al. (1992)
- Elemental analysis for organic carbon:
  - 10 mg milled samples in silver capsules
  - Acidified with 10% HCl to remove carbonate
  - Dried and sealed; OC content measured with Elemental Analyzer (Carlo Erba/Vario EL Cube)
  - Three replicates per sample; calibration with Acetanilide; accuracy monitored with standard (B2178)
- Quality control:
  - Independent two-person classification of soil descriptions; consensus used
- Data source linkage:
  - Related publication: Smeaton et al. (2020) Geoderma

## Data structure and formats
- Data resource description for Hammer_Core_KoT.csv (field types and formats)
  - Core (Text)
  - Collection_date (Number; date)
  - Lat_dec_deg (Number; decimal degrees, WGS84)
  - Long_dec_deg (Number; decimal degrees, WGS84)
  - Grid_Reference (Text; OSGB36)
  - X_easting (Number)
  - Y_northing (Number)
  - Depth_cm (Number)
  - Mid_Point_Depth_cm (Number)
  - Sampling_Method (Text; Hammer Core)
  - Simplified_Troels_Smith (Text)
  - Water_Content_perc (Number)
  - Wet_Bulk_Density_g_cm_3 (Number)
  - Dry_Bulk_Density_g_cm_3 (Number)
  - Porosity (Number)
  - OC_perc_Rep1 (Number)
  - OC_perc_Rep2 (Number)
  - OC_perc_Rep3 (Number)
  - Mean_OC_perc (Number)
  - Std_Dev (Number)
- File format: .csv
- Relationship: Data linked to Smeaton, Barlow, & Austin (2020) Geoderma (cited)

## Spatial information and GIS relevance
- Observations include precise geolocation data (lat/long, OS grid, easting/northing)
- Suitable for GIS mapping of core locations, sample depths, and spatial distribution of measured properties
- Data can be joined with other spatial layers (e.g., saltmarsh extent, carbon storage estimates) for integrated analyses

## Data quality, provenance, and references
- QA approach: independent verification of soil descriptions; replication in OC analysis
- Provenance: thorough methodological description of core collection, lab analyses, and calibration procedures
- References include foundational work on density, porosity, organic carbon analysis, and Troels-Smith soil classification; linked publication provides methodological context for blue carbon estimations

## Use and considerations for GIS specialists
- Practical use:
  - Visualize spatial distribution of water content, bulk density, porosity, and organic carbon within Kyle of Tongue saltmarsh
  - Integrate OC measurements with depth to estimate carbon stocks and burial rates
  - Link to core-level metadata (collection date, depth, sampling method) for temporal and vertical analyses
- Considerations:
  - Single timepoint sampling with no repeats; temporal variability not captured
  - Data format is CSV; ensure coordinate reference system (WGS84 or OSGB36) is consistently applied in GIS
  - Troels-Smith classifications are simplified; for advanced habitat characterization, may require reconciling with other soil descriptions

## End notes
- The dataset is a carefully documented, quality-controlled resource intended to support carbon stock estimation and blue carbon research in tidal saltmarsh environments, with clear guidance on methods, coordinates, and data structure to facilitate GIS-based analyses.