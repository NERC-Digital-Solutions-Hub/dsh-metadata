# Introduction

## Overview of datasets
- 1x1 km data sets for Average Accumulated Exceedance (AAE) of acidity and nutrient nitrogen critical loads, covering 2018–2020.
- AAE defined as the accumulated exceedance per grid square, summarising exceedances across habitats within each 1x1 km cell:
  - AE (keq year-1) = exceedance (keq ha-1 year-1) × exceeded habitat area (ha)
  - AAE (keq ha-1 year-1) = AE (keq year-1) / total habitat area (ha)
- Habitats included:
  - Acidity (acid_aae_2018-2020.tif): acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, productive coniferous woodland, productive broadleaved woodland, unmanaged coniferous and broadleaved woodland.
  - Nutrient nitrogen (nutn_aae_2018-2020.tif): acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, productive coniferous woodland, productive broadleaved woodland, unmanaged beech/oak/Scots pine woodland, other unmanaged woodland, dune grassland, saltmarsh.
- Values are expressed as keq ha-1 year-1 for both datasets; nutrient nitrogen can be converted to kg N ha-1 year-1 (1 keq ha-1 year-1 = 14 kg N ha-1 year-1), while acidity cannot be directly converted to kg S or N.

## Methods in brief
- Based on the UK Methods Report (Hall et al., 2015) and related CLRTAP guidance; trends published in annual Trends Reports and UK Biodiversity Indicators.
- Acidity critical loads:
  - Two approaches:
    - Empirical method for non-woodland habitats on mineral/organomineral soils.
    - Simple mass balance (SMB) for woodland habitats and for peat soils.
  - Peat soils have separate treatment due to buffering and lack of alkalinity inputs.
  - Acidity critical loads for freshwater habitats use the catchment FAB model (not used for grid-based AAE here).
- Nutrient nitrogen critical loads:
  - Empirical loads set under CLRTAP; assigned to habitat classes using EUNIS typology; expressed as ranges (e.g., 10–20 kg N ha-1 yr-1); revised in 2022.
- Calculation of exceedances:
  - Exceedance = actual deposition − critical load.
  - For acidity, deposition includes both sulfur and nitrogen; the calculation uses the Critical Load Function (CLF) and is staged across five regions, with “shortest distance” exceedance defined.
  - For nutrient nitrogen, exceedance is based on total N deposition minus the nitrogen CL.
- Graphical interpretation:
  - Acidity CL can be depicted by a 45-degree line on a S–N deposition plot; shifts along the N axis account for long-term N removal processes; S has no analogous removal.

## Inputs
- Deposition data: CBED (Concentration-Based Estimated Deposition) methodology.
- Land cover: UK CEH Land Cover Map 2019 1 km summary rasters.

## Nature & units of recorded values
- AAE values: keq ha-1 year-1.
- If deposition is below the critical load, AAE = 0.
- Nutrient nitrogen AAE can be converted to kg N ha-1 year-1 using 1 keq ha-1 year-1 = 14 kg N ha-1 year-1.
- Acidity AAE remains in keq ha-1 year-1 and cannot be converted to kg S or N.

## Data structure
- Two raster files:
  - acid_aae_2018-2020.tif: acidity AAE in keq ha-1 year-1.
  - nutn_aae_2018-2020.tif: nutrient nitrogen AAE in keq ha-1 year-1.
- Coverage differs by habitat sensitivity distributions.
- Projection: British National Grid (EPSG:27700); each file has one band.

## Use, interpretation, and caveats
- AAE indicates potential for long-term harmful effects under steady-state assumptions; exceeding a critical load does not imply immediate damage.
- Habitat distribution and total habitat area in the maps may differ from other national habitat datasets; calculations only include areas with data for CL derivation.
- Reducing deposition below the critical load does not guarantee immediate ecological recovery; chemical and biological recovery may be slow.

## Quality control
- Methods aligned with CLRTAP and international guidance; detailed transparency provided in Hall et al. (2015) Methods Report.
- A detailed methods report is available, ensuring traceability of data and calculations.

## Appendix I and data specifics
- Appendix I provides the simple mass balance equation for woodland acidity critical loads (Ca:Al-based) and related terms (ANC, BC, leaching, etc.) used in SMB calculations.
- The acidity critical load function is conceptually illustrated via diagonal plots of S and N deposition, with regional categorisation guiding exceedance calculations.

References
- Core methodological sources include Hall et al. (2015) for UK methods, Rowe et al. (2023) for Trends/UK Biodiversity indicators, and CLRTAP-related guidance. Additional foundational works cover empirical and SMB approaches for acidity and the FAB model for freshwater habitats.