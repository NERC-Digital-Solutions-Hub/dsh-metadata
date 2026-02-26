# Jakarta rainfall, river inflows, and max water depth (Jan-Feb 2007)

- Overview
  - A linked set of datasets covering Jakarta’s rainfall, river inflows, and maximum water depth for Jan 20, 2007 to Feb 8, 2007.
  - Data types and units: rainfall in mm/hr; river inflows in cubic meters per second (m3/s); water depths in meters.
  - Includes both measured data (rainfall gauges) and model outputs (river inflows and hydrodynamic water depths).
  - Formats: two CSV files and one georeferenced TIFF; locations and boundaries are defined, with the flood modelling context (CityCAT and Shetran).

- Datasets and Content
  - Jakarta-rainfall-jan-feb2007.csv
    - Hourly rainfall from 8 raingauges in the Jakarta metropolitan area.
    - Gauge details: SRS682 Depok, SRS779 Pondok, BMKG3 Curug, BMKG4 Tg.Priuk, BMKG5 Jakarta_BMKG, BMKG6 Halim, BMKG7 Cengkareng, BMKG9 Dermaga; coordinates provided.
    - Timeframe: 20/01/2007 00:00 to 08/02/2007 23:00.
    - Structure: CSV with one column per raingauge; header line present.
    - Quality: hourly and daily totals checked for inconsistencies and spurious values.
    - Purpose: rainfall at Jakarta_BMKG used to disaggregate daily rainfall for other locations.
  - Jakarta-riverInflows-jan-feb-2007.csv
    - Hourly modelled river inflows for 7 locations feeding the Jakarta metro area (Cisande, Ciliwung, Kalibekasi1–5).
    - Locations: Cisande, Ciliwung, Kalibekasi1–5 with coordinates; timeframe aligns with rainfall data.
    - Nature/Units: River Flow in m3/s.
    - Quality: output from calibrated Shetran hydrological model.
    - Structure: CSV with a column for each discharge point; header line.
    - Experimental design: Shetran model run for three catchments; inflows into Jakarta provided.
  - Jakarta-Jan-Feb2007_max_water_depth.tiff
    - Hourly modelled water depths represented as the maximum depth per 30m x 30m grid cell.
    - Quality: CityCAT hydrodynamic model output; used for validation against displaced people and flood damages.
    - Structure: Georeferenced TIFF; 30m grid; raster of maximum depths.
    - Modelling details: CityCAT model uses aw3d30 DEM elevations; OpenStreetMap river network embedded in DEM; no buildings included yet.
    - Fieldwork/Instrumentation: Model output only; no field measurements described for depth data.

- Data Quality, Provenance, and Modelling
  - Quality control
    - Rainfall: checked for inconsistencies and spurious values.
    - River inflows: model outputs derived from a calibrated hydrological model (Shetran).
    - Water depth: model outputs from CityCAT; validated against displacement and damage data.
  - Calibration details
    - Cisande catchment (Batubela) calibration for daily discharge (2003).
    - Ciliwung catchment calibration for hourly discharge (Katulampa, 2002–2005, 2007–2008).
    - Kalibekasi: calibration uses same parameters as Ciliwung.
  - Analytical methods
    - Rainfall data used to disaggregate daily rainfall at Jakarta_BMKG.
    - CityCAT model for depth uses DEM and river network to produce maximum depths; no buildings included in the current setup.
  - Metadata considerations
    - Units, coordinates, timeframes, and data structure clearly defined in each dataset.

- Data Structure and Access
  - File formats
    - Two CSV files for rainfall and river inflows.
    - One georeferenced TIFF for maximum water depth.
  - Structure details
    - CSVs: one header line, a column per location/gauge.
    TIFF: georeferenced 30m grid, raster values representing max depth per cell.
  - Geospatial context
    - Gauge coordinates, river inflow discharge points, and grid-based depth data tied to Jakarta metropolitan area.

- Gaps, Challenges, and Considerations for Data Leaders
  - Data fragmentation: scattered across separate files with different modelling origins (rainfall gauges vs. hydrological model outputs vs. hydrodynamic model outputs).
  - Granularity and integration: depth data is grid-based (30m) while inflows are at discrete points; aligning these for integrated analyses requires careful metadata and potential aggregation.
  - Urban features: CityCAT depth model excludes buildings, potentially limiting urban flood modelling accuracy in dense areas.
  - Metadata and discoverability: explicit metadata (temporal resolution, coordinate reference systems, data lineage) should be standardized to improve discoverability and reuse.
  - Reproducibility: calibration steps are documented but may require formal versioning and provenance tracking for ongoing use.

- Implications and Recommendations for Data Leaders
  - Establish a data catalog with consistent metadata schemas across datasets (units, timeframes, resolution, coordinate systems, data provenance).
  - Standardize naming conventions and data dictionaries to enable cross-dataset joins (rainfall gauges, inflow points, depth grid cells).
  - Document calibration and validation workflows as data lineage to support reproducibility and governance.
  - Consider extending the dataset to include urban building data or adjust CityCAT inputs to incorporate urban features for improved depth modelling.
  - Define access, sharing, and update policies to maintain data freshness and ensure responsible use of model outputs.