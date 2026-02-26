# Historic spatial patterns of storm-driven compound events in UK estuaries

## Overview
- Dataset of dates and magnitudes of extreme river discharge and associated skew surge peaks for UK estuaries from 1984 to 2013, including lag times between drivers.
- 30 years of river discharge and sea level data across 126 estuaries; data at 15-minute temporal resolution.
- Peaks over threshold analysis identifies river discharge peaks above the 95th percentile; largest skew surge within the storm window is paired with each extreme discharge event if it also exceeds the 95th percentile.

## Data sources and scope
- Tide gauge (total water level) data from 27 class-A tide gauges (UK National A-Class Tide Gauge Network, BODC). Observations at hourly frequency (1984–1992) and 15-minute frequency (1992–2013); pre-1992 data interpolated to 15 minutes.
- River discharge data for 265 rivers collected from the Environment Agency (England), Natural Resources Wales, and the Scottish Environment Protection Agency; gauges selected were the most downstream non-tidal and provided 30 years of data (1984–2013) with peaks >50 m3/s.
- Spatial coverage across Britain with good coverage, though southeast England is underrepresented due to shorter or absent records.
- Quality control includes discarding improbable, null, or interpolated TWL data; gaps exist in TWL coverage (79–98%), but only reliable observations were used.

## Analytic methods
- Quality control to remove tidal signals in river discharge using fast Fourier transform and Lomb-Scargle periodogram; river discharge data smoothed with a 24-hour running mean.
- Peaks-over-threshold analysis using a threshold of 3-month moving mean plus 95th percentile to identify extreme river discharge events.
- For each extreme river discharge, identify the largest skew surge (S) within a storm window; save the event if S also exceeds its 95th percentile.
- Times and magnitudes of co-occurring events are compiled per catchment; lag time is calculated between the river discharge peak and the skew surge peak.
- Data management: results initially recorded in Microsoft Excel and then converted to CSV.

## Data structure and files
- SEARCH_DATA.csv: contains spatial and temporal metadata for the 126 estuaries (10 columns: river/gauge name, ID, coordinates, time range, max discharge, nearest tide gauge, area, etc.).
- 126 co_occurrence.csv files: per estuary, named XXXXX_co_occurrence.csv (XXXXX corresponds to the gauge NUMBER); each file has 5 columns:
  - RiverDischarge_95thTime (Date/time)
  - RiverDischarge_95th (m3/s)
  - SkewSurge_95thTime (Date/time)
  - SkewSurge_95th (m)
  - LagTime (hours)

## Data quality, limitations, and references
- Missing tide gauge data led to gaps in TWL data (coverage between 79% and 98% for some gauges); only reliable observations used.
- Pre-1992 TWL data were interpolated to 15-minute resolution, introducing potential uncertainties.
- Southeast England has less complete data due to shorter records or lack of high-discharge events in the period.
- Storm window details and methodology are described in Lyddon et al. (2023), Historic spatial patterns of storm-driven compound events in UK estuaries.

## Alignment with the Analysts Monitoring the Environment archetype
- Data provenance, verification, quality assurance, cleaning, and transformation are applied to established monitoring data sources.
- Outputs are standardized (CSV files, clearly defined fields) and prepared for dissemination in reports, maps, or charts.
- Datasets are organized and stored with metadata (SEARCH_DATA.csv) and per-estuary co_occurrence files, supporting transparency and reuse.
- Emphasis on enabling access to underlying data and integrating the dataset with other datasets for expanded environmental monitoring.
- Outputs support assessment of environmental health and policy performance over time, enabling monitoring of compound flood risk across multiple estuaries.

## Reference
- Lyddon, C., Robins, P., Lewis, M., Barkwith, A., Vasilopoulos, G., Haigh, I. and Coulthard, T., 2023. Historic spatial patterns of storm-driven compound events in UK estuaries. Estuaries and Coasts, 46(1), pp.30-56.