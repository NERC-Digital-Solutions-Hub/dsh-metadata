# Groundwater level information for 10 locations within the Gandak River Basin, in Bihar, India

- Overview
  - Groundwater level data from 10 locations in the Gandak River Basin, Bihar, India, collected under the CHANSE (Coupled Human And Natural Systems Environment) project.
  - Timeframe: April 2017 to February 2019.
  - Data collection used Troll automatic groundwater level loggers with measurements every 15 minutes.
  - Measurements are corrected to local barometric pressure using a Troll barometer.

- Data collection and instrumentation
  - Automatic logging every 15 minutes.
  - Barometric pressure correction applied to all groundwater level readings.

- Variables and data fields
  - DateTime: timestamp of the recording.
  - Temp: water temperature.
  - mbgl: depth to water level below ground level reported by the logger (meters).
  - man_mbgl: manually measured depth to groundwater level using a dip meter.
  - PT: pressure transducer reading.
  - Baro: barometer reading.
  - Missing values are represented by blanks.

- Site locations and metadata
  - Ten sites are listed with coordinates (longitude and latitude), installation depth to base (mbgl), installation depth to water level (mbgl), installation date, last download date, and months of record.
  - Sites include: Chinta Manpur, Bagaha 1, Bagaha, Bagaha 3, Bettiah 1, Bettiah 2, Bettiah 3, Lalganj Basanta, Bettia4, Chalabhar.
  - Installation dates range from March 2017 to March 2018; last download dates go up to February 2019.
  - Depth to base (mbgl) and depth to water level at installation (mbgl) vary by site, indicating different well depths and initial water levels.
  - Recorded months of data per site vary (examples observed in the table include values such as 10.5 and 22 months, though the exact figures are inconsistently formatted in the source).

- Data quality, completeness, and notes
  - Data are aligned to a common time frame (2017–2019) and standardized with barometric corrections.
  - Some fields in the site table show formatting inconsistencies; users may need to clean or harmonize certain entries (e.g., coordinate formatting, date formats, and numeric fields).
  - Both logger-based (mbgl) and manual (man_mbgl) measurements are present, enabling cross-validation but requiring careful reconciliation.
  - Missing values are represented as blanks, so downstream analyses should account for gaps.

- Relevance and potential uses for data leaders
  - Provides multi-site groundwater level observations across a regulatory basin, suitable for trend analysis, groundwater resource assessment, and policy support.
  - Metadata supports data discovery, provenance, and governance (sensor type, calibration basis, and installation/last-downloaded timestamps).
  - The combination of automated and manual measurements enables data quality checks and calibration opportunities.
  - Highlights data governance considerations: need for consistent metadata standards, data formatting, and ongoing data updates to maintain discoverability and usability.

- Actions and considerations for leveraging the dataset
  - Validate and harmonize mbgl vs. man_mbgl readings to ensure consistency across sites.
  - Integrate with other regional datasets to analyze seasonality, trends, and responses to policy interventions.
  - Establish clear data standards for future CHANSE-related groundwater datasets to improve discoverability and collaboration across partners.
  - Plan for ongoing data updates beyond February 2019 to maintain a long-term groundwater monitoring record.