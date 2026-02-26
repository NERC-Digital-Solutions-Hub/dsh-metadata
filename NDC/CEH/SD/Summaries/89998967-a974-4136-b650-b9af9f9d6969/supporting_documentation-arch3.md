# Supporting documentation

## Brief description
- Dataset for validation of a potassium sensor intended for insertion into a plant stem.
- Shows sensor sensitivity and selectivity; data collected using a Keysight B1500A semiconductor device analyzer and an Ag/AgCl pellet as gate electrode.
- Measurements conducted inside a Faraday cage under ambient conditions (40% RH, 20 °C) and ambient light.
- In vivo validation in tomato stems ongoing; this dataset includes in vitro validation data only.

## Collection methods
- A small PDMS well attached atop the sensor confines the analyte solution.
- DI water baseline; drain current recorded at fixed gate and drain voltages (VG = 0 V, VD = -0.4 V) while varying ion concentrations.
- Potassium_target_ion_data: stepwise K+ concentrations from 1 to 80 mM (DI water baseline; 1, 10, 20, 40, 80 mM).
- Potassium_interfering_ion_data: Na+ as interfering ion, stepwise 1 to 80 mM.
- Potassium_invitro_data: Artificial sap with interfering ions (Na+ 15 mM, Ca2+ 10 mM, Mg2+ 15 mM) used; baseline stabilized in sap, then K+ increased from 1 to 80 mM.

## Data files
- Potassium_sensor_target_ion_data.csv: drain current recorded vs time for stepwise K+ concentrations.
- Potassium_sensor_interfering_ion_data.csv: drain current recorded vs time for stepwise Na+ concentrations.
- Potassium_sensor_invitro_data.csv: drain current recorded vs time in artificial sap with interfering ions, during K+ concentration increases.
- Each CSV contains five columns: Time_second, Drain_current, Gate_current, Gate_voltage, Drain_voltage.

## Nature and units of recorded values
- Time_second: real-time recording (seconds).
- Drain_current, Gate_current: currents (amperes).
- Gate_voltage, Drain_voltage: voltages (volts) applied to gate and drain electrodes.

## Quality control
- Five sensors validated; dataset is representative of in vitro validation.

## Details of data structure
- Three CSV files, each with three ion-concentration experiments.
- All files share consistent structure: five columns (Time_second, Drain_current, Gate_current, Gate_voltage, Drain_voltage).

## Layout design for fabrication of sensors
- Includes a section titled "Layout design for fabrication of sensors" (no additional details provided within this dataset).