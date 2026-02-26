# Data from automatic water monitoring buoy from Esthwaite Water 2008, 2009, 2010 and 2011. Jones, I., Feuchtmayr, H. (2017)

## Overview
- Autonomous lake buoy dataset from Esthwaite Water, Cumbria, England, covering 2008–2011.
- Measurements include air temperature, solar radiation, wind speed, and lake water temperatures at multiple depths.
- Data intended to support understanding of lake thermal structure and hydrological processes; used in several publications and by PhD researchers.

## Sampling regime and collection methods
- Instruments: meteorological sensors on the buoy and in-lake temperature sensors.
- Temperature depths: 0.43, 1.43, 2.43, 3.43, 4.43, 5.43, 6.43, 7.43, 8.43, 9.43, 10.43, and 11.43 m.
- Measurements: every 4 minutes; hourly averages calculated by a Campbell Scientific datalogger.
- Time reference: all data in GMT (Greenwich Mean Time).
- Depths and units described (degrees C for temperatures; Watts/m^2 for solar radiation; m/s for wind; GMT timestamp).

## Quality control
- Data provided as raw (not yet calibrated or quality controlled).
- Visual checks performed; obvious hardware errors removed.
- Gaps due to buoy maintenance or sensor/logger problems.
- 2010 January experienced ice cover and buoy damage, causing loss of temperature data.

## Data structure
- Format: comma-separated values (CSV).
- Columns include:
  - Date_GMT: date and time of measurement (GMT).
  - 0.43m, 1.43m, 2.43m, 3.43m, 4.43m, 5.43m, 6.43m, 7.43m, 8.43m, 9.43m, 10.43m, 11.43m: water temperature at specified depths (°C).
  - Air_Temperature: air temperature (°C).
  - Pyranometer: solar radiation flux (W/m^2).
  - Wind_Speed: wind speed (m/s).

## Usage and publications
- The buoy data underpin several scientific studies, including:
  - Woolway et al. (2014) on estimating onset of thermal stratification from surface measurements.
  - Woolway et al. (2015) on diel variability in epilimnetic temperature across multiple lakes.
  - Mackay et al. (2011–2014) on sediment processes and heterogeneity in small lakes.
  - Additional related works cited in the dataset description.
- Dataset used by PhD students and ongoing studies, indicating its ongoing relevance for lake monitoring research.

## Relevance to monitoring frameworks
- Demonstrates practical data collection from autonomous in-situ sensors, including multiple depth measurements and meteorological variables.
- Highlights governance considerations:
  - Need for metadata on measurement depths, units, timestamps, and data provenance.
  - Importance of quality assurance, data cleaning, and transparency about raw vs. processed data.
  - Implications of data sharing: public accessibility of underlying data and associated metadata.
  - Handling data gaps and sensor/site maintenance in long-term monitoring programs.