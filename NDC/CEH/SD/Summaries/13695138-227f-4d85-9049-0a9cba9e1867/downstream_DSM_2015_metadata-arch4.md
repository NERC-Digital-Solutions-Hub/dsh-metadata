# Digital Surface Models for the South Saskatchewan River, Canada

## Overview
- Dataset of Digital Surface Models (DSMs) for two sections of the South Saskatchewan River near Outlook, Canada.
- Covers four dates: 13 May 2015; 2 Sept 2016; 8 Jun 2017; 12 Jun 2017.
- Eight DSMs in total (two river sections × four dates), each stored as a separate file.
- Purpose: characterize river morphology and its temporal changes due to processes like erosion and sediment deposition.
- Data are provided with precise geospatial references and documented processing workflows to support reuse and validation.

## Data Contents
- Files:
  - downstream_DSM_2015.txt
  - downstream_DSM_2016.txt
  - downstream_DSM_2017a.txt
  - downstream_DSM_2017b.txt
  - upstream_DSM_2015.txt
  - upstream_DSM_2016.txt
  - upstream_DSM_2017a.txt
  - upstream_DSM_2017b.txt
- Each file contains three columns:
  - Column 1: UTM Easting (meters)
  - Column 2: UTM Northing (meters)
  - Column 3: UTM Elevation (meters)
- Coordinate system: UTM zone 13N (EPSG:32613); E/N coordinates correspond to the specified reference frame.

## Data Specifications and Geospatial Context
- Studied river sections: two parts of the South Saskatchewan River near Outlook, Canada.
- Spatial reference: UTM13N, with specific coordinates provided (Easting 356500, Northing 5712400; approx. 51.5°N, 107.07°W).
- Ground resolution: approximately 0.06 m for the DSMs (from photogrammetric imagery).
- DSM construction uses imagery from a fixed-wing aircraft at ~1500 m altitude, with UltraCamXp sensor.

## Data Collection and Processing (Methodology)
- Source imagery: high-quality aerial photographs suitable for photogrammetry.
- Processing workflow (three stages):
  1) Orthomosaic generation from up to 160 images using Pix4D with automated image matching and bundle adjustment; dense point cloud produced.
  2) Point cloud quality control using Ground Control Points (GNSS RTK) to correct tilt; downsampled to 0.5 m resolution; MATLAB filtering (Chauvenet criterion) to create the dry (non-submerged) DSM.
  3) Submerged bed elevation estimation via depth-brightness model:
     - Extract water surface elevations at dry/wet interface locations.
     - Obtain water depth measurements from image times; relate pixel brightness to depth via log-linear regression.
     - Derive submerged bed elevations by subtracting predicted depths from water surface elevations.
  - Final DSM combines elevations from dry and submerged bed areas.

## Data Standards, Metadata, and Accessibility
- Licensing and access details are provided via the data DOI and associated repository page.
- Required citation for data use:
  - Ashworth, P., Nicholas, A., Parsons, D., Sambrook Smith, G. (2019). Digital Surface Models for the South Saskatchewan River, Canada. NERC Environmental Information Data Centre. doi: [provided in the document]
- References for methodology and related work:
  - Strick et al. (2019) on bedform dynamics and sediment flux, Earth Surface Processes and Landforms.
- The dataset is designed to support verification, replication, and reuse, with explicit documentation of coordinate system, data format, processing steps, and dates of data acquisition.

## Relevance for Data Leaders
- Aligns with data-system thinking: documents data formats, coordinate references, resolution, and processing pipelines to enable discoverability and reuse.
- Supports data governance: clear citation requirements, licensing information, and provenance through documented methods and dates.
- Enables assessment of data gaps and quality: describes data coverage across two river sections and multiple dates, including both dry and submerged bed data handling.
- Facilitates collaboration and cross-network data sharing by providing standardized DSM files and a replicable photogrammetric workflow, enabling broader analyses of river morphology over time.

## Use Cases and Applications
- Analysis of river morphology changes over time (erosion/deposition patterns).
- Bedform dynamics and sediment transport studies when integrated with related datasets.
- Baseline for monitoring future morphological changes in similar braided river systems.
- Data provision for policy, planning, or environmental management tasks requiring high-resolution topographic information of riverbeds.