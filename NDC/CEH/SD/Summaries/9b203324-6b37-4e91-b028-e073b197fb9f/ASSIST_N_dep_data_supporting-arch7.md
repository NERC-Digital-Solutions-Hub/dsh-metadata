# Frame Modelling

## Overview
- FRAME (Fine Resolution Multi-pollutant Exchange) is a Lagrangian atmospheric transport model to assess annual mean deposition of reduced and oxidised nitrogen over the United Kingdom.
- Domain covers the UK and Ireland with a 1 km x 1 km grid; outputs are masked to land cells within the UK.
- Outputs represent average conditions within each 1 km grid cell and are provided for different land cover contexts.

## Domain, resolution and outputs
- Spatial resolution: 1 km x 1 km grid; domain includes UK and Ireland; deposition masked to UK land cells.
- Vertical structure: multi-layer scheme with 33 layers up to 2500 m.
- Deposition components: wet and dry deposition of reduced nitrogen (NHx) and oxidised nitrogen (NOy).
- Land-cover-specific deposition: outputs for forest and moorland, plus a grid-average (weighted by the five land-cover types within each grid cell: forest, moorland, grassland, arable, urban).
- Temporal scope: annual mean deposition values (kg N ha-1 year-1).

## Data inputs and sources
- Emissions: UK National Atmospheric Emissions Inventory (NAEI), 160 subsectoral categories aggregated into 11 SNAP sectors; includes diffuse and point sources for NH3, NOx, and SO2.
- Agricultural NH3: annual UK agricultural NH3 emissions estimates derived from census data, farming practices, and emission source strength data; distributed across 1 km x 1 km using land-cover weighting.
- Boundary conditions: ROI emissions from CLRTAP/EMEP and E-PRTR; 2016 maps scaled to year totals; UK-wide boundary conditions derived from wider European domain (50 km x 50 km).
- Atmospheric inputs: wind (from radiosondes or WRF), rain (Tanguy 2019; Walsh 2012), and land cover datasets (Land Cover Map 2015) to assist transport and deposition calculations.
- Deposition processes: deposition velocities depend on land cover; wet deposition uses precipitation ion concentrations; dry deposition uses land-cover-specific deposition velocities for five land-cover categories.

## Model outputs and data structure
- Output types: wet and dry deposition for NHx and NOy.
- Land-cover contexts: forest, moorland, and grid-average deposition.
- Data granularity: 1 km x 1 km grid, representing average deposition within each cell.
- File structure: 28 CSV files named ASSIST_N_dep_kgha_xxxx.csv (xxxx = year, 1990–2017).
- Each file format (for all files):
  - Columns include: x (eastings, OS British National Grid, metres), y (northings, metres),
  - grd_NHx_dry (kg N ha-1 year-1), grd_NOy_dry (kg N ha-1 year-1),
  - grd_NHx_wet (kg N ha-1 year-1), grd_NOy_wet (kg N ha-1 year-1),
  - for_NHx_dry/for_NOy_dry/for_NHx_wet/for_NOy_wet (forest-only),
  - mor_NHx_dry/mor_NOy_dry/mor_NHx_wet/mor_NOy_wet (moorland-only).
- Each row corresponds to a 1 km x 1 km grid cell; NA indicates no-data in non-terrestrial cells.
- Output deployment is masked to terrestrial UK cells; grid-average values reflect a weighted mean from the included land-cover classes within each cell.

## Data quality and validation
- Quality control: modelled concentrations and deposition values compared with UK Acidifying and Eutrophying Atmospheric Pollutants (UKEAP) observations.
- Validation: extensive peer review and inclusion in Defra model inter-comparison exercises; FRAME has been widely published in peer-reviewed literature.

## GIS implementation and usage
- Coordinate reference: OS British National Grid (metres).
- Data integration: join deposition values with a 1 km UK grid, or overlay with land-cover maps to reproduce grid-average deposition.
- Visualization: create map layers for:
  - Wet vs. dry deposition of NHx and NOy.
  - Forest-specific vs. moorland-specific deposition.
  - Grid-average deposition across all land-cover types.
- Analytical opportunities:
  - Compare spatial patterns of NHx and NOy deposition across land covers.
  - Assess deposition across administrative or ecological boundaries.
  - Use as input for exposure assessments or ecological impact studies at 1 km resolution.
- Data handling considerations:
  - 28 separate yearly files require careful file management and consistent cell indexing across years.
  - Some cells may be NA; account for masked regions outside the terrestrial UK domain.

## Access and references
- Resource locator: UK Acidifying and Eutrophying Atmospheric Pollutants (UKEAP) information page.
- Purpose: Supporting information for FRAME model outputs.
- References include key FRAME and emissions inventory literature (Dore et al., Aleksankina et al., Brown et al., Carlaw et al., etc.).