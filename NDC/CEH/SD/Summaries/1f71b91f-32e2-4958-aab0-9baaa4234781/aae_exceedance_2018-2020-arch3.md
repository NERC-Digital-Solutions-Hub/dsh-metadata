# Introduction

- What the data are
  - 1x1 km raster data sets for Average Accumulated Exceedance (AAE) of acidity and nutrient nitrogen critical loads due to acid and nitrogen deposition for 2018–2020.
  - AAE summarises exceedances across habitats within each grid square: AE is exceedance × exceeded habitat area; AAE = AE / total habitat area in the grid cell.
  - Two rasters: acid_aae_2018-2020.tif (acidity) and nutn_aae_2018-2020.tif (nutrient nitrogen).
  - Habitats included differ by pollutant (acidity vs. nitrogen), listed below.

- Habitats included
  - Acidity (acid_aae): acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, productive coniferous woodland, productive broadleaved woodland, unmanaged coniferous and broadleaved woodland.
  - Nutrient nitrogen (nutn_aae): acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, productive coniferous woodland, productive broadleaved woodland, unmanaged beech/oak/Scots pine woodlands, other unmanaged woodland, dune grassland, saltmarsh.

- Methods and key background
  - Builds on UK Methods Report (Hall et al., 2015) and uses CBED deposition data and UK Land Cover Map 2019 1 km rasters.
  - Summary exceedance statistics by habitat and country are published in annual Trends Reports and the UK Biodiversity Indicator (pollution pressures).
  - Freshwater exceedances (1752 locations) are reported separately (catchment-based) and not included in the AAE calculations.

- Calculation and interpretation of exceedances
  - Exceedances are the amount by which deposition exceeds the critical load (for N, deposition minus CL; for acidity, depends on S and N with a region-based approach).
  - Acidity critical loads combine S and N deposition; one diagonal CL function (plus adjustments for N removal) defines the threshold.
  - The Critical Load Function is partitioned into five regions to determine exceedance via the shortest distance to the threshold line.
  - Exceedances are expressed in keq ha-1 year-1 for acidity and in keq ha-1 year-1 (convertible to kg N ha-1 yr-1 by multiplying by 14) for nutrient nitrogen.
  - A grid cell is exceeded if its deposition lies beyond the habitat’s CL range.

- Data inputs and structure
  - Deposition data: CBED (Concentration-Based Estimated Deposition) for spatial deposition patterns.
  - Land cover: UKCEH Land Cover Map 2019 1 km summary rasters.
  - Projections: British National Grid (EPSG:27700); each file contains one band.
  - Nature of values: AAE values are in keq ha-1 year-1; below CL, AAE is set to zero.
  - Freshwater data are not included in these AAE rasters.

- Quality control and governance
  - Based on methods agreed at international CLRTAP meetings; detailed methodology documented in Hall et al. (2015).
  - Encourages transparency about methods and data used in deriving UK critical loads and exceedances.

- Use and interpretation guidance for monitoring frameworks (relevant considerations)
  - AAE maps indicate long-term exceedance potential rather than immediate damage; recovery is slow and time-lagged.
  - Habitat distribution maps and habitat areas used may differ from other national maps; totals may differ accordingly.
  - Data availability and sharing: the datasets rely on underlying datasets with metadata; some barriers may arise from data sharing and metadata completeness.
  - These datasets support policy evaluation, monitoring progress, and informing future decisions, with attention to data governance and openness.

- Appendix (conceptual formula)
  - For acidity in woodland: CLA = ANCw - ANCle(crit); with definitions for ANCw, ANCle(crit), BCle, Hle(crit), Ca:Al, and related terms (illustrative of the simple mass balance approach used for mineral and organo-mineral soils).