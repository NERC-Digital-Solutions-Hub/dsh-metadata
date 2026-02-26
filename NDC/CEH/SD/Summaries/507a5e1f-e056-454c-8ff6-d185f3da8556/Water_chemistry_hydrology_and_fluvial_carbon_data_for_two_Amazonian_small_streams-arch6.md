# Sampling Regime

## Overview
- Data collected from two small streams (MT – Main Trail; NC – New Colpita) in the Western Amazonian basin at Tambopata National Reserve, Madre de Dios, Peru (approx. 12°49'54.30'' S, 69°16'52.37'' W).
- Temporal coverage: February 2011 to October 2012.
- Measurements: water chemistry and hydrology continuously at 15-minute resolution (subject to instrument issues); stage height monitored continuously; periodic flow-velocity campaigns to build a rating curve for converting stage height to discharge.
- Sampling design: field campaigns targeted different seasons (wet and dry) and flow conditions to understand hydrological controls on carbon concentrations and fluxes. MT is seasonally active; NC flows during the dry season as well.
- Outputs for end users: time-series data enabling analyses of carbon dynamics and hydrology with supporting metadata and calibration details.

## Measurements and variables
- Key carbon variables: DIC (mg/L), DOC (mg/L), POC (mg/L).
- Water chemistry: temperature (°C), pH, oxygen saturation (%), conductivity (µS/cm).
- Hydrology: stage height (cm), flow velocity (m/s) at a fixed point, discharge (m³/s) derived from velocity and cross-section measurements; additional velocity from a hand-held meter at the chamber site.
- Time-step: 15-minute intervals; missing values indicated as NA.
- Data point counts (Table 1): NC vs MT
  - DIC: 172 (NC), 104 (MT)
  - DOC: 82 (NC), 52 (MT)
  - POC: 82 (NC), 53 (MT)
  - Temperature: 50,765 (NC), 16,164 (MT)
  - pH: 50,784 (NC), 15,012 (MT)
  - Oxygen saturation: 40,265 (NC), 15,241 (MT)
  - Conductivity: 50,784 (NC), 13,579 (MT)
  - Stage height: 56,610 (NC), 24,482 (MT)
  - Flow velocity (chamber): 46 (NC), 41 (MT)
  - Stream flow: 56,610 (NC), 24,931 (MT)
  - Discharge: 56,610 (NC), 37,016 (MT)

## Field methods and instrumentation
- In-field instruments:
  - Water chemistry, DO, temperature: Troll 9500 (In-Situ)
  - Stage height: Rugged Troll (In-Situ)
  - Flow velocity: Flowlink2150 (ISCO) and handheld flow meter for chamber site
- Cross-section measurements: used with velocity data to calculate discharge from stage height.
- Additional related data: CO2 flux data for streams from a separate dataset (Hazel Long et al., 2011-2013) referenced for context.
- Sampling campaigns for carbon measurements:
  - DIC, DOC, POC: collected during three field campaigns (Feb–Apr 2011; Sept–Dec 2011; Mar–May 2012); MT dries during the dry season, so no MT samples in Sep–Nov 2011.
  - DIC analysis: headspace method on Thermo-Fisher GasBench/Delta V Plus with isotopic composition (δ13C); triplicate sampling with a backup to verify agreement.
  - DOC analysis: filtered, acidified, degassed, and measured by combustion (TOC analyzer); filter papers dried and weighed to determine POC via loss on ignition (assuming 50% OC).
- Calibration and standards:
  - DIC standards spanning expected concentrations; isotopic triplicates with different δ13C; midrange check standard for drift.
  - DOC calibration across eight points with blanks and drift checks; POC calibration via mass loss on ignition.

## Data processing and quality control
- Calibration and cleaning:
  - Troll 9500 calibrated approximately monthly; field cleaning with brush and cotton buds; pH calibration with buffers (pH4, pH7); conductivity calibration with a low-standard solution; oxygen calibration using saturated and zero-oxygen solutions.
- Data gaps and adjustments:
  - NC perennial data gap in pH from 1 July to 7 September 2011 due to probe malfunction; gap filled with pooled coefficients from multiple fits using the MICE package in R.
  - MT stream water chemistry had larger 2012 data gaps due to instrument problems; those data are provided in non-gap-filled form.
  - Flooding events caused linear adjustments to velocity/discharge estimates in NC during high-water periods when water backup affected measurements.
  - NC oxygen saturation values occasionally dropped below 60% (minimum observed -1.3%); such low values are suspected to reflect instrument fouling; model data used in conjunction with carbon data never had O2 sat below 40% and CO2 efflux data not below 60% in corresponding periods; treat very low readings with caution.
- Instrument reliability:
  - Some issues with pressure sensor data (NC) in 2012; event peaks may be unreliable; stage, velocity, and derived discharge from these months should be treated with caution.

## Data structure and access
- Time series format: 15-minute time steps; missing values encoded as NA.
- CSV files:
  - Perennial_stream_NC.csv
  - Seasonal_stream_MT.csv
- Columns (common structure; summarized):
  - Site (MT or NC)
  - Date (dd/mm/yyyy)
  - Time (hh:mm:ss, 24h clock)
  - Water temperature (°C)
  - pH
  - Oxygen saturation (%)
  - Conductivity (µS/cm)
  - Stage height (cm)
  - DIC (mg/L)
  - DOC (mg/L)
  - POC (mg/L)
  - Flow velocity at chamber (m/s)
  - Velocity (m/s) at stage-recording point (derived)
  - Discharge (m³/s) (derived)
- Notes:
  - Discharge and flow-related variables are derived from velocity and cross-section measurements.
  - Datasets include detailed calibration and methods descriptions embedded in accompanying text.

## Methods and references
- Analytical methods and calibration procedures described for each measurement type (collection, preservation, and analysis).
- Related methodological reference: Waldron et al. 2014 on precision and accuracy of DIC isotopic measurements (Rapid Communications in Mass Spectrometry).

## Usage notes and caveats for data users
- Data are suitable for self-serve analyses of hydrology–carbon interactions, with clear documentation of QA steps and calibration.
- Be cautious with:
  - Gaps and instrument-induced anomalies (especially NC 2011 pH gap, 2012 MT gaps, NC pressure sensor issues, O2 saturation anomalies potentially due to fouling).
  - Flooding periods requiring velocity/discharge adjustments.
  - Dry-season cessation of MT sampling limiting MT data during certain seasons.
- Data provenance and replication: triplicate DIC measurements and isotope analyses available for quality checks; calibration standards and drift checks documented per batch.

## References
- Waldron, S., E. M. Scott, L. E. Vihermaa, and J. Newton (2014). Quantifying precision and accuracy of measurements of dissolved inorganic carbon stable isotopic composition using continuous-flow isotope-ratio mass spectrometry, Rapid Communications in Mass Spectrometry, 28(10), 1117-1126.