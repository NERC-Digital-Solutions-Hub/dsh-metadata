# Frame Modelling

## Overview
- FRAME (Fine Resolution Multi-pollutant Exchange) is a Lagrangian atmospheric transport model for estimating annual mean deposition of reduced/oxidised nitrogen and sulphur over the UK.
- Domain: British Isles on a 5 km grid (172 x 144).
- Outputs footprints for each emission source, enabling source attribution of deposition to protected sites.

## Data inputs and scope
- Emissions data: UK National Atmospheric Emissions Inventory (NAEI) with 160 sub-sector categories, including 22 major point sources and background area emissions across 11 SNAP sectors, international shipping, and European imports.
- Ammonia inputs: derived from NARSES with five sectors (livestock, fertiliser, non-agricultural abatable/non-abatable sources, waste sector).
- Spatial delineation: regional masks (England, Scotland, Wales, Northern Ireland) to aid regulators.
- Major point sources: top 22 (power stations, refineries, steel works, etc.).

## Model runs and footprints
- Baseline run (all sources) plus runs with each emission source abated by 25% to limit non-linearities; footprints computed as baseline minus abated run, then scaled by a factor of 4.
- Footprints produced for dry and wet deposition of SOx, NOy, NHx; further subdivided into short-range vs long-range input across 11 deposition-type categories (detailed in the document).
- Outputs separated by ecosystem types to reflect deposition variability:
  - Forest
  - Moorland
  - Grid average (arable, grassland, urban, forest, moorland)
- Includes a note on a special case: Wet NO2 deposition (short range) is not produced due to insolubility.

## Calibration and quality control
- Normalisation: individual source footprints are normalized so their sum matches the baseline deposition to account for model non-linearities.
- Calibration: FRAME outputs calibrated to the CBED (Concentration Based Estimated Deposition) dataset for 2011–2013 to produce robust annual averages (e.g., 2012 calibration). Equations provided for calibration of both deposition and footprints to CBED totals.
- Quality checks:
  - National budgets of total deposition checked against previous years.
  - Each footprint output saved as a jpg for quick error detection.

## Spatial mapping and final products
- Output structure: FRAME produces 160 footprint files per footprint type and pollutant; aggregated to 90 footprint files to ease processing.
- Spatial linking: merged with a gridded UK protected site shapefile (SAC, SPA, SSSI) to derive site-level deposition data.
- Site-level metrics: for each site, compute minimum, maximum, and grid-average deposition values for each pollutant and footprint type.
- Final data products are three files representing deposition to:
  - Forest
  - Moorland
  - Grid average
- Data is delivered as:
  - Depositional values per site for all footprint types (min, max, grid average).

## Data structure and datasets
- Units: keq/ha/year (convertible to kg/ha/year using multipliers: S = x16, N = x14).
- Datasets 1-3: 3-year mean (2013–2015) site attribution and deposition data for nitrogen and sulphur compounds; provided as min, max, and area-weighted values at each SAC/SPA/SSSI site.
  - Example file: APIS_source_attribution_nitrogen_sulphur_to_forest_bysite.csv
- APIS dataset files (structure):
  - APIS_source_attribution_nitrogen_sulphur_to_forest_bysite.csv
  - APIS_source_attribution_nitrogen_sulphur_to_moorland_bysite.csv
  - APIS_source_attribution_nitrogen_sulphur_to_gridaverage_bysite.csv
- Each bysite CSV includes site identifiers, coordinates, area, designation, footprint metadata, and extensive deposition fields (local and long-range contributions for S, N species across wet/dry, and multiple deposition components).

## Units, conversions, and interpretation
- Deposition values reported in kilo-equivalents per hectare per year (keq ha-1 yr-1).
- Convert to kg/ha/yr:
  - Sulphur deposition: keq/ha/yr * 16 = kg S/ha/yr
  - Nitrogen deposition: keq/ha/yr * 14 = kg N/ha/yr
  - Total nitrogen = NO2 + NO3 + NH3 + NH4 contributions summed together.

## Metadata, provenance, and governance considerations
- Provenance:
  - Inputs from NAEI and NARSES; CBED calibration reference (2011–2013).
  - FRAME model version, calibration steps, and year-specific calibrations are documented within the data products.
- Data management:
  - Large number of intermediate footprint files (160) and aggregated files (90); maintain clear naming conventions and version control.
  - Spatially explicit with site-level and ecosystem-type outputs to support regulatory assessments and ecosystem impact analyses.
- Reuse guidance:
  - Use site-level deposition values for policy-relevant assessments (e.g., critical loads exceedance, site vulnerability).
  - Document calibration status (calibrated vs uncalibrated footprints) and year-specific context in metadata.
  - Ensure consistent handling of unit conversions when aggregating or comparing across datasets.

## Practical guidance for data stewards
- Ensure comprehensive metadata:
  - Model version, input data versions (NAEI year, SNAP sectors), calibration references (CBED 2011–2013), and year of calibration (2012 for footprints).
- Maintain data lineage:
  - Link 160 raw footprint files, 90 aggregated footprints, and three site-attribution datasets to the FRAME model runs and calibration steps.
- Manage data at scale:
  - Plan storage and processing for large CSVs and image files (footprints as JPGs), with automation for validation checks.
- Support discovery and discoverability:
  - Tag datasets with keywords: FRAME, frame modelling, nitrogen deposition, sulphur deposition, 5 km, 2012 calibration, CBED, SAC/SPA/SSSI, forest, moorland, grid average.
- Maintain usability for users:
  - Provide clear documentation on how to interpret footprint-based source attributions and how to convert keq to kg for reporting.