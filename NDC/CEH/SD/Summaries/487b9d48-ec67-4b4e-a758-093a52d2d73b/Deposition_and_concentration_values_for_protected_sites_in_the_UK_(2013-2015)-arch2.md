# Step 1: Spatial Mapping of Deposition and concentration to UK protected sites (SAC, SPA, SSSI)

- Purpose andScope
  - Uses CBED (Concentration Based Estimated Deposition) and PCM (Pollution Climate Mapping) models to map deposition and pollutant concentrations onto UK protected sites (SAC, SPA, SSSI).
  - Produces standardized, comparable outputs to support environmental health assessment and policy performance monitoring.

- Process Overview
  - Step 1: Spatial mapping
    - Create a 5x5 km UK grid using Feature Manipulation Engine (FME).
    - Clip to UK protected site boundaries to produce gridded datasets for SAC/SPA/SSSI.
    - Merge gridded site data with 3-year averaged CBED outputs (2013–2015) to form a UK protected sites CBED dataset (see Figure 1).
    - Repeat for 1x1 km NOx and SO2 concentration datasets based on the PCM model.
    - Data sources for site boundaries: JNCC and respective country websites (SSSI).
  - Step 2: Deriving site-level statistics
    - Use SQL on the gridded data to compute for each site: minimum, maximum, and grid-average deposition/concentration.
    - Grid-average value is computed by weighting grid-square areas by site area and applying the CBED deposition value.

- CBED Modelling (Deposition)
  - Generates 5x5 km resolution maps of wet/dry deposition for sulphur, oxidised/reduced nitrogen, and base cations from air concentrations and precipitation data (UKEAP network).
  - Wet deposition: from precipitation maps plus occult deposition (cloud); includes atmospheric ion deposition components (SO4, NH4, NO3, Ca, Mg, acidity).
  - Dry deposition: derived from gas/PM concentrations and habitat-specific deposition velocities for five land-cover types (forest, moorland, grassland, arable, urban).
  - Habitat weighting: deposition to non-woodland vs. woodland uses respective forest/moorland values.
  - Orographic enhancement: accounts for upland precipitation effects (seeder-feeder) using observed altitude-related ion concentration increases.
  - Inter-annual variability: significant year-to-year variation; CBED values are averaged over a 3-year period to smooth variability; outputs are annual but presented as rolling 3-year means.
  - Outputs: ecosystem-specific deposition (moorland/forest) and grid-average values; provided as three ecosystem scenarios (moorland everywhere, forest everywhere, grid average).

- PCM Modelling (Concentrations and Background)
  - Produces background maps and 1x1 km grids of pollutant concentrations (NOx, NO2, PM10, PM2.5, SO2, etc.).
  - Structure: one model per pollutant with a base year and projection model; used for scenario assessment, population exposure calculations, and regulatory reporting (TEN applications for PM10 and NOx).
  - Outputs: 1x1 km concentration maps and approximately 9,000 representative road-side values.

- Data Output and Structure
  - Nature and Units
    - Deposition: keq ha-1 year-1 (convertible to kg S ha-1 year-1 or kg N ha-1 year-1 using factors 16 and 14, respectively).
    - Concentrations: micrograms per cubic metre (µg m-3).
  - Datasets (examples and resolutions)
    - Dataset 4: 3-year mean (2013–2015) ammonia concentrations, 5x5 km grid.
    - Datasets 1–3: 3-year mean ecosystem-specific deposition for N and S (moorland/forest/grid average), 5x5 km.
    - Dataset 5: 3-year mean NOx concentrations, 1x1 km.
    - Datasets 6: 3-year mean SO2 concentrations, 1x1 km.
    - Datasets 7–9: 3-year min/max/average ecosystem deposition values, 5x5 km.
    - Dataset 10: 3-year mean NH3/NH4 deposition to Moorland, 5x5 km.
    - Dataset 11: 3-year mean NO2/NO3 deposition to Moorland, 1x1 km.
    - Dataset 12: 3-year mean SO2 deposition to Moorland, 1x1 km.
    - Additional grid-average and site-by-grid CSVs exist for ammonia, NOx, and SO2 concentrations and depositions (with site metadata, grid overlap areas, and year midpoints).
  - Data structure notes
    - Each APIS_SRCL file contains site codes, site names, areas, centroids, country, designation, grid overlap area, year, and a set of deposition/concentration fields (by habitat type or grid-average) at specified resolutions.

- Data Sources and Access
  - Boundaries and site data from JNCC and national sources.
  - PCM/UK Eutrophying and Acidifying Pollutants network (UKEAP) measurements feed CBED.
  - PCM model runs conducted by Ricardo Energy & Environment for Defra; outputs support policy development and TEN applications.
  - Supporting information and data portals provided (web links included in the document).

- Quality Control and Validation
  - Methods aligned with government QA reviews of analytical models.
  - CBED data subjected to extensive peer review and model inter-comparison exercises.
  - Procedures for documenting method developments, version control, and centralized storage.
  - Mass-balance checks and cross-year consistency checks against previous years.
  - Outputs widely published in peer-reviewed literature.

- Practical Implications for Analysts Monitoring the Environment
  - Standardised, repeatable workflow enabling consistent assessment of environmental health over time.
  - Facilitates cross-site comparison through uniform 5x5 km grid mapping and 1x1 km concentration data.
  - Provides site-level statistics (min, max, grid-average) to support critical load exceedance assessments and policy evaluation.
  - Opportunities to increase dataset value by integrating with additional data sources and by providing underlying data access for broader use.

- References and Resources
  - Key publications and supporting information cited (e.g., Beswick et al., Dore et al., Fowler et al., RoTAP).
  - Resource locators and data portals listed for CBED/UGEAP/PCM data and supporting information.

- Key Takeaways for Analysts
  - The document outlines a robust, multi-scale approach to map deposition and concentration to protected sites using CBED and PCM models, with careful handling of inter-annual variability via 3-year rolling means.
  - Outputs are designed for standardised reporting and policy evaluation, while maintaining pathways for data sharing and broader reuse.