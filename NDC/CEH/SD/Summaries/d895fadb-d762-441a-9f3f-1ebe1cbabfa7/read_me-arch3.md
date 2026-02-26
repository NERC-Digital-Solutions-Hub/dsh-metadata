# Historic spatial patterns of storm-driven compound events in UK estuaries

## Aim
- Provide dates and magnitudes of extreme river discharge and associated skew surge peaks for UK estuaries from 1984 to 2013, including lag times between the drivers.
- Support understanding of compound flooding and inform policy decisions and future monitoring approaches.

## What the dataset covers
- 30 years of river discharge and sea level data for 126 estuaries across Britain.
- River discharge and tide gauge data at 15-minute resolution (1984–2013).
- Skew surge calculated for each extreme discharge event, with its largest value also requiring above-threshold criteria.
- Lag time between peak discharge and associated skew surge.

## Data sources and collection
- Tide gauge data: observed total water level (TWL) from 27 class-A gauges in the UK National A-Class Tide Gauge Network, provided by the British Oceanographic Data Centre (BODC). Temporal resolution: hourly (1984–1992) and 15-minute (1992–2013); pre-1992 data interpolated to 15 minutes.
- River discharge data: 15-minute river discharge measurements from the Environment Agency, Natural Resources Wales, and the Scottish Environment Protection Agency for 265 rivers; selected gauges represent 30 years of data (1984–2013) with continuous records and maximum discharge above 50 m3/s to indicate flood contributors.
- Data filtration: removed TWL data flagged as improbable, null, or interpolated; acknowledged gaps in tide gauge data (79–98% coverage for some gauges).

## Data processing and quality control
- Skew surge defined as the difference between maximum TWL and the maximum predicted TWL from astronomical tidal constituents, computed for each 12.42-hour tidal cycle (one S value per cycle, ~706 per year).
- A fast Fourier transform and Lomb-Scargle periodogram used to confirm the river records contained no tidal signal; a 24-hour running mean smoothed the river discharge data.
- A peaks-over-threshold approach applied to river discharge: thresholds set at 3-month moving mean + 95th percentile; the largest skew surge within a storm window around each peak is recorded if it exceeds the 95th percentile of skew surge.

## Data structure and file content
- SEARCH_DATA.csv: contains 10 columns with river gauge metadata and associated tide gauge information (name, identifier, location coordinates, time series start/end, maximum discharge, area, and tide gauge name).
- For each estuary, a co_occurrence CSV file named XXXXX_co_occurrence.csv (where XXXXX is a gauge number) with five columns:
  - RiverDischarge_95thTime: time of peak river discharge above the 95th percentile.
  - RiverDischarge_95th: peak river discharge value above the 95th percentile (m3/s).
  - SkewSurge_95thTime: time of peak skew surge above the 95th percentile.
  - SkewSurge_95th: peak skew surge value above the 95th percentile (m).
  - LagTime: hours lag between peak river discharge and peak skew surge.

## Analytical workflow
- Pair each river gauge with the nearest tide gauge on the same coastline.
- Identify peaks over the threshold (3-month moving mean + 95th percentile) in river discharge.
- Determine the largest skew surge within the storm window around each peak and retain the pair if the skew surge also exceeds its 95th percentile.
- Record dates and magnitudes of co-occurring events; results compiled in Excel and converted to CSV.

## Data governance, sharing, and metadata
- Metadata and data structure are documented to support reproducibility and reuse.
- The approach emphasizes transparent data provenance, quality checks, and clear presentation of results (time-stamped co-occurrence events).

## Limitations and caveats
- Data gaps in tide gauge records lead to incomplete time series for some sites; Southeastern England has notable gaps.
- Pre-1992 TWL data required interpolation to 15-minute resolution, which introduces potential uncertainties.
- Some gauges have relatively low coverage (e.g., 79–98%), which may affect spatial representativeness.

## References
- Lyddon, C., Robins, P., Lewis, M., Barkwith, A., Vasilopoulos, G., Haigh, I., and Coulthard, T., 2023. Historic spatial patterns of storm-driven compound events in UK estuaries. Estuaries and Coasts, 46(1), pp. 30-56.