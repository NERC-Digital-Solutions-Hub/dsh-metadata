# Overview

- The dataset contains the dates and magnitudes of extreme river discharge and associated skew surge peaks for UK estuaries from 1984 to 2013, with lag times between the drivers.
- Based on 30 years of river discharge and sea-level data for 126 estuaries around the UK, using river discharge and tide gauge data at 15-minute resolution.
- Peaks over threshold analysis identifies river discharge peaks above the 95th percentile; the largest skew surge within the storm window around each peak is saved if it also exceeds the 95th percentile.
- Tide gauge data come from 27 class-A tide gauges (BODC). Observations are hourly (1984–1992) and 15-minute (1992–2013); pre-1992 data were interpolated to 15-minute intervals.
- River discharge data come from 265 rivers (downstream non-tidal gauges) across Britain; 126 gauges meet the criteria of 30 years of data (1984–2013) with no data gaps and maximum discharge >50 m3/s.
- Skew surge is computed as the difference between maximum TWL (total water level) and the maximum predicted TWL from astronomical tidal constituents for each 12.42-hour tidal cycle, yielding ~706 skew surge values per year.
- Data quality controls include removing improbable or interpolated tide gauge data and verifying no tidal signal in river discharge records via FFT and Lomb-Scargle analyses; a 24-hour running mean smooths river discharge data.
- Data are provided as CSV files for 126 estuaries plus a SEARCH_DATA.csv with 10 descriptive fields and 126 co_occurrence CSV files (five columns each) describing co-occurring extreme river discharge and skew surge events.
- File structure:
  - SEARCH_DATA.csv: spatial and temporal info for rivers and tide gauges (start/end times, maximum discharge, nearest tide gauge, area, etc.).
  - 126 estuary CSVs (XXXXX_co_occurrence.csv): RiverDischarge_95thTime, RiverDischarge_95th, SkewSurge_95thTime, SkewSurge_95th, LagTime.
- Analytical workflow:
  - Pair river gauges with the nearest tide gauge on the same coastline.
  - Identify peaks over the 3-month moving mean + 95th percentile in river discharge.
  - Record the largest skew surge within the storm window for each peak; save if the skew surge also exceeds its 95th percentile.
  - Export results first to Excel, then to CSV.
- Practical uses: enables exploration of compound flood-hazard events, lag analysis between river discharge peaks and skew surges, and supports data-driven dashboards or self-serve analyses.
- Reference: Lyddon, C. et al., 2023. Historic spatial patterns of storm-driven compound events in UK estuaries. Estuaries and Coasts, 46(1), 30-56.