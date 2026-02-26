# Introduction

- The document presents 1x1 km raster data sets of Average Accumulated Exceedance (AAE) for acidity and nutrient nitrogen critical loads due to acid and nitrogen deposition for 2018–2020.
- AAE summarises exceedances across habitats within each grid square by combining habitat-specific exceedances with habitat area, then normalising by total habitat area in the grid cell.

- Key concepts
  - Accumulated Exceedance (AE): exceedance (keq ha-1 year-1) × exceeded habitat area (ha) for each habitat.
  - AAE: AE summed over habitats in a grid cell, divided by total habitat area in that cell (keq ha-1 year-1).
  - For nutrient nitrogen, 1 keq ha-1 year-1 equals 14 kg N ha-1 year-1.
  - Acidity exceedance combines S and N deposition; nitrogen exceedance is calculated as total N deposition minus the critical load.

- Data products
  - acid_aae_2018-2020.tif: AAE for acidity (keq ha-1 year-1).
  - nutn_aae_2018-2020.tif: AAE for nutrient nitrogen (keq ha-1 year-1).
  - Both are 1x1 km grid rasters, British National Grid (EPSG:27700), single-band rasters.
  - Coverage differs between the two datasets due to habitat distributions.

- Habitats included
  - Acidity (acid_aae): acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, productive coniferous woodland, productive broadleaved woodland, unmanaged coniferous and broadleaved woodland.
  - Nutrient nitrogen (nutn_aae): acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, productive coniferous woodland, productive broadleaved woodland, unmanaged beech/oak/Scots pine woodlands, other unmanaged woodland, dune grassland, saltmarsh.

- Methods and calculations
  - Critical loads and exceedances are based on UK methods (Hall et al., 2015) and CLRTAP frameworks.
  - Acidity: two approaches depending on habitat type
    - Empirical approach for non-woodland habitats on mineral/organomineral soils.
    - Simple mass balance (SMB) for woodland habitats and peat soils.
  - Peat soils use a threshold based on buffering with organic acids; freshwater habitats use a catchment-based FAB model (not used for AAE calculation here).
  - Exceedances are assessed against CL values (CLmaxS, CLmaxN, CLminN) and partitioned into five regions on the acidity function diagram.
  - Inputs: CBED deposition data (deposition estimated from air concentrations and land use) and UK Land Cover Map 2019 (1 km rasters).

- Data interpretation and limitations
  - AAE values reflect potential long-term harm at steady-state; exceeding a critical load does not imply immediate damage.
  - Habitat maps and critical-load areas reflect data-available areas and may differ from other habitat maps; totals may diverge accordingly.
  - Time lags in chemical and biological recovery mean reduction in deposition below CRLs does not guarantee rapid ecosystem recovery.

- Data quality and provenance
  - QC aligned with UNECE CLRTAP methods; detailed methodological transparency available in Hall et al. (2015).
  - Data and CBED deposition methods are documented; critical loads and exceedances are summarised in annual Trends Reports and UK biodiversity indicators (not included in the two AAE rasters).

- Use and accessibility
  - The UK national critical-load data and maps are produced for long-term assessment (steady-state focus) and are intended to indicate potential risk rather than immediate ecological change.
  - Data sources and deposition data described as part of a broader UK data ecosystem; critical-load data and CBED deposition data are available from the Environmental Information Data Centre (EIDC).

- Data structure and format
  - Two single-band GeoTIFF rasters (acid_aae_2018-2020.tif and nutn_aae_2018-2020.tif) in EPSG:27700.
  - Each raster contains 1x1 km grid cells with AAE values in keq ha-1 year-1.

- Appendix and technical details
  - Appendix I provides the simple mass-balance equation used for acidity critical loads in woodland (Ca:Al ratio criterion).
  - Methodological references and data sources are listed (Hall et al. 2015; Rowe et al. 2023; Calver et al.; etc.).

- Notes for data leaders
  - Useful for assessing data system coverage, provenance, and the applicability of AAE data for strategy and planning.
  - Highlights need for data discovery across scattered sources, data standardisation (habitat classes and units), and considerations of data gaps (e.g., freshwater catchments excluded from AAE calculation).