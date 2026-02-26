# Sampling Regime

## Overview
- Data from two small streams in the Western Amazonian basin at Tambopata National Reserve, Madre de Dios, Peru (approximate sampling point: 12°49'54.30"S, 69°16'52.37"W).
- Collected February 2011 to October 2012; continuous monitoring at 15-minute resolution for water chemistry and hydrology; cross-section measurements used to convert stage height to discharge.
- MT (Main Trail) is seasonally active; NC (New Colpita) flows during the dry season as well. MT can dry up; NC can be affected by flooding events.
- Data intended for hydrological and fluvial carbon analyses (DIC, DOC, POC) and related water quality and flow metrics.

## Data Collected (Table 1 counts)
- DIC (mg/L): NC 172; MT 104
- DOC (mg/L): NC 82; MT 52
- POC (mg/L): NC 82; MT 53
- Temperature (°C): NC 50,765; MT 16,164
- pH: NC 50,784; MT 15,012
- Oxygen saturation (%): NC 40,265; MT 15,241
- Conductivity (µS/cm): NC 50,784; MT 13,579
- Stage height (cm): NC 56,610; MT 24,482
- Flow velocity at chamber (m/s): NC 46; MT 41
- Stream flow (m/s): NC 56,610; MT 24,931
- Discharge (m³/s): NC 56,610; MT 37,016

Note: Stream flow velocity was periodically measured to establish the stage height–velocity relationship used to generate continuous velocity and discharge time series.

## Field Methods and Instrumentation
- Water chemistry and hydrology instruments:
  - Troll9500 (In-Situ) for pH, conductivity, dissolved oxygen, temperature
  - Rugged Troll for stage height
  - Flowlink2150 (ISCO) for flow velocity
- Cross-section measurements used to relate stage height to discharge
- Additional velocity measurements with a handheld flow meter at the sampling site of the flux chamber
- CO2 flux data linked from a separate dataset (Long et al., 2011–2013)

## Sampling Campaigns and Conditions
- Campaigns: Feb–Apr 2011, Sept–Dec 2011, Mar–May 2012
- MT stream dries during dry season; NC stream flows year-round
- MT sampling minimal Sept–Nov 2011 due to drying
- NC pressure sensor anomalies: potential data gaps and caution advised for August–October 2012
- Large river flooding can affect velocity estimates; adjustments applied to prevent unrealistic discharge during high flow and overbanking
- Oxygen saturation values occasionally very low (some data likely affected by instrument fouling); caution when interpreting values below ~60% in CO2-related analyses

## Data Structure and Access
- Time series at a 15-minute resolution; missing values indicated as NA
- CSV files:
  - Perennial_stream_NC
  - Seasonal_stream_MT
- Columns (shared across files):
  1) Site (MT or NC)
  2) Date (dd/mm/yyyy)
  3) Time (hh:mm:ss, 24-hour)
  4) Water temperature (°C)
  5) pH
  6) Oxygen saturation (%)
  7) Conductivity (µS/cm)
  8) Stage height (cm)
  9) DIC (mg/L)
  10) DOC (mg/L)
  11) POC (mg/L)
  12) Water flow velocity at spot (m/s)
  13) Velocity at fixed stage measurement point (m/s), derived from stage height relationship
  14) Discharge (m³/s), derived from velocity and cross-section data

## Data Quality and Notes
- Several data gaps due to instrument malfunctions (notably NC pH in mid-2011; MT 2012 time series with larger gaps)
- Flooding can cause unrealistic velocity during peak stages; velocities and discharges adjusted using field observations
- NC sensor issues in 2012 (pressure data) and potential fouling affecting oxygen readings
- Some low oxygen saturation values likely reflect sensor fouling; modeling datasets used select periods with carbon data present

## Relevance to GIS and Data Use
- Provides high-resolution, time-stamped hydrology and water chemistry data for two rivers with clear spatial context, enabling the creation of map-based visualizations of hydrological regimes and carbon flux dynamics.
- Enables calculation and mapping of discharge and velocity fields, and integration with cross-sectional measurements for spatially explicit flux analyses.
- Useful for policy, conservation planning, and public data visualizations related to riverine carbon cycling in the Amazon, with caveats on data gaps and sensor reliability. 

## References
- Waldron, S., E. M. Scott, L. E. Vihermaa, and J. Newton (2014), Quantifying precision and accuracy of measurements of dissolved inorganic carbon stable isotopic composition using continuous-flow isotope-ratio mass spectrometry, Rapid Communications in Mass Spectrometry, 28(10), 1117-1126.