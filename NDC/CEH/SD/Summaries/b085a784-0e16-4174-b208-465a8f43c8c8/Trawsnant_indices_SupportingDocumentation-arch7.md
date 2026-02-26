# Experimental Design/Sampling Regime/Collection Methods

- Location and catchment context
  - Nant Trawsnant experimental catchment (LI8), near Llyn Brianne reservoir, Powys, Wales, UK.
  - Contributory areas: streamflow station 1.23 km2; upstream pH monitoring 1.21 km2.
  - Geology and soils: Lower Palaeozoic shales, mudstones, greywackes, grits; Podzols and Histosols.
  - Land cover: ~88% conifer forest during data periods.
  - Spatial coordinates provided for key stations; data can be linked to GIS layers describing catchment, geology, land cover.

- Data sources and observation regime
  - Streamflow and pH monitored by Lancaster University from regular gauging stations and water-quality stations in Nant Trawsnant.
  - Temporal resolution: 15-minute intervals in 2013 (1 Jan–31 Dec 2013).
  - Data logging hardware: Campbell Scientific CR1000 data logger; sensors include a Sensortechnics pressure transmitter (for flow) and a Hach Lange pH sensor (SC200 controller).

- Meteorological and ancillary data
  - Monthly rainfall data (1982–2013) derived from Welsh Water Authority/National Rivers Authority/Environment Agency Wales records; gaps filled using nearby raingauges.
  - Monthly mean temperature from Felindre weather station; data from Met Office MIDAS (station 1243).
  - NAO index (monthly) sourced from public CRA data.
  - All data vetted for IP rights by NERC EIDC prior to release.

- Data processing and modelling approach
  - Daily rainfall, streamflow, and pH modeled and then aggregated to monthly statistics.
  - Model identification using the RIVC algorithm (CAPTAIN Toolbox for Matlab) to determine optimal structures/parameters.
  - Daily models calibrated on 1 Jan–31 Mar 2013; validated 1 Apr–31 Dec 2013.
  - Identified models applied with Matlab LSIM (daily streamflow and pH data) to simulate 1 Apr 1982–1 Apr 2013; monthly statistics derived from simulated data.

- Calibration and field instrumentation details
  - Salt-dilution gauging used for theoretical stage-discharge calibration of Nant Trawsnant flume.
  - SC200 pH controller recalibrated every 2–3 months; pH sensor recalibrated with pH 4.0 and pH 7.0 standards as needed.
  - Field measurements wired to data loggers and calibrated by field personnel.

- Variables, units, and data structure
  - Data delivered as a single .csv file with 159 statistical variables (columns); columns 2–5 are blank.
  - 32 rows total: header row plus 31 data rows; rows 2–32 correspond to statistics for the first day of each month from 1 Apr 1982 to 1 Apr 2013.
  - Derived variables include:
    - Rainfall metrics: mean, 10th percentile, total, maximum, CV.
    - Flow metrics: mean, 10th/95th percentiles, min/max of moving averages (10-day), total, max/min flow, range, CV.
    - Pulses and durations: number and duration of high/low flow pulses (thresholds based on 75th/25th percentiles), probabilities, and related metrics.
    - Flow change rates: average rise and fall rates.
    - pH metrics: mean and 10th percentile (over 365-day estimation period).
    - Temperature metrics: mean, 10th/95th percentiles, moving-average extrema, and range; growing-season indicators (5°C threshold) and durations of high/low periods (based on percentiles for given periods).
    - Temperature-derived statistics for 30-day and 5-day windows as applicable.
  - Estimation windows:
    - 365 days prior to biological sampling for most rainfall/flow/pH metrics.
    - 30 days prior for certain temperature and rate metrics.
  - Notable column-specific details include specialized metrics such as growing-season length, high/low pulse durations, and rate-based indicators.

- Quality control and data integrity
  - Quality checks on CR1000 data loggers to identify erroneous values (e.g., power/battery glitches).
  - Erroneous values replaced with NaN in QA routines to maintain data integrity.

- Data access, reproducibility, and licensing
  - Data released via the Environmental Information Data Centre (EIDC) and vetted for IPR.
  - Statistical routines implemented in MATLAB; code and DOIs referenced for reproducibility (RIVC CAPTAIN Toolbox, LSIM in MATLAB).

- GIS relevance and integration considerations
  - Spatial context anchored to a defined catchment with known area, coordinates, and land-cover characteristics, enabling integration with GIS layers (catchment boundary, soils, forest cover, hydrological features).
  - Time-series data (streamflow, pH, rainfall, temperature) can be linked with spatial datasets for hydrological modelling, catchment-scale analysis, and map-based visualization of regime changes and event-driven responses.
  - The data’s monthly statistics, while model-derived for some periods, provide climate- and hydrology-related indicators suitable for thematic mapping and trend analysis at the catchment scale.

- Practical considerations for GIS specialists
  - Ensure alignment of the catchment coordinates and area with local GIS layers before integration.
  - Take into account that certain metrics are model-derived using historical simulations (1982–2013) and may carry modeling assumptions.
  - Use the robust QA notes to mask or impute gaps when generating spatial time-series visualizations.