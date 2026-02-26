# High-resolution ammonia concentration data from Queensberry experimental site in Sri Lanka (2022)

## Overview
- Purpose: Document high-resolution NH3 concentration data from a tropical sub-montane forest to study the effects of elevated ammonia on vegetation, bryophytes, lichens, and soil.
- Location: Queensberry Estate, central Sri Lanka; coordinates 6.9693°, 80.5911°, altitude 1645 m.
- Campaign: 2022 NH3 enhancement experiment with an emphasis on release optimization and canopy plume behavior.
- Data product: Time-stamped measurements of NH3 concentration and related variables collected downwind of an NH3 release system.

## Data Collection and Experimental Setup
- Enhancement system: NH3 release triggered only when wind conditions are within specified directions and speeds to target monitoring quadrats.
- Release hardware: Three parallel 20 m PVC tubes (110 mm OD) with holes along their length; NH3 delivered from a cylinder via a mass flow controller and solenoid valve into a central manifold, creating a diluted plume.
- Control logic: Solenoid valve engages NH3 flow only under correct wind conditions.
- Downwind measurement: Picarro NH3/H2O analyser located ~10 m downwind in the northeastern sector; housed in a custom, air-conditioned enclosure.

## Sampling and Measurements
- Height-based sampling: NH3 concentration measured at four heights above ground (0.5, 1.0, 1.5, 2.5 m) using a four-inlet system spanning ~5.5 m per inlet.
- Temporal resolution: NH3 concentrations recorded at 10 Hz and averaged to 0.016 Hz intervals (effectively 1-minute intervals for the dataset).
- Sampling protocol: At each height, sampling occurred for 2 minutes via a valve manifold controlled by LabVIEW.
- Air handling: Inlet temperature ~40°C (±3°C) with heating tape and insulation; sampling lines purge between sampling events (7 to 12 standard L/min) to minimize lag and adsorption/desorption effects.
- Lag considerations: Some lag anticipated due to NH3 adsorption/desorption on inlet surfaces; potential volatilisation of NH4NO3 aerosol considered but expected to yield a smooth background.

## Quality Control and Data Processing
- Data vetting: Visual inspection to remove obvious instrument malfunctions, datalogger issues, and power interruptions.
- Gaps handling: Gaps introduced during valve switching are filled by linear interpolation.
- Background considerations: Acknowledgement of possible volatilisation effects and their impact on background levels.

## Data Structure and Metadata
- Scope: 14,094 measurements across 6 primary parameters.
- File format: CSV with timestamped records and accompanying metadata.
- Core columns (with instrumentation context):
  - Timestamp (with date/time in Sri Lanka Standard Time)
  - NH3_status (release status; coded values)
  - NH3_flow (NH3 flow rate and instrument source)
  - Wind_speed (downwind wind speed; instrument source)
  - Wind_direction (wind direction; instrument source)
  - NH3_conc (NH3 concentration in air at 10 m downwind; instrument source)
  - Inlet_height (height of measurement above ground; instrument source)
- Metadata: Instrument identifiers, manufacturers, and description fields accompany each parameter to enable traceability.

## Temporal Coverage and Location Details
- Timeframe: 24 March 2022 to 3 April 2022.
- Location details align with the Queensberry experimental site coordinates and altitude noted above.
  
## Data Access and Use
- Suitable for analyzing NH3 plume behavior, validating dispersion models, and exploring vertical and lateral concentration gradients within the canopy.
- Helpful for understanding the relationship between release conditions, wind fields, and downwind NH3 concentrations.
- Data come with detailed methodological and instrument metadata to support reproducibility and integration with other datasets.

## Funding
- Funded by the UKRI GCRF South Asian Nitrogen Hub.