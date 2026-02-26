# Introduction

- The document describes two 1x1 km raster data sets of Average Accumulated Exceedance (AAE) for UK habitat sensitivity to acidification and eutrophication, spanning 2019–2021.
- AAE summarizes exceedances of critical loads by integrating exceedance amount, affected habitat area, and total habitat area per grid cell.

## What the data represent

- AAE for acidity (acid_aae_2019-2021.tif): keq ha-1 year-1 across acidity-sensitive habitats.
- AAE for nutrient nitrogen (nutn_aae_2019-2021.tif): keq ha-1 year-1 across nutrient nitrogen-sensitive habitats.
- AAE equals the accumulated exceedance (AE) divided by total habitat area in each 1x1 km grid square.
- For nutrient nitrogen, AAE can be converted to kg N ha-1 year-1 by multiplying by 14 (1 keq ha-1 year-1 = 14 kg N ha-1 year-1); acidity AAE remains in keq ha-1 year-1.

## Data products and structure

- Two raster files (one for acidity, one for nutrient nitrogen) covering different habitat distributions.
- Projection: British National Grid (EPSG: 27700); each file has a single band.
- File naming:
  - acid_aae_2019-2021.tif
  - nutn_aae_2019-2021.tif

## Calculation methodology (high-level)

- Based on UK methods for critical loads and exceedances (Hall et al., 2015).
- Exceedances are calculated as the shorted distance from deposition to the acidity/ nitrogen critical load function, using:
  - Acidity: a function of sulfur and nitrogen deposition with regions defined in the Critical Load Function.
  - Nitrogen: exceedance is total deposition minus the critical load.
- Critical loads and exceedances depend on habitat type and soil/peat conditions:
  - Acidity: empirical approach for mineral/organomineral soils; simple mass balance for woodland and peat soils; peat uses a pH-based threshold.
  - Freshwaters: FAB model for catchments; not included in the grid-based AAE calculation.
- The AAE is the sum of AE across habitats within a grid divided by the grid’s total habitat area.
- For acidity, exceedances involve both S and N deposition; AAE for acidity is expressed in keq ha-1 year-1 and cannot be converted to kg S or N.

## Inputs and data sources

- Deposition data: CBED (Concentration-Based Estimated Deposition) model.
- Land cover: UK CEH Land Cover Map 2019 (1 km summary rasters).
- Habitat sensitivity and distribution data used to map critical loads and exceedances.

## Habitats included (selection per dataset)

- Acidity (acid_aae):
  - acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed/productive coniferous woodland, managed/productive broadleaved woodland, unmanaged coniferous and broadleaved woodland.
- Nutrient nitrogen (nutn_aae):
  - acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, woodland types (managed and unmanaged), dune grassland, saltmarsh, and several unmanaged woodland types (including beech, oak, Scots pine) and other unmanaged woodland.

## Quality control and provenance

- Methods and QA follow national/international standards under the UNECE CLRTAP framework.
- Detailed methodological documentation exists (e.g., Hall et al., 2015) to ensure transparency of critical loads and exceedances derivation.

## Use, interpretation, and limitations (Data Steward perspective)

- AAE indicates long-term potential for harmful effects under steady-state assumptions; it does not imply immediate ecological damage.
- Habitat distribution and total habitat areas used may differ from other national maps; results reflect areas with data available for calculation.
- Reducing deposition below critical loads does not guarantee quick ecological recovery; chemical and biological recovery can be lagged and long-term.
- Freshwater data (1752 locations) are treated separately and are not included in the grid-based AAE calculations because they are catchment-based rather than grid-based.
- The data are static for 2019–2021; annual trends are published separately in UK Trends Reports and other biodiversity indicators.

## Data access, updates, and documentation

- Data are accompanied by methodological documentation (e.g., UK Methods Report, Hall et al., 2015) and references to model inputs and habitat mappings.
- The document notes that summary statistics and trends are published separately and that the AAE rasters themselves reflect the 2019–2021 period.