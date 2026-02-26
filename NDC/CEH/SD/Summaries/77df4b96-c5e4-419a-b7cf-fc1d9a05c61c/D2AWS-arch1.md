# Automatic Weather Station recordings from Moor House and Helbeck, Cumbria, 1974 - 1987

## Overview
- A historic dataset of Automatic Weather Station (AWS) measurements from Moor House and Helbeck, Cumbria, UK.
- Collected by Ken Taylor and stored in a database described by Cuthbertson (1993).
- Covers data recorded between 1974 and 1987, with multiple recording periods and frequencies (hourly and daily).

## Site locations and context
- Helbeck AWS: located in a wood near Brough, Cumbria; grid reference 378900 516000.
- Moor House AWS: grid reference 375100 533400.
- The UK Environmental Change Network (ECN) has continued monitoring at Moor House (Rennie et al., 2017).

## Recording locations and temporal resolutions
- The dataset includes multiple blocks with different time spans and sampling frequencies (identified by DATID):
  - Helbeck: hourly readings; earliest 01-Jan-78 to 18-Oct-83.
  - Helbeck: May 1974 – June 1978; hourly readings.
  - Helbeck: May 1974 – June 1978; daily readings.
  - Moor House: July 1974 – August 1979; daily readings.
  - Moor House: 01-Jan-1979 to 08-Feb-1987; hourly readings.
  - Moor House: July 1974 – August 1979; hourly readings.

## Variables and data encoding
- DATID: Data set identification record number.
- NO_REC: Number of recordings used to establish the values of the record.
- REC_TIME: Date when the reading was recorded (DD-MM-YYYY).
- REC_HOUR: Hour of the reading (0–23).
- SOL_RAD: Solar radiation (W/m^2).
- AIR_TEMP: Air temperature (°C).
- DEP_TEMP: Temperature depression (°C) — difference between dry and wet bulb temperatures; proxy for humidity.
- WIND_VEL: Wind velocity (km/h).
- WIND_DIR: Wind direction.
- RAINFALL: Rainfall (mm).

## Data quality, limitations, and considerations
- There are missing values within the historic dataset; the reasons for missing data are unknown.
- Quality assurance procedures for this historical data are unknown.
- Potential issues to consider when using the data:
  - Different recording frequencies (hourly vs. daily) and periods of coverage across sites.
  - Variations in measurement conditions and instrumentation over time.
  - Incomplete metadata on data gaps and site maintenance.
- Data provenance indicates original storage in a dedicated environmental database (Cuthbertson, 1993), with later ECN continuity at Moor House (Rennie et al., 2017).

## Provenance and metadata references
- Cuthbertson, M. (1993). A database for environmental research programmes. Journal of Environmental Management, 37(4), 291-300.
- Rennie et al. (2017). UK Environmental Change Network (ECN) meteorology data: 1991-2015. NERC Environmental Information Data Centre. https://doi.org/10.5285/fc9bcd1c-e3fc-4c5a-b569-2fe62d40f2f5

## Potential uses and analyst takeaways
- Time-series analyses of temperature, humidity proxies (DEP_TEMP), wind, solar radiation, and rainfall at two Cumbria sites.
- Cross-site comparisons (Helbeck vs. Moor House) to study local climatic variability in the 1970s–1980s.
- Integration with ECN data for extended climatological studies at Moor House.
- Development of historical climate models or validation datasets for calibrating environmental impact assessments.

## Notes for analysts
- Validate and document missing data patterns before analysis.
- Align datasets by DATID, recording times, and units to ensure consistency across site and time periods.
- Consider metadata gaps when interpreting trends or correlations, especially around changes in measurement practices or instrumentation.