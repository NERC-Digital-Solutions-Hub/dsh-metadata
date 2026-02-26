# Overview

- Dataset of the dates and magnitudes of extreme river discharge and associated skew surge peaks for UK estuaries, covering 1984–2013, with lag times between river drivers and skew surge.
- Analysis spans 126 estuaries across Britain using river discharge and tide gauge data at 15-minute resolution; peaks over threshold (top 5%) are identified and paired with the largest skew surge within a storm window.
- Skew surge is the difference between maximum observed total water level and the maximum predicted from astronomical tides, calculated for every 12.42-hour tidal cycle.
- Tide gauge data come from 27 class-A gauges in the UK National A-Class Tide Gauge Network; observations are hourly (1984–1992) and 15-minute (1992–2013), with pre-1992 data interpolated to 15 minutes and questionable data discarded.

- River discharge data are from 265 rivers (most downstream non-tidal gauges) provided by EA, NRW, and SEPA; 126 gauges meet 30-year continuous data and exceed 50 m3/s to indicate potential flood contributions.

- Data collection results in SEARCH_DATA.csv (metadata) and 126 XXXXX_co_occurrence.csv files (co-occurrence details per estuary).

- 15-minute data resolution enables map-based visualization of spatial patterns and temporal sequences of extreme events for GIS audiences.

- Quality control includes spectral checks to remove tidal signals from river records and a 24-hour smoothing of discharge data.

- The dataset builds on Lyddon et al. (2023) and provides detailed temporal and spatial attributes suitable for GIS analyses of compound coastal flood risk.