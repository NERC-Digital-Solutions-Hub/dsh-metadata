# Mass balance and channel morphology data from an experimental river experiencing flood events

## Overview
- Experimental dataset from a 10 m long, 2.5 m wide flume (Total Environment Simulator, University of Hull, UK) studying the evolution of a generic alluvial river under discharge variations.
- Three integrated data files documenting sediment mass balance, channel morphology changes during floods, and area of newly inundated land.

## Datasets Included
- Sed_fluxes.csv
  - Sediment discharge injected during intervals and collected at the outlet, plus time, discharge, duration, and cumulative sums.
  - Includes Qsout, Qsin, Q_in, Qw, durations, times, and corrected outlet mass (Qout_corrected) with cumulated values (Cum_qout, Cum_qin).
  - Sediment collected at the outlet is weighed wet and corrected to a dry mass using a correction coefficient derived from comparing wet/dry masses.
- Flood_data.csv
  - Measurements on the digital elevation model (DEM) to compute changes in channel conveyance capacity (D_CC) during floods.
  - Key fields: Qw, flood duration, number of scans before/after flood, Qw_star, Sum_Qw, time, experiment number, and D_CC (cm^2).
  - D_CC derived from difference in DEM elevations, scaled by pixel area and channel length.
- Percentage_flooded.csv
  - Area of the channel newly inundated by each flood event.
  - Key fields: Newly_flooded_area (m^2), Qw, flood number, time, duration, Sum_qw, and experiment number.

## Data collection and context
- Data generated to study how a controlled alluvial river responds to varying discharge, capturing sediment transport and morphological response during floods.
- Measurements tied to discrete flood events and corresponding DEM assessments to quantify hydromorphological change.

## Data processing and corrections
- Sed_fluxes: manual sediment collection at the outlet, with wet mass corrected to dry mass using a correction coefficient.
- Flood_data: DEM-based calculation of changes in channel conveyance capacity (D_CC) using elevation differences, pixel area, and channel length.
- Percentage_flooded: analysis combining post-flood imagery with pre-flood DEMs to determine new inundation areas relative to the experimental footprint.

## How this supports monitoring framework goals
- Provides a structured, traceable data suite for evaluating sediment balance, hydromorphological change, and flood extent in a controlled setting—useful for benchmarking monitoring approaches and validating indicators of environmental health.
- Demonstrates end-to-end data handling: from raw measurements to corrected mass balances, morphological change metrics, and spatial extent of flooding.
- Can inform data governance practices: explicit data descriptions, units, and processing steps; highlights needs for metadata completeness and data sharing practices when applying monitoring frameworks.

## Metadata, governance, and usability considerations
- Metadata depth: descriptions and units are provided for each field; however, explicit data licensing or sharing norms are not stated.
- Data quality considerations: wet-to-dry mass correction, measurement timing, cumulative sums, and DEM-derived metrics require careful metadata to ensure reproducibility.
- Potential barriers: dataset scale (experimental flume) may affect generalizability; transformation steps and measurement methodologies should be well-documented when integrating into larger monitoring frameworks.
- Interoperability: data are tied to an associated DEM dataset for the same experimental setup, enabling combined hydro-morphological analyses.

## Limitations and cautions
- Experimental context may limit applicability to natural rivers without adjustments for scale, boundary conditions, and material properties.
- Some fields (e.g., data sharing, licensing) are not specified; users should verify data access terms and ensure appropriate metadata for reuse.

## Practical takeaways for monitoring practice
- Use sediment balance data to quantify input–output budgets and assess transport efficiency under variable discharge.
- Apply DEM-based D_CC measurements to track conveyance capacity changes and relate them to morphological evolution during floods.
- Combine area inundation data with water discharge and duration to evaluate flood impact and inform flood risk monitoring protocols.