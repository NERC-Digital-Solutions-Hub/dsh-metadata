# Historic spatial patterns of storm-driven compound events in UK estuaries

- Aim and scope
  - Presents a dataset of extreme river discharge and associated skew surge peaks for UK estuaries from 1984 to 2013.
  - Includes lag times between river discharge and skew surge, enabling analysis of compound flood drivers.
  - Based on 30 years of river discharge and sea level data at 15-minute resolution across 126 estuaries.

- Data sources and collection
  - Tide gauge data
    - 27 class-A tide gauges from the British Oceanographic Data Centre (BODC) National A-Class Network.
    - Total Water Level (TWL) data: hourly (1984–1992) and 15-minute (1992–2013); pre-1992 data interpolated to 15-minute cadence.
    - Quality control: discard improbable/null/interpolated observations; results in gaps (79–98% coverage for some sites) to ensure reliability.
    - Skew surge: calculated as the difference between maximum TWL and the maximum predicted TWL from astronomical tides within every 12.42-hour tidal cycle.
  - River discharge data
    - 265 rivers across Britain; 15-minute discharge measurements from Environment Agency, Natural Resources Wales, and Scottish Environment Protection Agency.
    - Used the most downstream non-tidal gauge for each river.
    - 30-year records (1984–2013) with no data gaps; selected gauges with maximum discharge >50 m3/s to identify potential flood contributors.
    - Resulted in 126 gauges corresponding to 126 estuaries, providing broad spatial coverage.

- Data processing and quality control
  - Peaks-over-threshold method to identify river discharge peaks exceeding the 95th percentile of the 30-year 15-minute dataset.
  - For each extreme discharge event, the largest skew surge within a defined storm window is identified and saved if it also exceeds the 95th percentile of the skew surge record.
  - Frequency analysis and tidal filtering:
    - Fast Fourier transform and Lomb-Scargle periodogram to confirm no tidal signal in river discharge records.
    - A 24-hour running mean applied to discharge data for smoothing.

- Data structure and files
  - SEARCH_data.csv: 10 columns containing spatial and temporal context for river and tide gauges (e.g., NAME, NUMBER, ID, EASTING, NORTHING, START, END, Max discharge, Tide gauge name, AREA).
  - 126 estuary-specific files: XXXXX_co_occurrence.csv, where each file contains:
    - RiverDischarge_95thTime: date/time of 95th percentile peak discharge.
    - RiverDischarge_95th: peak discharge value (m3/s).
    - SkewSurge_95thTime: date/time of 95th percentile skew surge.
    - SkewSurge_95th: skew surge value (m).
    - LagTime: lag between peak discharge and peak skew surge (hours).
  - File naming: XXXXX_co_occurrence.csv; XXXXX corresponds to a NUMBER code defined in the accompanying data table.
  - The methodology converts initial Excel records of co-occurrences to CSVs for interoperability and reuse.

- Analytical methods and outputs
  - Pairing approach: each river gauge is paired with the nearest tide gauge along the same coastline as the estuary discharges into the sea.
  - Co-occurrence analysis: identify dates where extreme river discharge (above 95th percentile) co-occurs with a skew surge exceeding its 95th percentile within a storm window.
  - Outputs provide timing and magnitude of co-occurrences and the associated lag times, enabling investigations into relationships and potential predictive links between riverine and coastal extreme events.

- Practical considerations and limitations
  - Data gaps in tide gauge records (<100% coverage) for several gauges, which may influence continuity and representativeness at some estuaries.
  - Southeast England is underrepresented due to shorter data records or lack of high-discharge events.
  - Skew surge calculations rely on accurate TWL decomposition into astronomical tide and residual components; quality control steps mitigate but do not eliminate potential uncertainties.

- Reference
  - Lyddon, C., Robins, P., Lewis, M., Barkwith, A., Vasilopoulos, G., Haigh, I., and Coulthard, T. (2023). Historic spatial patterns of storm-driven compound events in UK estuaries. Estuaries and Coasts, 46(1), 30-56.