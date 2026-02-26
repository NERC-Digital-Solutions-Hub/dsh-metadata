# Step 1: Spatial Mapping of Deposition and concentration to UK protected sites (SAC, SPA, SSSI)

## Aim and scope
- Map deposition and concentrations to UK protected sites and generate site-level metrics.
- Create 1x1 km resolution maps for pollutants and relate them to SAC, SPA, and SSSI sites.
- Produce minimum, maximum, and area-weighted (grid-average) deposition values for each site based on 2018–2020 three-year means.

## Methodology

- Step 1: Spatial data preparation
  - Create a 1x1 km grid covering the UK domain.
  - Clip the grid to UK protected sites boundaries (SAC, SPA, SSSI/ASSI) to produce a gridded dataset for these sites.
  - Merge gridded CBED 3-year mean data (2018–2020) with the site grid to generate a UK protected sites CBED dataset.
  - Repeat for 1x1 km concentration datasets for NOx and SO2 based on the PCM model.
  - Data on site boundaries and features are sourced from each country’s national site datasets.

- Step 2: Generating minimum, maximum, and grid-average values
  - Use SQL queries on the gridded dataset to compute:
    - Minimum, maximum, and grid-average deposition/concentration for each protected site.
    - Grid-average deposition per site is calculated as (grid square area / total site area) × CBED deposition value; sum across grid squares within the site.
  - CBED results provide deposition values for nitrogen, sulfur, and related ions; PCM provides concentration maps for NOx, SO2, and related species.

- CBED modelling (Concentration Based Estimated Deposition)
  - Produces 1x1 km resolution maps of wet and dry deposition for S, N, and base cations from measured air concentrations and precipitation ions (from the UKEAP network).
  - Wet deposition derived from rainfall and occult deposition; separated anthropogenic vs total components using ion ratios relative to sea salt; includes an orographic enhancement factor for uplands.
  - Dry deposition uses habitat-specific deposition velocities for five land cover categories (forest, moorland, grassland, arable, urban); deposition apportioned by land-cover mix within each grid square.
  - Interannual variability exists; CBED values are averaged over three years to smooth annual fluctuations.
  - Outputs are annual values, provided as rolling 3-year means (except non-marine Ca+Mg values), with ecosystem-specific scenarios (moorland, forest, grid average).

- PCM modelling (Pollution Climate Mapping)
  - Generates background maps and 1x1 km grids of pollutant concentrations for the UK.
  - One model per pollutant (NOx, NO2, PM10, PM2.5, SO2, and others) with base year and projection runs.
  - Used for scenario assessment, population exposure calculations, and TEN submissions; provides road-side values and supports policy development.

## Data quality, units, and documentation

- Units
  - Deposition values: kilo-equivalents per hectare per year (keq ha⁻¹ year⁻¹).
  - Converted to kg S ha⁻¹ year⁻¹ or kg N ha⁻¹ year⁻¹ by multiplying by 16 (S) or 14 (N), respectively.
  - Concentrations: micrograms per cubic metre (µg m⁻³).

- Quality control
  - CBED/PCM methods align with QA practices for government analytical models; extensive peer review and inter-comparison exercises.
  - Mass-balance checks and version control; documented method developments; central storage of code; senior officer approvals.

- Data structure and files
  - Files store 3-year means (2018–2020) for grid-based and site-based deposition/concentration data at 1x1 km resolution.
  - Data cover forest, moorland, and grid-average ecosystem categories; include minimum, maximum, average values for forest and moorland, and grid-average figures.
  - File descriptions (examples)
    - File 1: APIS_srcl_nitrogen_acid_deposition_forest_sitebygrid_2018_2020.csv
      - Fields include SITECODE, SITENAME, SITEAREA, GRIDAREA, YEAR, NH3_NH4_FOREST, NO2_NO3_FOREST, SO2_SO4_NM_FOREST, CA_MG_NM_FOREST.
    - File 2–3: Deposition by moorland and grid-average site-by-grid.
    - File 4–6: Concentrations for ammonia, NOx, and SO2 by grid.
    - File 7–9: Generated minimum/maximum/average deposition for forest/moorland and grid-average.
    - File 10–12: Concentrations by site for ammonia, NOx, and NO2/SO2 as grid/forest/moorland statistics.
  - Files include site metadata (SITECODE, SITENAME, COUNTRY, DESIGNATION), SITEAREA, GRIDAREA, and coordinates.

- Data accessibility
  - Data are tied to CBED and PCM outputs, with references and resource locators provided for the UK Eutrophying and Acidifying Pollutants datasets and PCM data.
  - Metadata describes units, description, and data provenance for each field.

## Outputs and use for analysis

- UK protected site CBED dataset (2018–2020, 3-year mean) linking site boundaries to gridded deposition values.
- Per-site deposition metrics:
  - Minimum, maximum, and average deposition values for forest, moorland, and grid-average scenarios.
- Per-site concentration metrics (NOx, NH3, SO2) at the same aggregation levels.
- Spatially explicit deposition/concentration data at 1x1 km grid resolution, with site-level summaries for impact assessment, policy evaluation, and compliance with environmental directives.

## Key considerations and challenges for analysts

- Inter-annual variability is averaged out to 3-year means; short-term trends may be obscured.
- Alignment of data scales: 1x1 km grid versus site areas; area-weighted calculations required for site-level summaries.
- Data accessibility and standardisation: CBED/PCM outputs embedded in multiple files with consistent but complex metadata; careful data integration is essential.
- Habitat-specific deposition (forest vs moorland) affects deposition values; users should apply ecosystem-specific values appropriately.
- Orographic enhancement and separation of anthropogenic components add methodological complexity to interpretation.

## References and resources

- References to foundational studies and model evaluations (e.g., Beswick et al., Fowler et al., Dore et al., Carslaw 2011) and Defra/ROTA P materials.
- Resource locators for datasets and PCM model outputs:
  - UK Acidifying and Eutrophying Atmospheric Pollutants dataset info
  - UK Air Defra PCM data portal
  - PCM data repository and supporting information

## Takeaways for analysts
- A robust, three-year-mean, grid-based framework links gridded pollutant concentrations and CBED deposition to UK protected sites, enabling site-level risk assessment and policy-oriented scenario analysis.
- The workflow combines CBED wet/dry deposition modelling with PCM concentration modelling, delivering both spatially explicit maps and aggregated site metrics.
- Detailed data files provide granular and ecosystem-specific deposition and concentration values, suitable for correlation analyses, trend detection, and predictive modelling within environmental decision-making contexts.