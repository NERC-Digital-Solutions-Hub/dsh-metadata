# Allometric modelling of plant biomass from drone-acquired photographs: drone images, ground control marker coordinates and biomass data from 36 sites, 2016-2020

## Overview
- A dataset combining drone-acquired imagery, ground control markers, and biomass measurements from 36 sites (2016–2020) in low-stature, non-forest ecosystems.
- Aims to support allometric modelling of above-ground biomass using photogrammetry-derived canopy heights.
- Data and protocol designed to enable reproducibility, data sharing, and integration with ongoing biomass research.

## Data access and citation
- Access: Open Government Licence.
- Repository: NERC Environmental Information Data Centre (EIDC) with dataset DOI: 10.5285/1ec13364-cbc6-4ab5-a147-45a103853424.
- Citation guidance: Cunliffe, A. et al. (2020). Allometric Relationships for Predicting Aboveground Biomass and Sapwood Area of Oneseed Juniper (Juniperus Monosperma) Trees (as context) and the specific dataset citation provided.
- Data are organized for each drone survey and linked to biomass observations; metadata and units provided in accompanying files.

## Dataset structure and scope
- 38 drone survey directories (one per flight), each containing:
  - A markers.csv with ground control marker data.
  - A subdirectory of image files.
- Metadata and biomass observations stored in drone_allometry_observations.csv, with units in an accompanying .txt file.
- Survey IDs: 15-digit codes (date + investigator initials + site code) linking images to data.
- Focus on capturing canopy height in non-forest vegetation to inform biomass estimations.

## Site and species selection
- Target environments: grasslands, open/closed shrublands, woody savannas (non-forest).
- Rationale: forest biomass better characterized by other methods; photogrammetry used for non-forest canopies.
- Species: regionally widespread, accessible taxa; highly artificial vegetations excluded.
- Sampling timed to peak canopy cover to minimize phenological effects.

## Aerial imaging surveys
- Equipment: unmanned aerial systems (UAS) collecting nadir and oblique imagery.
- Flight setup per site:
  - Nadir imagery for ~5 mm per pixel (canopy-top GSD).
  - Oblique imagery (~20°) from ~3–4 m higher.
  - Typical altitude ~20 m AGL; 75% forward/side overlap; minimum 30 images per area.
- Environmental data: wind speed measured just before surveys.
- Ground control: 13 markers per site (20 cm x 20 cm squares) with high-precision GNSS coordinates (typical accuracy ±0.015 m horizontal, ±0.03 m vertical).
- Coordinate systems: drone imagery geotagged in WGS84; marker coordinates provided in meters with site-specific UTM zones and EPSG codes.

## Vegetation harvests
- Plot selection: harvest plots spanning the natural canopy-height range; minimum size ~0.5 m x 0.5 m.
- Biomass collection: biomass harvested to ground level (or moss level for certain species); plots geolocated with GNSS corners before harvest.
- Biomass processing: dry biomass to constant weight (50–80°C); moisture-content subsamples for large taxa.
- Plot area calculation: from corner coordinates or harvesting frame area when applicable.
- Target representativeness: emphasis on capturing biomass and canopy from target taxa within plots.

## Image-based modelling workflow
- Software: Agisoft PhotoScan (v1.4.3) for Structure-from-Motion (SfM) processing; dense point clouds generated for each survey.
- Pre-processing and alignment:
  - Import geotagged images and ground control markers; convert to UTM.
  - Image sharpness filter: all images with sharpness score ≥ 0.5.
  - Alignment settings: high-quality; point limits and preselection enabled; adaptive model fitting disabled.
  - Lens and distortion parameters enabled; bundle adjustment optimized.
  - Sparse clouds reviewed; obviously erroneous tie points removed.
- Ground control usage: 13 markers constrained the model; 10 markers per marker used to constrain reconstructions; 3 markers reserved for independent accuracy evaluation.
- Output: dense point clouds with color; export in laz format for subsequent analysis.

## Digital terrain models and canopy height estimation
- DTM creation: interpolated terrain models using inverse distance weighting (power = 1) from harvest plot corners.
- Canopy-height derivation: height above ground calculated from point clouds relative to the interpolated ground surface; handling of discontinuities by using high-quality DTMs from the photogrammetric cloud or alternative data sources (e.g., leaf-off UAV surveys, LiDAR, walkovers) when appropriate.
- Canopy height data: used to derive canopy-height metrics for biomass modelling.

## Dense point cloud analysis and data products
- Tools: PDAL (Point Data Abstraction Library) used to process point clouds.
- Plot extraction: subset point cloud using GNSS corner coordinates; remove points associated with non-vegetation infrastructure when detected.
- Height calculations: HAG (height above ground) relative to a surface interpolated from plot corners; negative heights coerced to zero.
- Grid resolution: 0.01 m; cell-based max height extraction; interpolation for empty cells using 7x7 neighbor window; empty cells left empty if no nearby points.
- Output focus: plot-level canopy-height metrics intended to support biomass allometry.

## Data management, metadata, and governance
- Metadata and provenance are embedded in the dataset structure (survey IDs, corner coordinates, ground control markers).
- Emphasis on open licensing and clear citation to enable reuse in monitoring frameworks.
- The protocol cites a comprehensive collection and processing workflow to ensure transparency, reproducibility, and cross-study comparability.

## Relevance to monitoring frameworks
- Demonstrates end-to-end data lifecycle: data acquisition (field plots, UAV surveys), data processing (SfM, DTMs, dense clouds), and data products (canopy height metrics linked to biomass).
- Highlights data quality assurance steps: image sharpness thresholds, photogrammetric alignment settings, ground-control constraints, and accuracy assessment via reserved markers.
- Addresses common monitoring challenges: explicit data sharing/licensing, metadata completeness, data standardization, and governance considerations to enable data reuse and integration.

## References
- Protocols and prior work spanning data collection, photogrammetry, and biomass modelling are cited to situate the dataset within the broader methodological context.