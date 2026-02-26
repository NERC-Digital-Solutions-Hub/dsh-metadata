# UK Acidifying and Eutrophying Atmospheric Pollutants Supporting information

- Purpose: Describe CBED and PCM modelling approaches used to map deposition and pollutant concentrations in the UK, generate site-specific summaries for protected sites (SAC, SPA, SSSI), and provide data products for policy analysis and impact assessment.

## Step 1: Spatial mapping to UK protected sites

- A 5x5 km grid covering the UK domain was created and clipped to UK protected site boundaries (SAC/SPA/SSSI) to produce gridded datasets for these sites.
- The 5x5 km gridded site data were merged with the 3-year mean CBED output (2013–2015) to create UK protected sites CBED datasets.
- For NOx and SO2, the 1x1 km concentration datasets from PCM were prepared and aligned with the protected sites.
- Protected site boundary data were sourced from JNCC and national sources.

## Step 2: Generating minimum, maximum, and grid-average values

- For each protected site, minimum, maximum, and grid-average deposition and concentration values were derived from the gridded data using SQL queries.
- Grid-average deposition for a site was computed by weighting grid-square CBED deposition by the overlap area with the site.

## CBED modelling

- Purpose: Generate 5x5 km resolution maps of wet and dry deposition for sulphur, oxidised and reduced nitrogen, and base cations, using concentrations from the UK Eutrophying and Acidifying Pollutants (UKEAP) network.
- Process:
  - Site-based concentration measurements are interpolated to create UK concentration maps.
  - Wet deposition combines precipitation with direct deposition from cloud droplets (occult deposition), mapped for several ions; uses UK precipitation maps and sea-salt distinctions.
  - Dry deposition uses gas and PM concentrations and habitat-specific deposition velocities for five land-cover categories (forest, moorland, grassland, arable, urban).
  - Deposition to non-woodland vs woodland habitats is assigned based on habitat type.
  - Orographic enhancement factors (from upstream observations) adjust precipitation-related deposition in uplands.
- Variability and averaging:
  - Inter-annual variability is significant; deposition values are averaged over a rolling 3-year period (annual calculations, presented as 3-year means).
  - Outputs are ecosystem-specific, providing three sets: moorland/short vegetation everywhere, forest everywhere, and a grid-average across ecosystems.

## PCM modelling

- Purpose: Produce background maps and 1x1 km grid pollutant concentrations for the UK to support policy and exposure assessments.
- Details:
  - PCM comprises separate models per pollutant (e.g., NOx, NO2, PM10, PM2.5, SO2, etc.) with base year and projection runs.
  - Outputs include 1x1 km background concentration maps and ~9,000 representative road-side values.
  - Used for scenario assessment, population exposure calculations, and regulatory reporting (e.g., TEN applications for PM10/NOx).

## Nature and units of recorded values

- Deposition values (nitrogen and sulphur compounds) are in keq ha⁻¹ year⁻¹ and can be converted to kg ha⁻¹ year⁻¹ via appropriate multipliers (S: ×16, N: ×14).
- Concentration values (NH3, NOx, SO2) are in µg m⁻³.
- Three-year means (2013–2015) are provided for all outputs, with ecosystem-specific and grid-average variations.

## Data structure and content (selected datasets)

- Dataset 4: 3-year mean NH3 concentration at 5x5 km grid squares for SAC/SPA/SSSI.
- Datasets 1–3: 3-year mean ecosystem-specific deposition (N and S) at 5x5 km resolution (forest, moorland, or grid-average).
- Dataset 5: 3-year mean NOx concentration at 1x1 km resolution.
- Datasets 6–12: concentrations and depositions for NH3, NO2, SO2 with various aggregations (minimum, maximum, average) and grid/forest/moorland designations; resolutions include 1x1 km or 5x5 km.
- Datasets 7–9: minimum, maximum, and average ecosystem-specific depositions at 5x5 km.
- Datasets 10–12: minimum, maximum, and average concentrations/depositions in grid-average format for NH3/NH4, NO2/NO3, and SO2/SO4, respectively.
- Site-level fields include SITECODE, SITENAME, SITEAREA, CENTROID coordinates, COUNTRY, DESIGNATION, YEAR, GRIDAREA, and the relevant deposition or concentration values.

## Quality control and data management

- Methods align with government QA standards and have undergone extensive peer review and inter-comparison exercises.
- Mass-balance checks ensure numerical consistency; documented method developments and version control are enforced; central storage of code and metadata to enable discoverability and reproducibility.

## References and data sources

- Key supporting sources include:
  - UK Acidifying and Eutrophying Atmospheric Pollutants (UKEAP) network data for CBED.
  - Pollution Climate Mapping (PCM) model outputs for background concentrations.
  - Related literature and validation studies (e.g., Holme Moss measurements and inter-comparison reports such as RoTAP).
- Access and background information available via Defra/UK air and related portals.