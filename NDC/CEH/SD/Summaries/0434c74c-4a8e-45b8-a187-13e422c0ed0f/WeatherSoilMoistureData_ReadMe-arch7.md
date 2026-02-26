# ReadMe file for WeatherSoilMoistureData.csv

- Overview
  - Dataset includes rainfall (mm), soil temperature at 5 cm depth (°C), air temperature (°C), and soil water-filled pore space (WFPS) at 5 cm and 10 cm depths (%), measured at the Henfaes Research Station, North Wales.
  - Data come from a meteorological station at the site and soil moisture probes calibrated to compute volumetric water content.
  - Measurements span seasonal sheep urine application studies, providing a time-series of weather and soil moisture variables.
  - Suitable for GIS-based time-series analysis or map-based visualization, especially when combined with other spatial datasets.

- Location and context
  - Site: Henfaes Research Station, Abergwyngregyn, North Wales; 270 m above sea level; coordinates 53°13'N, 4°0'W.

- Variables and data headers (with units)
  - TimeDate: date and time of measurements (dd/mm/yyyy hh:mm:ss)
  - Rain_mm: rainfall in millimeters
  - SoilTemp_5cm: soil temperature at 5 cm depth in °C
  - AirTemp: air temperature in °C
  - WFPS_5: soil water-filled pore space at 5 cm depth in %
  - WFPS_10: soil water-filled pore space at 10 cm depth in %

- Data collection and instrumentation
  - Weather data collected from a meteorological station (Skye Instruments Ltd., Llandrindod Wells, UK) installed at the site.
  - Soil moisture derived from 10HS Moisture Sensor probes (Decagon Devices Inc., WA, USA) calibrated per manufacturer instructions to compute volumetric water content.

- Data quality and usage notes
  - Authors must be acknowledged if data are reused or reproduced.
  - The dataset describes a single site; consider time notation and sensor calibration when performing GIS analyses.
  - No explicit data quality metrics provided; users should assess calibration, data gaps, and time alignment during integration.

- GIS and analysis opportunities
  - Create time-series visualizations of rainfall, soil temperature, air temperature, and soil moisture at 5 cm and 10 cm.
  - Combine with other spatial layers for site-level environmental analyses (e.g., soil moisture trends related to rainfall events).
  - Examine relationships between meteorological conditions and soil moisture dynamics across depths.