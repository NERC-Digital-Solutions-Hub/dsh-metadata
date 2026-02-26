# Water discharge data for Trout Beck, Cumbria.  1961 - 1980

## Overview
- Dataset of water discharge for Trout Beck, Cumbria, UK, covering 1961–1980.
- Collected by multiple staff at Moor House Research Station for the Wear and Tees River Board and the NRA; recorder names not captured.
- Stored in a database described in Cuthbertson (1993).

## Site and scope
- Location: Trout Beck Weir, grid reference 375900 533600.
- Recording locations (DATID) and periods:
  - 39: Trout Beck gauging station. Imperial units originally; converted to metric. Earliest 01-Oct-1961, latest 30-Sep-1968.
  - 17: TROUTBECK gauging station (Northumberland Water Authority). Earliest 01-Oct-1968, latest 30-Jun-1980.

## Data variables and format
- DATID: Recording location identifier.
- REC_TIME: Date (the day represented by the record).
- TCMD: Total Mean Daily Discharge (cumecs).
- MEAN: Mean discharge (cumecs).
- HIGHEST: Highest discharge during the day (cumecs).
- HGH_TIME: Hour of the greatest discharge.
- LOWEST: Lowest discharge during the day (cumecs).
- LOW_TIME: Hour of the lowest discharge.

## Temporal coverage and data characteristics
- Time span: 01-Oct-1961 to 30-Sep-1980, with two sequential recording locations over time.
- Units: Imperial originally, converted to metric (cumecs).

## Notable data notes
- A large peak in March 1979 observed; likely related to snowmelt after a major snow event in the UK. No accompanying notes in the database.

## Quality, provenance, and references
- Data gathered by various staff; no individual contributor names recorded.
- Database described in Cuthbertson (1993): A database for environmental research programmes (J. Env. Management, 37(4), 291-300). DOI: 10.1006/jema.1993.1023.

## How this data could be used (Data Support perspective)
- Time-series analysis of river discharge trends and seasonal patterns.
- Cross-location comparisons between Trout Beck gauging stations (DATID 39 vs 17).
- Building self-serve dashboards or pivot-table summaries (daily, monthly, yearly discharge metrics).
- Anomaly detection (e.g., unusual displacement in 1979 peak) and data quality checks.
- Data integration with other hydrological datasets (unit conversions, temporal alignment).