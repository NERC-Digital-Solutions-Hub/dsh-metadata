# UK Acidifying and Eutrophying Atmospheric Pollutants Supporting information

- The document describes CBED and PCM modelling approaches for UK protected sites (SAC, SPA, SSSI), using 2014–2016 rolling means and providing data at different spatial resolutions.
- It covers spatial mapping steps, data structures, units, quality control, and where to access supporting information.

## Step 1: Spatial Mapping of Deposition and Concentration to UK Protected Sites
- A 5x5 km UK-wide grid is created and clipped to SAC/SPA/SSSI boundaries to produce gridded site datasets.
- These gridded site datasets are merged with 3-year averaged CBED output data (2014–2016) to form a UK protected sites CBED dataset.
- The same process is repeated for 1x1 km concentration datasets for NOx and SO2 based on the PCM model.
- Data sources for protected site boundaries come from JNCC and country-level sites portals.
- The purpose is to enable site-level deposition/concentration assessment across UK protected areas.

## CBED Modelling
- CBED (Concentration Based Estimated Deposition) generates 5x5 km resolution maps of wet and dry deposition for sulfur, oxidised and reduced nitrogen, and base cations from air concentrations and precipitation ion data.
- Ion concentrations in precipitation are combined with UK precipitation maps to estimate wet deposition.
- Dry deposition uses gas/PM concentrations and habitat-specific deposition velocities across five land cover types (forest, moorland, grassland, arable, urban).
- Deposition values are allocated to non-woodland vs woodland habitats (moorland vs forest rules) for critical load calculations.
- Wet deposition includes direct deposition and occult deposition (cloud droplets); an Orographic enhancement factor accounts for upland precipitation patterns.
- Inter-annual variability exists due to weather; CBED deposition values used for exceedance calculations are averaged over a 3-year period to smooth variability.
- Outputs are annual but provided as rolling 3-year means, ecosystem-specific (moorland, forest) and a grid average.
- Units: deposition values in keq ha^-1 year^-1; conversions to kg S ha^-1 year^-1 or kg N ha^-1 year^-1 are possible (multipliers: 16 for S, 14 for N).
- Datasets provide diverse representations (minimum, maximum, and area-weighted values) for site-specific deposition under different ecosystem assumptions.

## PCM Modelling
- PCM (Pollution Climate Mapping) produces background maps and 1x1 km grids of pollutant concentrations (NOx, NO2, PM10, PM2.5, SO2, etc.) for the UK.
- Runs include a base year model and projections model, supporting policy development, exposure calculations, and TEN-related model runs.
- Outputs also include around 9,000 representative roadside values.
- PCM supports EU Directive 2008/50/EC reporting requirements and scenario analyses.

## Nature and Units of Recorded Values
- Deposition:
  - Sulphur deposition and nitrogen deposition are expressed as keq ha^-1 year^-1.
  - Conversion to kg S ha^-1 year^-1 or kg N ha^-1 year^-1 is possible via multipliers (S: x16, N: x14).
- Concentrations:
  - Concentrations of NH3, NOx, and SO2 are expressed in µg m^-3.
- Inter-annual variability is acknowledged and addressed by using 3-year rolling means.

## Quality Control
- CBED data/calculations have undergone extensive peer review and inter-comparison (e.g., Carslaw 2011).
- Procedures include documented method development, version control, centralized code storage, and regular mass-balance checks against prior years.
- Methods are overseen by senior responsible officers and widely published in peer-reviewed literature.

## Details of Data Structure
- The data comprise multiple datasets (primarily 12), organized by site and grid.
- Common fields across datasets include:
  - SITECODE, SITENAME, SITEAREA, CENTROID_X, CENTROID_Y, COUNTRY, DESIGNATION, YEAR.
  - GRIDAREA and specific deposition or concentration values (e.g., NH3_NH4, NO2_NO3, NO2_CONC, SO2_CONC, NH3_CONC, etc.).
- Deposition datasets provide 5x5 km grid squares with ecosystem-specific values (moorland, forest) and grid averages.
- Concentration datasets provide 1x1 km grid squares for NOx, NO2, and SO2 concentrations.
- Datasets capture minimum, maximum, average values for deposition and concentration where applicable.
- Some dataset descriptions in the source contain formatting artifacts, but the intended structure differentiates forest vs moorland deposition and grid-average values across 2014–2016.

## Data Access and Resource Locators
- Supporting information and data are accessible via the UK pollutant deposition and PCM resources:
  - UK Acidifying and Eutrophying Atmospheric Pollutants Supporting information (general hosting page)
  - UK Air Defra PCM data portal
  - Pollution Climate Mapping (PCM) model information and data
- These resources provide model outputs, datasets, and methodological details referenced in the document.