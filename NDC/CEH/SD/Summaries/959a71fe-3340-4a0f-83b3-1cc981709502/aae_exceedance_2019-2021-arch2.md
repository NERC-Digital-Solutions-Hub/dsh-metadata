# Average Accumulated Exceedance (AAE) of acidity and nutrient nitrogen critical loads by acid and nitrogen deposition for 2019-21

- Purpose: Provide 1x1 km grid datasets summarising exceedances of acidity and nutrient nitrogen critical loads due to acid and nitrogen deposition, enabling consistent monitoring of environmental health and policy performance over time.
- Scope: AAE for two pollutants (acidity and nutrient nitrogen) across habitats sensitive to acidification and eutrophication, for the period 2019–2021.

## What the data represent

- AAE is the sum of exceedances across multiple habitats within each 1x1 km grid cell, divided by the total habitat area in that cell.
- Two raster datasets:
  - acid_aae_2019-2021.tif: AAE for acidity (keq ha^-1 year^-1)
  - nutn_aae_2019-2021.tif: AAE for nutrient nitrogen (keq ha^-1 year^-1)
- Habitat coverage differs by pollutant:
  - Acidity: acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, and various woodlands (productive and unmanaged).
  - Nutrient nitrogen: additional habitats including dune grassland, saltmarsh, various unmanaged woodlands, and beech/oak pine woodlands.

## Methodological framework

- Based on UK methods for calculating critical loads and their exceedances (Hall et al., 2015).
- Exceedances are determined by comparing deposition to habitat-specific critical loads.
- For acidity, the critical load function combines sulfur and nitrogen deposition; for nitrogen, exceedances are total nitrogen deposition minus the critical load.
- Freshwater exceedances are not included in AAE (they’re catchment-based and not 1x1 km grid-based).

## Key inputs and data sources

- Deposition data: CBED (Concentration-Based Estimated Deposition)
- Land cover: UK CEH Land Cover Map 2019 (1 km summary rasters)

## Data structure and format

- Two raster files (one per pollutant), projected in British National Grid (EPSG: 27700), each with a single band.
- Units:
  - Acidity AAE: keq ha^-1 year^-1
  - Nutrient nitrogen AAE: keq ha^-1 year^-1 (convertible to kg N ha^-1 year^-1 by multiplying by 14; 1 keq ha^-1 year^-1 = 14 kg N ha^-1 year^-1)
  - If deposition is below the critical load, AAE values are zero.

## Interpretation and caveats

- Exceedance does not imply immediate ecological damage; recovery times (chemical and biological) may be long.
- Habitat area maps and critical load calculations may differ from other national habitat maps; totals may not be directly comparable.
- Acidity AAE cannot be expressed as a simple kg of S or N due to the combined S and N nature of acidity exceedances.
- For peat and mineral soils, acidity critical loads follow different calculation methods (empirical vs. simple mass balance), with peat requiring special treatment.

## Quality control and provenance

- Data production follows internationally agreed methods under the UNECE CLRTAP framework.
- A detailed UK Methods Report (Hall et al., 2015) documents transparency in calculations and data.
- Summary exceedance statistics and trends are published separately (e.g., Rowe et al., 2023).

## Use and interpretation guidance for analysts

- Outputs support assessment of environmental health and policy effectiveness over time in a standardised, comparable format.
- The datasets are suitable for integration with other environmental data to enhance analysis beyond single-use applications.
- Data are designed to be stored and uploaded to appropriate data portals for long-term accessibility.

## Accessibility and data management considerations

- Associated datasets and methods are positioned for easy access within national data portals.
- The architecture supports enabling others to access underlying data used to derive final outputs.

## Appendix and references (context for methods)

- Appendix I provides the simple mass balance equation for woodland acidity critical loads (Ca:Al-based) used in SMB calculations.
- References include foundational methods and case studies (e.g., Hall et al., 2015; Henriksen & Posch, 2001; Sverdrup & De Vries, 1990s; Rowe et al., 2023).