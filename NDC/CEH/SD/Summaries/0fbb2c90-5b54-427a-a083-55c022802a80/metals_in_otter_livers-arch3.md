# Otter Collection and Post Mortem Examination

- Purpose and scope
  - Otter carcasses are submitted by local authorities, environmental organisations, and the public to Cardiff University Otter Project.
  - For each otter, location and collection date are recorded; otters undergo a standard post-mortem examination collecting phenotypic data (sex, length, weight, age class) and deriving a condition score.
  - Liver tissue is retained for analysis; this study analysed 278 liver samples from otters that died between 2006 and 2017, a stratified random sub-sample predominantly from England and Wales, with three animals found in Scotland.

- Biological sampling and laboratory analysis
  - For each otter: all the following were recorded or derived — sex, age class (juvenile, sub-adult, adult), year found, body weight, body length, and a scaled mass index as a condition proxy.
  - Tissue handling: liver samples stored at -20°C prior to analysis; two 1 g subsamples were used per otter.
    - Subsample 1: acid-digested and analyzed for trace elements using inductively coupled plasma mass spectrometry (ICP-MS).
    - Subsample 2: used to determine dry matter content via oven-drying (105°C for 18 hours).
  - Elemental concentrations are reported on a dry weight basis (μg/g) and are not recovery corrected; analysis spanned 2009, 2011, and 2017 with method refinements over time.
  - Metals measured in liver include a broad panel: Ag, As, Cd, Cr, Co, Cu, Fe, Hg, Mn, Mo, Ni, Pb, Se, Zn, plus additional elements such as Al, Sr, Sb, etc. The dataset includes a wide range of metals and some non-metal parameters.

- Spatial data and environmental context
  - Spatial variation in environmental contaminants and context variables were compiled from multiple sources (streams, soils, weather, anthropogenic sources).
  - A predicted nanosilver concentration layer in surface water was generated from a model incorporating household loadings, sewer connectivity, treatment plants, dilution, downstream transport, rainfall, and sedimentation.
  - All spatial data were mapped in ArcGIS (ArcMap, v10.4.1) as continuous rasters or points.
  - Otter exposure area: each otter was assumed to have a potential 20-km-diameter circular home-range around the carcass location (midpoint of the otter’s linear range along watercourses varied 5–40 km). This area was used to extract environmental covariates.
  - For each otter-area, a suite of geological and anthropogenic variables was summarized (as mean or sum values) and used as potential exposure indicators.
  - Distances and geography:
    - Distance from otter carcass to the coast calculated via the river network; otters located beyond the relevant catchment (N=4) excluded from scoring due to uncertainty about riverine linkage.
    - River mouth distance computed with RivEx to test potential diet- and habitat-related differences in metal accumulation.

- Table of data sources and variables
  - A comprehensive table (Table 1) lists the geological and anthropogenic contaminant data used, including:
    - Soil elements, soil carbon, soil pH (with resolutions and time periods)
    - Sediment elements and sediment pH
    - River/stream pH
    - Predicted silver nanoparticle concentrations in surface water
    - Past and present mining sites within 10 km
    - Consented discharges to controlled waters (and related proxies for urban/industrial density)
    - Annual mass inputs of metals to controlled waters
    - Human population density
  - Data are described with units, spatial resolution, time period, and references (e.g., BGS G-BASE, CEH soil maps, NAEI, Met Office datasets, etc.).
  - Abbreviations and column definitions are provided (e.g., UWCRef as otter casualty identifier, DM as dry matter content, nA/ND/NA as applicable/not detected, etc.).

- Data handling, quality, and governance
  - Data integration combines biological measurements with extensive environmental covariates across multiple sources and time periods.
  - Quality and interpretation depend on metadata completeness, cross-dataset compatibility, and consistent data processing (e.g., standardizing units to μg/g dry weight for liver metals; consistent covariate summarization within 20-km buffers).
  - The document notes the presence of missing data indicators (NA) where data could not be extracted or analyzed for a given area or sample, and ND for not detected in analytical results.

- References and sources
  - The study cites a wide range of methodological and data sources (genetic, geochemical, environmental, and modelling references) to support sample analysis, spatial data processing, and environmental covariate construction.