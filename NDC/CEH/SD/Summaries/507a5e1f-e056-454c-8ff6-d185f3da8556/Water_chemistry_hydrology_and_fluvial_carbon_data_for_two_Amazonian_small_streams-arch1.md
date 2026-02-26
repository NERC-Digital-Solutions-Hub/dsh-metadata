# Sampling Regime

- A data collection from two small streams in the Western Amazonian basin, Tambopata National Reserve, Madre de Dios, Peru (coordinates provided). 
- Time frame: February 2011 to October 2012.
- Streams: NC (New Colpita) and MT (Main Trail). NC flows year-round; MT is seasonally active.
- Sampling resolution: continuous measurements at 15-minute intervals (water chemistry and hydrology), with additional field campaigns for carbon measurements during wet and dry conditions.
- Study goals: quantify hydrology and carbon dynamics (DIC, DOC, POC) and understand hydrological controls on carbon concentrations and fluxes.

## Study Area and Sampling Regime

- NC stream: 4.5–7.5 m wide at sampling point; drains about 7.2 km² upstream; experiences flow during the dry season.
- MT stream: 3.5–5 m wide; drains about 4.9 km² upstream.
- Field campaigns targeted different flow conditions to capture wet/dry season variability and event-driven changes.

## Measurements and Analytes

- Hydrology: stage height (continuous), discharge (derived from stage height and cross-sectional data), and flow velocity (periodic measurements used to establish velocity–stage relationship).
- Water chemistry: pH, conductivity, temperature, dissolved oxygen (saturation).
- Carbon measurements: DIC, DOC, POC.
- Additional data: time series data provided with 15-minute resolution; NA indicates missing values.

## Sampling Campaigns and Seasonal Coverage

- Campaigns for carbon data occurred in three periods: Feb–Apr 2011, Sept–Dec 2011, and Mar–May 2012.
- MT is dry-season active; NC continues to flow during the dry season, enabling year-round data in NC but with seasonal gaps in MT due to operational issues.

## Analytical Methods and Calibration

- DIC: measured by headspace method using Thermo-Fisher Scientific Gas Bench/Delta V Plus; isotopic composition δ13C also measured.
- DOC: filtered samples (GF/F filters), acidified to pH ~3.9, degassed, analyzed by combustion (TOC analyzer).
- POC: measured by loss on ignition after drying and furnace treatment; assumed percent OC 50%.
- Replicates: triplicate DIC samples for quality control; triplicate isotopic measurements with varied standards.
- Calibration and standards: multi-point calibrations for DIC and DOC; standards spanning expected concentration ranges; routine instrument calibration and drift checks.

## Instrumentation and Calibration

- pH, conductivity, dissolved oxygen, temperature: Troll 9500 (In-Situ Inc., USA) with regular monthly calibration and weekly cleaning.
- Stage height: Rugged Troll (In-Situ Inc., USA).
- Flow velocity: Flowlink2150 (ISCO Inc., USA); used with cross-sectional data to compute discharge.
- Calibration details: two-point pH calibration (pH 4 and 7), conductivity standard (84 µS/cm), saturated oxygen reference, zero-oxygen solution for calibration.

## Data Processing and Derived Variables

- Discharge derived by combining flow velocity with detailed cross-sectional measurements and stage height.
- A rating curve established from velocity measurements to convert stage height into continuous velocity and thus discharge.
- Adjustments made during high-flow/flood events when linear rating curves produced unrealistic velocities; velocity corrected to reflect observed maximums and stage limits.
- NC sensor data during August–October 2012 suspected to have issues; stage/velocity/discharge values treated with caution in this period.

## Data Quality, Gaps, and Cautions

- Data gaps: perennial NC pH time series missing from 1 July to 7 September 2011 due to probe malfunction; MT 2012 data gaps due to instrument problems.
- Flooding: large river influence caused non-linear flow behavior; adjustments applied to maintain plausible discharge estimates.
- Oxygen saturation: some periods with very low readings (<60% saturation) likely due to sensor fouling; such values should be treated cautiously in analyses.
- NC pressure sensor: possible lack of event peaks in August–October 2012; stage-height-derived values during those months should be used with caution.

## Data Structure and Files

- Time series with 15-minute intervals; missing values indicated as NA.
- CSV files:
  - Perennial_stream_NC
  - Seasonal_stream_MT
- Columns include:
  - Site (MT or NC)
  - Date (dd/mm/yyyy)
  - Time (hh:mm:ss)
  - Temperature (°C)
  - pH
  - Oxygen saturation (%)
  - Conductivity (µS/cm)
  - Stage height (cm)
  - DIC (mg/L)
  - DOC (mg/L)
  - POC (mg/L)
  - Water flow velocity (m/s) at the measurement spot
  - Velocity (m/s) derived at fixed point from stage-height relationship
  - Discharge (m³/s) derived from velocity and cross-section data

## References

- Waldron, S., E. M. Scott, L. E. Vihermaa, and J. Newton (2014) on precision/accuracy of DIC isotope measurements (Rapid Communications in Mass Spectrometry).
- Related CO2 flux dataset by Hazel Long et al. (not included here) for two Scottish and four Amazonian streams (DOI provided in the document).