# Groundwater level information for 10 locations within the Gandak River Basin, in Bihar,    India are presented.

## General overview
- Groundwater level data for 10 locations in the Gandak River Basin, Bihar, India.
- Collected under the CHANSE (Coupled Human And Natural Systems Environment) project.
- Recording period: April 2017 to February 2019.
- Instrument: Troll automatic groundwater level loggers with measurements every 15 minutes.
- Data are corrected to local barometric pressure using Troll barometer readings.

## Variable description
- DateTime: date and time of recording.
- Temp: water temperature.
- mbgl: depth to water level below ground level as recorded by the logger.
- man_mbgl: manually measured depth to groundwater level (dip meter).
- PT: pressure transducer.
- Baro: barometer reading.
- Missing values are recorded as blanks.

## Site locations and metadata
- Ten sites are listed with location and instrument details, including:
  - Site name (e.g., Chinta Manpur, Bagaha 1, Bagaha, Bagaha 3, Bettiah 1, Bettiah 2, Bettiah 3, Lalganj Basanta, Bettia4, Chalabhar).
  - Geographic coordinates (longitude and latitude).
  - Depth_to_base_mbgl (depth to borehole base) and depth_to_water_level_on_installation_mbgl (water level depth at installation).
  - Installation date and last download date.
  - Months of record (varying per site, as reported in the dataset).

## Notes on data structure
- The dataset provides both logger-derived depths (mbgl) and manually measured depths (man_mbgl) for calibration and validation.
- Site records indicate data coverage spans multiple months per site, with installation and download timestamps, enabling temporal analyses.
- Some fields in the site table show formatting inconsistencies (likely transcription artifacts), but the key metadata fields (coordinates, installation/download dates, depths, and months of record) are present.

## Purpose and potential uses
- Enables analysis of groundwater depth trends across multiple locations in the Gandak Basin.
- Supports assessment of spatial and temporal variability, correlations with climatic factors, and potential predictive modeling for groundwater management.
- Data can be linked with CHANSE-derived environmental and human-system indicators to inform decision-making.