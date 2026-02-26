# Soil organic carbon changes of agricultural land areas under different land use and climate scenarios till 2100, globally.

## Overview
- Global dataset tracking changes in soil organic carbon (SOC) on agricultural land under various land use and climate scenarios up to 2100.
- SOC changes are presented as differences from a baseline business-as-usual (BAU) scenario, which assumes continuous tillage, no residue incorporation, and no added organic amendments.
- Values are provided as annual averages for 10-year periods (e.g., 2020–2030, 2030–2040, ..., 2090–2100) in Mg C ha^-1 yr^-1.
- Outputs are grid-based (0.5-degree) and compiled per management scenario and climate scenario.

## What the dataset contains
- A set of files describing SOC changes for different management strategies (relative to BAU) under different climate scenarios.
  - Examples of management changes include: no tillage (notill), residue incorporation (residincorp), reduced tillage (redtill), cover crops (covercrop), use of cover crops with residue incorporation (covercrop_residincorp), and manure addition (manure). Each has climate variants A1B or A2.
- Table 2 describes the grid-cell level data included in each file (latitude, longitude, area_km2, LU_agr_nrs_grid_cell) and SOC change variables by decade (SOC_20_30_MgC_ha_yr, SOC_30_40_MgC_ha_yr, …, SOC_90_100_MgC_ha_yr).
- The SOC change in each cell is expressed as SOC_CH = SOC_BAU - SOC_SC, where SOC_SC is the SOC under a given management scenario and SOC_BAU is the BAU baseline. The dataset reports averaged SOC_CH over 10-year periods.
- The dataset provides a global view, with outputs mapped and quality-checked against existing literature.

## Modelling approach
- Uses ECOSSE model, version 6.2b, to simulate SOC (monthly) on a 0.5-degree grid with site-appropriate inputs.
- Inputs include crop yields (wheat), fertiliser inputs, sowing and harvesting dates, and soil management details (tillage and residue management).
- The model runs until 2100 for each grid cell; outputs are processed in R (R v4.3.0) to obtain annual SOC totals and 10-year averages.
- Results are validated through mapping, visual screening, and comparison of global, regional, and local statistics with other literature to ensure plausibility.

## Data inputs and sources
- Climate data: Climate Research Unit (CRU) data from the University of East Anglia (UEA).
  - Link: https://www.uea.ac.uk/web/groups-and-centres/climatic-research-unit/data
- Soil data: Harmonized World Soil Database (HWSD).
  - Link: https://www.fao.org/soils-portal/data-hub/soil-maps-and-databases/harmonized-world-soildatabase-v12/en/
- Land use data: Hilda global land use map (2019) for cropland.
  - Link: https://doi.pangaea.de/10.1594/PANGAEA.921846
- Fertiliser inputs: PANGAEA dataset.
  - Link: https://doi.pangaea.de/10.1594/PANGAEA.861203
- Crop yields (wheat): FAOSTAT (national statistics).
  - Link: https://www.fao.org/faostat/en/#data
- Sowing and harvest dates: LUH data (Luh.umd.edu).
  - Link: https://luh.umd.edu/data.shtml
- Additional context on land for soil-based GHG removal: CEH catalog entry.
  - Link: https://catalogue.ceh.ac.uk/documents/3fa5921b-244a-4944-ab90e690dbc05a7e
- Manure application reference: Gerber et al. 2016.
  - Link: https://onlinelibrary.wiley.com/doi/full/10.1111/gcb.13341
- Key references for ECOSSE model and applications:
  - Smith et al. 2010a, 2010b; Gerber et al. 2016.

## Data structure and file layout
- Table 1 enumerates the individual dataset files, each representing a specific management change (e.g., notill, residincorp, redtill, covercrop, manure) under climate scenarios A1B or A2.
- For each management-climate combination, the file reflects the SOC change relative to BAU.
- Table 2 describes per-file header content, including:
  - Latitude, longitude, area_km2, LU_agr_nrs_grid_cell (agricultural land use within grid cell)
  - SOC change columns by decade: SOC_20_30_MgC_ha_yr, SOC_30_40_MgC_ha_yr, SOC_40_50_MgC_ha_yr, SOC_50_60_MgC_ha_yr, SOC_60_70_MgC_ha_yr, SOC_70_80_MgC_ha_yr, SOC_80_90_MgC_ha_yr, SOC_90_100_MgC_ha_yr
- Each file provides grid-cell level SOC changes (annual averages) across the specified decades, enabling regional and global analyses.

## Outputs and interpretation
- SOC_CH values indicate the change in SOC relative to BAU for each grid cell and time window under each management scenario.
- The dataset supports mapping, regional and local statistical analyses, and cross-validation against existing literature to assess plausibility.
- The 0.5-degree grid resolution enables broad-scale assessment of management practices, climate scenarios, and potential SOC sequestration or emissions across the globe.

## Use considerations for data leaders
- User needs and applicability: offers scenario-based insights into how different agricultural management practices may alter SOC by 2100, useful for strategy, policy analysis, and cross-sector collaboration.
- Data quality and standards: metadata includes explicit variable definitions and decadal SOC change values; relies on ECOSSE model outputs and publicly available input datasets with documented sources.
- Discoverability and governance: dataset organization by management and climate scenarios, with clear file naming and header descriptions; supports reproducibility via documented modelling workflow (ECOSSE v6.2b, R 4.3.0).
- Data gaps and limitations: results depend on model assumptions (BAU baseline, climate scenarios A1B/A2, specific management implementations) and grid-based resolution (0.5-degree); uncertainties inherent to model inputs and parameters should be considered in interpretation.
- Reuse and integration: compatible with other land-use, soil, and climate datasets; potential to integrate with policy analyses, land management planning, and emissions mitigation assessments.