# Jakarta rainfall and hydrodynamic model data (Jan-Feb 2007)

## Data files (Files)
- Jakarta-rainfall-jan-feb2007.csv: hourly rainfall data from 8 raingauges in the Jakarta metropolitan area (20/01/2007 00:00 to 08/02/2007 23:00), mm/hr.
- Jakarta-riverInflows-jan-feb-2007.csv: hourly modeled river inflows for 7 discharge points feeding the Jakarta area (same date range), m3/s.
- Jakarta-Jan-Feb2007_max_water_depth.tiff: georeferenced 30m grid maximum water depth in meters.

## Data collection and methods
- Rainfall data
  - Source: hourly measurements from 8 raingauges with coordinates:
    - SRS682 Depok (106.85, -6.40)
    - SRS779 Pondok (106.75123, -6.26113)
    - BMKG3 Curug (106.65, -6.2333)
    - BMKG4 Tg.Priuk (106.8667, -6.1)
    - BMKG5 Jakarta_BMKG (106.8333, -6.1833)
    - BMKG6 Halim (106.9, -6.25)
    - BMKG7 Cengkareng (106.65, -6.1167)
    - BMKG9 Dermaga (106.75, -6.5)
  - Timeframe: 20/01/2007 00:00 to 08/02/2007 23:00
  - Units: millimeters per hour (mm/hr)
  - Quality: hourly and daily totals checked for inconsistencies and spurious values
  - Purpose: hourly rainfall at Jakarta_BMKG used to disaggregate daily rainfall at other locations

- River inflows data
  - Source: hourly modeled discharge for 7 locations:
    - Cisande (106.649, -6.380)
    - Ciliwung (106.815, -6.449)
    - Kalibekasi1 (106.882, -6.454)
    - Kalibekasi2 (106.899, -6.462)
    - Kalibekasi3 (107.008, -6.258)
    - Kalibekasi4 (107.065, -6.145)
    - Kalibekasi5 (107.064, -6.039)
  - Timeframe: 20/01/2007 00:00 to 08/02/2007 23:00
  - Units: river flow in cubic meters per second (m3/s)
  - Quality: output from calibrated Shetran hydrological model
  - Details: CSV with a column per discharge point

- Water depth data
  - Source: hourly modeled water depths via CityCAT hydrodynamic model
  - Spatial resolution: 30m grid
  - Coordinates/coverage: 30m x 30m grid over Jakarta
  - Timeframe: 20/01/2007 00:00 to 08/02/2007 23:00
  - Units: meters (water depth)
  - Quality: CityCAT output; maximum modelled depth per grid cell
  - Details: georeferenced TIFF; DEM input uses aw3d30 elevations; OpenStreetMap river network embedded in DEM; no buildings included
  - Input data: rainfall and inflows from the other files; CityCAT validation against measured displaced people and damages

## Data structure and units
- Rainfall CSV: one column per raingauge plus header line; unit mm/hr
- River inflows CSV: one column per discharge point plus header line; unit m3/s
- Water depth TIFF: georeferenced raster; value in meters

## Experimental design and modelling
- Rainfall-disaggregation approach
  - Use hourly rainfall at Jakarta_BMKG to disaggregate daily rainfall at other locations
- Hydrological modelling (inflows)
  - Shetran hydrological model applied to three catchments: Cisande, Ciliwung, Kalibekasi
  - Model calibration:
    - Cisande (Batubela) daily discharge calibration for 2003
    - Ciliwung (Katulampa) hourly discharge calibration for 2002–2005 and 2007–2008
    - Kalibekasi uses the same parameters as Ciliwung
  - Output: hourly discharge for 7 inflow points feeding Jakarta
- Hydrodynamic modelling (water depths)
  - CityCAT hydrodynamic model configured for Jakarta
  - Elevation data: aw3d30 DEM
  - Rivers: OpenStreetMap river network embedded in the model
  - Buildings: not included
  - Calibration/validation: against measured numbers of people displaced and flood damages
  - Outputs: hourly maximum water depths on a 30m grid (GeoTIFF)

## Fieldwork, instrumentation, and analytical methods
- Model outputs constitute the primary data products
- Calibration and validation rely on historical flood impacts (displacements and damages) and matched hydrological outputs

## GIS considerations and practical notes
- Spatial resolution and alignment: raster depth at 30m grid; rainfall points and inflow locations with precise coordinates
- Data fusion: integrates multiple data sources (rainfall gauges, hydrological model outputs, and hydrodynamic model results) into a common Jakarta metropolitan area frame
- Data limitations: buildings not modeled; discrepancies between calibrated years and target event periods; resolution limits for some analyses

## Use-case considerations for GIS specialists
- Useful for map-based flood exposure, risk assessment, and scenario visualization
- Requires aligning CSV time series with raster depth data for spatial analyses
- Potential data quality caveats due to model-based inflows and simplified land-use (no buildings) in the hydraulic model
- Suitable for interactive visualization of rainfall-driven floods, river inflows, and resulting water depths across Jakarta at 30m grid resolution