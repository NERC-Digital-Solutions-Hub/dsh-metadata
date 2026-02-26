# Soil survey of Moor House, 1965.

## Overview
- Historical soil survey dataset from Moor House, Cumbria, UK (1965) by Mike Hornung.
- Supporting thesis available; related documentation and database description referenced in Cuthbertson (1993).
- Data intended for GIS and map-based analysis, suitable for visualising soil profiles and properties across locations.

## Data structure and contents
- Data organized into three CSV files:
  - D2SOIL_P.csv — Site Locations
    - Key fields: PROF_NO (unique profile number), EASTING, NORTHING, LOCATION, REL_DATA, ALTITUDE (m), GEO_DATA, VEG_DATA.
  - D3SOIL_P.csv — Horizon analysis
    - Key fields: PROF_NO (links to D2SOIL_P), HORIZON, FDEPTH (cm), TDEPTH (cm), REM1, REM2, TYPE (ORGANIC or MINERAL).
  - D4SOIL_P.csv — Chemical analysis and soil mineralogy
    - Key fields: PROF_NO (links to D2SOIL_P), SMPL_NO (sample number; used with PROF_NO for unique samples), FDEPTH, TDEPTH, and a comprehensive suite of chemical/physical properties (pH, CaCO3, Fe2O3, textures, base saturations, cations/extractables, carbon/nitrogen, CEC, LOI, and more) with two-series variants (1 and 2) for some attributes.

## Relationships and data linkage
- D3SOIL_P and D4SOIL_P are linked to D2SOIL_P via PROF_NO.
- D4SOIL_P also uses SMPL_NO in combination with PROF_NO to form unique sample identifiers.
- Horizon data (D3SOIL_P) reference corresponding site-level data (D2SOIL_P); horizon depths define sample intervals for each profile.

## Provenance and references
- Original field data from 1965 Moor House soil survey; supporting PhD thesis available via Durham E-Theses repository.
- Database description and environmental data management context discussed in Cuthbertson (1993) J. Environ. Manage., 37(4), pages 291-300.

## GIS applicability and usage
- plot site locations using EASTING/NORTHING coordinates on a map.
- join D2, D3, and D4 datasets on PROF_NO to create integrated soil profiles for each site.
- Visualise horizon boundaries and depths (FDEPTH/TDEPTH) alongside site attributes.
- Map and analyse soil properties (pH, texture components US_SAND/I_SAND/US_SILT/ I_SILT/ CLAY, CEC, LOI, nutrient/element concentrations, and other chemical metrics) by location and horizon.
- Potential outputs: horizon-based maps, profile charts, and summary statistics per site or region.

## Data quality, preparation and considerations
- Data originate from a mid-1960s survey; check for historical formatting and potential resolution differences.
- Data exist in multiple files; plan for data cleaning, standardisation, and consistent coordinate systems.
- Some attributes have paired 1/2 variants (e.g., CLAY, US_SILT, etc.); decide how to consolidate or separately analyze series.
- Ensure proper handling of depth intervals (FDEPTH–TDEPTH) when aggregating across horizons.

## Suggested workflow for GIS analysts
- Import D2SOIL_P, D3SOIL_P, and D4SOIL_P CSVs into a GIS or data analysis environment.
- Validate PROF_NO keys across files; merge datasets to create a comprehensive soil profile per site.
- Create map layers:
  - Site locations with location metadata (LOCATION, ALTITUDE, REL_DATA, VEG_DATA, GEO_DATA).
  - Horizon boundaries per profile using FDEPTH/TDEPTH and HORIZON codes.
  - Thematic layers for selected chemical/physical properties (e.g., pH, texture components, CEC, LOI).
- Generate visualisations:
  - Horizon depth profiles for individual sites.
  - Regional maps of selected soil properties.
  - Summary charts comparing sites or horizons.
- Reference provenance when presenting results (thesis and Cuthbertson 1993 references).

## Access and references
- Primary data files: D2SOIL_P.csv, D3SOIL_P.csv, D4SOIL_P.csv.
- Supporting materials: Mike Hornung’s PhD thesis (available via the provided URL) and Cuthbertson (1993) database description.