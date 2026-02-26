# Turf2Surf WP2 Supporting documentation for data

- The Turf2Surf project examines coupled nutrient cycling in terrestrial and freshwater ecosystems, focusing on nitrogen and phosphorus impacts on carbon exchange between land and atmosphere, with implications for water quality, carbon sequestration, and biodiversity.
- Aims aligned with policy-informed monitoring: identify environmental health measures, document data collection, and support data-driven decision making.

## 1.0 Information about the Conwy catchment
- Location: North Wales, ~500 km2 catchment with diverse landscapes enabling comparative study.
- Objectives: understand ecological, biogeochemical, and hydrological processes from gene to landscape scale; assess how pressures affect natural resources and benefits.
- Features: strong climatic gradient; varied habitats (blanket bogs, moorlands, woodlands, grasslands, lakes, estuary); mix of land uses (agriculture, forestry, water supply, conservation, recreation).
- Stakeholders: water industries, shell fisheries, farmers, foresters, tourism, conservation groups, local communities.
- Extensive baseline data available for cross-project use.

## 2.0 Habitats and sampling sites
- Site overview: 17 sites with multiple plots across a broad habitat types; site numbers and plots associated with dominant plant species.
- Examples of habitats: blanket bogs, acid grasslands, conifer and broadleaf woodlands, hay meadows, improved/improved grasslands, montane communities.
- Sampling focus: aboveground biomass and soil cores across habitats to capture plant and soil variability.

## 3.0 Plant and soil data components and methods

- 3.1.1 Aboveground net primary productivity (NPP) and standing biomass
  - Data responsibility: Simon Smart.
  - Temporal coverage: 2013–2015 across dominant species; winter clipping with grazing exclusion where applicable; biomass estimates per habitat.
  - Biomass calculations: herbaceous biomass in 1 m x 1 m plots; woodland biomass via tree cores and allometric estimates; combines with litter measurements.
  - Policy relevance: provides baseline NPP and biomass inputs for ecosystem carbon models.

- 3.1.2 Plant photosynthesis measures
  - Data responsibility: Lina Mercado.
  - Parameters: Vcmax, Jmax, Asat (leaf-level photosynthesis metrics) measured on dominant species using CO2-response curves and field/bench measurements; temperature and CO2 corrections applied; modeling to estimate parameters (Farquhar model) with data processing scripts (GitHub link provided).
  - Policy relevance: informs photosynthetic capacity and carbon gain under varying environmental conditions for ecosystem models.

- 3.1.3 Leaf traits and plant community traits
  - Data responsibility: Lina Mercado, Simon Smart.
  - Traits: leaf N and P, leaf dry matter content (LDMC), specific leaf area (SLA), leaf mass per area (LMA), canopy height, bryophyte cover.
  - Methods: leaf area and mass measurements; element analyses (N, P) via standard lab procedures.
  - Policy relevance: trait data improve understanding of resource use strategies and model parameterization (e.g., for JULES).

- 3.2.1 General soil measures
  - Data responsibility: Helen Glanville.
  - Sampling: intact cores from 17 habitats; depth profile to 1 m; analyses include soil water content, bulk density, LOI/LOI-C, pH, EC, total C and N.
  - QA/QC: formal QA/QC procedures; data linked to Turf2Surf integration with soil-plant processes in models.

- 3.2.2 Phosphorus
  - Data responsibility: Helen Glanville.
  - Fractions and methods: Olsen P; Root-P (CaCl2 extraction); Complex-P (10 mM citrate); Enzyme-P (phosphatase and phytase); Protons P (1 M HCl) for recalcitrant P; all measured by colorimetric Malachite Green method.
  - Policy relevance: comprehensive P pool characterization to inform nutrient management and soil fertility monitoring.

- 3.2.3 Available carbon and nitrogen
  - Data responsibility: Helen Glanville.
  - Methods: soil extraction with 0.5 M K2SO4; analyses for DOC and TDN via appropriate instrumental methods; nitrate and ammonium quantified by colorimetric/enzymatic assays.
  - Policy relevance: immediate indicators of soil C and N availability linked to soil fertility and ecosystem functioning.

- 3.2.4 Soil available cations (Ca, Na, K)
  - Data responsibility: Helen Glanville.
  - Method: extraction with 0.5 M acetic acid; cation concentrations measured with flame photometry.
  - Policy relevance: informs soil fertility status and nutrient accessibility for plants.

- 3.2.5 Root biomass
  - Data responsibility: Helen Glanville.
  - Measurements: total and fine root biomass via soil cores; root scanning (WinRhizo) for architecture; dry weight estimates; in-growth root cores to assess production.
  - Policy relevance: belowground carbon and nutrient pools, important for holistic monitoring of soil-plant interactions.

- 3.2.6 Soil elements – TXRF
  - Data responsibility: Helen Glanville.
  - Method: TXRF analysis of ground soil samples for multi-element profiling (Al, Fe, Ca, K, etc.); sample prep and calibration described; limitations discussed in accompanying notes.
  - Policy relevance: broad elemental baselines to support mineral nutrient status and biogeochemical studies.

## 4.0 Dataset structure
- Data files: five CSVs
  - Turf2Surf_Plant_biomass_data.csv
  - Turf2Surf_Plant_structural_data.csv
  - Turf2Surf_Plant_physiological_data.csv
  - Turf2Surf_Soil_Carbon_data.csv
  - Turf2Surf_Soil_raw_data.csv
- Common structure across files:
  - Site number (Table 1 mapping)
  - Habitat and habitat description
  - Site name
  - Ecosystem component (plant, soil, roots)
  - For plants: species information; otherwise NA
  - Plot number (1–4) and replicate number
  - Soil depth interval for soil and roots
- Data quality: missing values marked as NA due to depth limitations, limited replicates, or restricted access; data governance and responsible personnel are documented per dataset (e.g., 3.1.x sections).

## Data governance and policy-relevant considerations for monitoring frameworks
- Clear assignment of data responsibilities for each data domain, supporting accountability and traceability.
- Data provenance and methodological transparency enable replication and comparison across programs.
- Data sharing and openness are addressed via public sharing of underlying data and links to data processing scripts (e.g., GitHub for photosynthesis modeling).
- The collection spans multiple habitats and scales (plot-level to landscape), supporting policy-relevant indicators of nutrient cycling, carbon balance, and biodiversity responses.
- Documentation of data limitations (e.g., TXRF limitations, depth/replicate constraints) informs interpretation for monitoring and decision-making.