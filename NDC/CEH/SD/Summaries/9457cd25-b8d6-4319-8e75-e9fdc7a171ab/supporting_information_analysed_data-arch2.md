# Mass balance and channel morphology data from an experimental river experiencing flood events

## Overview
- Dataset from an experimental flume study of a generic alluvial river subjected to discharge variations.
- Purpose: study sediment mass balance and channel morphology changes during flood events, in conjunction with a Digital Elevation Model (DEM) dataset of the same experimental river.
- Experimental setup: 10 m long, 2.5 m wide flume (Total Environment Simulator, University of Hull, UK).

## Data files and content
- Sed_fluxes.csv
  - Purpose: mass balance – sediment injected vs. sediment collected at the outlet.
  - Key columns:
    - date, Measurement_time: timing of each measurement.
    - Qsout(kg): sediment mass collected at outlet.
    - Qsin(g/s): sediment discharge imposed during the interval.
    - Duration(h): interval duration.
    - Time(h): hours since experiment start.
    - Qw(L/min): water discharge during the interval.
    - Qout_corrected(kg): outlet sediment mass corrected for water content.
    - Cum_qout(kg): cumulative sediment at outlet.
    - Q_in(kg): sediment injected during the interval (Qsin × Duration).
    - Cum_qin(kg): cumulative sediment injected.
  - Notes: sediment collected at outlet was weighed wet and corrected to a dry mass using a correction coefficient based on the wet/dry mass ratio.

- Flood_data.csv
  - Purpose: measurements of channel morphology changes to calculate change in channel conveyance capacity (D_CC) during floods.
  - How D_CC is calculated: difference in DEM elevations within the channel (negative values indicate contraction), multiplied by pixel area (0.0025 cm^2) and divided by channel length.
  - Key columns:
    - Qw(L/min): water discharge during the flood.
    - Duration(h): flood duration.
    - Number_scan_before / Number_scan_after: number of scans before and after the flood.
    - Qw_star(m3): characteristic water discharge during the flood (Qw × duration).
    - Sum_Qw(m3): volume of water delivered before the flood (proxy for time).
    - Time(h): hours since start.
    - Exp_number: experiment number (1 or 2).
    - D_CC(cm2): average change in channel conveyance capacity between pre- and post-flood DEMs.

- Percentage_flooded.csv
  - Purpose: quantify area newly inundated by each flood event.
  - Method: combine post-flood overhead imagery with pre-flood DEM to identify flooded areas; compare against experimental area (26.5 m^2).
  - Key columns:
    - Newly_flooded_area(m2): area newly inundated.
    - Qw(L/min): water discharge during the flood.
    - Flood_number: flood event number.
    - Time(h): hours since start.
    - Duration(h): flood duration.
    - Sum_qw(m3): volume of water delivered before the flood (proxy for time).
    - Exp_number: experiment number (1 or 2).

## Data collection and processing
- Sediment mass balance
  - Sediment injected and collected measured; outlet masses corrected for water content to obtain dry mass estimates.
- Morphology and conveyance
  - DEM-based analysis of elevation differences used to derive changes in channel conveyance capacity due to floods.
  - Flood-related inundation areas derived by integrating imagery and DEM data.

## Experimental setup details
- Physical scale: 10 m long, 2.5 m wide flume.
- Location: Total Environment Simulator, University of Hull, UK.
- Objective: understand how a representative alluvial river responds to discharge variations, including sediment transport and morphological adjustments during floods.

## Relationship to related datasets
- These data are intended to be used in conjunction with the "Digital Elevation Model of an experimental river generated in a flume under variable discharge conditions" dataset to enable integrated analysis of sediment balance and channel morphology over time.

## Relevance for environmental analytics
- Provides standardized, time-stamped metrics of sediment input/output, flood-driven channel capacity changes, and area inundation.
- Enables assessment of environmental health indicators related to sediment dynamics and flood morphology in a controlled, repeatable setting.
- Supports cross-dataset comparisons and longitudinal monitoring by keeping clear units, timing, and experiment identifiers (Exp_number).

## Access and usage notes
- Data are organized in three CSV files with clearly defined column headers and descriptions.
- Intended for analytical workflows that combine sediment balance, DEM-derived morphology, and flood-area metrics.
- Caution: results reflect a controlled flume environment and may require adaptation before applying to natural river systems.