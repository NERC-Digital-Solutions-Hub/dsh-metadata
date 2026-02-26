# Turf2Surf WP2 Supporting documentation for data

- Purpose and scope
  - The Turf2Surf project investigates coupled nutrient cycling in terrestrial and freshwater ecosystems and links nitrogen and phosphorus impacts on carbon exchange between land and atmosphere.
  - WP2 focuses on nitrogen and phosphorus related impacts on carbon exchange, generating baseline data across a Welsh catchment to support ecosystem process understanding and modeling in JULES.

- Study area and data scope
  - Conwy catchment in North Wales (~500 km2) with diverse habitats and a strong climatic gradient; extensive baseline data across multiple plant and soil parameters.
  - 17 soil habitats/sites sampled (sites 1-10, 14-21), with 1-3 or more plots per habitat; various habitats including blanket bog, moorland, woodlands, grasslands, lakes, reservoirs, and arable land.
  - Data collection spans plant measures (biomass, NPP, photosynthesis, leaf traits) and soil chemistry (C, N, P pools, available nutrients, cations, root biomass) and elemental composition (TXRF).

- Data assets and structure
  - Five main data files
    - Turf2Surf_Plant_biomass_data.csv
    - Turf2Surf_Plant_structural_data.csv
    - Turf2Surf_Plant_physiological_data.csv
    - Turf2Surf_Soil_Carbon_data.csv
    - Turf2Surf_Soil_raw data.csv
  - Common structure and fields
    - Site number (links to Table 1)
    - Habitat and detailed habitat description
    - Site name
    - Ecosystem component (Plant, Soil, Roots)
    - For plants: species details; for soil/roots: NA
    - Plot number (1–4) and Replicate number (where measurements are co-located or allocated by dominant species)
    - Soil depth interval for Soil and Roots components
  - Missing values indicated as NA
  - Abundant metadata on measurement contexts and data provenance

- Key data collection and processing domains
  - Aboveground net primary productivity (NPP) and standing biomass (3.1.1)
    - Annual NPP measured 2013–2015 for dominant species across four plots per site
    - Winter clipping and, where applicable, grazing exclusion via wire cages
    - Biomass allometries and site-specific adjustments for life strategies
  - Plant photosynthesis measures (3.1.2)
    - Vcmax, Jmax, and Asat for dominant species
    - Field and lab measurements using CIRAS-I and Licor 6400 across CO2 regimes
    - Data processing via Farquhar-based models; temperature corrections to 25°C
    - Code and workflow references available (e.g., GitHub: mdekauwe/FitFarquharModel)
  - Leaf traits and plant community traits (3.1.3)
    - Leaf N, Leaf P, LDMC, SLA, LMA, canopy height, bryophyte cover
    - Leaf traits measured on 10 leaves per sampled area; LMA via image analysis; N and P via standard chemical methods
  - General soil measures (3.2.1)
    - Intact soil cores to 1 m depth; cores split into depth intervals
    - Analyses: soil water content, bulk density, LOI and LOI-C, pH, EC, total C and N
  - Phosphorus pools and related measures (3.2.2)
    - Olsen P, Root-P, Complex-P, Enzyme-P, Protons-P across multiple extraction schemes
    - Colorimetric malachite green method; standard curves and QA/QC
  - Available carbon and nitrogen (3.2.3)
    - DOC and TDN measured from 0.5 M K2SO4 extracts; detailed spectrophotometric and QA/QC steps
  - Soil available cations (3.2.4)
    - Ca, Na, K extracted with 0.5 M acetic acid; concentrations determined by flame photometry
  - Root biomass and growth (3.2.5)
    - Total and fine root biomass via soil cores; WinRhizo analysis for morphology; in-growth root cores to assess root growth
  - Soil elements via TXRF (3.2.6)
    - Comprehensive elemental analysis (Al, Fe, Ca, K, etc.) on 17 sites; TXRF with sample prep and internal standards; lab work and data analysis described; limitations discussed in Turf2Surf_WP2_TXRF_Limitations_Glanville.rft

- Data quality, standards, and governance
  - Methods and QA/QC notes included for laboratory analyses, calibration ranges, and reference materials
  - TXRF limitations documented in a dedicated file
  - Data are intended to be integrated into JULES and related analyses; explicit links to modeling workflows and code (e.g., NPP processing, photosynthesis modeling)
  - Versioned documentation with multiple release dates (01/06/2016; 25/08/2016; 04/11/2016)
  - Data responsible individuals listed for each data domain (e.g., Simon Smart for NPP, Lina Mercado for photosynthesis and leaf traits, Helen Glanville for soils and TXRF)
  - Authors and corresponding author identified (Sabine Reinsch; correspondence details)

- Dataset usage, accessibility, and reuse considerations
  - Dataset designed for cross-site comparison and for informing framework parameters in process-based models (e.g., JULES)
  - Clear mapping between site/habitat, plot, replicate, and depth interval to support stratified analyses
  - Documentation provides guidance on data processing steps and scripts to reproduce analyses
  - Potential users should refer to methodology notes and linked code repositories for reproducibility
  - Data may support assessments of nutrient cycling, carbon fluxes, and land-management implications across diverse Welsh habitats

- Provisions for collaborators and future work
  - Strong emphasis on linking plant and soil nutrient data to ecosystem processes
  - Collaboration across researchers and institutions (CEH, Bangor University, Exeter University) to enhance data breadth and integration
  - Encouragement of data sharing and cross-network collaboration to strengthen data assets and community of practice

- Abbreviations and glossary
  - Includes definitions for Asat, BD, Jmax, C, LDMC, EC, JULES, LMA, LOI, LOI-C, N, NH4, NO3, aNPP, P, SLA, SWC, Vcmax
  - References provided for foundational methods and models (Farquhar et al., De Kauwe et al., Medlyn et al., Kattge & Knorr)