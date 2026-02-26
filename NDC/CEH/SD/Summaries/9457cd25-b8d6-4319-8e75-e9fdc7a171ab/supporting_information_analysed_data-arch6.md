# Mass balance and channel morphology data from an experimental river experiencing flood events

## Overview
- Data supporting a study of an experimental alluvial river in a 10 m long, 2.5 m wide flume at the University of Hull.
- Collected to examine sediment transport and channel morphology under varying discharge conditions.
- Meant to be used alongside a related Digital Elevation Model (DEM) dataset of the same experiments.

## Data files and key fields

- Sed_fluxes.csv
  - Contents: Sediment discharge injected and collected at the outlet, with corrections.
  - Key columns:
    - date, Measurement_time: timestamps of measurements
    - Qsout(kg): mass of sediment collected at the outlet
    - Qsin(g/s): sediment discharge imposed during intervals
    - Duration(h), Time(h): interval duration and elapsed time
    - Qw(L/min): water discharge during the interval
    - Qout_corrected(kg): outlet sediment mass corrected for water content
    - Cum_qout(kg): cumulative sediment out at outlet
    - Q_in(kg): sediment injected during the interval
    - Cum_qin(kg): cumulative sediment injected
  - Processing note: sediment weighed wet and corrected to dry mass using a correction coefficient derived from comparing wet vs dry masses.

- Flood_data.csv
  - Contents: Measurements on the DEM to quantify changes in channel conveyance capacity during floods.
  - Key columns:
    - Qw(L/min), Duration(h): water discharge and flood duration
    - Number_scan_before, Number_scan_after: DEM scan counts surrounding the flood
    - Qw_star(m3): characteristic water discharge over flood duration
    - Sum_Qw(m3): total water volume delivered before the flood (time proxy)
    - Time(h): hours since start
    - Exp_number: experiment identifier (1 or 2)
    - D_CC(cm2): averaged change in channel conveyance capacity (DEM before vs after)

- Percentage_flooded.csv
  - Contents: Area newly inundated by each flood event.
  - Key columns:
    - Newly_flooded_area(m2): area newly flooded
    - Qw(L/min): water discharge during flood
    - Flood_number: flood event number
    - Time(h), Duration(h): timing and duration of flood
    - Sum_qw(m3): cumulative water volume delivered before flood (time proxy)
    - Exp_number: experiment identifier (1 or 2)
  - Notes: inundated area is compared to the experimental area of 26.5 m^2.

## Experimental setup and context
- Purpose: study evolution of channel morphology and sediment balance under discharge variations.
- Data collection context: three datasets generated to characterize sediment flux, DEM-based channel changes, and flood-induced inundation areas.

## Data processing and quality considerations
- Sediment measurements are corrected from wet mass to dry mass using a calculated coefficient.
- DEM-based measurements involve comparing elevations before and after floods to derive changes in channel capacity (D_CC) and are paired with flood timing and discharge data.
- Scans and time markers are aligned with experiment numbers to enable integrated analysis across datasets.

## Potential analyses and data products
- Compute cumulative sediment balance by comparing Cum_qin and Cum_qout over time.
- Link sediment fluxes with changes in channel capacity (D_CC) and flood inundation area to study sediment transport- morphology coupling.
- Develop self-serve analyses combining Sed_fluxes with Flood_data and Percentage_flooded to explore relationships between discharge, sediment delivery, and channel evolution.
- Create dashboards or reports that visualize time series of discharge, sediment flux, DEM changes, and inundated areas.

## Notes for users
- Datasets are tied to a related DEM dataset describing morphologic changes; integration with that dataset enables comprehensive analysis of sediment transport and channel evolution under flood conditions.
- All units and column descriptions are documented within each file to aid data harmonization and reproducibility.