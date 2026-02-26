# Supporting documentation

## Overview
- Dataset supporting validation of a potassium sensor intended for insertion into a plant stem.
- Focus: in vitro validation data (real-time sensor responses to stepwise changes in K+ concentration); in vivo validation is ongoing.
- Data were collected under ambient conditions (40% relative humidity, 20 °C, ambient light) using a semiconductor device analyzer and an Ag/AgCl pellet as the gate electrode within a Faraday cage.

## Data files and structure
- Three CSV files:
  - Potassium_sensor_target_ion_data.csv
  - Potassium_sensor_interfering_ion_data.csv
  - Potassium_sensor_invitro_data.csv
- Each file contains five columns:
  - Time_second
  - Drain_current
  - Gate_current
  - Gate_voltage
  - Drain_voltage
- All values are recorded while applying fixed gate and drain voltages.

## Data collection methods
- Real-time drain current measured as K+ concentration increases stepwise:
  - DI water baseline with K+ concentrations: 1, 10, 20, 40, 80 mM (target ion dataset).
- Interfering ion assessment:
  - Stepwise Na+ concentrations (1, 10, 20, 40, 80 mM) with DI water baseline (interfering ion dataset).
- In vitro validation in artificial sap:
  - Baseline artificial sap with interfering ions (Na+ 15 mM, Ca2+ 10 mM, Mg2+ 15 mM); K+ then increased from 1 to 80 mM.
- Experimental setup:
  - PDMS well confines analyte solution on top of sensor.
  - Gate voltage V_G = 0 V; Drain voltage V_D = -0.4 V.

## Quality and validation
- Five sensors validated; dataset is representative of in vitro validation.
- Data reflect real-time responses to ion concentration changes under specified conditions.

## Metadata and provenance
- Sensor fabrication and measurement context:
  - Equipment: Keysight B1500A semiconductor device analyzer; Ag/AgCl pellet as gate electrode; Faraday cage.
  - Environment: ambient conditions specified above; ambient light considered.
- Data structure details:
  - Each CSV contains the same five-column schema with consistent units (Time_second in seconds; currents in Amps; voltages in Volts).

## Data sharing and access considerations
- In vivo validation is ongoing; thus, current dataset is limited to in vitro observations.
- Documentation provides clear descriptions of measurement conditions, ion concentrations, and data organization to facilitate reuse and replication.

## Governance and stewardship considerations
- Ensure complete metadata for future datasets (instrument models, electrode types, environmental conditions, and exact protocol steps).
- Maintain consistency in units and column naming across datasets; verify that time units and current/voltage units remain uniform.
- Provide versioning and clear provenance so updated data (e.g., future in vivo data) can be integrated without ambiguity.
- Consider linking datasets to a data catalog entry and assigning a persistent identifier (DOI) to support discoverability.
- Document assumptions and limitations (in vitro focus; ongoing in vivo validation) to guide users on applicability.

## Limitations and caveats
- Data represent in vitro validation only; performance in vivo may differ.
- Sensor responses measured under specific voltages and environmental conditions; extrapolation beyond these conditions should be avoided without additional validation.