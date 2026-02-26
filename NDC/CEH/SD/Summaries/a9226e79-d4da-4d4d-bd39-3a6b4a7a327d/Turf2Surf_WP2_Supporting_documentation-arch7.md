# Turf2Surf WP2 Supporting documentation for data

## Overview
- Turf2Surf WP2 focuses on coupled nutrient cycling in terrestrial and freshwater ecosystems, examining nitrogen and phosphorus impacts on carbon exchange between land and atmosphere.
- The Conwy catchment in North Wales (≈500 km2) is the study area, with a diverse habitat range and a network of stakeholders.
- Project team and authors include researchers from CEH, Bangor University, Exeter University, and Exeter. Key contributors: Sabine Reinsch (corresponding author), Helen Glanville, Simon Smart, Bridget Emmett, Lina Mercado, Harry Harmens, among others.
- Data coverage spans 2013–2016, with multiple datasets and a common aim to relate plant and soil nutrients to ecosystem processes within JULES (a land-surface model).

## Geospatial and catchment context
- Conwy catchment characteristics:
  - Drains ~380 km2 to the tidal limit plus 200 km2 to the estuary; strong climatic gradient (500–1064 mm rainfall).
  - Habitats include blanket bog, montane moorland, forests, grasslands, lakes, reservoirs, flood plains, and salt marshes.
  - Wide range of stakeholders (water utilities, agriculture, forestry, conservation groups, tourism, communities).
- Sampling locations cover 17 sites with diverse habitats (e.g., Nant-y-Brwyn, Llyn Serw, Capel Curig, Glasgwm, Bery’ls Wood, Ingleborough NNR, Red Kite Woods, Coed Dolgarrog NNR, Montane sites, Conwy arable and grassland sites).
- Table 1 (habitats and site details) provides unique site numbers, plots, locations, and dominant species where available.

## Datasets and data files
- Five data files comprise the dataset structure:
  - Turf2Surf_Plant_biomass_data.csv
  - Turf2Surf_Plant_structural_data.csv
  - Turf2Surf_Plant_physiological_data.csv
  - Turf2Surf_Soil_Carbon_data.csv
  - Turf2Surf_Soil_raw data.csv
- Common schema elements:
  - Column A: Site number (links to Table 1)
  - Column B–C: Habitat name and detailed habitat description
  - Column D: Site name
  - Column E: Ecosystem component (Plant, Soil, Roots)
  - Column F: Plant species for Plant components; NA for Soil/Root
  - Column G–H: Plot number (1–4) and Replicate number
  - Column I: Soil depth interval (for Soil and Roots)
- Data availability and completeness:
  - Some fields contain NA values where data are not available due to depth limits, replication constraints, or restricted sampling.
- Data provenance:
  - Data responsible and processing notes accompany each data section (e.g., NPP, photosynthesis, leaf traits, soil measures, TXRF).
  - Authors and coordinators for each data type are listed (e.g., Simon Smart for NPP; Lina Mercado for photosynthesis; Helen Glanville for soil chemistry and TXRF).

## Key measurements and methodologies (GIS-relevant aspects)
- Aboveground net primary production (NPP):
  - Measured annually (2013–2015) across dominant species at all sites; 4 plots per site; winter clipping with grazing protection where applicable.
  - Biomass estimates include herbaceous biomass in grassland/bog and tree/shrub biomass in woodland, scaled to per m2.
  - Aims to integrate parameters into JULES for ecosystem-process modeling.
- Plant photosynthesis measures:
  - Vcmax, Jmax, and Asat measured for dominant species using CIRAS-I and LICOR systems; CO2 curves and 25°C temperature corrections applied.
  - Data processed with specialized scripts to fit Farquhar-based models; temperature correction to 25°C.
- Leaf traits and community traits:
  - Measurements include leaf N and P (%), LDMC, SLA, LMA, canopy height, bryophyte cover.
  - LMA/x methods involve leaf scanning, drying, and image analysis; elemental analyses conducted for N and P.
- Soil and root measurements (3.x sections):
  - General soil measures: intact cores to 1 m; depth-resolved sampling; SWC, BD, LOI, LOI-C, pH, EC; total C and N by thermal oxidation (Vario Cube).
  - Phosphorus fractions: Olsen P, Root-P, Complex-P, Enzyme-P (various extraction and colorimetric methods).
  - Available carbon and nitrogen: 0.5 M K2SO4 extraction with subsequent analyses for DOC and TDN.
  - Soil available cations: Ca, Na, K via 0.5 M acetic acid extraction and flame photometry.
  - Root biomass: total and fine roots via soil cores, WinRhizo scanning, and oven-dried weights; in-growth root cores for dynamic root data.
  - Soil elements: TXRF (multielement analysis) on 17 sites; detailed laboratory protocol and internal standards used; limitations noted in related document.
- Dataset-specific notes:
  - All methods emphasize linking plant/soil nutrient data to ecosystem processes for integration into JULES.
  - Data processing and QA/QC often conducted by named personnel across CEH Bangor, CEH Lancaster, and Bangor University.

## Practical use for GIS specialists
- Spatially-enabled data products:
  - Site-level and plot-level metrics (NPP, biomass, leaf traits, soil chemistry) can be joined to GIS layers using Site number, Habitat, and Site name.
  - Depth-specific soil data and root data provide a vertical dimension that can be represented in 3D GIS analyses.
- Recommended mapping strategies:
  - Create thematic maps by habitat type, with per-site clusters showing NPP, biomass, and soil properties.
  - Visualize soil depth intervals as stacked layers or interpolated surfaces where appropriate.
  - Use TXRF and phosphorus fractions to map nutrient status across the catchment.
- Data integration considerations:
  - Maintain linkages between site-level metadata (Table 1) and the five CSVs through Site number, Plot, and Replicate.
  - Handle missing values (NA) explicitly in GIS workflows and note data limitations per site.
  - Document data lineage and processing steps for reproducibility when creating map-based products or dashboards.

## Dataset structure and data access
- The dataset comprises five CSV files with consistent site identifiers and habitat descriptors.
- Each row corresponds to a specific combination of site, habitat, component (plant/soil/root), and plot/replicate, with soil depth details where applicable.
- This structure supports robust GIS analyses and integration with other spatial datasets for Conwy catchment studies.

## Version and access notes
- Version dates: 01/06/2016; 25/08/2016; 04/11/2016.
- The work is part of Turf2Surf WP2 and designed to provide baseline data for broader ecological and biogeochemical analyses.
- Data accessibility is framed for use by other research projects, with detailed methodological references and supplementary files available as cited (e.g., Turf2Surf_WP2_NPP_Smart.rft and Turf2Surf_WP2_TXRF_Limitations_Glanville.rft).