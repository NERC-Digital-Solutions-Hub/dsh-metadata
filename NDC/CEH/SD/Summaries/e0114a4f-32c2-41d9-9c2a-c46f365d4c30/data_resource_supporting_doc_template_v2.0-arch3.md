# Emissions of Ammonia (NH 3 ) from Agriculture in South Asia in 2015.

- Overview
  - A gridded, bottom-up inventory of annual NH3 emissions from agricultural sources in SAARC for 2015.
  - Spatial resolution: 0.1° x 0.1°; domain covers Afghanistan, Bangladesh, Bhutan, India, Maldives, Nepal, Pakistan, and Sri Lanka.
  - Five agricultural sub-sectors: crop residue burning, crop residues left in fields, livestock management, livestock grazing and manure applications, application of synthetic fertilisers.
  - Methods align with EDGARv6.1, IPCC 2006/2019 Guidelines, and EMEP/EEA guidebooks to improve region-specific NH3 representation.

- Spatial and temporal scope
  - Temporal coverage: annual emissions for the year 2015.
  - Spatial coverage: SAARC region; cells outside the specified countries set to NA.
  - Coordinate reference: WGS84.

- Data format and structure
  - File format: GeoTIFF.
  - File naming conventions correspond to sub-sector: CRB (crop residue burning), CRR (crop residues left in fields), GRM (livestock grazing and manure), MNM (livestock management), SFA (synthetic fertilisers).
  - Units: grams of NH3 flux per square meter per year (g m^-2 yr^-1).
  - No-data values indicated as NA.

- Sub-sectors and emission processes
  - NH3_CRB_SouthAsia_2015_gm2_0.1.tif: emissions from burning crop residues (with country-specific burnt crop sets).
  - NH3_CRR_SouthAsia_2015_gm2_0.1.tif: emissions from crop residues left in the field.
  - NH3_GRM_SouthAsia_2015_gm2_0.1.tif: emissions from livestock management and manure handling.
  - NH3_MNM_SouthAsia_2015_gm2_0.1.tif: emissions from housing, storage, and management of manures/slurries, and yarding.
  - NH3_SFA_SouthAsia_2015_gm2_0.1.tif: emissions from synthetic fertiliser application.

- Input data and data sources
  - Crop distributions and harvest data (EarthStat; FAOSTAT 2023; state-level data for India and Nepal).
  - Crop residue data and parameters; soil and crop yields by country and crop.
  - Fertiliser usage by type and country totals (FAOSTAT 2023); fertiliser nitrogen content (FAOSTAT 2023).
  - Livestock data: populations, distributions, management practices (FAOSTAT 2023; global livestock distributions).
  - Soil data: topsoil pH (Batjes et al., 2024).
  - Emission factors and methodologies drawn from: EDGARv6.1; IPCC 2006 Guidelines; IPCC 2019 Refinement; EMEP/EEA guidebooks (2019, 2023); and various referenced studies (e.g., emission factors for fertilisers and livestock, crop burning literature).

- Methodology and calculation approach
  - Bottom-up calculations combining activity data with emission factors (EFs) per sector.
  - Burning: crop burnt fractions and EF mean values from multiple sources; crop-specific burnt sets per country.
  - Crop residues left in field: EF determined by EEA Guidebook (2023) based on above-ground biomass and N content; distribution onto EarthStat crops.
  - Livestock emissions: nitrogen-flow (N-flow) approach; excretion rates by livestock type; emissions distributed by country and livestock type across relevant management stages.
  - Synthetic fertilisers: total N application per country; spatially distributed N application by crop type; conversion to NH3 using fertiliser-type EF and soil pH dependencies; updates to Urea EF.
  - Data are reweighted to align with FAOSTAT national totals and country-specific data where available.

- Quality control and validation
  - Extreme value checks and NA-value checks.
  - Sectoral totals calculated and sense-checked; spatially distributed to GeoTIFFs; cross-validated against non-spatial calculations and compared with other NH3 agriculture emissions estimates.

- Data governance, sharing, and applicability
  - Data are generated to incorporate region-specific information and improve accuracy over generic inventories.
  - Notes on data sharing: underlying data and metadata handling can pose barriers; data governance and openness are addressed, with explicit reference to sharing requirements and quality standards.

- Relevance for monitoring frameworks
  - Demonstrates a transparent, multi-source, bottom-up approach aligned with established global methodologies (EDGAR, IPCC, EMEP/EEA), suitable for monitoring environmental health and informing policy decisions.
  - Highlights the integration of sub-national data (e.g., state-level fertiliser use, country-specific emission factors) to reduce regional biases.
  - Provides a template for sectoral disaggregation (burning, field residues, livestock, and fertilisers) to track policy impacts and target mitigation strategies.

- Key references (selected)
  - EDGAR v6.1 methodology; IPCC 2006 and IPCC 2019 guidelines; EMEP/EEA guidebooks 2019 and 2023.
  - Supporting datasets and regional studies for crop residue burning, fertiliser use, livestock distributions, and soil data (e.g., FAOSTAT, EarthStat, Batjes et al. 2024; Jain et al.; Lin & Begho; Yosh references listed in the document).