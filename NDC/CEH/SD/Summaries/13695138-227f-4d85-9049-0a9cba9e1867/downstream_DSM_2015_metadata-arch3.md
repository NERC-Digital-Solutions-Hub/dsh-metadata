# Digital Surface Models for the South Saskatchewan River, Canada

## Overview
- A dataset of Digital Surface Models (DSMs) for two sections of the South Saskatchewan River near Outlook, Canada.
- DSMs produced for four dates: 13 May 2015; 2 Sept 2016; 8 Jun 2017; 12 Jun 2017.
- Purpose: quantify river morphology and its changes over time due to erosion and sediment deposition.
- Location and coordinates: two river sections, UTM13N (Easting 356500, Northing 5712400); approximate geographic coordinates 51.5 N, 107.07 W.
- Data format: eight DSM files (one per section per date), each with three columns (UTM Easting, UTM Northing, UTM Elevation). EPSG:32613.

## Data contents and formats
- Files:
  - downstream_DSM_2015.txt
  - downstream_DSM_2016.txt
  - downstream_DSM_2017a.txt
  - downstream_DSM_2017b.txt
  - upstream_DSM_2015.txt
  - upstream_DSM_2016.txt
  - upstream_DSM_2017a.txt
  - upstream_DSM_2017b.txt
- Resolution and coverage:
  - Ground resolution: 0.06 m in the aerial imagery; final DSM distribution at 0.5 m post-processing.
  - Derived from photogrammetric aerial images captured from ~1500 m altitude using an UltraCamXp sensor.
- File contents: each DSM file contains rows of (UTM Easting, UTM Northing, Elevation in meters).

## Methods and processing workflow
- Step 1: Orthomosaic generation from up to 160 images using Pix4D with automated image matching and bundle adjustment; nadir imagery; fixed camera calibrations.
- Step 2: Point cloud correction and resampling:
  - Ground Control Points with RTK differential GPS to align and reduce density to 0.5 m.
  - MATLAB filtering with a Chauvenet-type criterion to finalize dry-zone elevations.
- Step 3: Wet (submerged) bed elevation estimation:
  - Extract water surface elevations at interfaces between wet and dry bed areas from the corrected point cloud.
  - Use a depth-brightness model: correlate pixel brightness with water depth via log-linear regression based on in-image depth measurements.
  - Compute submerged bed elevations by subtracting predicted depth from the water surface elevations.
- Final DSMs are produced by merging dry-zone elevations and submerged-bed elevations.

## Data access, licensing, and citation
- Data access and licensing information are available at: https://doi.org/10.5285/13695138-227f-4d85-9049-0a9cba9e1867
- Data citation required:
  - Ashworth, P., Nicholas, A., Parsons, D., Sambrook Smith, G. (2019). Digital Surface Models for the South Saskatchewan River, Canada. NERC Environmental Information Data Centre. https://doi.org/10.5285/13695138-227f-4d85-9049-0a9cba9e1867
- References include related methodology and applications:
  - Strick et al. (2019). Quantification of bedform dynamics and bedload sediment flux in sandy braided rivers from airborne and satellite imagery. Earth Surf. Process. Landforms, 44:953-972. https://doi.org/10.1002/esp.4558

## Applications for monitoring frameworks and policy decisions
- Enables temporal monitoring of river morphology to detect erosion, deposition, and bedform dynamics.
- Supports assessments of sediment transport and bedload flux, informing river management, flood risk, and habitat conservation policies.
- Provides a reproducible, data-driven basis for evaluating changes across multiple years and river sections.
- The processing workflow demonstrates how high-resolution DSMs can be derived from aerial imagery, including handling submerged bathymetry through depth-brightness modeling, which can guide data governance and transparency in monitoring programs.

## Quality, metadata, and governance considerations
- Data quality controls embedded in processing:
  - RTK-DGPS-based ground control for alignment and accuracy.
  - Density reduction and filtering to improve reliability of the dry-bed DSM.
  - Validation through residual tilt checks and standardized processing in Pix4D.
- Metadata considerations:
  - Detailed description of acquisition dates, sensor, altitude, and coordinate system.
  - Clear file naming conventions and per-date, per-section DSMs.
- Governance and sharing:
  - Data sharing requires adherence to licensing terms; licensing details are provided in the data access link.
  - Methodology transparency supports replicability and governance of monitoring outputs.