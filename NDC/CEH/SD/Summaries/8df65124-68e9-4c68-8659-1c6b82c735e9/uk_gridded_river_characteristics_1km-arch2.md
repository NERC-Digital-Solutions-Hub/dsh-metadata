# UK gridded physical river characteristics at 1km: Supporting Information

- A UKCEH-derived set of 1km × 1km gridded datasets for hydrological and inundation modelling across the UK, including:
  - Outflow drainage directions
  - Catchment areas
  - Bankfull river widths
  - Bankfull river depths
  - NRFA gauging station locations on the 1km grid

- Datasets are produced from a range of sources and provide a consistent, national-resolution framework for modelling and environmental health monitoring.

## Data components and how they are produced

- Outflow drainage directions and catchment areas
  - Primary datasets required before bankfull width and depth can be estimated.
  - Derived at 1km from higher-resolution data (50m IHDTM) using the Paz et al. (2006) method, with manual QA against the 50m IHDTM river network.
  - Uses the D8 eight-direction approach; two numbering schemes are provided: ESRI (East=1, South=4, etc.) and Unifhy/Hydro-JULES.
  - Catchment areas are computed as the number of upstream 1km cells (including the cell itself).

- Bankfull river widths
  - Derived for 1km cells from a regression using OS MasterMap Water Network Layer (WNL) widths, catchment area, and catchment SAAR (1961–1990).
  - Regression: RW = 0.0042 × A^0.409 × SAAR^0.86 (RW in metres; A in km²; SAAR in mm); R² ≈ 0.80 across ~38,600 sites.
  - For some cells with missing SAAR, the nearest cells’ SAAR is used.
  - A GB-wide width estimate is applied to areas lacking direct WNL data (including NI).

- Bankfull river depths
  - Derived via regression relating bankfull depth to catchment area and SAAR.
  - Regression: RD = 0.02643 × A^0.202 × SAAR^0.402; RD in metres; R² ≈ 0.57 based on 90 depth measurements.
  - For coastal cells with missing SAAR, nearest cells’ SAAR are used.
  - Noted scatter, especially for larger depths, reflecting measurement and representation challenges.

- NRFA river flow gauging stations on the 1km network
  - An accompanying NRFA_gauging_station_locations_1km.csv links 1km network cells to 1499 NRFA gauging stations.
  - Includes OSGB coordinates, 1km and IHDTM catchment areas, and errors/overlaps between delineations.
  - Northern Ireland stations have incomplete overlap statistics due to grid reprojection.

## Data quality and caveats

- Spatial discretisation
  - Expected discretisation error around 0.5 km; some areas more affected.

- Outflow directions
  - Manual QA and correction performed by comparing 1km network to the 50m IHDTM river network.

- Catchment areas
  - 1km delineation does not allow fractions of grid-cells to lie in multiple catchments; can yield catchments that are too large or too small. Median catchment area error for gauging stations is about 1%, with overlap error ranges 0.8%–44% (median ≈ 7%).

- Bankfull widths and depths
  - Derived from regression relationships; reasonable correspondence to observations but with scatter.
  - Typical uncertainties: ~0.5 m in width and ~0.36 m in depth.

- Domain and data coverage
  - 656 km × 1220 km British National Grid domain; includes GB fully and NI (via UK datasets and NI data handling); estuarine/tidal regions extended but width/depth values are not representative in estuaries.

## Dataset format and access

- File formats
  - Gridded data: NetCDF (.nc) files
  - Gauging station metadata: CSV (.csv)

- File names
  - UK_outflow_drainage_directions_1km_ESRI.nc
  - UK_outflow_drainage_directions_1km_Unifhy.nc
  - UK_catchment_areas_1km.nc
  - UK_bankfull_river_widths_1km.nc
  - UK_bankfull_river_depths_1km.nc
  - NRFA_gauging_station_locations_1km.csv

- Usage notes
  - Datasets can be read directly into ArcGIS to generate 1km UK river networks.
  - Datasets include extended tidal regions; caution: estuary areas may not reflect true depths/widths.

## How this supports environmental monitoring and analysis

- Provides a standardised, repeatable baseline for configuring hydrological components of gridded land-surface models and environmental health assessments.
- Enables analysis and policy scrutiny over time by offering consistent 1km-resolution river characteristics across the UK.
- Facilitates data integration by supplying explicit QA/metadata (including gauging station localization and catchment overlap metrics) and a straightforward data structure.

## Domain relevance and accessibility

- The data underpin hydro- and flood-modelling and can be used to assess river connectivity, catchment-scale hydrology, and river network properties across the UK.
- Acknowledges infrastructure support from NERC (Hydro-JULES and UK-SCAPE) and provides references for methodological background.

## Acknowledgements and references

- Supported by NERC awards NE/S017380/1 (Hydro-JULES) and NE/R016429/1 (UK-SCAPE).
- Key references include Davies & Bell (2009), Jenson & Domingue (1988), Morris & Flavin (1990), Naden & McCartney (1991), Nixon (1959), and Paz et al. (2006).