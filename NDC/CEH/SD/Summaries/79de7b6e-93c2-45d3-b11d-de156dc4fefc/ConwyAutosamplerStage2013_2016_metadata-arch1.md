# Experimental design/Sampling regime

- Study scope: 15-minute river stage height data for 6 monitoring stations in the Conwy catchment, North Wales, collected 2013–2016; Cwm Llanerch also includes water temperature data.
- Project context: Data collection by CEH for the NERC project NE/J011991/1, with gaps due to equipment/battery or system failures.

- Location and sites
  - Cwm Llanerch (with water temperature sampled)
  - Glasgwm
  - Nant y Brwyn
  - Nant y Coed
  - Hiraethlyn
  - Dyffryn Mymbyr
  - Coordinates provided for all sites; data availability start/end dates documented per site.

- Data collected and units
  - Water level: Stage_ht_mm (millimetres above the transducer)
  - Battery voltage: Battery_volt (Volts)
  - Temperature: Temp_degC (degrees Celsius; only at Cwm Llanerch)
  - Notes: Temperature data available only where specified; data structure includes an extra Temp_degC column for Cwm Llanerch.

- Sampling and measurements
  - Water level recorded every 10 seconds; mean value stored every 15 minutes on data loggers.
  - Temperature (Cwm Llanerch) sampled and recorded with the same cadence.

- Instrumentation and sampling regime
  - Five sites (Glasgwm, Nant y Brwyn, Nant y Coed, Hiraethlyn, Dyffryn Mymbyr): Druck PDCR 1830 pressure transducers + Campbell Scientific CR10 data loggers.
  - Cwm Llanerch site: Campbell CS451 pressure transducer + Campbell CR1000 logger.
  - Instrument changes explained by equipment discontinuation and availability at CEH stores.

- Calibration and quality assurance
  - Druck PDCR 1830 calibrated in 2013 using Druck DPI 510 at CEH Wallingford.
  - CS451 transducer at Cwm Llanerch was new and factory calibrated before deployment.
  - Routine QA: data checks during site visits; power failures are the main cause of data gaps.

- Data storage, structure, and metadata
  - Data organized as separate CSV files per site; filenames indicate site and time span (example: 2013-2016).
  - Five sites (Dyffryn Mymbyr, Glasgwm, Hiraethlyn, Nant y Coed, Nant y Brwyn): 5 columns per file
    - ID, Date, Time, Stage_ht_mm, Battery_volt
  - Cwm Llanerch files include an additional Temp_degC column.
  - Data downloaded to field laptop and then uploaded to an Access database.
  - Supporting metadata provided: site coordinates; start/end dates for data availability (note: some year fields appear truncated in the source).

- Data accessibility and potential issues for analysts
  - Data gaps due to power/battery failures; typically resolved by site visits and battery changes.
  - Variability in instrumentation across sites may affect cross-site comparability.
  - Raw data stored in CSVs with clear site-based organization; metadata facilitates data discovery.