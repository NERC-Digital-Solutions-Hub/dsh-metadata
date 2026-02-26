# Sampling Regime

- Location and timeframe
  - Two small Amazonian streams (NC: New Colpita, MT: Main Trail) in Tambopata National Reserve, Madre de Dios, Peru.
  - Data collected February 2011 – October 2012.
  - Continuous monitoring at 15-minute resolution for water chemistry and hydrology; stage height monitored continuously; discharge derived from stage height and velocity.

- Study sites details
  - NC (New Colpita): perennial stream, upstream area ~7.2 km², width 4.5–7.5 m depending on water level.
  - MT (Main Trail): seasonally active, width 3.5–5 m, upstream area ~4.9 km², dries in dry season (no sampling in Sept–Nov 2011).

- Variables measured (data points and units)
  - Dissolved inorganic carbon (DIC, mg/L)
  - Dissolved organic carbon (DOC, mg/L)
  - Particulate organic carbon (POC, mg/L)
  - Temperature (°C)
  - pH
  - Oxygen saturation (%)
  - Conductivity (µS/cm)
  - Stage height (cm)
  - Flow velocity (m/s) at a fixed point
  - Stream flow (m/s) and Discharge (m³/s)
  - Data organized in 15-minute time steps; missing values denoted as NA

- Sampling campaigns and methods
  - Three field campaigns: Feb–Apr 2011, Sept–Dec 2011, Mar–May 2012.
  - Targeted different flow conditions and seasons to understand hydrological controls on carbon fluxes.
  - DIC/DOC/POC samples collected with triplicates; DIC analyzed with headspace method and δ13C; DOC via filtration and combustion; POC by loss on ignition.
  - Water chemistry measured in the field (pH, conductivity, dissolved oxygen, temperature); stage height measured with Rugged Troll; velocity with a handheld meter; cross sections used to convert velocity to discharge.

- Instrumentation and calibration
  - Field instruments: Troll9500 for chemistry and dissolved oxygen; Rugged Troll for stage height; Flowlink2150 for flow velocity; handheld Geopacks for spot velocity.
  - Calibration and maintenance: Troll9500 calibrated ~monthly; field cleaning performed weekly; two-point pH calibration (pH 4 and 7); conductivity standard; oxygen saturation standards.

- Data structure and metadata
  - CSV files: Perennial_stream_NC and Seasonal_stream_MT.
  - Columns include Site, Date, Time, Temperature, pH, Oxygen saturation, Conductivity, Stage height, DIC, DOC, POC, Spot flow velocity, Calculated velocity, and Discharge.

- Data quality and limitations
  - Data gaps due to probe malfunction in NC pH time series (Jul–Sept 2011); MT stream had larger gaps in 2012.
  - Flooding could distort velocity and discharge calculations; stage/discharge adjustments applied during flooding.
  - NC oxygen saturation values occasionally very low (down to -1.3%); many low readings attributed to instrument fouling; caution advised for values <60% in datasets used with carbon data.
  - NC NC 2012 pressure sensor may underreport event peaks; stage height-derived metrics should be treated with caution for those months.

- Data processing notes
  - For NC when flood conditions caused overbanking, velocity/discharge were adjusted from maximum observed velocity toward zero as stage height reached flooding limit.
  - DIC and isotopic measurements followed standardized calibration with multiple standards; blanks and drift checks routinely included.

- Related data
  - CO2 efflux and hydraulic data dataset by Hazel Long et al. (2011–2013) referenced as an accompanying data source.

- Reference
  - Waldron, S., E. M. Scott, L. E. Vihermaa, and J. Newton (2014). Quantifying precision and accuracy of measurements of dissolved inorganic carbon stable isotopic composition using continuous-flow isotope-ratio mass spectrometry. Rapid Communications in Mass Spectrometry.