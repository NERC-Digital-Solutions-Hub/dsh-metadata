# Step 1: Spatial Mapping of Deposition and concentration to UK protected sites (SAC, SPA, SSSI)

## Purpose and scope
- Develop site-level deposition and concentration metrics at UK protected sites to inform policy scrutiny, evaluation, and future decisions.
- Combine model outputs with site boundaries to produce minimum, maximum, and grid-average deposition/concentration values for SACs, SPAs, and SSSIs.

## Data sources and inputs
- CBED (Concentration Based Estimated Deposition) data:
  - 5x5 km grid covering the UK; 3-year mean 2016–2018; deposition of nitrogen and sulphur compounds.
  - Wet and dry deposition components, including occult deposition and land-cover specific deposition velocities.
  - Ecosystem-specific deposition (moorland, forest/woodland) and a grid-average scenario.
- PCM (Pollution Climate Mapping) data:
  - 1x1 km grids of background pollutant concentrations (NOx, NO2, SO2, PM, etc.) with base-year and projection-model outputs.
  - About 9,000 road-side values; used for scenario assessment and population exposure calculations.
- UK protected sites data:
  - Boundary and site attributes for SAC, SPA, and SSSI from national sources.
- Ancillary data:
  - Annual precipitation maps (for wet deposition) and meteorological factors.
  - Orographic enhancement factors for precipitation concentration in upland regions.

## Step 1: Spatial processing and mapping
- Create a 5x5 km UK grid and clip to protected-site boundaries to generate a gridded dataset aligned with site footprints.
- Merge gridded CBED-derived deposition values with protected-site boundaries to produce a UK protected sites CBED dataset.
- Repeat for 1x1 km concentration datasets (NOx and SO2) using PCM outputs.

## Step 2: Generating minimum, maximum, and grid-average values
- For each protected site, compute:
  - Minimum deposition/concentration across grid cells within the site.
  - Maximum deposition/concentration across grid cells within the site.
  - Grid-average deposition/concentration for the site.
- Grid-average calculation formula (conceptual): CBEDDepositionValue × (GridArea / TotalSiteArea), summed across grid cells within the site.

## CBED modelling details
- CBED produces 5x5 km resolution maps of wet/dry deposition for sulphur, oxidised and reduced nitrogen, and base cations from gas/PM concentrations and precipitation-derived ions.
- Wet deposition: from precipitation plus occult deposition; includes orographic enhancement for upland regions.
- Dry deposition: derived from gas/PM concentrations and habitat-specific deposition velocities across five land-cover categories (forest, moorland, grassland, arable, urban).
- Habitat-specific application: for critical load exceedance, moorland deposition applied to non-woodland habitats; forest deposition applied to woodland habitats.
- Inter-annual variability: deposition values vary yearly; results are averaged over a rolling 3-year period to smooth variability.
- Outputs and scenarios: annual values presented as rolling 3-year means for ecosystem-specific cases:
  - Moorland-only
  - Forest-only
  - Grid-average across all ecosystems

## PCM modelling details
- Produces background maps and 1x1 km grids of pollutant concentrations for the UK.
- Used to support policy development, scenario testing, and exposure calculations; also feeds into TEN (Time Extension Notification) applications for PM10 and NOx.
- Separate models exist for each pollutant, run with base year and projections.

## Data outputs and structure
- Datasets cover the 3-year mean (2016–2018) period with 5x5 km or 1x1 km resolutions, and include multiple deposition/concentration metrics:
  - Dataset 1–3: 5x5 km deposition by ecosystem (forest, moorland) and grid-average
  - Dataset 4–6: 1x1 km concentrations for NH3, NO2, SO2
  - Dataset 7–9: site-level minimum, maximum, and average deposition by ecosystem (forest/moorland)
  - Dataset 10: grid-average deposition/concentration by site
  - Dataset 11–12: site-level concentrations for NH3, NO2, SO2 (min/max/avg)
- Units:
  - Deposition: keq ha^-1 year^-1
  - Concentrations: µg m^-3
- Data organization includes site codes, site areas, grid areas, centroids, country, designation (SAC/SPA/SSSI), year, and the respective deposition/concentration variables.

## Data quality, governance, and validation
- Methods follow QA practices aligned with government analytical model governance:
  - Extensive peer review of CBED data and calculations; participation in model inter-comparison exercises.
  - Version control, documentation of method developments, and central storage of code.
  - Mass-balance checks and comparison to previous years to ensure numerical consistency.
  - Results published in peer-reviewed literature; responsible-officer approvals for method changes.

## Practical implications for monitoring framework authors
- Addresses common monitoring challenges by providing:
  - A structured workflow to map and aggregate deposition/concentration data to protected sites.
  - Clear, harmonized metrics (min, max, grid-average) across multiple ecosystem types and resolutions.
  - Rolling 3-year means to mitigate inter-annual variability and provide stable indicators for policy evaluation.
  - Detailed data structures and metadata descriptions to support reproducibility and transparency.
- Highlights data governance considerations, including data sharing, metadata adequacy, and transformation requirements for creating usable site-level indicators.