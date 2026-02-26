# Human impact on river planform within the context of multi-timescale river channel dynamics in a Himalayan river system

## Aim and context
- A dataset described and analyzed in Vercruysse and Grabowski (2021) to evaluate human impacts on river planform across centennial, annual, seasonal, and episodic timescales.
- Case study: Himalayan Sutlej-Beas River system, linking observed planform changes to human-environment drivers and conceptualising evolutionary trajectories over multiple timescales.

## Dataset components
- Post-monsoon season wet river area, annually 1989–2018
- Post-monsoon season active gravel bars, annually 1989–2018
- Active channel area (maximum extent between 1989–2018)
- Active channel width, annually 1989–2018
- Active channel width assessed from historic map (1847–1850)
- Anabranching Index (AI), annually 1989–2018
- Metrics (annual) for Beas and Sutlej: AI, mean active channel width, wet river area
- Reaches and sections definitions (shapefile) and related data tables

## Scope and spatial extent
- Beas River: Pong Dam to confluence with Sutlej; Sutlej River: Bhakra Dam to confluence with Beas
- Each river divided into Reach 1 (below dams) and Reach 2 (wide plains of Punjab)
- Reach 2 subdivided into 4 Beas sections and 5 Sutlej sections
- Coordinate System: WGS84
- Study extents bounded by approximate longitudes 74.957–76.706 and latitudes 30.780–32.225

## Data generation and key variables
- Wet river area
  - Derived from Landsat 5–8 imagery (1989–2018) using post-monsoon mNDWI; threshold mNDWI > 0.15
  - Manual edits to remove isolated water pixels; converted to polygon shapefiles
  - Yearly measurements, applicable to Reaches 1 and 2 and Reach 2 sections
- Active gravel bars
  - Identified from red reflectance (>0.16) in post-monsoon imagery
  - Pixels within the maximum observed wet-area buffer used to define active bars
  - Shapefiles produced with one feature per year
- Active channel area
  - Created by aggregating annual wet-area shapefiles (1989–2018) to delineate the overall active channel across years
- Active channel width
  - Width of the wet area (including enclosed gravel bars)
  - Calculated every 2 km; also derived from historic map (1847–1850)
  - Width measured perpendicular to riverbanks; mean width computed per reach/section
- Anabranching Index (AI)
  - Reflects the number of active channels separated by bars or islands
  - Calculated across at least 10 cross sections spaced roughly one braid-plain width apart
  - Values provided for Reaches 1 and 2 and each section annually

## Temporal and spatial format
- Time span: 1989–2018 for most variables; historic width from 1847–1850; post-monsoon season focus
- Spatial: Beas and Sutlej rivers with defined Reach 1/Reach 2 structure and Reach 2 sections

## Data formats and file listing
- Primary formats: ESRI Shapefiles (with mandatory/optional supporting files)
- Ancillary format: CSV files for annual metrics
- Key files:
  - Beas_PM_Wetted_annual.shp, Sutlej_PM_Wetted_annual.shp
  - Active_Gravel_Bars_Annual.shp
  - Beas_ActiveChannel_BelowDam.shp, Sutlej_ActiveChannel_BelowDam.shp
  - Beas_Width_Annual.shp, Sutlej_Width_Annual.shp
  - Beas_Width_1847.shp, Sutlej_Width_1847.shp
  - Metrics_Annual_Beas.csv, Metrics_Annual_Sutlej.csv
  - Reaches_sections.shp (definitions)

## Quality control and validation
- Landsat spectral data used with QA bands to select cloud-free images
- Validation against aerial imagery for spot checks
- Project team at Cranfield University performed data checks at all stages

## Usage and accessibility
- Datasets are designed for analysis of multi-timescale river-channel dynamics and to connect planform changes to human-environment drivers
- Outputs include ready-to-use spatial features and annual metrics suitable for dashboards, reports, or further self-serve analysis

## References
- Huang et al. (2018) on water detection from optical sensors
- Langat et al. (2019) on monitoring river channel dynamics with remote sensing and GIS
- Li et al. (2017) on automatic mapping of bare land from Landsat
- Revenue Survey of India (1852) historic map source
- Vercruysse & Grabowski (2021) main research paper detailing human impact on river planform in the Himalayan river system