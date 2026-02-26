# Average Accumulated Exceedance (AAE) of Acidity and Nutrient Nitrogen Critical Loads for 2018-2020

- Purpose and scope
  - 1x1 km raster data sets representing the Average Accumulated Exceedance (AAE) of acidity and of nutrient nitrogen critical loads due to acid and nitrogen deposition for 2018–2020.
  - AAE aggregates exceedances across habitats within each grid square, enabling consistent assessment of environmental health and policy performance over time.
  - Distinct rasters exist for acidity and nutrient nitrogen, reflecting different habitat sensitivities and distributions.

- What AAE represents
  - For each habitat, AE = exceedance (keq ha^-1 year^-1) × exceeded habitat area (ha).
  - AAE = total AE across all habitats in a 1x1 km grid cell ÷ total habitat area in that cell (keq ha^-1 year^-1).
  - Values are typically zero when deposition is below the corresponding critical load.
  - For nutrient nitrogen, AAE can be converted to kg N ha^-1 year^-1 by multiplying by 14 (1 keq ha^-1 year^-1 = 14 kg N ha^-1 year^-1). Acidity AAE remains in keq ha^-1 year^-1.

- Habitats included
  - Acidity (acid_aae_2018-2020.tif): 
    - acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed (productive) coniferous woodland, managed (productive) broadleaved woodland, unmanaged coniferous and broadleaved woodland.
  - Nutrient nitrogen (nutn_aae_2018-2020.tif):
    - acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed (productive) coniferous woodland, managed (productive) broadleaved woodland, unmanaged beech woodland, unmanaged oak woodland, unmanaged Scots pine woodland, other unmanaged woodland, dune grassland, saltmarsh.

- Methods and context
  - Based on UK Methods Report (Hall et al., 2015) for calculating acidity and nitrogen critical loads and their exceedances; deposition and critical loads are derived from standardized methods used in CLRTAP.
  - Summary exceedance statistics by habitat and country are published in annual Trends Reports and UK Biodiversity Indicators; freshwater data (1752 locations) are reported separately and are not included in these AAE calculations because they use catchment-based areas, not 1x1 km grids.
  - Critical loads concept:
    - Acidity: uses empirical methods for non-woodland and simple mass balance for woodland and peat habitats; peat critical loads reflect buffering by organic matter and are tied to an effective rain pH threshold (4.4).
    - Freshwaters use the FAB model (not part of these grid-based AAE calculations).
    - Nitrogen: empirical critical loads anchored to habitat classes in EUNIS; ranges reflect ecosystem response variability; latest revision in 2022.

- Calculation of exceedances
  - Exceedance equals total pollutant deposition minus the corresponding critical load.
  - For acidity, both sulfur (S) and nitrogen (N) deposition contribute; the Critical Load Function is divided into five regions to determine the shortest-distance exceedance relative to CLmaxS, CLminN, and CLmaxN.
  - For acidity, a diagonal CL plot (S vs N) is used to define the critical load boundary, with long-term N removal processes shifting the boundary to allow more N before exceeding acidity.
  - AAE represents accumulated exceedance normalized by habitat area within each grid cell.

- Inputs and data sources
  - Deposition data: CBED (Concentration-Based Estimated Deposition) methodology.
  - Land cover: UK Land Cover Map 2019 (1 km summary rasters).

- Data structure and presentation
  - Two raster files in British National Grid (EPSG:27700), each with one band:
    - acid_aae_2018-2020.tif: acidity AAE (keq ha^-1 year^-1)
    - nutn_aae_2018-2020.tif: nutrient nitrogen AAE (keq ha^-1 year^-1)
  - Coverage differs between the two rasters due to habitat distributions.
  - Data are suitable for storage in standard data portals and downstream analysis.

- Units, interpretation, and caveats
  - AAE units: keq ha^-1 year^-1. If below the critical load, AAE is set to zero.
  - Nitrogen AAE can be converted to kg N ha^-1 year^-1 by multiplying by 14; acidity AAE remains in keq ha^-1 year^-1.
  - Exceedance data indicate potential for harmful effects under long-term steady-state assumptions; absence of immediate damage or rapid recovery is implied.
  - Habitat distribution and total habitat area may differ from other national maps; reductions in deposition below the CL do not guarantee immediate ecosystem recovery due to possible time lags.

- Quality control and reproducibility
  - Methods aligned with national/international agreements (UNECE CLRTAP); detailed quality assurance reported in Hall et al. 2015.
  - Transparency and reproducibility supported by published methodology and references.

- Appendix and key methodology
  - Appendix I provides the simple mass balance equation for woodland acidity critical loads (Ca:Al ratio-based), detailing components such as ANC, calcium weathering, base cation contributions, and leaching terms.

- Relevance for monitoring and data sharing
  - Provides a standardized, time-bound snapshot of AAE in 1x1 km grids to monitor environmental health and policy performance over time.
  - Data are designed for integration with other datasets to increase value beyond single-use analyses and to support broader accessibility to underlying data.