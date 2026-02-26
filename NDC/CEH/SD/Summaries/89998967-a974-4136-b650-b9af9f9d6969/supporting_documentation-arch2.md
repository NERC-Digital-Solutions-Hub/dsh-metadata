# Supporting documentation

## Overview
- Dataset validates a potassium sensor intended for insertion into a plant stem.
- Focuses on sensitivity and selectivity of the fabricated sensor.
- In vivo validation inside a tomato stem is ongoing; dataset includes in vitro validation only.

## Data and measurement context
- Real-time drain current responses are recorded as ion concentrations change.
- Measurements performed with fixed gate and drain voltages:
  - Gate voltage V_G = 0 V
  - Drain voltage V_D = -0.4 V
- Ambient, in vitro conditions:
  - 40% relative humidity, 20 °C, ambient light
- Equipment:
  - Semiconductor device analyzer (Keysight B1500A)
  - Ag/AgCl pellet as gate electrode
  - Faraday cage

## Collection methods
- A small PDMS well confines analyte solution atop the sensor to enable stepwise ion concentration changes.
- Procedure:
  - Start with DI water; record drain current continuously at fixed voltages.
  - Increment K+ concentration stepwise to 1, 10, 20, 40, 80 mM.
- Interfering ion test uses Na+ at the same stepwise concentrations.
- In vitro validation uses artificial sap containing interfering ions (Na+ 15 mM, Ca2+ 10 mM, Mg2+ 15 mM) with subsequent K+ concentration increases from 1 to 80 mM.

## Data files and structure
- Files:
  - Potassium_sensor_target_ion_data.csv
  - Potassium_sensor_interfering_ion_data.csv
  - Potassium_sensor_invitro_data.csv
- Common structure: each CSV has five columns
  - Time_second
  - Drain_current
  - Gate_current
  - Gate_voltage
  - Drain_voltage

## Sensor validation and quality control
- Five sensors validated; dataset is representative of in vitro validation.
- Data are intended to support verification of sensor performance and comparability across devices.

## Data interpretation and environmental monitoring relevance
- Enables assessment of potassium sensor performance in conditions relevant to plant tissue monitoring.
- Provides standardized data format for evaluating sensitivity to K+ and resistance to interference from Na+ and other ions.
- Helps inform environmental health assessments where plant physiological status and ion balance are indicators.

## Layout and fabrication notes
- Includes a design/layout reference for sensor fabrication.