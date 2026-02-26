# Ozone flux, dynamic global vegetation, and carbon storage modelled data of tropical forests using the Joint UK Land Environment Simulator (JULES), 1900-2015

- Purpose and scope
  - A spatially-explicit dataset (1900–2015) modelling the ozone (O3) impact on tropical forests using JULES v5.6.
  - Includes extant, current-secondary, and potential-secondary forest extents, plus preindustrial (1900–1910) and recent (2005–2014) mean O3 concentrations at 1.25° x 1.875° resolution.
  - Outputs the modeled impact of O3 on tropical forest net primary productivity (NPP) under current O3 and the cumulative impact on the global carbon cycle from 1900–2014.
  - Built to support understanding of O3 effects on tropical vegetation and carbon storage, and to be interpreted alongside empirical O3 susceptibility data for tropical trees (Trop-Oz project).

- Modelling framework
  - Uses JULES v5.6, a land-surface model that simulates soil-vegetation-atmosphere interactions with spatially explicit meteorology and O3 inputs.
  - Incorporates vegetation responses to atmospheric composition (CO2, aerosols, O3) and interactions with temperature, drought, and nutrient cycling.
  - O3 damage scheme modifies net photosynthesis (Anet) and stomatal conductance (gs) via an O3-damage factor (F), with F depending on a sensitivity parameter (α) and a flux threshold (y).
  - Equations (conceptual): F reduces Anet and gs as O3 flux exceeds threshold; A_mod = Anet × F; g_mod = gs × F.

- Calibration of O3 susceptibility
  - Tropical broadleaf evergreen PFT (BET-Tr) calibrated to three observed O3 susceptibilities: low, moderate, high.
  - α values adjusted to match annual NPP (2009–2011) with dose–response functions (DRFs) for biomass decline.
  - For other tropical PFTs, α values are set by analogy (e.g., C3 grasses to trees; C4 grasses to Saccharum spontaneum).

- Simulation design and forcing
  - Pan-tropical simulations from 1900-01-01 to 2014-12-31 with homogeneous O3 susceptibility levels (low, moderate, high).
  - Dynamic vegetation, varying CO2, land-use/land-cover changes (as in Global Carbon Budget 2020).
  - Forcing from CRU-JRA v2.3 meteorology; O3 inputs from UKESM1 (CMIP6 historical) for both fixed (1900–1909) and transient (1900–2014) scenarios.
  - 1000-year spin-up (1900–1920) with climatology cyclically repeated; comparisons focus on differences between fixed and transient O3 scenarios.

- Impacts assessed and outputs
  - Impacts of changing O3 over the 20th century on current pan-tropical NPP (2005–2014 mean) for BET-Tr, weighted by present forest extent (ESA CCI).
  - Time series of total terrestrial carbon pools (vegetation and soils) for fixed vs transient O3, incorporating NPP declines, vegetation dynamics, and soil biogeochemistry.
  - Evaluation of potential impacts on nature-based climate solutions (secondary forest regrowth and restoration) using the same O3 susceptibility spectrum, regridded to JULES resolution.
  - Outputs include NPP declines and percentage changes by forest type, and annual changes to carbon stocks.

- Data structure and accessibility
  - Deposited as 19 gridded data files at 1.25° x 1.875° resolution and multiple CSV summary files.
  - Forest cover and area data (current, secondary, and potential forest) plus grid area (m2).
  - O3 concentrations: preindustrial (1900–1909), present-day (2005–2014), and O3_change between the two.
  - Future O3 predictions by SSP2050 scenarios (SSP_2050.csv) and regional O3 projections by forest type.
  - Calibration and output files for NPP declines under different susceptibilities (JULES_susceptibility.csv; Low_NPP, Mod_NPP, High_NPP and their percent changes).
  - Accumulated carbon impacts (Delta_carbon.csv) by year, detailing vegetation and soil changes for each susceptibility level.
  - Forest-type specific NPP declines by day for each susceptibility level (Forest_types_NPP_Low/Mod/High.csv).
  - Data quality checks referenced against prior JULES CMIP6 applications.

- Quality, validation, and provenance
  - Outputs subjected to quality control by comparison with previous JULES runs used in CMIP6.

- Relevance for environmental monitoring and policy analysis
  - Provides a standardised, spatially explicit framework to monitor ozone-driven effects on tropical forest productivity and carbon storage over a century.
  - Enables policy performance assessment by comparing modeled outputs under different O3 exposure scenarios and susceptibilities.
  - Facilitates integration with other environmental datasets for broader health and resilience analyses, aligning with monitoring best practices of data verification, standardised analysis, and clear presentation.

- References and data provenance
  - Documents model description, calibration approaches, and supporting literature for JULES, ozone damage pathways, and tropical vegetation responses.
  - Related data and methods draw on CMIP6, CRU-JRA meteorology, ESA CCI forest extents, and published Trop-Oz empirical studies.