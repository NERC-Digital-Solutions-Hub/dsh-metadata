# Supporting documentation

- The dataset validates a potassium sensor intended for insertion into a plant stem. It focuses on the sensor’s sensitivity and selectivity in vitro; in vivo tomato-stem validation is ongoing.

- The data were collected using a Keysight B1500A semiconductor device analyzer with an Ag/AgCl pellet as the gate electrode, inside a Faraday cage under ambient conditions (40% relative humidity, 20 °C, ambient light).

- Experimental setup:
  - A small PDMS well was placed on the sensor to confine the analyte solution.
  - Gate voltage (Vg) = 0 V; Drain voltage (Vd) = -0.4 V (constant during measurements).
  - Real-time drain current was recorded as the K+ concentration was increased stepwise (DI water baseline, then 1, 10, 20, 40, 80 mM K+).

- Data files and structure:
  - Potassium_sensor_target_ion_data.csv: records drain current as K+ concentration steps through 1, 10, 20, 40, 80 mM (DI water baseline).
  - Potassium_sensor_interfering_ion_data.csv: records drain current with a stepwise increase in Na+ (interfering ion) at the same concentrations (1, 10, 20, 40, 80 mM).
  - Potassium_sensor_invitro_data.csv: artificial sap prepared with interfering ions (Na+ 15 mM, Ca2+ 10 mM, Mg2+ 15 mM); after baseline stabilization, K+ is increased from 1 to 80 mM.
  - All three CSV files share five columns: Time_second, Drain_current, Gate_current, Gate_voltage, Drain_voltage.

- Measurements and units:
  - Time_second: real-time recording in seconds.
  - Drain_current, Gate_current: currents in amperes.
  - Gate_voltage, Drain_voltage: voltages in volts.

- Quality and scope:
  - Five sensors were validated; the dataset represents in vitro validation.
  - The dataset supports assessment of K+ sensing performance, selectivity against Na+, and behavior in artificial sap.
  - There is a layout design section referenced for sensor fabrication.