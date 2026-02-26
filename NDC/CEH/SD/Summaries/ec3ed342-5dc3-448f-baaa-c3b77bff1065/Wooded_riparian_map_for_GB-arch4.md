# Wooded areas in riparian zones across Great Britain (1km raster)

## Overview
- Provides a 1km resolution raster coverage of woodland within riparian zones across Great Britain.
- Riparian zones are defined by a 50-metre buffer around the CEH 1:50,000 watercourse network.
- Wooded areas are those classified as either coniferous or deciduous woodland (based on Land Cover Map of Great Britain 2007).
- Each 1km cell expresses the proportion of riparian woodland as a percentage.

## Data Scope and Structure
- Spatial reference: OSGB 1936 / British National Grid.
- Format: GeoTIFF raster at 1km resolution.
- Data value: percentage (0–100) representing the proportion of woody riparian area within each 1km square.

## Data Processing (Methodology)
- Buffer the CEH 1:50,000 watercourse network by 50 metres.
- Dissolve the buffered watercourse to create a single polygon.
- Clip the LCM2007 25m raster to the buffered polygon.
- Extract woodland classes from LCM2007 (class 1: Coniferous, class 2: Deciduous).
- Calculate total woodland area per 1km cell and express as the percentage of riparian area.

## Data Inputs and Provenance
- CEH 1:50,000 watercourse network (derived from UK river centreline network; originally from OS maps).
- Land Cover Map 2007 (LCM2007) 25m raster (GB): woodland classification informed by UK Biodiversity Action Plan habitats.
- References for inputs:
  - Moore, R.V., Morris, D.G., Flavin, R.W. (1994). Sub-set of UK digital 1:50,000 scale river centreline network.
  - Morton, R.D. et al. (2014). Land Cover Map 2007 (25m raster, GB) v1.2.

## Data Structure Details
- File: 1km resolution GeoTIFF (.tif).
- Spatial alignment: aligned to OSGB 1936 / British National Grid.
- Each cell value: proportion of wooded riparian areas within that 1km square (as a percentage).

## Usage and Applications
- Enables assessment of riparian woodland distribution at a national scale.
- Useful for ecological network planning, habitat prioritization, and policy evaluation related to riparian environments.

## Reproducibility and References
- Processing workflow implemented in ESRI ArcMap 10.3.
- Key references for data sources:
  - ESRI (2016) ArcGIS Desktop 10.3.
  - Moore et al. (1994) river centreline dataset.
  - Morton et al. (2014) Land Cover Map 2007.

## Considerations and Limitations
- Based on 2007 land cover data; may not reflect recent changes in woodland cover.
- Coarse 1km resolution may obscure fine-scale variability within riparian zones.
- Riparian definition relies on a fixed 50m buffer around the watercourse network; other riparian extents are not captured.
- Data quality and metadata depend on the original inputs (e.g., LCM2007 classifications) and their accuracy.