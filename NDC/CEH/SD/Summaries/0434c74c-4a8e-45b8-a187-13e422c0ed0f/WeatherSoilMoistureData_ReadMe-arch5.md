# ReadMe file for WeatherSoilMoistureData.csv

## Overview
- Dataset records rainfall, soil temperature at 5 cm, air temperature, and soil water-filled pore space (WFPS) at 5 cm and 10 cm depth.
- Collected at Henfaes Research Station, Abergwyngregyn, North Wales (270 m above sea level; 53°13'N, 4°0'W).
- Time period encompasses seasonal sheep urine application studies.
- Weather data from a meteorological station installed at the site; soil WFPS calculated from 10HS moisture probes calibrated per manufacturer instructions.

## Data collection and measurement methods
- Instruments:
  - Meteorological data from Skye Instruments Ltd. weather station (Llandrindod Wells, UK).
  - Soil moisture from 10HS Moisture Sensor (Decagon Devices Inc., WA, USA).
- Calculations:
  - Soil % water-filled pore space (WFPS) derived from soil moisture data using the manufacturer’s calibration instructions.
- Data management:
  - Data may require author acknowledgment when reused or reproduced.

## Dataset structure and headers
- TimeDate: date and time of measurements (format: dd/mm/yyyy hh:mm:ss).
- Rain_mm: rainfall amount in millimeters.
- SoilTemp_5cm: soil temperature in degrees Celsius at 5 cm depth.
- AirTemp: air temperature in degrees Celsius.
- WFPS_5: soil water-filled pore space (%) at 5 cm depth.
- WFPS_10: soil water-filled pore space (%) at 10 cm depth.

## Data provenance and usage rights
- Authors must be acknowledged in any reuse or reproduction of the data.

## Considerations for data stewardship and reuse
- Clear metadata and consistent header definitions support data discoverability and interoperability.
- Provided unit conventions and measurement depths aid standardized data integration.
- Potential enhancements for future stewardship:
  - Add dataset-level metadata (time span, data quality checks, data validity flags, contact person).
  - Include licensing details, data version, and any known data limitations or gaps.