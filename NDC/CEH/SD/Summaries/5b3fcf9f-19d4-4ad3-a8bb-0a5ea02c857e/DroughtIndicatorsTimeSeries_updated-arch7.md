# Drought indicator time series for European NUTS regions based on remote sensing data (2000-2015)

## Overview
- Remotely sensed drought indicators time series for Europe, derived from gridded drought indices (VCI, TCI, VHI) at European NUTS regional levels (0, 1, 2, 3).
- Data extracted from CEH gridded drought indicators product (2000–2015) and masked by a simplified land-use/land-cover (LULC) map (4 classes: forest, crop, shrub, grass) plus an overall all-classes series.
- Aimed to support monitoring and early warning (M&EW) systems within the DrIVER project; near real-time data potential discussed.

## Data content
- Drought indicators included:
  - VCI (Vegetation Condition Index) based on NDVI
  - TCI (Temperature Condition Index) based on Land Surface Temperature
  - VHI (Vegetation Health Index) = α VCI + (1−α) TCI, with α often 0.5
- Regions and resolutions:
  - European NUTS regions (levels 0, 1, 2, 3); 2013 NUTS version referenced
- LULC differentiation:
  - Dustinct time series produced per region for 4 LULC classes plus an overall series (15 time series per region: 5 per indicator)
- Time series handling:
  - Time steps are recorded only if at least 50% of non-masked area pixels have valid values
  - Two kinds of No Data values used: “--” (no valid pixels) and “nan” (some valid pixels but <50% valid)
- Output:
  - Data stored in CSV format

## Data sources and methodology
- Primary data source:
  - Gridded drought indices product for Europe (2000–2015)
- LULC reference:
  - MODIS Land Cover Type (MCD12C1) at 0.05° for 2012
- Calculation method:
  - VCI: based on monthly NDVI values with min/max normalization
  - TCI: based on monthly LST with min/max normalization
  - VHI: combination of VCI and TCI using α (commonly 0.5)
- Regional extraction:
  - Drought indicator time series generated per NUTS region; 4 LULC masks applied per region
  - 15 time series per region (4 classes + all classes) for each drought indicator (VCI, TCI, VHI)
- NUTS references:
  - Uses NUTS nomenclature for statistical regionalization (2013 version)

## Format, structure, and organization
- File format:
  - CSV
- Organization:
  - Data stored in folders (structured by region/indicator/class/time)
- Content per region:
  - 15 time series (5 per indicator: 4 land cover classes + all classes)

## Data quality and processing rules
- Validity threshold:
  - A time step is included only if ≥50% of non-masked area pixels are valid
- No Data handling:
  - “--” indicates no valid pixels; “nan” indicates some valid pixels but insufficient coverage
- LULC masking:
  - Simplified four-class mask (forest, crop, shrub, grass) applied to isolate land-cover–specific responses

## Geographic scope and applicability
- Spatial scope:
  - European NUTS regions (levels 0–3) with 2013 NUTS version
- Temporal scope:
  - 2000–2015 (annual/monthly time steps from gridded data)
- Use cases for GIS:
  - Map-based visualization of drought indicators by region and land cover
  - Comparative analyses across regions, land covers, and indicators
  - Support for validation of drought impact datasets at NUTS scales

## Usage notes and limitations
- Aggregation level:
  - Regional (NUTS) rather than grid-by-grid; reduces detail but aligns with common impact datasets
- LULC simplification:
  - Only four land-cover classes, potentially omitting finer-grained land-cover distinctions
- Data provenance and credits:
  - DrIVER project; supported by Natural Environment Research Council (NE/L010038/1) funding
  - Data sources include CEH gridded drought indicators and MODIS LULC

## Acknowledgments and references
- Acknowledgments to the DrIVER project and funding bodies
- Key references include:
  - Kogan (1995, 1996, 1997) on drought indices
  - Tanguy et al. (2016) gridded drought indices for Europe
  - Bachmair et al. (2016, 2018) on drought indicators and their applicability
  - Related dataset: Gridded drought indices for Europe (2000–2015) by Tanguy et al. (2016)