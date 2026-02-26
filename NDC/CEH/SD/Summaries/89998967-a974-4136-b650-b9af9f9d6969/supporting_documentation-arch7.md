# Supporting documentation

## Overview
- This dataset is for validation of a potassium sensor that will be inserted into a plant stem.
- It demonstrates the sensor's sensitivity and selectivity; current validation is in vitro, with in vivo validation ongoing.

## Data files and contents
- Potassium_sensor_target_ion_data.csv: drain current recorded as K+ concentration steps increase (DI water, 1, 10, 20, 40, 80 mM).
- Potassium_sensor_interfering_ion_data.csv: drain current recorded with Na+ as interfering ion (DI water, 1, 10, 20, 40, 80 mM).
- Potassium_sensor_invitro_data.csv: artificial sap with interfering ions (Na+ 15 mM, Ca2+ 10 mM, Mg2+ 15 mM); baseline current stabilized, then K+ increased from 1 to 80 mM.

## Experimental setup and data collection methods
- A small PDMS well is attached on top of the sensor to confine analyte solution.
- DI water used to establish baseline; real-time responses recorded at fixed voltages.
- Gate voltage Vg = 0 V; drain voltage Vd = -0.4 V.
- Real-time drain current recorded during stepwise increases in ion concentrations.

## Measurements and variables
- Time_second: real-time recording (seconds).
- Drain_current: current measured as ion concentrations change (A).
- Gate_current: current at the gate (A).
- Gate_voltage: applied gate voltage (V).
- Drain_voltage: applied drain voltage (V).

## Data structure and formats
- Three CSV files, each containing five columns: Time_second, Drain_current, Gate_current, Gate_voltage, Drain_voltage.

## Quality control
- Data derived from five validated sensors; dataset is representative of in vitro validation.

## Environmental and experimental conditions
- Ambient conditions: 40% relative humidity, 20 °C, ambient light.

## Additional notes
- Layout design for fabrication of sensors is included. 
- This dataset is non-geospatial and comprises time-series sensor data; to use in a GIS context, geospatial metadata would need to be added separately.