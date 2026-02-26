# Supporting documentation

- Purpose: Dataset for validation of a potassium sensor intended for plant stems, showing sensor sensitivity and selectivity. In vitro validation data are included; in vivo validation is ongoing.
- Equipment and conditions: Measurements taken with a Keysight B1500A semiconductor device analyzer and an Ag/AgCl gate electrode inside a Faraday cage, under ambient conditions (40% RH, 20 °C, ambient light).

## Experimental setup and collection methods
- Structure: A PDMS well confines the analyte over the sensor; deionized water used as the baseline.
- Procedure: Real-time drain current recorded at fixed voltages (VG = 0 V, VD = -0.4 V) while stepwise increasing ion concentrations.
- Data capture: Changes in drain current tracked as K+ concentration increases.

## Data files and structure
- Potassium_sensor_target_ion_data.csv: Drain current recorded with stepwise K+ concentrations; concentrations: DI water, 1, 10, 20, 40, 80 mM.
- Potassium_sensor_interfering_ion_data.csv: Drain current recorded with stepwise Na+ concentrations as an interfering ion; concentrations: DI water, 1, 10, 20, 40, 80 mM.
- Potassium_sensor_invitro_data.csv: Artificial sap containing interfering ions at max expected levels (Na+ 15 mM, Ca2+ 10 mM, Mg2+ 15 mM); after stabilization, K+ concentration increased from 1 to 80 mM.
- All files share the same five columns: Time_second, Drain_current, Gate_current, Gate_voltage, Drain_voltage.

## Data fields and units
- Time_second: Real-time recording time in seconds.
- Drain_current, Gate_current: Currents in Amperes.
- Gate_voltage, Drain_voltage: Voltages in Volts.

## Data quality and provenance
- Quality control: Five sensors were validated; dataset is representative of in vitro validation.
- Data structure: Each CSV contains the same five columns for consistent cross-file comparison.
- Notes: In vivo validation is not yet included in this dataset.

## Layout design
- A layout design for fabrication of sensors is referenced but not detailed in the provided data.

## How to use and potential data products
- Analyses to perform:
  - Plot Drain_current versus Time_second for each concentration step to assess response dynamics.
  - Convert to sensor response versus K+ concentration to derive sensitivity and linearity.
  - Evaluate selectivity by comparing responses in Potassium_sensor_target_ion_data.csv vs Potassium_sensor_interfering_ion_data.csv.
  - Assess interference effects under artificial sap conditions (Potassium_sensor_invitro_data.csv).
- Data products to create:
  - Self-service dashboards showing real-time sensor response and calibration curves.
  - Summary reports highlighting sensitivity, selectivity, and robustness to interfering ions.
  - Guidance materials for end users on interpreting drain/gate current changes and operating voltages.
- Integration ideas:
  - Combine in vitro data with ongoing in vivo validation data as it becomes available.
  - Normalize drain current to baseline to facilitate cross-sensor comparisons.