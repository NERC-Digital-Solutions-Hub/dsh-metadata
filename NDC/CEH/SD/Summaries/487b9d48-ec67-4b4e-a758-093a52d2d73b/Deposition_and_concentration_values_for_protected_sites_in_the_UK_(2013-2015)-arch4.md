UK Acidifying and Eutrophying Atmospheric Pollutants Supporting information

Overview
- Describes two modelling approaches used to map deposition and concentrations affecting UK protected sites (SAC, SPA, SSSI):
  - CBED Modelling: deposition of sulphur, oxidised/reduced nitrogen, and base cations at 5x5 km resolution, with wet and dry deposition processes and ecosystem-specific applications.
  - PCM Modelling: background pollutant concentrations on 1x1 km grids (and road-side values) for multiple pollutants, for policy support and exposure assessment.
- Spatial focus: deposition and concentrations are aligned with UK protected site boundaries, using grid-based mapping and site aggregation.
- Temporal focus: results are presented as rolling 3-year means, based on 2013–2015 data, with annual calculations smoothed over three years.

Modelling approaches and outputs
- CBED Modelling
  - Generates 5x5 km resolution maps of wet and dry deposition for sulphur, oxidised nitrogen, reduced nitrogen, and base cations.
  - Data inputs: measured gas/ PM concentrations and precipitation-derived ion concentrations from the UKEAP network; wet deposition incorporates precipitation plus occult deposition; dry deposition uses habitat-specific deposition velocities for five land-cover categories (forest, moorland, grassland, arable, urban).
  - Wet deposition includes an orographic enhancement factor in upland regions.
  - Outputs are annual values, summarized as 3-year means (2013–2015), and provided in three ecosystem scenarios: moorland/short vegetation, forest/woodland, and grid average.
  - Exceedance calculations (e.g., critical loads) apply moorland or forest deposition depending on habitat type.
- PCM Modelling
  - Produces background pollutant concentration maps on a 1x1 km grid, plus around 9,000 road-side values.
  - One model per pollutant (e.g., NOx, NO2, SO2, PM10, PM2.5, etc.), with a base year and projection runs.
  - Supports policy development, population exposure assessments, and TEN (Time Extension Notification) applications.
  - Outputs are used alongside CBED results for comprehensive exposure and deposition assessment.

Step-by-step data preparation and integration
- Step 1: Spatial mapping
  - Use Feature Manipulation Engine (FME) to create a UK-wide 5x5 km grid.
  - Clip grids to boundaries of SAC/SPA/SSSI and merge with 3-year CBED outputs (2013–2015) to produce a UK protected sites CBED dataset.
  - For NOx and SO2, generate concentration datasets from PCM outputs (1x1 km grids) and clip/aggregate to protected sites.
  - Data sources for site and boundary information include JNCC and national sites’ websites.
- Step 2: Deriving deposition/concentration statistics for each site
  - SQL queries compute minimum, maximum, and grid-averaged deposition/concentration values for each protected site.
  - Grid-average calculation: grid-square area weighting (GridArea/TotalSiteArea) times the CBED deposition value, then summed across the site.
  - Outputs include site-level deposition and concentration values aligned to SAC/SPA/SSSI boundaries and 5x5 km grid squares.

Nature and units of recorded values
- Deposition
  - All deposition values are expressed as kilo-equivalents per hectare per year (keq ha-1 year-1).
  - Conversion to kg S ha-1 year-1 or kg N ha-1 year-1 is possible by multiplying by factors: 16 for S, 14 for N.
  - Separate components: NH3/NH4 (reduced N), NO2/NO3 (oxidised N), SO2/SO4 (non-marine S) for forest and moorland contexts.
- Concentrations
  - Concentrations are expressed as micrograms per cubic metre (µg m-3) for pollutants like NH3, NOx, and SO2.
- Data structure and datasets
  - The project provides a comprehensive set of 3-year mean data and derived statistics (minimum, maximum, grid-average) at 5x5 km and 1x1 km resolutions, for multiple pollutants and habitat types.
  - Outputs are organized per site (SAC/SPA/SSSI) with site metadata (site code, name, area, centroid coordinates, grid overlap, designation, year) and pollutant-specific fields (deposition or concentration values by ecosystem type or grid average).

Quality control and data governance
- Quality assurance and validation
  - CBED methods have undergone extensive peer review and model inter-comparison exercises (e.g., Carslaw 2011).
  - Procedures for documenting method developments, version control, and central storage are followed.
  - CBED and PCM results are published in peer-reviewed literature; mass-balance checks are routinely performed to ensure numerical consistency and coherence with previous years.
- Metadata and standardization
  - Clear definitions of units, dataset structure, and the description of each field (e.g., SITECODE, GRIDAREA, YEAR, NH3_NH4_FOREST) are provided to support consistent interpretation and reuse.
  - Data are produced as rolling 3-year means to smooth inter-annual variability inherent to weather patterns and emissions.

Implications for data strategy and use
- For data leaders, the document highlights:
  - The value of aligning data products to protected site boundaries for impact assessment and policy support.
  - The importance of grid-based deposition and concentration data at multiple resolutions (5x5 km and 1x1 km) to support both site-specific and landscape-scale analyses.
  - The need for robust workflow governance, clear metadata, and documented QA processes when integrating deposition and concentration data from multiple models (CBED and PCM).
  - The potential to identify data gaps (e.g., granularity, data accessibility, and sector coordination) by comparing model outputs with monitoring data and user needs.

Access and references
- Data sources and access
  - CBED data drawn from the UK Eutrophying and Acidifying Pollutants network (UKEAP) and related modelling efforts.
  - PCM data produced by Ricardo Energy & Environment for Defra; used for road-side and background concentration mapping.
  - Supporting information and data portals are listed in the resource locators accompanying the document.
- Selected references and background
  - Key studies and reports cited include works by Beswick et al., Dore et al., Fowler et al., RoTAP, and Carslaw (inter-comparison and QA context).

Notes
- Outputs are designed to support assessment of deposition and concentration impacts on protected sites and to assist policy development, scenario analysis, and exposure estimation.
- The data are presented in both original deposition units (keq ha-1 year-1) and their converted mass units, along with concentration units (µg m-3), enabling flexible interpretation and integration with other ecological and policy datasets.