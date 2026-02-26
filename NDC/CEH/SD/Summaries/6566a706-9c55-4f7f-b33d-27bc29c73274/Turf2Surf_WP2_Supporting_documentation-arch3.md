# Turf2Surf WP2 Supporting documentation for data

- Focus and purpose: Documentation of WP2 activities on linking plant and soil nutrients to ecosystem processes, with the aim of informing models (e.g., JULES) and providing datasets on coupled nitrogen and phosphorus cycling, carbon exchange, water quality, and biodiversity in terrestrial and freshwater systems.

- Project scope and contributors: Turf2Surf project members across CEH, Bangor University, Exeter University; authors Sabine Reinsch (corresponding), Helen Glanville, Simon Smart; version history dating 2016.

- Study area at a glance: Conwy catchment in North Wales (~500 km2) with a strong climatic gradient and diverse habitats (bogs, moorland, forestry, grasslands, lakes, reservoirs, floodplains, salt marsh). Stakeholders include water utilities, agriculture, forestry, conservation groups, and local communities. The catchment supports integrated ecological, biogeochemical, and hydrological studies from gene to landscape scale.

- Habitats and sampling design: Sampling across multiple habitats and sites (e.g., blanket bog, heaths on bog, conifer woodland, deciduous woodlands, oakwoods, grasslands, montane communities, arable and improved/grain habitats). 17 soil habitats sampled across numerous sites with varied plot replication; site descriptions include dominant vegetation and habitat type.

- Key measurement streams and data produced:
  - 3.1.1 Aboveground net primary productivity (NPP) and standing biomass
    - Annual NPP measured for dominant species at all sites (2013–2015); 4 plots per site representing main species; winter clipping with grazing exclosures where applicable.
    - Aboveground biomass measured at 10 of 17 sites (3–9 replicates per habitat), with distinct methods for grassland/bog versus woodland (tree cores, 200 m2 plots, and biomass calculations).
    - Linking to ecosystem processes and integration with JULES through Turf2Surf WP2.
  - 3.1.2 Plant photosynthesis measures
    - Parameters measured: Asat, Vcmax (25°C), Jmax (25°C) for dominant species; field measurements with CIRAS-I and LICOR 6400 across CO2 curves (50–2000 ppm) and 20°C leaf temperature.
    - Temperature corrections to 25°C using established functions; modelling scripts available (GitHub) to fit Farquhar-based models.
  - 3.1.3 Leaf traits and plant community traits
    - Traits measured: leaf N and P (%), leaf dry matter content (LDMC), specific leaf area (SLA), leaf mass per area (LMA), canopy height, bryophyte cover.
    - LMA via leaf area and dry weight; N and P via chemical analyses; SLA derived as inverse of LMA.
    - Leaf sampling around measurement area; data processed to support ecosystem trait analyses and JULES parameterization.
  - 3.2.1 General soil measures
    - Intact soil cores collected to 1 m depth across 17 habitats; sub-sampling by depth (0–15 to 90+ cm) for SWC, BD, LOI, LOI-C, pH, EC, and total C/N via elemental analysis; QA/QC in place; data processed collaboratively.
  - 3.2.2 Phosphorus
    - Olsen P, root-P, complex-P, enzyme-P, and related fractions measured with colorimetric Malachite Green methods; detailed extraction protocols (Olsen P, CaCl2-extractable P, citrate extractable P, enzyme-associated P) to reflect plant/microbial mineralization and rhizosphere dynamics.
  - 3.2.3 Available carbon and nitrogen
    - DOC and TDN measured; NO3 and NH4 analyzed via established colorimetric/vanadate and salicylate-nitroprusside methods; 0.5 M K2SO4 extraction for available C/N.
    - Methods include QA steps and sample handling protocols.
  - 3.2.4 Soil available cations (Ca, Na, K)
    - 0.5 M acetic acid extraction followed by flame photometry; QA steps and standard curves documented.
  - 3.2.5 Root biomass
    - Standing root biomass via 15 cm soil cores, separation into coarse/fine roots; WinRHizo scanning for root architecture metrics; dry weight calculations; in-growth root cores to assess root growth dynamics; linked to aboveground biomass for total carbon/nutrient budgeting.
  - 3.2.6 Soil elements – TXRF
    - Total elemental analysis (Al, Fe, Ca, K, Ti, S, Mn, P, Zn, etc.) by TXRF on 17 sites; meticulous sample prep (drying, grinding, dispersion on discs) and internal standards; limitations acknowledged in a dedicated file.
    - Data processing, lab work, and calculations described; linked to broader nutrient analyses for JULES parameterization.

- Dataset structure and contents:
  - Five data files covering biomass, structure, physiological traits, soil carbon, and raw soil data.
  - Common schema: Site number, Habitat and detailed habitat description, Site name, Component (Plant, Soil, Roots), Species (for plants; NA otherwise), Plot number, Replicate number, and Soil depth interval (for Soil/Roots components).
  - Missing values indicated as NA to reflect restricted depths, limited replicates, or outliers.
  - Dataset designed to support integration with JULES and other ecosystem models; documentation notes the need to link plant and soil nutrients to above/belowground processes.

- Data processing, modelling, and governance:
  - WP2 explicitly aims to incorporate measured parameters into the JULES land-surface model; detailed data processing workflows for photosynthesis and related traits are documented, with scripts available (e.g., FitFarquharModel) to facilitate model parameterization.
  - Metadata, QA/QC, and data management are emphasised; originators of datasets are identified as data responsible persons, and collaboration across institutions supports data quality and openness.
  - The documentation notes that some analyses rely on separate methodology documents, and there are explicit references to limitations and caveats (e.g., TXRF limitations).

- Versioning and authorship:
  - Version dates included: 01/06/2016, 25/08/2016, 04/11/2016.
  - Authors listed: Sabine Reinsch (corresponding), Helen Glanville, Simon Smart, among others; data responsibilities attributed to specific team members for each measurement domain.

- Data accessibility and contact:
  - Data are organized into clearly named CSV files; the document specifies data responsibilities and responsible contacts for each measurement area, enabling governance, reuse, and potential data sharing with appropriate metadata.