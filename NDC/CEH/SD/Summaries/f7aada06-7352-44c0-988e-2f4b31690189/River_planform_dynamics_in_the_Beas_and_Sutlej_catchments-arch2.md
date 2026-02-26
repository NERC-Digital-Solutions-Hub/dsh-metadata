# Human impact on river planform within the context of multi-timescale river channel dynamics in a Himalayan river system.

## Overview
- Describes and analyzes a dataset accompanying Vercruysse and Grabowski (2021) that investigates human impacts on river planform across centennial, annual, seasonal, and episodic timescales.
- Case study: Himalayan Sutlej-Beas River system.
- Aims to quantify planform changes, link them to human-environment drivers, and conceptualize geomorphic trajectories by timescale.

## Study system and scope
- Rivers covered: Beas and Sutlej.
- Spatial extent:
  - Beas: Pong Dam to confluence with Sutlej; Reach 1 (below dams) and Reach 2 (plains) with Reach 2 subdivided into 4 sections.
  - Sutlej: Bhakra Dam to confluence with Beas; Reach 1 and Reach 2 with Reach 2 subdivided into 5 sections.
- Coordinate system: WGS 1984.
- Study extents: West 74.957, East 76.706, North 32.225, South 30.780.

## Data components (annual time series and historic reference)
- Wet river area (post-monsoon, annual 1989–2018).
- Active gravel bars (post-monsoon, annual 1989–2018).
- Active channel area (maximum extent, 1989–2018).
- Active channel width (annual, 1989–2018).
- Active channel width from historic map (1847–1850).
- Anabranching index (AI) (annual, 1989–2018).

## Data sources and methods
- Wet river area: derived from Landsat 5–8 imagery (October–December) using mNDWI > 0.15; manual editing; converted to polygon shapefiles; annual values by reach/section.
- Active gravel bars: identified via high red reflectance (>0.16) from Landsat imagery; buffer around maximum wet area; yearly shapefiles.
- Active channel area: union of wet-area polygons across 1989–2018 to represent the active channel extent.
- Active channel width: measured as the width of the wet area (including enclosed gravel bars) every 2 km; historic-width from 1847–1852 map; width measured perpendicular to banks; mean width by reach and section; annual series.
- Anabranching Index: counts active channels separated by bars/islands using at least 10 cross sections; computed for each reach and section; annual series.

## Data formats and archival structure
- Primary format: ESRI Shapefiles with mandatory/optional accompanying files.
- Width data: point-based shapefiles with attributes Year and Width; summary metrics provided in CSV files.
- File listing includes:
  - Wet river area shapefiles for Beas and Sutlej (1989–2018).
  - Active gravel bars shapefile (1989–2018).
  - Active channel area shapefiles for Beas and Sutlej.
  - Active channel width shapefiles for Beas and Sutlej.
  - Historic width shapefiles (1847–1850) for Beas and Sutlej.
  - Metrics CSVs and a Reach/Section shapefile capturing reach definitions.

## Quality control and provenance
- Data derived from Landsat imagery with QA bands for cloud-free selection.
- Processing included spot validation against aerial photography.
- Independent verification and checks conducted by Cranfield University.

## How this supports environmental monitoring
- Provides standardised, time-series spatial data suitable for tracking river planform health and policy impact.
- Facilitates cross-temporal comparisons (century-scale to annual) and integration with other datasets.
- Enables data dissemination and reuse by making outputs available as shapefiles and CSVs, with clear reach/section definitions.

## References and methodological context
- Methods and validation guided by remote-sensing and GIS techniques for river dynamics (Huang et al., 2018; Langat et al., 2019; Li et al., 2017).
- Historic map reference from Revenue Survey of India (1852).
- Core analysis framework outlined in Vercruysse & Grabowski (2021).