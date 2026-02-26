# Emissions of metals and air pollutants in the UK, 1750 - 2100 (1km x 1km)

## Purpose and Scope
- Provides 1km x 1km gridded estimates of emissions for seven air pollutants (CO, NH3, NOx, PM2.5, PM10, SO2, NMVOCs) and five metals (Cd, Cu, Ni, Pb, Zn) in the UK from 1750 to 2100.
- Emissions are reported across 11 SNAP sectors (European Environment Agency) used in the UK National Atmospheric Emissions Inventory (NAEI).
- Data span historical, contemporary, and future periods to support analysis of trends, correlations, and predictions.

## Time Periods and Data Structure
- Historical emissions: 1750–1960 (based on literature; pre-1970 EF adjustments; S-shaped interpolation where multiple EFs exist).
- Contemporary emissions: 1970–2018 (from UK NAEI 2021; NH3 starts 1980).
- Future emissions: 2040, 2070, 2100 across five Shared Socioeconomic Pathways (SSPs).
- File structure: 3,688 files covering 7 pollutants and 5 metals across 11 SNAP sectors.
- Year and scenario notation in filenames: Sxx_p_emis_SSPi_y_km2.tif, with y including 1750–1960 timeline and 2040/2070/2100; SSP i ranges 0–5 (0 = past to present); 1–5 = SSP scenarios.

## Spatial and Temporal Resolution
- Grid: 1 km x 1 km.
- Units: tonnes of pollutant per km² per year (t km⁻² yr⁻¹).
- Northern Ireland proxies estimated via random forest due to limited pre-1950 data.

## Methodology by Time Period

### Historical (1750–1960)
- Emissions inferred from literature on key fuels and processes; prioritisation by contribution to 1970–2018 emissions.
- Emission factors (EFs) adjusted for coal, coke, oil practices; where pre-1970 EF not available, earliest UK EF used with an S-shaped interpolation to 1970.
- Metals from fuel combustion linked to coal/oil metal content and ash enrichment; changes in PM EF affect metal emissions.
- Spatial distribution using proxies (population surfaces, census data, land use, proximity to water/roads, digitised data) at 1 km resolution (OSGB projection).
- For Northern Ireland (pre-1950 data scarce), proxies estimated with random forest using UK GB data.

### Contemporary (1970–2018)
- APs and metals from UK NAEI 2021; NH3 begins in 1980.
- Diffuse emissions distributed using the 2018 spatial pattern back to 2000 for 2000–2018; year-specific scaling applied to SNAP totals (1970–1995).
- Metals: diffuse+point surfaces for each SNAP scaled to UK totals back to 1970 (no separate 1970 point data for metals).
- NH3 distribution anchored to 1970; 2018 EF data used for NH3 distribution and scaled as needed.

### Future (2040–2100)
- UK-specific SSPs (SSP0–SSP5) used; 18 key indicators (population, fertiliser use, transport, livestock, etc.) inform semi-quantitative trends.
- Indicators converted to scaling factors and applied to 2018 UK emission baselines.
- NH3 EF adjustments use Defra’s Scenario Modelling Tool aligned to 2018 values and SSP projections.
- Land-use inputs for diffuse sources derived from CRAFTY-GB model outputs.

## Data Quality and Validation
- QA/QC tied to NAEI 2021 methodologies; visual checks for UK-wide deposition patterns; comparison of time-series surface concentrations with observations where available.
- Full QA/QC performed for 2018 for multiple species.
- Emissions totals (1970–2018) linked to NAEI data to ensure consistency.

## Data Organization and Access
- File naming: Sxx_p_emis_SSPi_y_t_km2.tif.
- Folder structure: data/p/y/filename.tif.
- Data coverage: 3,688 files across the specified pollutants, metals, SNAP sectors, years, and SSPs; not all combinations exist where modeling did not generate emissions.

## Key Data Sources and References
- SNAP sectors: 11 sectors (NAEI framework).
- Historical EF sources: Bond et al. 2007; WebFIRE (EPA 2021); EMEP/EEA guidebook (2019).
- Contemporary inventories: NAEI 2021 (Garland et al., 2022).
- SSP and scenario work: Pedde et al. 2021; Science of the Total Environment.
- Spatial proxies and methodological foundations: Levy et al. 2018; Nalbandian 2012; Shaws-Taylor et al. 2006.
- Supporting tools/models: Defra Scenario Modelling Tool; CRAFTY-GB model.

## Considerations for Analysts
- Heavily data-intensive with regional and temporal heterogeneity; pre-1970 uncertainties due to proxy-based EFs.
- Spatial proxies introduce uncertainties in historical distributions, especially in NI.
- Future projections depend on SSP narratives and semi-quantitative indicators; scenario interpretation required.
- Data integration with atmospheric models requires careful alignment of SNAP sector definitions and unit conventions.

## How This Supports Analysis and Decision-Making
- Enables assessment of historical emissions burden and spatial distribution at high resolution.
- Facilitates scenario-based forecasting of deposition, air quality, and metal exposure under SSP futures.
- Supports correlations between emissions, land use, population, and policy interventions.
- Provides a consistent, reproducible dataset with metadata and QA/QC tied to established inventories (NAEI).