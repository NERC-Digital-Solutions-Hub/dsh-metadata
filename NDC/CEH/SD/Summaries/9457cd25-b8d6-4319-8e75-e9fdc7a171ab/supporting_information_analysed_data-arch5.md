# Mass balance and channel morphology data from an experimental river experiencing flood events

## Overview
- Dataset accompanying the Digital Elevation Model of an experimental river generated in a flume under variable discharge conditions.
- Generated in a 10 m long, 2.5 m wide flume (Total Environment Simulator, University of Hull, UK).
- Aimed at studying the evolution of a generic alluvial river subjected to discharge variations.
- Three data files cover sediment mass balance, channel morphology changes during floods, and flood-impacted area.

## Datasets included

### Sed_fluxes.csv
- Purpose: Mass balance information for sediment injected and collected at the outlet.
- Key contents:
  - date, Measurement_time: timing of measurements.
  - Qsout(kg): mass of sediment collected at the outlet.
  - Qsin(g/s): sediment discharge imposed during the interval.
  - Duration(h): interval duration.
  - Time(h): hours since the experiment began.
  - Qw(L/min): water discharge during the interval.
  - Qout_corrected(kg): mass at outlet corrected for water content.
  - Cum_qout(kg): cumulative sediment collected at the outlet.
  - Q_in(kg): mass of sediment injected during the interval (discharge × duration).
  - Cum_qin(kg): cumulative mass injected.
- Processing note: sediment collected wet and corrected to dry mass using a correction coefficient derived from comparing volumes of wet and dry sediment.

### Flood_data.csv
- Purpose: Measurements on the Digital Elevation Model (DEM) to determine changes in channel capacity during floods.
- Key contents:
  - Qw(L/min): water discharge during the flood.
  - Duration(h): flood duration.
  - Number_scan_before / Number_scan_after: number of scans before/after the flood.
  - Qw_star(m3): characteristic water discharge during the flood (Qw × duration).
  - Sum_Qw(m3): total volume of water delivered before the flood (proxy for time).
  - Time(h): hours since experiment start.
  - Exp_number: experiment identifier (1 or 2).
  - D_CC(cm2): averaged change in channel conveyance capacity, calculated from elevations (DEM difference) within the channel, using the pixel area (0.0025 cm2) and channel length.

### Percentage_flooded.csv
- Purpose: Measurements of the area newly inundated by each flood event.
- Key contents:
  - Newly_flooded_area(m2): area newly inundated.
  - Qw(L/min): water discharge during the flood event.
  - Flood_number: flood event index.
  - Time(h): hours since experiment start.
  - Duration(h): flood duration.
  - Sum_qw(m3): cumulative water delivered before the flood (proxy for time).
  - Exp_number: experiment identifier (1 or 2).
- Method: area identified from overhead photos post-flood and pre-flood DEM to compare against the experimental area of 26.5 m2.

## Experimental setup and context
- Purpose: understand how the channel morphology and sediment behavior respond to varying discharge in an experimental alluvial river.
- The dataset is part of a broader data collection effort including DEM-based assessments of channel changes.

## Data collection and processing notes
- Sediment data: sediment is collected at the outlet, weighed wet, and corrected to dry mass using a correction coefficient.
- DEM-based calculations: changes in channel conveyance capacity (D_CC) derived from DEM differences between pre- and post-flood states, with per-pixel area and channel length considered.
- Imaging and DEM integration used to determine newly flooded areas.

## Key variables and units (by file)
- Sed_fluxes.csv: dates, times, Qsout (kg), Qsin (g/s), Duration (h), Time (h), Qw (L/min), Qout_corrected (kg), Cum_qout (kg), Q_in (kg), Cum_qin (kg).
- Flood_data.csv: Qw (L/min), Duration (h), Number_scan_before/after, Qw_star (m3), Sum_Qw (m3), Time (h), Exp_number, D_CC (cm2).
- Percentage_flooded.csv: Newly_flooded_area (m2), Qw (L/min), Flood_number, Time (h), Duration (h), Sum_qw (m3), Exp_number.

## Data relationships and calculated metrics
- Sediment balance uses Q_in and Cum_qin versus Qout and Cum_qout to quantify injected vs. collected sediment over time.
- D_CC represents the change in channel conveyance capacity computed from DEM differences, normalized by pixel area and channel length.
- Qw_star and Sum_Qw provide context on flood magnitude and exposure time, used alongside D_CC and flooded area to relate hydrodynamics to morphologic response.
- The Percentage_flooded data ties morphological change to inundated extent, using imaging and DEM comparisons.

## Usage and potential reuse
- Designed to be used alongside the associated DEM dataset to analyze sediment transport and morphodynamic responses to floods.
- Useful for researchers and data stewards focusing on data governance, metadata completeness, and interoperability across hydrology and geomorphology datasets.
- Clear documentation of measurement times, units, corrections, and cumulative calculations supports reproducibility and reuse.

## Data quality, provenance, and governance notes
- Clear provenance: experimental flume at University of Hull; controlled discharge variations.
- Explicit processing steps (wet-to-dry correction, DEM-based calculations) enhance traceability.
- Metadata should capture measurement protocols, correction coefficients, and DEM processing steps to ensure discoverability and appropriate reuse.

## Access considerations and dependencies
- Datasets are interdependent; Sed_fluxes, Flood_data, and Percentage_flooded should be used together with the accompanying DEM dataset mentioned in the overview.