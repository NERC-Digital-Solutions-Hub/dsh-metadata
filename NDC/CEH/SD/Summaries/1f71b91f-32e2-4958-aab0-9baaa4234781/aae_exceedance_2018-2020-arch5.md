Introduction These 1x1 km data sets comprise the Average Accumulated Exceedance (AAE) of acidity and of nutrient nitrogen critical loads by acid and nitrogen deposition for 2018-20. 

## Overview
- Two raster datasets summarise long-term exceedances of acidity and nutrient nitrogen critical loads across the UK at 1x1 km grid cells.
- AAE combines per-habitat exceedance, the exceeded habitat area, and total habitat area within each grid cell; expressed in keq ha-1 year-1.
- For nutrient nitrogen, AAE can be converted to kg N ha-1 year-1 (1 keq ha-1 year-1 = 14 kg N ha-1 year-1). For acidity, AAE remains in keq ha-1 year-1.
- Habitats differ between acidity and nutrient nitrogen datasets.

## Data Content
- Files:
  - acid_aae_2018-2020.tif: AAE for acidity (keq ha-1 year-1)
  - nutn_aae_2018-2020.tif: AAE for nutrient nitrogen (keq ha-1 year-1)
- Coverage: extends where habitats are sensitive to acidity or eutrophication; each file contains one band.
- Projection: British National Grid (EPSG:27700).
- Habitat sets:
  - Acidity: acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, productive/wide woodland (two categories), unmanaged coniferous and broadleaved woodland.
  - Nutrient nitrogen: same as acidity plus several additional woodland and grassland types, including unmanaged beech/oak Scots pine woodland, dune grassland, saltmarsh, etc.
- Data are designed to complement national UK assessments and are not the same as catchment-based freshwater datasets.

## Calculation Methodology
- Based on UK Methods Report (Hall et al., 2015) with inputs from CBED deposition data and the UK Land Cover Map 2019.
- Exceedances:
  - Critical loads (for acidity and nitrogen) are compared with deposition to derive exceedances.
  - For acidity, exceedances involve combination of sulfur and nitrogen deposition; for nitrogen, exceedances are total N deposition minus the critical load.
  - Exceedance type used is the “shortest distance” method relative to the critical load function (CLmaxS, CLminN, CLmaxN) and is regionally defined (five regions in the function).
- Acidity critical loads:
  - Two approaches: empirical for non-woodland (mineral/organomineral soils) and simple mass balance for woodland/peat habitats.
  - Peat soils use a pH-buffering-based target (rain pH ~4.4).
- Nitrogen critical loads:
  - Empirical, aligned to EUNIS habitat classes, with ranges to reflect ecosystem variability.
- Output interpretation:
  - Exceedance indicates potential for long-term harm under steady-state assumptions; does not specify current damage or immediate recovery.

## Inputs and Data Sources
- Deposition data: CBED (Concentration-Based Estimated Deposition) – deposition estimated from air concentrations and land use.
- Land cover: UK CEH Land Cover Map 2019 1km summary rasters.
- These inputs underpin the spatial patterns and habitat distributions used in calculating AAE.

## Data Structure and Format
- Two GeoTIFF rasters, each with a single band:
  - acid_aae_2018-2020.tif
  - nutn_aae_2018-2020.tif
- Extents differ between datasets due to habitat distributions.
- Values are expressed in keq ha-1 year-1; nutrient nitrogen AAE can be converted to kg N ha-1 year-1 via multiplication by 14.

## Quality Control, Provenance, and Documentation
- Data produced following internationally agreed methods under CLRTAP; QA documented in detailed methods (Hall et al., 2015).
- Summary trends and indicators are published annually (e.g., Rowe et al., 2023) but freshwater data used for AAE calculation are not included due to differing spatial basis (catchment-based vs grid-based).
- Documentation notes alignment with national/international standards and transparency of methodology.

## Use and Sharing Guidance for Data Stewards
- Metadata considerations:
  - Dataset name, purpose, 2018-2020 time period, 1x1 km grid, EPSG:27700, single-band rasters.
  - Variables: AAE acidity (keq ha-1 yr-1) and AAE nitrogen (keq ha-1 yr-1); conversion factor to kg N for nitrogen dataset.
  - Habitat classes included per dataset; data sources (CBED, Land Cover Map 2019), and methodological references (Hall et al. 2015; Rowe 2023).
  - Calculation method summary (shortest-distance exceedance relative to CL functions) and acknowledgment of regional variation in the critical load function.
  - caveats: steady-state interpretation; potential lag in chemical/biological recovery; differences vs other habitat maps; exclusion of freshwater grid-based data.
- Governance actions:
  - Ensure complete metadata and lineage, including versioning and update plans if datasets are revised.
  - Maintain traceability of inputs (CBED, Land Cover Map) and the calculation methodology.
  - Address interoperability considerations: fixed grid resolution, projection, and habitat classification schemes.
  - Document limitations and user guidance for interpretation and transformation (e.g., converting nitrogen AAE to kg N ha-1 year-1).

## Limitations and Caveats
- Exceedance indicates potential long-term effects, not immediate damage, and recovery may lag after deposition reductions.
- Habitat maps and grid-based extents may differ from other national habitat datasets.
- Freshwater data (1752 locations) are not included in these AAE calculations due to catchment-based methodology, not grid-based.
- Differences in data availability across habitats may influence comparisons across acidity and nitrogen AAE datasets.

## References and Notes
- Hall et al. 2015; Rowe et al. 2023; Calver et al.; Sverdrup et al.; Henriksen and Posch; Skiba and Cresser; Morton et al. 2022 (Land Cover Map 2019); CEH methods and related appendices.