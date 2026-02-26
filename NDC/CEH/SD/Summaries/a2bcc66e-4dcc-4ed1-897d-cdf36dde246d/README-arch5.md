# Satellite-derived geomorphic river mobility for ten catchments in the Philippines, 1988-2019

## Overview
- A dataset package combining example workflows and processed outputs for analyzing geomorphic river mobility across ten catchments in the Philippines (1988–2019).
- Provides runnable code snippets and ready-to-use raster products for GIS visualization.

## Data components
- 01_Abulug_Example
  - Google Earth Engine (GEE) code to generate binary active channel images.
  - MATLAB code to calculate per-pixel locational probabilities.
  - MATLAB code to calculate and plot along-valley locational probabilities using TopoToolbox 2.4.
- 02_Processed_Locational_Probabilities
  - Raster images of per-pixel locational probabilities for the analyzed catchments, intended for GIS visualization.

## Data governance and usability considerations
- Metadata and provenance: The files indicate processing steps and software used, but explicit metadata (dataset origin, temporal/spatial extents, coordinate reference system, data dictionary, versioning) should be documented for governance and discovery.
- Licensing and reuse: The document does not specify licensing; define access rights and usage terms for both code and raster outputs.
- Dependencies and reproducibility: Ensure clear dependency information (software versions for GEE, MATLAB, TopoToolbox) to enable reproducibility.
- Versioning and updates: Outline how new catchments, additional years, or revised processing would be versioned and shared.

## Standards and interoperability
- File formats and structure:
  - Code in 01_Abulug_Example (GEE JavaScript, MATLAB .m scripts).
  - Raster outputs in 02_Processed_Locational_Probabilities (GIS-ready rasters).
- Naming and organization should be maintained to support cross-project reuse and alignment with metadata schemas (e.g., describing coordinate systems, resolutions, and data layers).

## Data quality and validation
- The provided scripts imply QA steps (probability calculations, along-valley analyses) and deliverables (probability rasters); formal QA documentation and validation results should be captured in metadata or a README.
- Document assumptions, data sources (satellite observations), and any known limitations (e.g., resolution constraints, potential biases in probability estimates).

## Access, storage, and sharing
- Structure suggests a modular package separating code from processed results, aiding discoverability and reuse.
- Plan for long-term storage, backups, and a stable access point; include a concise README with usage instructions and software requirements.

## Potential challenges and mitigation
- Diverse toolchain (GEE, MATLAB, TopoToolbox) requires clear setup guidance; provide a consolidated environment setup or containerization where feasible.
- Large data transfers: consider distributing only processed rasters or providing cloud-access links for heavy outputs.
- Interoperability: ensure coordinate reference systems and raster metadata are explicit to facilitate integration with other datasets.

## Recommendations for Data Stewards
- Create a comprehensive metadata record covering:
  - Dataset title, creators, contact, and publication date.
  - Spatial extent, temporal range, and coordinate reference system.
  - Data dictionary for locational probabilities and along-valley metrics.
  - File formats, version history, processing steps, and software requirements.
  - Licensing, access rights, and redistribution terms.
- Include a cohesive README linking 01_Abulug_Example to 02_Processed_Locational_Probabilities with clear workflow steps to reproduce results.
- Establish data governance for updates (e.g., adding more catchments or extended timeframes) and version control.
- Provide guidance for users on how to integrate outputs into GIS workflows and how to cite the dataset.