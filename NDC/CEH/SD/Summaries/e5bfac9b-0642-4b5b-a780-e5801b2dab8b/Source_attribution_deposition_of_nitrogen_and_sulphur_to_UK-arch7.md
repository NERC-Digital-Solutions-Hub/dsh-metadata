# Frame Modelling

## Overview
- FRAME is a Lagrangian atmospheric transport model used to estimate annual mean deposition of reduced and oxidised nitrogen and sulphur over the United Kingdom.
- Domain covers the British Isles on a 5 km grid (172 x 144).

## Model Inputs and Source Categories
- Emissions data sourced from UK National Atmospheric Emissions Inventory (NAEI) with 160 sub-sector categories.
- Emissions include 22 individual point sources and background area emissions (SO2, NOx, NH3) across 11 SNAP sectors.
- Ammonia inputs derived from the National Ammonia Reduction Strategy Evaluation System (NARSES), split into five sectors.
- Regional land masks applied to emission maps to separate sources by country (England, Scotland, Wales, Northern Ireland) for regulators.

## Point Sources and Emissions Detail
- Major inputs include large point sources (e.g., power stations, refineries, steel works) and offshore/international shipping, plus European imports.
- Outputs cover pollutants SOx, NOx, NHx with year-specific configurations (e.g., 2012 for many sources).

## Output Footprints and Attribution
- For each 5 km grid cell, deposition footprints are computed for SOx, NOy, and NHx.
- Initial FRAME run (baseline) is compared with runs where each emission source is abated (25% reduction per run to avoid non-linearities).
- Footprints are calculated as FP(id) = DEP(id=0) − DEP(id=n) for each source, representing that source’s contribution.
- Outputs are further divided into detailed deposition components to separate short-range vs long-range contributions:
  1. Wet NH3 (short range)
  2. Wet NH4+ (long range)
  3. Dry NH3 (short range)
  4. Dry NH4+ (long range)
  5. Wet HNO3 + Wet NO3− (long range)
  6. Dry NO2 (short range)
  7. Dry HNO3 + Dry NO3− (long range)
  8. Dry SO2 (short range)
  9. Dry SO4 (long range)
  10. Wet SO2 (short range)
  11. Wet SO4 (long range)

## Ecosystem and Habitat Mapping
- Deposition data output for three ecosystem types: forest, moorland (representing short semi-natural vegetation), and grid average (arable, grassland, urban, forest, moorland).
- Deposition varies by habitat surface roughness; forests/moorlands tend to have higher deposition velocities, especially for ammonia.

## Post-Processing and Calibration
- Individual source footprints are normalised so their sum matches the baseline to account for model non-linearities.
- National budgets of total deposition are checked against previous years for consistency.
- Calibration using CBED (Concentration Based Estimated Deposition, 2011–2013) aligns FRAME outputs with observed deposition data.
- Calibration equations:
  - DEP_CAL(2012) = DEP_UNC(2012) × [ DEP_CBED(2011–2013) / DEP_UNC(2012) ]
  - FP_CAL(2012, id=n) = FP_UNC(2012, id=n) × [ DEP_CAL(2012) / Σ FP_UNC(2012, id=1..160) ]
- Calibrated footprints, when summed, reproduce official CBED totals for 2012.

## Spatial Mapping and Data Structure
- FRAME yields 160 files per footprint type per pollutant; aggregated to 90 footprint files to reduce processing time.
- 90 footprint datasets cover ecosystem-specific source attribution and deposition for nitrogen and sulphur compounds.
- Data at 5 x 5 km grid resolution with fields including:
  - Easting, Northing (grid midpoints)
  - FOOTPRINT_ID and FOOTPRINT_NAME
  - SOURCE LOCATION (country)
  - Deposition fields by local (grid/forest/moorland) and long-range components for SOx, NOx, NHx
  - Local and long-range deposition for each species (e.g., S- and N-containing species, ammonia species)

## Data Quality and Quality Control
- Post-processing normalisation ensures consistency with baseline deposition.
- National budgets cross-checked against previous years.
- Each footprint output is also generated as a JPEG for quick error identification.

## Access and Documentation
- Resource locator: http://www.pollutantdeposition.ceh.ac.uk/node/319
- Data products include x90 footprint datasets with 5 km grid resolution and ecosystem-specific deposition attributes.
- Sensitivity to different emission sources and spatial distribution supports map-based GIS analyses for policy, regulatory, and environmental assessments.