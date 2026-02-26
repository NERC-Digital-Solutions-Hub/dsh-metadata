# Supporting documentation for the dataset Soil survey in England, Scotland and Wales carried out during 2013 and 2014, 2016, Toberman et al.

## Overview
- Metadata and methods for a soil survey conducted in England, Scotland and Wales during 2013–2014 as part of the NERC Macronutrient Cycles LTLS project.
- Data comprise soil core samples collected from 100 m by 100 m areas, with cores taken along a central line at regular intervals.
- The dataset supports map-based data products and GIS analyses of soil properties across landscapes.

## Spatial scope and coordinates
- Site identifiers and sampling locations include:
  - OS Grid reference
  - Easting and Northing
  - Latitude and Longitude
  - Site name and catchment area (surface water convergence point)
- Data structured to enable georeferenced mapping and spatial analysis of soil properties.

## Data structure and tables
The documentation defines multiple data tables, each with column definitions, explanations, units, and measurement notes:
- Locations_and_dates
- Bulk_density_data
- Charcoal_and_coal_data
- Radiocarbon_codes
- Site_vegetation_data
- Soil_chemistry_and_isotope_data
- Soil_classifications_England_and_Wales
- Soil_classifications_Scotland
- Soil_cores_and_depth
- Soil_texture_data

Each table includes fields for identifiers (e.g., Sample_ID), site metadata, and measured attributes.

## Key variables and units (highlights)
- Core sampling and depth
  - Depths sampled up to 40 cm; depth descriptors include shallow/deep; mean_thickness_cm in cm
  - Number of cores per site (no_of_cores)
- Bulk density (BD)
  - BD_T, BD_P, BD_F in g cm-3
  - Related measurements: measured dry weight, core volume
- Soil chemical properties (per table and field)
  - pH (glass electrode method with moist soil + water)
  - Total carbon and nitrogen content (C_tot_%? N_tot_%; by mass, %)
  - Phosphorus: P_tot_% (total), including inorganic (P_inorg_%) and organic (P_org_%)
  - Delta13C (‰), 14C_pMC (percent modern)
  - LOI (loss on ignition, % by mass)
  - Pooled analyses via Aqua regia / microwave digestion and ICP-OES
- Isotope and radiocarbon data
  - Radiocarbon_codes linked to SUERC/NERC Radiocarbon Facility entries
- Soil texture and structure
  - Clay, Silt by mass (%), with Beckman Coulter LS200 laser granulometer
  - High Organic Content (HOC) flag when texture not determined

## Sampling method and depths
- Sampling of soil cores from each site:
  - Removal of vegetation and loose litter
  - Cores driven to 40 cm depth (top 20 cm sampled at some sites)
  - Central line with regular points at 11 m (10 cores) or 16 m (6 cores)
  - Randomized core positions around line points
- Depth-specific data recorded in Soil_cores_and_depth and Soil_chemistry_and_isotope_data tables

## Abbreviations and habitat types
- Habitat types include:
  - AG: Acid grassland
  - Ar: Arable
  - C: Conifer plantation
  - CG: Calcareous grassland
  - H: Heathland
  - IG: Improved grassland
  - M: Montane
  - SP: Scots pine woodland – ancient semi-natural
  - W: Broadleaved woodland
  - HOC: High organic content (texture not analysed)

## Data provenance and contributors
- Project context: LTLS – Analysing and simulating long-term and large-scale interactions of carbon, nitrogen and phosphorus in UK land, freshwater, and atmosphere
- Related organizations and facilities:
  - National Soil Resources Institute (NSRI)
  - James Hutton Institute (Scotland classifications)
  - SUERC (Scottish Universities Environmental Research Centre) Radiocarbon Facility
  - NERC Radiocarbon Facility / East Kilbride (AMS)
  - NERC LTLS / Maconutrient Cycles program

## How GIS analysts can use this dataset
- Link and join across tables using Sample_ID, Site_code, and other identifiers to build site-level and depth-specific GIS layers.
- Create spatial layers for:
  - Bulk density, pH, C and N contents, phosphorus forms, LOI, and isotopic data by site and depth
  - Soil texture classes (clay, silt) with HOC indicators
  - Radiocarbon and delta13C / pMC data where relevant
- Integrate with existing regional basemaps using coordinates (OS Grid references, Easting/Northing, Latitude/Longitude) and convert to common CRS as needed.
- Generate maps of soil properties by habitat type, catchment, or vegetation data for policy, client, or public audiences.
- Use sampling metadata (depth, number of cores, mean core thickness) to design aggregation schemes and uncertainty estimates across landscapes.

## Data quality notes and caveats
- Some measurements indicated as not determined (ND) or not available (na) in parts of the tables.
- Depth sampling sometimes did not reach the full 40 cm.
- Texture determinations rely on specific instruments (Beckman Coulter LS200) and may have method-specific limitations.
- Methods described for pH, LOI, and elemental analyses include standard chemical digestion and instrumental analyses with documented detection limits.