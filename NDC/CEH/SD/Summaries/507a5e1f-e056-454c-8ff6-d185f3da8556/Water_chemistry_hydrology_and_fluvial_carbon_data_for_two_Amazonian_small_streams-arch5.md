# Sampling Regime

- Two small streams in the Western Amazonian basin at Tambopata National Reserve, Madre de Dios, Peru (MT: Main Trail; NC: New Colpita). Data collection Feb 2011–Oct 2012.
- Continuous monitoring of water chemistry and hydrology at 15-minute resolution; stage height continuously recorded; periodic flow velocity campaigns used to derive a discharge rating curve and continuous velocity time series.
- Field campaigns targeted different seasons (wet/dry) and flow conditions to understand hydrological controls on carbon concentrations and fluxes.
- MT dries seasonally; NC flows during the dry season as well. Sampling points: NC stream width 4.5–7.5 m (upstream area ~7.2 km2); MT stream width 3.5–5 m (upstream area ~4.9 km2).

## Data Collected and Variables

- DIC (mg/L), DOC (mg/L), POC (mg/L); Temperature (°C); pH; Oxygen saturation (%); Conductivity (µS/cm); Stage height (cm); Flow velocity (m/s) at a fixed point; Stream flow (m/s) and Discharge (m3/s) derived from velocity and cross-section data.
- Data points per parameter vary; time series largely 15-minute steps with NA for missing values.
- Related CO2 data available from a separate dataset (Hazel Long et al., 2011–2013) referenced but not included here.

## Methods and Instrumentation

- Field instruments: Troll9500 for water chemistry (pH, conductivity, dissolved oxygen, temperature); Rugged Troll for stage height; Flowlink2150 for flow velocity; handheld flow meter for spot velocity.
- Cross-section surveys used to convert stage height to discharge; additional velocity measurements used to support the rating curve.
- Sampling for carbon: DIC via headspace method with pre-acidified exetainers; DOC via filtration, acidification, degassing, and combustion; POC via loss on ignition.
- Laboratory calibrations and standard procedures described for DIC, DOC, isotope measurements (δ13C), and calibration standards.

## Sampling Campaigns and Conditions

- Campaigns: Feb–Apr 2011; Sept–Dec 2011; Mar–May 2012.
- MT: seasonally active; NC: flows also during dry season.
- Moisture/flow variability intentional to capture hydrological controls on carbon dynamics.
- MT no sampling in Sep–Nov 2011 due to MT drying; NC had broader data gaps in 2012 due to instrument issues.

## Data Structure and File Format

- Two CSV files:
  - Perennial_stream_NC
  - Seasonal_stream_MT
- 15-minute time step; missing values indicated as NA.
- Core columns (in order):
  - Site (MT or NC)
  - Date (dd/mm/yyyy)
  - Time (hh:mm:ss, 24h)
  - Water temperature (°C)
  - pH
  - Oxygen saturation (%)
  - Conductivity (µS/cm)
  - Stage height (cm)
  - DIC (mg/L)
  - DOC (mg/L)
  - POC (mg/L)
  - Water flow velocity at the spot (m/s)
  - Velocity at fixed point (m/s) derived from stage-height relationship
  - Discharge (m3/s)

## Quality Control and Limitations

- Data gaps due to probe malfunction in NC pH time series (Jul 1–Sep 7, 2011); gap filled using pooled model fits based on conductivity and stage height (MICE in R) but MT 2012 data had larger gaps.
- Flooding periods caused unrealistic high predicted velocities; velocity/discharge adjusted linearly with stage height during flooding.
- NC pressure sensor data (Aug–Oct 2012) may miss event peaks; stage height and derived discharge from these months should be treated with caution.
- Oxygen saturation values occasionally drop below 60% during non-ideal conditions; some low readings may reflect fouling; use with caution in analyses, especially when CO2 fluxes are involved.
- Calibration and drift checks indicated; data values within method detection limits; some sensors required cleaning and recalibration.

## Data Use, Provenance, and Documentation

- Time series documented with 15-minute resolution; NA indicates missing values.
- Documentation includes instrumentation details, collection and calibration protocols, and quality control notes.
- Data reference: Waldron, S.; Scott, E. M.; Vihermaa, L. E.; Newton, J. (2014) on precision/accuracy of DIC stable isotopes measurements (context for DIC data).
- Related CO2 efflux and hydraulic data available from a separate dataset (DOI placeholder mentioned).

## Governance and Reuse Considerations for Data Stewards

- Source and scope clearly defined; two distinct streams with separate data files and naming conventions.
- Comprehensive metadata on instruments, calibration, sampling campaigns, and QC steps; caveats and data gaps explicitly documented.
- Ensure clear citation (Waldron et al., 2014) and acknowledge linkage to related CO2 data where used.
- Assess data completeness and instrument reliability when integrating into broader datasets; account for known gaps and caution flags in analyses.