# Climatic data (Meteorological Office recordings) from four sites along an altitudinal gradient in Cumbria. 1952 - 1990

## Overview and provenance
- Climate dataset from four sites along an altitudinal gradient in Cumbria, collected according to standard Meteorological Office procedures (Observer's Handbook, 4th ed., 1982).
- Data stored in a database described by Cuthbertson (1993); summary available in MM.pdf.
- UK Environmental Change Network has continued monitoring at Moor House (1991-2015); reference Rennie et al. (2017).

## Site details
- Newton Rigg
  - Grid reference: 349300 531000
  - Altitude: 171 m
  - Data collection staff: Newton Rigg Agricultural College
- Widdybank Fell
  - Grid reference: 381700 529700
  - Altitude: 527 m
  - Data collection staff: Ian Findlay
- Moor House
  - Grid reference: 375100 533400
  - Altitude: 549 m
  - Data collection staff: Andy Millar
- Great Dun Fell
  - Grid reference: 371600 532100
  - Altitude: 847 m
  - Data collection staff: Unknown

## Recording locations and data periods
- Each site is identified in the dataset by a DATID.
- Site date ranges:
  - Moor House: 01-MAY-1952 to 31-DEC-1979
  - Newton Rigg: 01-JAN-1959 to 31-DEC-1990
  - Widdybank Fell: 01-JUN-1974 to 31-DEC-1989
  - Great Dun Fell: 01-JAN-1973 to 29-AUG-1975

## Data schema and key variables
- identifiers:
  - DATID: dataset identification number
  - REC_DTE: record date
- weather and climate variables (with units):
  - MAXTMP, MINTMP, MEANTMP: daily temperatures (°C)
  - MINGRTMP: daily minimum grass temperature (°C)
  - E10TMP, E20TMP, E30TMP, E100TMP: soil temperatures at 10 cm, 20 cm, 30 cm, and 1 m (°C)
  - DRYTMP, WETTMP, DEWTMP: dry bulb, wet bulb, and dew point temperatures (°C)
  - HUMIDITY: humidity (%)
  - VAPPRESS: vapour pressure (mb)
  - SUNSHINE: hours of sunshine
  - WINDDIR: wind direction (degrees)
  - WINDVEL: wind velocity (knots)
  - HALFSNOW, SNOWDEPTH, NEWSNOW: snow indicators (0/1 or cm)
  - CLOUD: cloud cover (scale)
  - VISIBILITY: visibility (km)
  - VISCODE: visibility code (reference table)
  - WEATHDESC: weather description
  - THUNDER, GALE, FOG: presence indicators (Y/other codes)
- visibility code table (mapping 1–9 to qualitative descriptions from thick fog to excellent)

## Data quality, metadata and discoverability
- Data documented with explicit fields and codes; VISCODE references a separate visibility code table.
- Metadata and supporting documentation available (MM.pdf); MO procedures referenced (Observer's Handbook, 1982).
- Dataset linked to an ongoing data continuum via ECN Moor House monitoring (post-1990 context).

## Relevance for data strategy and use
- Demonstrates multi-site, long-term environmental data collection with standardized procedures and clear provenance.
- Provides a structured data schema suitable for cross-site comparison, trend analysis, and integration with broader environmental datasets.
- Highlights importance of metadata (dates, site altitudes, staff, data IDs) for discoverability and data governance.
- Illustrates potential continuation opportunities and data lineage through ECN, enabling extended temporal analyses beyond 1990.