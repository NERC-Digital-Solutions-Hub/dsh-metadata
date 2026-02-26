# Sampling Regime

## Overview
- Data from two small streams in the Western Amazonian basin at Tambopata National Reserve, Madre de Dios, Peru (latitude 12°49'54.30" S, longitude 69°16'52.37" W).
- Collected February 2011 to October 2012.
- Continuous monitoring at 15-minute resolution for water chemistry and hydrology; continuous stage height measurements in both streams.
- Flow velocity campaigns used to build a rating curve to convert stage height to discharge.
- Field campaigns collected DIC, DOC, and POC under different seasons (wet and dry) and flow conditions; MT (Main Trail) is seasonally active; NC (New Colpita) flows during the dry season as well.
- Sampling points: NC stream width 4.5–7.5 m, upstream drainage ~7.2 km²; MT stream width 3.5–5 m, upstream drainage ~4.9 km².

## Data Collected
- DIC (mg/l), NC = 172; MT = 104
- DOC (mg/l), NC = 82; MT = 52
- POC (mg/l), NC = 82; MT = 53
- Temperature (°C), NC = 50,765; MT = 16,164
- pH, NC = 50,784; MT = 15,012
- Oxygen saturation (%), NC = 40,265; MT = 15,241
- Conductivity (µS/cm), NC = 50,784; MT = 13,579
- Stage height (cm), NC = 56,610; MT = 24,482
- Flow velocity at a chamber (m/s), NC = 46; MT = 41
- Stream velocity (m/s) at fixed point (for discharge calculation), NC = 56,610; MT = 24,931
- Discharge (m³/s), NC = 56,610; MT = 37,016
- Note: Stream flow velocity used with stage height to derive continuous velocity time series and discharge.

## Collection Methods and Instrumentation
- In-field measurements:
  - Water chemistry: Troll9500 (pH, conductivity, dissolved oxygen, temperature)
  - Stage height: Rugged Troll
  - Flow velocity: Flowlink2150
  - Stream cross sections measured to calculate discharge from stage height and velocity data
  - Additional velocity measurements (handheld flow meter) at the flux chamber site
- CO2 data: Additional data available from a related dataset (Hazel Long et al.)
- Sampling campaigns: February–April 2011; September–December 2011; March–May 2012
- MT stream dries in the dry season; NC stream flows during the dry season as well
- DIC sampling: pre-acidified evacuated exetainers; headspace method and δ13C isotopic measurements
- DOC sampling: filtered and refrigerated; acidified to pH 3.9; degassed; analyzed by combustion
- POC: measured by loss on ignition after drying and burning filter papers
- Lab calibrations:
  - Troll 9500 calibrated monthly; cleaned weekly
  - pH calibration with two-point buffers (pH 4 and pH 7)
  - Conductivity calibration with a standard solution
  - Oxygen saturation calibrated with oxygen-saturated water and a zero-oxygen solution

## Analytical Methods
- DIC: headspace method on GC-MS/Delta V Plus; isotope analyses for δ13C
- DOC: filtration, degassing, and combustion-based concentration determination
- POC: weight-based mass fraction from dried and ignited filter papers

## Quality Control
- Data gaps due to probe malfunction: NC pH time series July–September 2011
- Larger data gaps in 2012 for MT and NC seasonal time series due to instrument issues
- Flooding events affecting velocity and discharge calculations; adjustments applied based on field observations when maximum flow velocity and stage height indicated flooding
- NC pressure sensor in Aug–Oct 2012 showed lack of event peaks; stage height and derived metrics should be treated with caution
- Oxygen saturation readings: periods of very low values likely due to instrument fouling; values below 60% (and especially below 40%) should be treated cautiously in analyses

## Data Structure and File Format
- Time step: 15-minute intervals; missing values indicated as NA
- CSV files:
  - Perennial_stream_NC
  - Seasonal_stream_MT
- Columns (as described in the dataset):
  - Site (MT for Main Trail, NC for New Colpita)
  - Date (dd/mm/yyyy)
  - Time (hh:mm:ss, 24-hour)
  - Water temperature (°C)
  - pH
  - % oxygen saturation
  - Electrical conductivity (µS/cm)
  - Stage height (cm)
  - Dissolved inorganic carbon (DIC, mg/l)
  - Dissolved organic carbon (DOC, mg/l)
  - Particulate organic carbon (POC, mg/l)
  - Water flow velocity (m/s) at hand-held measurement spot
  - Velocity (m/s) at the fixed point (derived from stage height relationship
  - Discharge (m³/s) derived from velocity and cross-section data

## References
- Waldron, S., E. M. Scott, L. E. Vihermaa, and J. Newton (2014), Quantifying precision and accuracy of measurements of dissolved inorganic carbon stable isotopic composition using continuous-flow isotope-ratio mass spectrometry, Rapid Communications in Mass Spectrometry, 28(10), 1117-1126.