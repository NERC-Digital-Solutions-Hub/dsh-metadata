# UK Acidifying and Eutrophying Atmospheric Pollutants Supporting information

## Overview
- Describes methodology to map and quantify deposition of acidic and eutrophying pollutants to UK protected sites (SAC, SPA, SSSI) using CBED and PCM models.
- Combines gridded deposition/concentration data with protected site boundaries to produce site-specific metrics.
- Uses 3-year rolling means (2015–2017) to smooth inter-annual variability.
- Outputs include 5x5 km grid deposition/concentration for sites and 1x1 km concentration grids, along with minimum, maximum, and area-weighted values for various ecosystem types (moorland and forest/woodland) or grid averages.
- Data support UK policy reporting and assessment of pollutant impacts on protected sites; data portals host the underlying datasets and supporting information.

## Step 1: Spatial Mapping of Deposition and Concentration to UK Protected Sites
- Create a UK-wide 5x5 km grid and clip to SAC, SPA, and SSSI boundaries to produce a gridded dataset for protected sites.
- Merge gridded CBED outputs (3-year mean, 2015–2017) with the protected-site grid.
- Repeat process for 1x1 km NOx and SO2 concentration datasets from the PCM model.
- Data sources include boundary and feature lists downloaded from national websites.

## Step 2: Generating Minimum, Maximum, and Grid Average Values
- Use SQL on the gridded dataset to compute:
  - Grid average deposition/concentration for each site using the formula: CBEDDepositionValue × (GridArea / TotalSiteArea), then sum across grids.
  - Outputs include minimum, maximum, and area-weighted (grid-average) values for site-level assessment.

## CBED Modelling
- The Concentration Based Estimated Deposition (CBED) method produces 5x5 km resolution maps of wet and dry deposition for:
  - Sulphur, oxidised and reduced nitrogen, and base cations.
- Input data come from the UK Eutrophying and Acidifying Pollutants (UKEAP) network.
- Wet deposition:
  - Combines precipitation, direct deposition, occult deposition, and an orographic enhancement factor (upland regions) derived from field studies (e.g., Great Dun Fell, Holme Moss).
  - Includes seasalt corrections to separate anthropogenic components for sulphur and calcium.
- Dry deposition:
  - Uses gas/PM concentrations and habitat-specific deposition velocities across five land-cover categories (forest, moorland, grassland, arable, urban).
  - Applies forest vs non-woodland values depending on vegetation.
- Temporal context:
  - Inter-annual variability leads to averaging over three years; values are produced as rolling 3-year means and ecosystem-specific (moorland/short vegetation, forest, or grid average).
- Units:
  - Deposition values expressed as keq ha⁻¹ yr⁻¹; concentrations in µg m⁻³.
- Notes:
  - Wet deposition includes occult deposition; dry deposition covers deposition to vegetation including gases and PM.
  - Annual variability from weather is acknowledged; deposition data are averaged to reduce noise.

## PCM Modelling
- Pollution Climate Mapping (PCM) provides:
  - Background maps and
  - 1x1 km grids of pollutant concentrations (NOx, NO2, PM10, PM2.5, SO2, etc.) across the UK.
- Outputs support EU Directive 2008/50/EC reporting, scenario assessments, exposure calculations, and regulatory reporting (TEN applications for PM10 and NOx).
- Structure:
  - One model per pollutant with a base year and projection model.
  - Includes around 9,000 roadside representative values.
- Data usage:
  - Used to complement CBED outputs for broader spatial coverage and scenario analyses.

## Data Structure, Units, and Quality Control
- Deposition and concentration data are provided in specific datasets with detailed metadata (SITECODE, SITENAME, SITEAREA, CENTROID coordinates, grid area, YEAR, and pollutant-specific fields).
  - Example deposit/concentration fields include NH3/NH4, NO2/NO3, SO2/SO4 across forests, moorlands, and grid averages.
  - Concentration fields include NH3, NOx, and SO2 with grid- or site-level granularity.
- Units:
  - Deposition: keq ha⁻¹ year⁻¹ (convertible to kg S ha⁻¹ year⁻¹ or kg N ha⁻¹ year⁻¹ using conversion factors).
  - Concentrations: µg m⁻³.
- Quality control:
  - Methods align with government QA standards; extensive peer review and model inter-comparisons.
  - Version control, documentation, and central storage of code.
  - Mass-balance checks and comparisons to previous years for consistency.

## Data Availability and References
- Data and supporting information are accessible via Defra/UK-AIR portals and related project resources.
- References include peer-reviewed studies and project reports validating CBED/PCM approaches and site-specific deposition/concentration assessments.

## Practical Takeaways for Analysts
- The framework combines fine-scale (5x5 km) deposition and 1x1 km concentration data with protected-site boundaries to produce site-relevant exposure metrics.
- Three-year rolling means are used to mitigate year-to-year variability in deposition and concentration.
- Outputs enable assessment of critical loads and policy-relevant exposure for designated sites, with separate ecosystem-type (moorland/forest) assessments and grid-average scenarios.
- Data provenance, QA, and metadata are integral to ensuring discoverability and reproducibility.