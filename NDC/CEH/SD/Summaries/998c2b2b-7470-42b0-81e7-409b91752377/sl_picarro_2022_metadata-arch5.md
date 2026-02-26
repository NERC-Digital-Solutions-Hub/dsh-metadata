# High-resolution ammonia concentration data from Queensberry experimental site in Sri Lanka (2022)

## Overview
- Purpose: To study the effects of high ambient ammonia (NH3) on forest components and to analyze NH3 plume behavior within the canopy.
- Location: Queensberry Estate, central Sri Lanka; coordinates 6.9693° N, 80.5911° E; altitude 1645 m.
- Timeframe: Data collection conducted from 24 March 2022 to 3 April 2022.
- Funding: UKRI GCRF South Asian Nitrogen Hub.

## Data Collection Details
- NH3 release system
  - Triggered by wind conditions measured below the canopy; NH3 released only when wind direction is within 5–75° and 185–255°, at threshold speeds of 0.3–10 m/s.
  - Release hardware: three 20 m long PVC tubes (110 mm OD) arranged in parallel with holes every 20 cm around the circumference.
  - Gas delivery: 6.35 mm stainless steel pipe transports pure anhydrous NH3 from a cylinder to a manifold, through a mass flow controller (MFC) and a solenoid valve, injecting NH3 into the fan airflow to dilute and release via the tubes.
  - Valve control: Solenoid valve opens only under correct wind conditions.
- Monitoring and sampling system
  - Analyzer: Picarro G2123 NH3/H2O analyzer placed 10 m downwind; housed in a custom air-conditioned enclosure.
  - Sampling heights: 0.5 m, 1.0 m, 1.5 m, and 2.5 m above ground.
  - Sampling mechanism: Four height inlets connected via a valve manifold; automatic control implemented in LabVIEW.
  - Sampling duration: 2 minutes per height.
  - Casing and lines: PTFE tubing (4 mm diameter) for sampling lines, each ~5.5 m long.
  - Temperature control: Inlet system heated to ~40°C ± 3°C using self-regulating heating tape and insulation.
  - Flow management: Purge flow 7 standard L/min between sampling; during sampling, flow increases to 12 standard L/min.
  - Lag considerations: Acknowledgement of potential lag due to NH3 adsorption/desorption on inlet surfaces; some lag expected when switching heights.
  - Background volatilisation: Heating may volatilise NH4NO3, but background is expected to be smooth.
- Data capture specifics
  - Measurement frequency: NH3 concentrations recorded at 10 Hz; data averaged to 0.016 Hz intervals.
  - Time standard: Sri Lanka Standard Time (SLST).

## Quality Control
- Visual inspection to identify and remove obvious instrument malfunctions, datalogger issues, and power cuts.
- Gaps during valve switching are filled by linear interpolation.

## Data Structure and Content
- Dataset size: 14,094 measurements across 6 parameters.
- Format: CSV file.
- Columns and metadata (examples)
  - Timestamp: date and time (SLST); units unspecified.
  - NH3_status: operational status of NH3 release (coded with 0, 1, 2, 3, 4, etc.); instrument/source: Type 6027 (Bürkert).
  - NH3_flow: flow through the release system (units: slpm); instrument/source: MFC; description includes NH3 flow through MFC into manifold.
  - Wind_speed: wind speed (units: m/s); instrument/source varies (e.g., WXT536, Vaisala, below-canopy sensor).
  - Wind_direction: wind direction (units: degrees); instrument/source varies.
  - NH3_conc: NH3 concentration in air (units: ppb); instrument/source varies (G2123, Picarro).
  - Inlet_height: height of NH3 concentration measurement (units: m); instrument/source varies.
- Data provenance: Multiple instruments and components documented (G2123 NH3/H2O analyzer, Picarro, MFCs, solenoid valve, lab automation, below-canopy wind sensor).

## Temporal and Spatial Scope
- Spatial scope: Downwind monitoring sector relative to NH3 release system; measurements taken at four vertical heights to characterize plume structure within canopy.
- Temporal scope: 24 March 2022 to 3 April 2022; data aligned to SLST.

## Data Governance and Stewardship Considerations for Data Stewards
- Standards and interoperability
  - Ensure consistent metadata for each instrument (type, manufacturer) and for each data stream (NH3_status, NH3_flow, Wind_speed, Wind_direction, NH3_conc, Inlet_height).
  - Include clear definitions of status codes and units; document any instrument-specific qualifiers.
- Metadata requirements
  - Provide a detailed data dictionary and methods section describing release logic, sampling sequence, heights, and timing.
  - Document lag potential due to adsorption/desorption and any heating-related volatilisation effects.
- Data quality and processing
  - Record quality control steps (visual checks, interpolation of gaps) and rationale for gap filling.
  - Maintain a log of any data exclusions or corrections (e.g., instrument errors, power interruptions).
- Accessibility and reuse
  - Prepare dataset for sharing in a data portal; include licensing, citation information, and contact for data access.
  - Consider providing a README with context, site coordinates, dynamical sampling schedule, and maintenance notes.
- Limitations and caveats
  - Note possible lag between actual NH3 concentration changes and recorded values due to inlet surface adsorption/desorption and flow dynamics.
  - Acknowledge that the dataset represents a controlled release campaign with specific wind-condition triggers, which may limit generalizability to ambient conditions.
- Provenance and governance
  - Include funding attribution (UKRI GCRF South Asian Nitrogen Hub) and facility description to support reproducibility and accountability.

## Funding and Acknowledgments
- Funded by the UKRI GCRF South Asian Nitrogen Hub.