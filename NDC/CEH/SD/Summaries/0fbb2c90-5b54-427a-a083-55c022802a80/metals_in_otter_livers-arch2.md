# Otter Collection and Post Mortem Examination.

- Purpose and scope
  - Describes a study of otter liver tissue to assess environmental metal exposure over time.
  - Uses 278 liver samples from otters that died 2006–2017, as a stratified random sub-sample primarily from England and Wales (with 3 from Scotland).
  - Aims to relate metal accumulation to environmental context using standardized data and spatial modelling.

- Data collection and sample handling
  - Otters are submitted by local authorities, environmental organisations, and the public; each sample has a National Grid Reference and collection date.
  - Post-mortem examination follows a standard protocol; phenotypic data recorded include sex, length, weight, and age class to derive a condition score (scaled mass index, sSMI) per Peig & Green (2009).
  - Tissue samples (including liver) are retained and archived at -20°C prior to analysis.
  - Otters are categorized by age (juvenile, sub-adult, adult) and a subset with complete metadata is used for analysis.

- Analytical methods
  - Liver concentrations of 13 elements measured: Ag, As, Cd, Cr, Co, Cu, Fe, Hg, Mn, Mo, Ni, Pb, Se, Zn.
  - Two 1 g subsamples per otter liver: one for acid-digestion and ICP-MS analysis; the other for dry matter determination (18 h at 105°C).
  - Results expressed as μg/g dry weight; not recovery corrected but with consistent recoveries across periods; methods are validated and align with established trace-element protocols.
  - Batch-wise reporting includes detailed laboratory metadata (e.g., which metals are measured per batch).

- Spatial data integration and environmental context
  - Compiles spatial data on stream/soil biochemistry, weather, and anthropogenic contaminant sources from multiple sources.
  - A map of predicted nanosilver concentrations in surface water is included, derived from a model of household loadings to rivers.
  - Spatial data are mapped in ArcGIS (ArcMap 10.4.1) as continuous rasters or points.
  - Otter exposure area defined as a 20-km-diameter circle centered on each carcass (midpoint of the otter’s 5–40 km riverine range), from which environmental variables are extracted.
  - Geospatial Modelling Environment (GME) is used to extract data for each otter area; variables summarized as means (e.g., soil elements, soil pH, sediment elements, stream pH, rainfall, predicted nAg) or sums (e.g., number of consented discharges, annual metal mass inputs to controlled waters, etc.).
  - Distances to coast calculated via river networks; otters outside the river-coast zone (N=4) excluded due to uncertain relevance to river catchments.
  - Specifics include integration of numerous data layers: geological elements, soil chemistry, pH, sediment chemistry, nanoparticle predictions, mining presence, discharges, metal fluxes, population density, and rainfall.

- Otter selection and geographic considerations
  - Location data snapped to a 1:50,000 watercourse network; RivEx used to compute the shortest distance to coast along rivers.
  - 4 otters excluded from scoring due to uncertain river catchment relevance.
  - The study acknowledges otter home-range considerations by centering analyses on a 20-km-diameter circle around each carcass.

- Variables and data sources
  - Data table includes a wide range of environmental and biological variables (soil, sediment, water pH, metal concentrations, mining indicators, discharges, metal inputs, nanosilver, population density, rainfall).
  - Variables are linked to primary sources such as BGS G-BASE geological data, environmental agencies, UK weather/climate datasets, and population statistics.
  - Notes clarify data column meanings (e.g., units, methods, data availability) and reflect the integrated approach to linking otter metal burdens with environmental context.

- Data management and outputs
  - Emphasizes standardized data collection, careful QA of sample collection and processing, and the creation of a harmonized dataset for downstream analysis.
  - The approach supports monitoring and policy evaluation by enabling correlation of otter liver metal burdens with environmental exposure metrics across a defined geographic and temporal scope.
  - Outputs include a structured dataset of metal concentrations in otter livers and a rich set of environmental covariates mapped to each otter’s catchment area.