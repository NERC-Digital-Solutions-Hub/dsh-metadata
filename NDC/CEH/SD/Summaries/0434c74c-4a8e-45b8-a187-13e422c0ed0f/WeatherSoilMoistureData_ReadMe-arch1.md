# ReadMe file for WeatherSoilMoistureData.csv

## Overview
- Measurements include rainfall, soil temperature at 5 cm depth, air temperature, and soil water-filled pore space (WFPS) at 5 cm and 10 cm depths.
- Collected at Henfaes Research Station, Abergwyngregyn, North Wales (270 m above sea level; 53°13'N, 4°0'W).
- Time period encompasses seasonal sheep urine application studies.
- Weather data come from a meteorological station at the experimental site; soil moisture via calibrated sensors.

## Data provenance and sensors
- Weather data: collected from a Skye Instruments meteorological station installed at the site.
- Soil moisture: calculated WFPS from 10HS Moisture Sensor (Decagon Devices Inc.), calibrated for volumetric water content per manufacturer instructions.
- Data are stored in WeatherSoilMoistureData.csv; authors must be acknowledged if data are reused or reproduced.

## Data headers and structure
- TimeDate: date and time of measurements (format: dd/mm/yyyy hh:mm:ss)
- Rain_mm: rainfall in millimeters (mm)
- SoilTemp_5cm: soil temperature at 5 cm depth (°C)
- AirTemp: air temperature (°C)
- WFPS_5: soil water-filled pore space at 5 cm depth (%)
- WFPS_10: soil water-filled pore space at 10 cm depth (%)

## Considerations for analysis
- The dataset enables exploring correlations between rainfall, air/soil temperatures, and soil moisture at two depths.
- Suitable for developing predictive models of soil moisture response to precipitation and temperature stimuli within the study site context.