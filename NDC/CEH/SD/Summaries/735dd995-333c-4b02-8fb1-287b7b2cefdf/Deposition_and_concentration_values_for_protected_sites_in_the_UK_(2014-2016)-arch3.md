# CBED Modelling and PCM Modelling for UK Protected Sites: Spatial Mapping of Deposition and Concentration (2014-2016)

- Overview
  - Purpose: identify environmental health measures to scrutinise and evaluate policy, informing future decisions by mapping pollutant deposition and concentrations to UK protected sites (SACs, SPAs, SSSIs).
  - Scope: UK-wide 5x5 km grid for deposition; 1x1 km grid for NOx and SO2 concentrations; outputs linked to designated sites through site-by-grid calculations.
  - Main data sources: Concentration Based Estimated Deposition (CBED) modelling outputs from the UKEAP network and Pollution Climate Mapping (PCM) model outputs (Defra/ Ricardo Energy & Environment); boundary data from JNCC and national sites data; precipitation and land-cover information for deposition processes.

- Step-by-step Methodology
  - Step 1: Spatial mapping to protected sites
    - Create a 5x5 km gridded dataset covering the UK.
    - Clip grids to SAC/SPA/SSSI boundaries and merge with the 3-year CBED output (2014–2016) to produce a UK protected sites CBED dataset.
    - Repeat for 1x1 km NOx and SO2 concentration datasets using the PCM model.
  - Step 2: Deriving site-level deposition/concentration values
    - Compute minimum, maximum, and grid-average deposition/concentration for each protected site via SQL queries on the gridded data.
    - Grid-average deposition per site is calculated by weighting grid values by grid area relative to the site area (CBEDDepositionValue × (GridArea / TotalSiteArea)) and summing across all grid squares within the site.
  - CBED modelling details
    - Generates 5x5 km resolution maps for wet and dry deposition of sulphur, oxidised and reduced nitrogen, and base cations using gas/PM and precipitation data.
    - Wet deposition: from precipitation plus occult deposition; uses UK precipitation map; includes orographic enhancement for upland regions.
    - Dry deposition: uses gas/PM concentrations plus habitat-specific deposition velocities for five land-cover categories (forest, moorland, grassland, arable, urban).
    - Habitat-specific deposition: moorland applied to non-woodland habitats; forest applied to woodland habitats.
    - Temporal aspect: inter-annual variability is averaged; 3-year means are used to smooth fluctuations. Outputs are annual but provided as rolling 3-year means with three ecosystem-specific scenarios (moorland, forest, grid-average).
  - PCM modelling details
    - Produces background maps and 1x1 km grid concentration maps for UK pollutants; supports policy development, scenario assessment, and TEN applications; includes base-year and projection-model outputs for multiple pollutants.

- Data, Outputs, and Unit Conventions
  - Outputs
    - Dataset set comprises 12 data files with 3-year means (2014–2016) for deposition and concentration, across different spatial scales and ecosystem assumptions.
    - Dataset 4 and 5 provide 5x5 km grid ammonia and NOx concentrations; Dataset 6 provides 1x1 km SO2 concentrations; Dataset 1–3 provide tree- or habitat-specific deposition by forest/moorland/grid-average.
    - Datasets 7–9 present minimum, maximum, and average deposition for forest/moorland/grid for the 3-year window.
    - Dataset 10–12 present grid-average concentration statistics for NH3, NO2, and SO2, respectively.
  - Spatial and temporal coverage
    - 3-year means (2014–2016) used for all deposition and concentration values.
    - Outputs cover SAC/SPA/SSSI boundaries with region-specific site attributes and grid-area overlap.
  - Units
    - Deposition: keq ha-1 year-1 (kilo-equivalents per hectare per year); can be converted to kg S ha-1 year-1 or kg N ha-1 year-1 using conversion factors (S: ×16, N: ×14).
    - Concentrations: µg m-3.

- Data Structure and Content Details
  - Dataset 1–3: 5x5 km grid deposition by ecosystem type (forest, moorland) and grid-average; includes SITECODE, SITENAME, SITEAREA, grid overlap, YEAR, and deposition components (NH3/NH4, NO2/NO3, SO2/SO4 for forest or moorland).
  - Dataset 4: Ammonia concentration (NH3) by site and grid with YEAR and CENTROID coordinates.
  - Dataset 5: NOx concentration (NOx/NO2) by site and grid with YEAR.
  - Dataset 6: SO2 concentration by site and grid with YEAR.
  - Dataset 7–9: Minimum, maximum, and average NH3/NH4, NOx/NO3, and SO2/SO4 for forest/moorland across sites.
  - Dataset 10–12: Grid-average NH3, NO2, and SO2 concentrations with min/avg/max values for each site and YEAR.
  - Missing data: NaN cells indicate lack of data from the originating pollutant dataset.

- Quality Control and Governance
  - Quality assurance aligned with the government analytical model framework and inter-comparison exercises (peer review, version control, and central code storage).
  - Mass-balance checks and cross-year comparisons to ensure numerical consistency; results published in peer-reviewed literature.

- Relevance for Monitoring Frameworks
  - Provides concrete, policy-relevant environmental health measures that link emissions/concentrations to protected sites, enabling scrutiny of policy effectiveness and informing future decisions.
  - Demonstrates endpoints (minimum/maximum/grid-average) and scenario planning (ecosystem-specific assumptions) to guide monitoring design.
  - Highlights data governance considerations: data provenance, metadata needs, and openness; notes barriers such as data sharing constraints and metadata gaps, while documenting dataset structures and access points.

- Practical Considerations and Limitations
  - Inter-annual variability in deposition/concentration; mitigated by 3-year rolling means.
  - Data gaps and access constraints; reliance on detailed metadata; transformation requirements for some data formats.
  - Orographic and atmosphere–habitat interactions are approximated within the modelling framework.

- References and Resources
  - Cited studies and supporting information (e.g., Beswick et al., Dore et al., Fowler et al., RoTAP) and links to CBED/ UKEAP and PCM resources.
  - Resource locators and documentation for the underlying data and models (CBED/PCM) are provided for further detail and replication.