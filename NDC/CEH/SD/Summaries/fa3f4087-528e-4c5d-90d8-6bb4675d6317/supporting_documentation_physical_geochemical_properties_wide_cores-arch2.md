# Physical_geochemical_properties_wide_cores_essex.csv

## Overview
- Project: Carbon Storage in Intertidal Environments (C-SIDE)
- Funding: NERC (NE/R010846/1)
- Dataset purpose: Physical and geochemical measurements of saltmarsh soils from wide-diameter gouge cores in Essex, UK (collected in 2019) to support understanding of carbon storage in intertidal environments.
- Spatial scope: Essex coastline, United Kingdom; eight sites representing natural, historic breach, and managed realignment saltmarsh origins.

## What is included
- Observations/parameters:
  - Location: latitude (decimal degrees, WGS84), longitude (decimal degrees, WGS84), plus X (Easting) and Y (Northing)
  - Elevation above ordnance datum (m)
  - Substrate: Troels-Smith classification
  - Dry bulk density (g cm-3)
  - Organic carbon content (OC, %)
- Data granularity:
  - 19 wide-diameter gouge cores across 8 sites
  - Cores described and sectioned into 1 cm increments (n = 1952 sub-samples)
- Sample handling and storage:
  - DGPS for site locations; samples frozen at -20°C until analysis

## Methods
- Core collection: 60 mm gouge cores; core descriptions recorded at collection
- Core processing: cores cut into 1 cm sections (n = 1952)
- Drying: samples dried at 60°C for 72 hours to determine bulk density
- Carbon analysis: milled samples; 50 mg aliquots analyzed with Elementar Soli TOC using a temperature-gradient method (DIN 19539)
- Calibration and QC:
  - TOC calibration with CaCO3 and silty soil TOC/ROC/TIC standards
  - Isotopic QC via repeat analysis of high OC sediment standard (reference C and N values)
  - Laboratory equipment calibrated per University of St Andrews practices
- Data format: CSV

## Site details and context
- Locations: eight sites around the Essex coastline
- Saltmarsh types represented: Natural, Historic Breach, Managed Realignment
- Rationale: sites chosen to reflect different origins of saltmarsh while maintaining similar environmental regions for comparability

## Data structure and content
- Core_ID: core identification (text)
- Saltmarsh: name (text)
- Marsh_type: Natural, Managed Realignment, Historic Breach (text)
- Lat_dec_deg: latitude (decimal degrees, WGS84) (number)
- Long_dec_deg: longitude (decimal degrees, WGS84) (number)
- X_easting: Easting coordinate (number)
- Y_northing: Northing coordinate (number)
- Elevation_above_OD__m: elevation above ordnance datum (m) (number)
- Sample_depth_cm: depth interval of sub-sample (cm) (number)
- Mid_Point_depth_cm: depth interval mid-point (cm) (number)
- Substrate: Troels-Smith classification (text)
- Dry_bulk_density_g_cm_3: dry bulk density (g cm-3) (number)
- OC_perc: organic carbon content (% wt.) (number)

## Data quality, provenance, and references
- Data quality and QA:
  - GPS-based location accuracy via DGPS
  - Consistent sample preparation and instrumental calibration
  - Calibration and QC steps tied to established standards and procedures
- References underpinning methods:
  - Dadey et al., 1992 (dry-bulk density methodology)
  - DIN 19539 (TOC/TIC/ROC differentiation)
  - Natali et al., 2020 (thermal stability of soil carbon pools)
  - Smeaton et al., 2021a (marine sedimentary carbon stocks)
  - Troels-Smith, 1955 (sediment classification)

## Accessibility and usage considerations for Analysts Monitoring the Environment
- Format: CSV data resource with described headers and units
- Metadata clarity: comprehensive header definitions and data description to support reuse
- Interoperability: geospatial coordinates in both decimal degrees (WGS84) and projected X/Y, enabling mapping and integration with GIS and other environmental datasets
- Reusability: dataset designed to enable comparison across saltmarsh types and origins; suitable for aggregation with additional environmental datasets to enhance monitoring value
- Practical applications:
  - Estimating carbon stocks in intertidal saltmarsh soils
  - Assessing differences in physical and geochemical properties by marsh type
  - Supporting intertidal ecosystem monitoring and policy evaluation through standardized data
- Data integration considerations:
  - Align with other datasets (e.g., additional saltmarsh cores, shallower/longer cores, or different geographic regions) to increase dataset value
  - Ensure accessibility of underlying data and metadata for transparency and reproducibility