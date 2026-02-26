# Derwent X-ray powder diffraction (XRD) Sediment Fingerprinting

## Overview
- A dataset of sediment fingerprinting in the River Derwent catchment, Yorkshire, UK.
- Uses X-ray diffraction (XRD) to qualitatively identify mineral phases in sediment samples.
- Data provided as raw CSV output (2 theta values and counts) rather than phase-table identified minerals.
- Designed to understand mineralogical composition and potential sediment sources.

## Collection and Laboratory Methods
- Collection: Grab samples taken around the Derwent Catchment from various soil types and in-stream sediment associated with river bars and banks.
- Field/Lab workflow: Samples dried, sieved, and powdered; processed with Bruker D8 XRD instrument.
- Analytical approach: Qualitative phase analysis to determine the range of minerals present in each sample.
- Quality control: XRD instrument calibrated; data are raw outputs (not phase-table processed).

## Data Content and Structure
- Primary data format: CSV files.
- Key fields:
  - Sample site name (e.g., Derwent_XRD_SedimentFingerprinting_(n)).
  - Spatial coordinates (X and Y) for each sample site.
  - XRD measurements: 2 theta value and associated count per measurement.
- Site coverage: Numerous sampling locations across the catchment (e.g., Lower Rye upstream of Derwent confluence, Derwent U/S Rye River, Jugger Howe soils, Boxa Woods, various banks and floodplain sites, etc.).
- Data notes: The provided text includes many explicit site entries with coordinates, though some lines are garbled or inconsistently formatted, indicating potential data quality or transcription issues that may require cleaning prior to GIS use.

## Geospatial Aspects
- Geographic scope: Derwent Catchment, Yorkshire, UK.
- Each record ties a sampling site to spatial coordinates, enabling GIS mapping and spatial analyses.
- Coordinates are provided in the CSV (X, Y), suitable for joining to GIS layers and performing spatial joins or visualizations.

## Quality Assurance and Processing Status
- Instrument calibration confirmed for XRD measurements.
- Data represent raw XRD outputs; mineral identification requires further processing with phase tables.
- Some dataset rows in the text are corrupted or inconsistently formatted, suggesting the need for data cleaning before integration into a GIS workflow.

## Practical Considerations for GIS Specialists
- How to use in GIS:
  - Import CSVs as point features using the provided X, Y coordinates.
  - Map sampling locations to visualize spatial distribution of sediment fingerprinting efforts.
  - Attach 2 theta and count values as attributes for potential analysis or quality checks.
  - Combine with other geospatial datasets (land use, hydrology, erosion hotspots) to investigate sediment source contributions.
- Data preparation tips:
  - Clean and standardize coordinate formats (address garbled entries) before GIS import.
  - Consider converting 2 theta/count data into summarized statistics per site if needed for visualization.
  - Plan for mineralogical interpretation by integrating phase-table processing if mineral identities are required for GIS analyses.