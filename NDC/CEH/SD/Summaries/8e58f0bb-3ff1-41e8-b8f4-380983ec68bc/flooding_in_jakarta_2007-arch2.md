# Files

## Overview
- Three data products documenting Jakarta metropolitan area hydrology for Jan-Feb 2007: rainfall, river inflows, and flood depth outputs.
- Purpose aligned with environmental monitoring: verify data, support standardised analysis, and enable policy-relevant insights.

## Data files (content and purpose)
- Jakarta-rainfall-jan-feb2007.csv
  - Hourly rainfall data from 8 raingauges (with coordinates).
  - Time window: 20/01/2007 00:00 to 08/02/2007 23:00.
  - Units: millimetres per hour (mm/hr).
  - Data structure: CSV with a column per raingauge; single header line.
- Jakarta-riverInflows-jan-feb-2007.csv
  - Hourly modeled river inflows for 7 discharge points feeding Jakarta.
  - Time window: 20/01/2007 00:00 to 08/02/2007 23:00.
  - Units: cubic metres per second (m3/s).
  - Data structure: CSV with a column per discharge point; single header line.
- Jakarta-Jan-Feb2007_max_water_depth.tiff
  - Georeferenced raster of maximum modeled water depth.
  - Spatial resolution: 30m x 30m grid.
  - Data format: TIFF; relates to CityCAT hydro model outputs.

## Data collection and generation methods
- Rainfall
  - Source: hourly data from 8 raingauges in the Jakarta metropolitan area.
  - Includes station coordinates and coverage for the period above.
  - Jakarta_BMKG rainfall used to disaggregate daily rainfall at other locations.
- Inflows
  - Source: hourly modeled river inflows for 7 locations.
  - Model: Shetran hydrological model; outputs feed into the Jakarta area.
  - Calibration: used for 3 catchments (Cisande, Ciliwung, Kalibekasi).
  - 30m grid resolution across the Jakarta region.
- Water depth
  - Source: CityCAT hydrodynamic model outputs.
  - DEM: aw3d30; river network from OpenStreetMap; buildings not included.
  - Rainfall and inflows come from the other files in this collection.
  - Output: maximum water depth per 30m grid cell.

## Quality control, calibration, and validation
- Quality control
  - Rainfall: checked for inconsistencies and spurious values.
  - Inflows: model outputs derived from calibrated hydrological model.
  - Water depth: validated as CityCAT outputs, with further calibration/validation context.
- Calibration
  - Cisande catchment: daily discharge calibration at Batubela (2003).
  - Ciliwung catchment: hourly discharge calibration at Katulampa (2002–2005, 2007–2008).
  - Kalibekasi catchment: parameterization aligned with Ciliwung.
- Validation
  - CityCAT: validated against observed flood impacts (number of displaced people and damages).

## Data structure and formats
- Rainfall and inflows: CSV files with a single header line; one column per location.
- Depth: georeferenced TIFF; grid-based, 30m resolution.
- Spatial references: coordinates provided for all raingauges and inflow locations.

## Temporal and spatial coverage
- Temporal: 2007-01-20 to 2007-02-08 23:00.
- Spatial: Jakarta metropolitan area; includes 8 rainfall stations, 7 inflow points, 30m grid for depth modeling.

## Use cases and data integration
- Data integration pipeline
  - Rainfall data supports disaggregation and input to hydrological modeling.
  - Inflows model outputs feed into the hydrodynamic CityCAT model along with rainfall inputs to produce depth.
- Analytical outputs
  - Depth maps (TIFF) and discharge time series (CSV) support flood risk assessment, environmental monitoring, and policy performance evaluations.

## Data management and access
- Data should be stored and uploaded to appropriate data portals for reuse and transparency.
- Aligns with the aim of increasing dataset value through integration with additional relevant data and enabling access to underlying data for broader analysis.