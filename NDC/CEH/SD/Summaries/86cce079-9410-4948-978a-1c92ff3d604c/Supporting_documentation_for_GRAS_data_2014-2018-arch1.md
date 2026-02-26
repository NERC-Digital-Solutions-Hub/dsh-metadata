# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Grasmere 2014 to 2018.

- Purpose and scope
  - Long-term monitoring dataset from Grasmere, Cumbria, England, with fortnightly sampling from January 2014 to March 2018.
  - Aims to measure surface temperature, surface oxygen, water clarity, water chemistry, and phytoplankton chlorophyll a to support ecological analyses and environmental assessments.

- Variables and units included
  - TEMP: surface temperature (°C)
  - OXYG: surface oxygen saturation (% air-saturation)
  - SECC: Secchi depth (m)
  - ALKA: alkalinity (µg CaCO3 per L)
  - pH: pH
  - NH4N: ammonium (µg N per L)
  - NO3N: nitrate (µg N per L)
  - PO4P: soluble reactive phosphate (µg P per L)
  - TOTP: total phosphorus (µg P per L)
  - SIO2: dissolved reactive silicon (µg per L)
  - TOCA: phytoplankton chlorophyll a (µg per L)

- Sampling regime and Method
  - Water samples integrated from 0 to 5 m.
  - Collected from a boat at the deepest part of the lake (buoy); when not possible, samples taken from the shore.
  - Measurements include surface temperature and oxygen at the measurement site; sampling chronology for 2014–2018.

- Data quality and limitations
  - Data are raw and have not been quality controlled or calibrated.
  - Double entered and visually checked; some data missing due to weather or staff shortages.
  - Some samples were not integrated (Flag 2) when buoy sampling was not possible.

- Data structure and format
  - Delivered as a CSV with columns:
    - Date: measurement date
    - Variable, Description: the measured parameter
    - Value, Description: measurement value
    - Sign (if<LOD): indicates values below detection limit (a "<" sign)
    - Flag: 1 = buoy-site sample, 2 = shore sample
  - Example publications cite the dataset’s use in broader ecological and geochemical studies.

- End date and accessibility
  - Long-term monitoring ended in March 2018 due to funding shortages.
  - Data are available for download; includes raw measurements to support reanalysis and model development.

- Context and usage
  - Referenced in several publications exploring lake biogeochemistry and carbon-silicon cycles, demonstrating potential uses for time-series analysis, trend detection, and coupling of biological and chemical processes.
  - Related overview works provide context on long-term ecological data generation and informatics.