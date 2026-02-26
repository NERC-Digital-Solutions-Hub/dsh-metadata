# Mass balance and channel morphology data from an experimental river experiencing flood events

## Overview
- Data from an experimental river in a 10 m long, 2.5 m wide flume (Total Environment Simulator, University of Hull, UK) studying channel evolution under varying discharge.
- Three CSV files intended to be used together with the DEM-based dataset titled “Digital Elevation Model of an experimental river generated in a flume under variable discharge conditions.”
- Focus on mass balance (sediment flux) and channel morphology changes before, during, and after flood events.

## Data files and content

- Sed_fluxes.csv
  - Sediment mass balance data: sediment injected into the channel and sediment collected at the outlet.
  - Key columns:
    - date and measurement_time: when the interval was recorded.
    - Qsout(kg): mass of sediment collected at the outlet.
    - Qsin(g/s): sediment discharge imposed during the interval.
    - Duration(h) and Time(h): interval duration and hours since start.
    - Qw(L/min): water discharge during the interval.
    - Qout_corrected(kg): outlet sediment mass corrected for water content.
    - Cum_qout(kg): cumulative sediment collected at the outlet.
    - Q_in(kg) and Cum_qin(kg): sediment injected during the interval and its cumulative total.
  - Note: sediment was weighed wet and corrected to dry with a correction coefficient derived from a wet/dry mass comparison.

- Flood_data.csv
  - Measurements on the DEM to quantify changes in channel conveyance capacity during floods.
  - How D_CC is computed: difference in channel elevation (negative values in the DEM difference), multiplied by pixel surface (0.0025 cm^2) and divided by the channel length.
  - Key columns:
    - Qw(L/min) and Duration(h): water discharge and flood duration.
    - Number_scan_before and Number_scan_after: raster/DEM scans before and after flood.
    - Qw_star(m3): characteristic water discharge during the flood (discharge × duration).
    - Sum_Qw(m3): total water volume delivered before the flood (time proxy).
    - Time(h): hours since the start.
    - Exp_number: experiment number (1 or 2).
    - D_CC(cm^2): average change in channel conveyance capacity between pre- and post-flood DEMs.

- Percentage_flooded.csv
  - Measurements of area newly inundated by each flood event using overhead imagery and pre-flood DEMs (compared to a 26.5 m^2 experimental area).
  - Key columns:
    - Newly_flooded_area(m2): area newly inundated.
    - Qw(L/min) and Time(h): water discharge and time.
    - Flood_number and Duration(h): flood event identifier and duration.
    - Sum_qw(m3) and Exp_number: volume of water delivered before the flood and experiment number.

## Experimental context and dataset linkage
- Data describe sediment flux and morphological responses of an alluvial river in controlled flood events.
- Designed to be used in conjunction with the DEM dataset to analyze how discharge variations affect sediment transport and channel morphology.
- Experiments include two runs (Exp_number 1 or 2) and multiple flood events with corresponding scans and measurements.

## GIS and data usage implications
- Enables spatial analysis of sediment transport, channel capacity changes, and floodplain inundation when integrated with DEM data.
- Useful for visualizing:
  - Temporal changes in sediment flux at the outlet and within the channel.
  - Spatially derived changes in channel conveyance capacity from DEM differences.
  - Spatial extent of newly inundated areas per flood event.
- Data units and processing notes to consider:
  - Sediment flux data require conversion between mass and time units; corrected outlet masses account for water content.
  - D_CC is derived from DEM differencing and pixel-area assumptions (pixel area given as 0.0025 cm^2; note potential unit inconsistency to verify during integration).
  - Time is tracked in hours since experiment start, with separate experiment numbers.

## Quality, limitations, and considerations
- Data collected in a controlled flume environment; applicability limited to similar lab-scale, alluvial river setups.
- Manual collection and correction steps introduce potential measurement uncertainties (e.g., wet-to-dry corrections, DEM difference interpretation).
- Requires alignment with the associated DEM dataset for coherent spatial-temporal analysis.
- Multiple files are interrelated by time and experiment number, enabling integrated analysis but requiring careful data stitching.