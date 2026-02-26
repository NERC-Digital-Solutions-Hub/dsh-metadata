# Experimental design/Sampling regime

- Purpose and scope
  - 15-minute river stage height data collected for 6 monitoring stations in the Conwy catchment, North Wales, covering 2013–2016.
  - At Cwm Llanerch, water temperature was also sampled.
  - Data gaps due to equipment, battery, or system failures are noted.

- Sites and parameters sampled
  - Cwm Llanerch: water level (mm) and water temperature (°C); coordinates 53.106627, -3.7916149.
  - Glasgwm: water level (mm); coordinates 53.027723, -3.8462502.
  - Nant y Brwyn: water level (mm); coordinates 52.990162, -3.8018288.
  - Nant y Coed: water level (mm); coordinates 53.049063, -3.7183329.
  - Hiraethlyn: water level (mm); coordinates 53.204355, -3.7827381.
  - Dyffryn Mymbyr: water level (mm); coordinates 53.089587, -3.9718091.

- Data collection methods
  - Water level recorded every 10 seconds; mean value stored every 15 minutes.
  - Cwm Llanerch temperature recorded with the same sampling cadence as depth data.

- Instrumentation and field setup
  - All sites (except Cwm Llanerch) used Druck PDCR 1830 pressure transducers with Campbell CR10 data loggers.
  - Cwm Llanerch used Campbell CS451 pressure transducer with Campbell CR1000 data logger.
  - Transducers located in still wells at the channel edge.
  - Replacement kit at Cwm Llanerch due to discontinuation of CR10x/PDCR equipment; CS451/CR1000 installed as substitute.

- Calibration
  - Druck PDCR 1830 sensors calibrated at CEH Wallingford (2013).
  - CS451 transducer at Cwm Llanerch was factory-calibrated prior to deployment.

- Data structure and content
  - Data stored in separate CSV files for each site; filenames indicate site and time span (e.g., 2013–2016).
  - Common columns (for all sites except Cwm Llanerch): ID, Date (dd/mm/yyyy), Time (hh:mm:ss), Stage_ht_mm (water level above transducer, mm), Battery_volt (logger/transducer power in Volts).
  - Cwm Llanerch file includes an additional Temp_degC column (water temperature in °C).
  - Nature/units: Stage_ht_mm is the water height above the transducer (mm); Battery_volt is the logger/battery voltage (V); Temp_degC is water temperature (°C).

- Quality control
  - Routine site visits and data downloads with visual checks for anomalies.
  - Primary issues: periods with no data due to power failures, resolved by site visits to replace batteries.

- Data availability and misc notes
  - Data coverage spans 2013–2016, with 6 monitoring locations.
  - Data gaps acknowledged (equipment/battery/system failures).
  - Supporting information provides start/end dates by site; for example:
    - Cwm Llanerch: start 12/03/2013 (approx.) to 03/02/2016.
    - Glasgwm: start around 18/04/2013 to 01/03/2016.
    - Nant y Brwyn: start around 11/03/2013 to 01/03/2016.
    - Nant y Coed: start around 21/03/2013 to 01/01/2016.
    - Hiraethlyn: start around 05/11/2013 to 01/01/2016.
    - Dyffryn Mymbyr: start around 14/03/2013 to 04/02/2016.