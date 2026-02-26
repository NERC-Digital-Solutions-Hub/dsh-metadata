# Overview

- This dataset contains the dates and magnitudes of extreme river discharge and associated skew surge peaks for UK estuaries between 1984 and 2013, plus the lag time between the drivers.
- Analysis covered 30 years of river discharge and sea level data for 126 estuaries around the UK, using a 15-minute temporal resolution.

- Key outputs:
  - Peaks over threshold in river discharge (above the 95th percentile).
  - The largest skew surge for each extreme discharge event, saved if it also exceeds the 95th percentile.
  - Lag times between peak discharge and peak skew surge.

Data scope and sources
- River discharge data
  - Collected from 265 rivers across Britain (Environment Agency, Natural Resources Wales, Scottish Environment Protection Agency).
  - 30-year period (1984-2013) from the most downstream, non-tidal gauges.
  - 126 gauges identified with full 30-year data and with maximum discharge >50 m3/s to ensure potential flood relevance.
- Tide gauge data (total water level, TWL)
  - Observations from 27 class-A tide gauges within the UK National A-Class Tide Gauge Network (BODC).
  - Observed TWL at hourly frequency (1984-1992) and 15-minute frequency (1992-2013).
  - Pre-1992 data interpolated to 15 minutes to align with river data; data flagged as improbable, null, or interpolated were discarded.
  - Missing TWL data led to gaps in time series (79–98% coverage for some sites), but only reliable observed values were used.

Derived metrics and calculations
- Skew surge (S)
  - Calculated from detrended TWL as the difference between maximum TWL and the maximum predicted TWL based on astronomical tides for every 12.42-hour tidal cycle.
  - Produces one S value per tidal cycle (about 706 per year) with the time of maximum TWL assigned to each S value.
- Peaks over threshold
  - River discharge peaks exceeding the 95th percentile of the 30-year 15-minute discharge dataset (upper 5%).
  - For each extreme discharge event, the largest skew surge within a storm window was identified and retained if also above the 95th percentile.

Data structure and files
- SEARCH_DATA.csv
  - Contains 10 columns with metadata for river gauges: name, river gauge reference code, ID, coordinates (Easting/Northing), time series start/end, maximum discharge, closest tide gauge, catchment area.
- 126 co_occurrence.csv files (one per estuary)
  - Five columns: RiverDischarge_95thTime (date/time of peak discharge above 95th percentile), RiverDischarge_95th (peak discharge in m3/s), SkewSurge_95thTime (date/time of peak skew surge above 95th percentile), SkewSurge_95th (peak skew surge in m), LagTime (hours between peak discharge and peak skew surge).
- File naming
  - XXXXX_co_occurrence.csv where XXXXX is NUMBER (as defined in accompanying documentation).

Analytical methods and data processing
- River gauges paired with the nearest tide gauge on the same coastline.
- Peaks over threshold defined as 3-month moving mean plus 95th percentile; the largest skew surge within a storm window around each peak was recorded if also above the threshold.
- Results compiled in Microsoft Excel spreadsheets per catchment and then converted to CSVs.

Quality control and provenance
- Quality checks include:
  - Fast Fourier transform and Lomb-Scargle periodogram to confirm no tidal signal in river discharge records.
  - 24-hour running mean applied to river discharge data as smoothing.
- Provenance reference: Lyddon et al. (2023) Estuaries and Coasts, detailing historic spatial patterns of storm-driven compound events in UK estuaries.