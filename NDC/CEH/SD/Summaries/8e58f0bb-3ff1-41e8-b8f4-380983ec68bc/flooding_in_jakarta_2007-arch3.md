# Jakarta rainfall, river inflows and maximum water depth (Jan-Feb 2007)

## Overview
- A data package describing rainfall observations, modeled river inflows, and maximum water depth for the Jakarta metropolitan area during 20 January 2007 to 8 February 2007.
- Includes three files: rainfall observations, modeled river inflows, and a georeferenced maximum water depth raster.
- Data are intended to support flood risk assessment, hydrological/modelling validation, and informing policy monitoring and decision-making.

## Data Files and Contents
- Jakarta-rainfall-jan-feb2007.csv
  - Hourly rainfall (mm/hr) from 8 raingauges in the Jakarta area.
  - Raingauge locations and coordinates: Depok (SRS682), Pondok (SRS779), Curug (BMKG3), Tg.Priuk (BMKG4), Jakarta_BMKG (BMKG5), Halim (BMKG6), Cengkareng (BMKG7), Dermaga (BMKG9).
  - Time period: 20/01/2007 00:00 to 08/02/2007 23:00.
  - Quality control: hourly and daily totals checked for inconsistencies and spurious values.
  - Data structure: CSV with a column per raingauge and a header line.
  - Notes: Jakarta_BMKG rainfall data used to disaggregate daily rainfall at other locations.
- Jakarta-riverInflows-jan-feb-2007.csv
  - Hourly modeled river inflows (m3/s) for 7 discharge points that feed the Jakarta area.
  - Inflow locations: Cisande, Ciliwung, Kalibekasi1–Kalibekasi5 with coordinates provided.
  - Time period: 20/01/2007 00:00 to 08/02/2007 23:00.
  - Quality control: output from calibrated Shetran hydrological model.
  - Data structure: CSV with a column for each discharge point and a header line.
  - Experimental design: Shetran model run for 3 catchments (Cisande, Ciliwung, Kalibekasi); hourly discharges produced for the Jakarta inflow aggregation.
  - Calibration notes: daily discharge calibration for Cisande (Batubela, 2003); hourly discharge calibration for Ciliwung (Katulampa, 2002–2005, 2007–2008); Kalibekasi uses the same parameters as Ciliwung.
  - Fieldwork/Instrument: Model output.
- Jakarta-Jan-Feb2007_max_water_depth.tiff
  - Maximum modeled water depth per 30 m x 30 m grid square (meters).
  - Quality control: CityCAT hydrodynamic model outputs used for depth; validation against observed displacement and damages.
  - Data structure: Georeferenced TIFF file.
  - Experimental design: CityCAT hydrodynamic model configured for Jakarta; uses aw3d30 DEM elevations; OpenStreetMap river network embedded in the DEM; rainfall and lateral inflows sourced from the other files; no buildings included.
  - Fieldwork/Instrument: Model output.
  - Calibration/Validation: Model validation performed against measured displacement and damage data.

## Methods and Modelling Details
- Rainfall data collection
  - Hourly observations from 8 raingauges; rainfall data used to disaggregate daily rainfall at other locations.
  - Calibration/quality checks applied to hourly totals and daily totals.
- River inflows modelling
  - Hydrological modelling with Shetran for three catchments (Cisande, Ciliwung, Kalibekasi).
  - Calibration steps include daily discharge calibration for Cisande and hourly discharge calibrations for Ciliwung; Kalibekasi adopts Ciliwung parameters.
  - 30 m grid resolution for spatial representation of inflows.
- Flood depth modelling
  - CityCAT hydrodynamic model driven by rainfall-derived inflows and lateral inflows from the river network.
  - DEM: aw3d30; river network from OpenStreetMap embedded in the DEM; buildings not included in this version.
  - Model outputs include maximum water depth per grid cell; validation against numbers of displaced people and flood-related damages.
  - Outputs integrated with rainfall and inflow data for interpretation of flood extent and severity.

## Data Quality, Metadata and Governance Considerations
- Quality control measures implemented at data collection and model outputs, including checks for inconsistencies and spurious values, and calibration/validation against observed outcomes.
- Metadata considerations include multiple data sources, spatial coordinates, units, and model parameters; standardised structure (CSV for time series, TIFF for spatial depths) facilitates reproducibility and governance.
- Data transformations (e.g., rainfall disaggregation) and model dependencies (Shetran, CityCAT) are explicitly documented to support interpretation and reuse.

## Applications for Monitoring Frameworks and Policy
- Supports evaluation of flood risk and hydrological responses under a short-term Jakarta event window.
- Enables comparison between observed rainfall, modeled inflows, and modeled flood depths to inform data quality requirements and governance needs.
- Highlights the importance of linking observational datasets with model outputs, transparent calibration steps, and validation against real-world impact metrics (displacements, damages) for policymaking and monitoring.
- Illustrates potential data access and interoperability considerations, such as metadata completeness, data sharing of model inputs/outputs, and handling of data gaps or silos.