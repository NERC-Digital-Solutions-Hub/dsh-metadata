# Mass balance and channel morphology data from an experimental river experiencing flood events

## Overview
- A dataset from a 10 m long by 2.5 m wide flume study (Total Environment Simulator, University of Hull, UK) used to examine how an experimental alluvial river evolves under varying discharge.
- Data are intended to be used with a Digital Elevation Model (DEM) dataset of the same experiment to assess sediment dynamics and channel morphology changes during flood events.
- Three data files capture sediment mass balance, channel profile changes due to floods, and area newly flooded by each flood event.

## Experimental setup
- Experimental environment: 10 m long, 2.5 m wide flume at the Total Environment Simulator, University of Hull.
- Objective: study evolution of a generic alluvial river subjected to discharge variations.
- Data are linked to measurements before and after specific flood events and to DEM-derived channel changes.

## Data files

### Sed_fluxes.csv
- Purpose: sediment discharge injected into the channel and collected at the outlet; includes cumulative values.
- Key columns:
  - date, Measurement_time: timing of each measurement.
  - Qsout(kg): mass of sediment collected at the outlet.
  - Qsin(g/s): sediment discharge imposed during the interval.
  - Duration(h), Time(h): interval duration and hours since start.
  - Qw(L/min): water discharge during the interval.
  - Qout_corrected(kg): outlet sediment mass corrected for water content.
  - Cum_qout(kg): cumulative sediment collected at the outlet.
  - Q_in(kg): sediment mass injected during the interval (Q_in = sediment discharge × duration).
  - Cum_qin(kg): cumulative mass injected.
- Data collection: sediment weighed wet at outlet; a correction coefficient is applied to convert to dry-equivalent mass by comparing the mass of a volume of wet sediment to the same volume dry.

### Flood_data.csv
- Purpose: measurements on the DEM to quantify changes in channel conveyance capacity due to floods.
- How D_CC is computed: difference in elevation within the channel (negative values in DEM Difference) × pixel area (0.0025 cm^2) ÷ channel length; results in the averaged change in channel conveyance capacity (D_CC in cm^2).
- Key columns:
  - Qw(L/min): water discharge during the flood event.
  - Duration(h): flood duration.
  - Number_scan_before, Number_scan_after: number of scans before/after flood.
  - Qw_star(m3): characteristic water discharge during the flood (Qw × duration).
  - Sum_Qw(m3): volume of water delivered before the flood (proxy for time).
  - Time(h): hours since start.
  - Exp_number: experiment number (1 or 2).
  - D_CC(cm2): averaged change in channel conveyance capacity between pre- and post-flood DEMs.

### Percentage_flooded.csv
- Purpose: area of channel newly inundated by each flood event.
- How inundated area is measured: using overhead imagery post-flood and pre-flood DEM to identify flooded areas; area is compared to the experimental area (26.5 m^2).
- Key columns:
  - Newly_flooded_area(m2): area newly inundated.
  - Qw(L/min): water discharge during the flood event.
  - Flood_number: flood event number.
  - Time(h): hours since start.
  - Duration(h): flood duration.
  - Sum_qw(m3): volume of water delivered before the flood (proxy for time).
  - Exp_number: experiment number (1 or 2).

## Related data and usage
- These datasets are designed to be used together with the Digital Elevation Model of an experimental river generated in a flume under variable discharge conditions.
- The data enable analyses of sediment balance (injected vs. collected), morphological response (DEM-based channel changes, D_CC), and hydraulic impact (flood discharge and inundation areas).

## Potential analyses for analysts
- Correlate cumulative sediment injection (Cum_qin) with cumulative outlet sediment (Cum_qout) to assess mass balance.
- Link Q_in, Qsout, and D_CC to explore how sediment input and water discharge drive channel capacity changes.
- Examine relationships between flood discharge/duration (Qw, Duration) and yields in D_CC and Newly_flooded_area.
- Compare flood-event metrics across Exp_number 1 vs 2 to assess reproducibility.
- Integrate with DEM data to map spatial patterns of channel morphologic change alongside volumetric water inputs.