# Mass balance and channel morphology data from an experimental river experiencing flood events

- Purpose and context
  - Dataset accompanying the DEM-based dataset titled “Digital Elevation Model of an experimental river generated in a flume under variable discharge conditions.”
  - Created to study the evolution of an alluvial river in a controlled flume under varying discharge conditions.
  - Experimental setup: 10 m long, 2.5 m wide flume at the Total Environment Simulator, University of Hull, UK.
  - Three data files capture sediment mass balance, channel morphology changes during floods, and area newly flooded per event.

## Data files and contents

- Sed_fluxes.csv
  - Focus: sediment discharge injected into the channel and collected at the outlet.
  - Key columns:
    - date, Measurement_time: timing of each measurement
    - Qsout(kg): mass of sediment collected at the outlet
    - Qsin(g/s): sediment discharge imposed during the interval
    - Duration(h), Time(h): interval duration and hours since start
    - Qw(L/min): water discharge during the interval
    - Qout_corrected(kg): outlet sediment mass corrected for water content
    - Cum_qout(kg): cumulative sediment collected at outlet
    - Q_in(kg), Cum_qin(kg): sediment injected during the interval and cumulative injected
  - Data handling detail: sediment collected wet and corrected to dry mass using a correction coefficient derived from comparing wet vs. dry masses.

- Flood_data.csv
  - Focus: measurements on the DEM to quantify changes in channel conveyance capacity due to floods.
  - Key columns:
    - Qw(L/min), Duration(h): water discharge and flood duration
    - Number_scan_before, Number_scan_after: scan counts relative to flood start
    - Qw_star(m3): characteristic water discharge during the flood
    - Sum_Qw(m3): volume of water delivered before the flood (proxy for time)
    - Time(h), Exp_number: time since start and experiment number (1 or 2)
    - D_CC(cm2): averaged change in channel conveyance capacity between pre- and post-flood DEMs
  - Calculation note: D_CC derived from DEM elevation differences multiplied by pixel area, normalized by channel length.

- Percentage_flooded.csv
  - Focus: area newly inundated by each flood event.
  - Key columns:
    - Newly_flooded_area(m2): area newly inundated
    - Qw(L/min), Time(h), Duration(h): water discharge, time, and flood duration
    - Flood_number: sequence number of flood event
    - Sum_qw(m3): volume of water delivered before the flood (time proxy)
    - Exp_number: experiment number (1 or 2)
  - Method: flood-extent identified from overhead photos and pre-flood DEMs, compared to the experimental area of 26.5 m2.

## Data provenance and relationships

- All datasets pertain to the same experimental campaign and can be integrated with the associated DEM-based dataset to analyze how sediment balance and flood events drive channel morphology and conveyance changes.
- Data collection includes both manual measurements (sediment masses) and DEM-derived metrics (D_CC and flooded area).

## Data quality, limitations, and considerations for use

- Measurement basis: manual mass measurements and DEM differencing; may require careful calibration and documentation of correction factors (e.g., water-content correction for sediment masses).
- Spatial-temporal granularity: flood-related metrics rely on discrete scans and event timing; alignment with other datasets should consider scan timing and event boundaries.
- Applicability: results are specific to a controlled 10 m × 2.5 m flume and may require caution when extrapolating to natural rivers.
- Missing details: while column descriptions are provided, external data quality checks (e.g., metadata standards, units consistency, versioning) should be confirmed when integrating across systems.

## Practical relevance for Data Leaders

- Discoverability and interoperability
  - Three clearly named CSV files with explicit column descriptions that facilitate integration with the companion DEM dataset.
  - Aligns with broader data-system goals: understanding data availability, provenance, and how data serve user needs (e.g., policy colleagues or partners studying flood impacts on channel morphology).

- Data management and governance
  - Emphasizes the importance of documenting data corrections (e.g., wet-to-dry mass correction) and metadata to enable reproducibility.
  - Supports end-to-end analysis workflows from sediment balance to morphological change and flood extent.

- Collaboration and reuse
  - Dataset design supports cross-disciplinary use (hydraulics, geomorphology, watershed management) and potential collaboration to extend the dataset or compare with other experimental setups.
  - The explicit link to the accompanying DEM dataset enables more robust, model-driven analyses of channel evolution under varying discharges.