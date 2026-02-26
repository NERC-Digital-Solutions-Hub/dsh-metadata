# Jakarta rainfall, river inflows and water depth data (Jan-Feb 2007)

## Overview
- A three-part data package for Jakarta rainfall, river inflows, and flood depth modeling covering 20 January 2007 00:00 to 8 February 2007 23:00.
- Datasets enable cross-analysis of observed rainfall, modeled inflows, and resulting maximum water depths at a 30 m grid resolution.

## Datasets Included
- Jakarta-rainfall-jan-feb2007.csv: hourly rainfall (mm/hr) from 8 raingauges; columns correspond to each gauge; header line present.
- Jakarta-riverInflows-jan-feb-2007.csv: hourly modeled river inflows (m3/s) at 7 discharge points feeding Jakarta; columns correspond to each point; header line present.
- Jakarta-Jan-Feb2007_max_water_depth.tiff: georeferenced 30 m grid of maximum water depths (meters) from CityCAT model.

## Data Collection and Methods

- Rainfall data
  - Source: 8 raingauges in the Jakarta metropolitan area; coordinates provided (Depok, Pondok, Curug, Tg.Priuk, Jakarta_BMKG, Halim, Cengkareng, Dermaga).
  - Temporal coverage: 20/01/2007 00:00 to 08/02/2007 23:00.
  - Units: mm/hr.
  - Quality: hourly and daily totals checked for inconsistencies and spurious values.
  - Purpose: Jakarta_BMKG rainfall used to disaggregate daily rainfall to other locations.

- River inflows (modeled)
  - Location: 7 discharge points (Cisande, Ciliwung, Kalibekasi1–5) feeding the Jakarta area; coordinates provided.
  - Temporal coverage: 20/01/2007 00:00 to 08/02/2007 23:00.
  - Units: m3/s.
  - Quality: outputs from a calibrated Shetran hydrological model.
  - Design/calibration: 3 catchments modeled (Cisande, Ciliwung, Kalibekasi); calibration for Cisande daily discharge (Batubela, 2003) and Ciliwung hourly discharge (Katulampa, 2002–2005 and 2007–2008); Kalibekasi parameterized using Ciliwung.
  - Output: hourly model results at 30 m grid resolution.

- Water depth (flood extent)
  - Model: CityCAT hydrodynamic model for Jakarta.
  - Temporal/spatial: hourly outputs on a 30 m grid; georeferenced TIFF of maximum water depth (meters).
  - Data inputs: DEM (aw3d30 elevations) and OpenStreetMap river network embedded in the DEM; rainfall and lateral inflows drawn from the other files; buildings not included.
  - Quality and validation: model outputs include maximum depths; calibration/validation performed against observed flood impacts (measured displaced people and flood damage).

## Data Structure and Formats
- Rainfall: CSV with a single header line; one column per raingauge; values in mm/hr.
- River inflows: CSV with a single header line; one column per discharge point; values in m3/s.
- Water depth: Georeferenced TIFF grid (30 m resolution) of maximum depths (meters).

## Timeframe and Coverage
- Overall period: 20 January 2007 00:00 to 8 February 2007 23:00.

## Data Quality and Processing
- Rainfall data subjected to quality checks on hourly and daily totals to identify inconsistencies.
- River inflows derived from a calibrated hydrological model (Shetran); calibration steps documented for individual catchments.
- Flood depth modeled with CityCAT; validation against human impact metrics (displacements, flood damage).

## Reuse and Applications
- Supports data exploration and self-serve analysis of rainfall, river inflows, and flood depth within Jakarta for Jan–Feb 2007.
- Enables cross-dataset analyses to assess flood risk, model validation, and scenario planning.
- Suitable for GIS-enabled dashboards, mapping of inundation extents, and comparative studies across observed and modeled data.

## Considerations and Limitations
- CityCAT model does not include buildings; results reflect hydrodynamics with DEM-based topography and river network.
- Buildings absence and model calibration specifics should be considered when interpreting flood depths and damages.
- Data integration requires aligning time steps across observed rainfall, modeled inflows, and depth outputs; unit consistency is essential (mm/hr, m3/s, meters).