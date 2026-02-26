# Digital Surface Models for the South Saskatchewan River, Canada

- Purpose and scope
  - Digital Surface Models (DSMs) of two sections of the South Saskatchewan River near Outlook, Canada.
  - Aimed at quantifying river morphology and its changes over time due to erosion and sediment deposition.
  - DSMs cover four dates: 13 May 2015; 2 Sept 2016; 8 Jun 2017; 12 Jun 2017.
  - Eight DSMs in total (two river sections × four dates), provided as separate files.

- Data contents
  - Each DSM file contains three columns: UTM Easting (m), UTM Northing (m), and UTM Elevation (m).
  - Coordinate system: UTM zone 13N (EPSG:32613).
  - Two river sections located at UTMs: Easting ~356,500; Northing ~5,712,400; location near Outlook, Canada (latitude ~51.5 N, longitude ~107.07 W).

- Files included
  - downstream_DSM_2015.txt
  - downstream_DSM_2016.txt
  - downstream_DSM_2017a.txt
  - downstream_DSM_2017b.txt
  - upstream_DSM_2015.txt
  - upstream_DSM_2016.txt
  - upstream_DSM_2017a.txt
  - upstream_DSM_2017b.txt

- Data acquisition and processing
  - Imagery: photogrammetric quality aerial images with ground resolution of 0.06 m, acquired from ~1500 m altitude using a fixed-wing aircraft with an UltraCamXp sensor.
  - Processing workflow:
    - (1) Orthomosaic construction from up to 160 images using Pix4D; bundle adjustment with calibrated camera properties.
    - (2) Point cloud generation; quality check and tilt correction using RTK GPS-derived Ground Control Points; DSM density reduced to 0.5 m.
    - (3) Wet (submerged) areas: derive bed elevations via a depth-brightness model. Water surface elevations extracted from the point cloud, depth measured at image locations, brightness-based depth regression, and bed elevations calculated by subtracting depth from surface elevations.
  - Final DSM combines dry-area elevations (from corrected point cloud) and submerged-area bed elevations (from the depth-brightness model).

- Spatial and temporal scope
  - Two river sections near Outlook, Canada (UTM13N coordinates provided).
  - Four dates spanning 2015–2017 (two sections × four dates).

- Data quality and characteristics
  - Final DSM resolution effectively 0.5 m for the dry areas; wet-area bed elevations derived via depth modelling.
  - DSMs reflect surface morphology and changes over time, suitable for analyzing bedform dynamics and sediment flux.

- Usage, access, and citation
  - Data and licensing details available at the provided DOI: https://doi.org/10.5285/13695138-227f-4d85-9049-0a9cba9e1867
  - Required citation: Ashworth, P., Nicholas, A., Parsons, D., Sambrook Smith, G. (2019). Digital Surface Models for the South Saskatchewan River, Canada. NERC Environmental Information Data Centre. https://doi.org/10.5285/13695138-227f-4d85-9049-0a9cba9e1867
  - Referenced in context: Strick et al. (2019) on bedform dynamics and sediment flux (Earth Surf. Process. Landforms, 44: 953-972).

- Potential analytical use for analysts
  - Track temporal changes in river morphology and bed elevations to identify erosion/deposition patterns.
  - Develop correlations between bedform dynamics and sediment transport indicators.
  - Build or validate predictive models of bed elevation changes using multi-date DSMs.