# Climatic data (Meteorological Office recordings) from four sites along an altitudinal gradient in Cumbria. 1952 - 1990

## Overview
- Four-site climatological dataset collected along an altitudinal gradient in Cumbria, spanning 1952–1990.
- Collected according to standard Meteorological Office procedures (Observer's Handbook, 4th edition, 1982).
- Data stored in a database described by Cuthbertson (1993); a summary is available in MM.pdf.
- Intended for environmental research and monitoring, with documentation to support data use and interpretation.

## Sites and timing
- Newton Rigg: grid reference 349300 531000; altitude 171 m; data period 1959–1990; staff: Newton Rigg Agricultural College.
- Widdybank Fell: grid reference 381700 529700; altitude 527 m; data period 1974–1989; staff: Ian Findlay.
- Moor House: grid reference 375100 533400; altitude 549 m; data period 1952–1979; staff: Andy Millar.
- Great Dun Fell: grid reference 371600 532100; altitude 847 m; data period 1973–1975; staff: Unknown.
- Dataset records the site-specific data using DATID; earliest and latest dates per site are noted.

## Data content and structure
- Variables cover meteorological and related environmental measurements, including:
  - Temperature: MAXTMP, MINTMP, MEANTMP, MINGRTMP, E10TMP, E20TMP, E30TMP, E100TMP, DRYTMP, WETTMP, DEWTMP (all in °C).
  - Humidity-related: HUMIDITY (percentage).
  - Vapour pressure: VAPPRESS (mb).
  - Sunshine: SUNSHINE (hours).
  - Wind: WINDDIR (direction in degrees), WINDVEL (knots).
  - Snow and snowfall: HALFSNOW (binary), SNOWDEPTH (cm), NEWSNOW (cm).
  - Cloud and visibility: CLOUD (codes for cloud cover), VISIBILITY (km), VISCODE (visibility code with a lookup table).
  - Weather and extreme events: WEATHDESC, THUNDER, GALE, FOG (codes/Y indicators).
- Data fields include REC_DTE (date) and DATID (data set identifier).
- Visibility codes provide descriptive categories from thick fog to excellent visibility.

## Data provenance, metadata, and documentation
- Original data described as climatic data recorded for the Met Office at each site.
- Recording locations and data ranges are documented in associated tables (including DATID mappings and earliest/latest dates per site).
- Supporting documentation MM.pdf provides a summarized view of the data.
- The broader metadata and data lineage are connected to the referenced 1993 Cuthbertson database description.

## Data continuity and related monitoring
- A note indicates ongoing monitoring at Moor House by the UK Environmental Change Network (ECN) with datasets continuing beyond the original 1952–1990 window (Rennie et al., 2017).
- The UK ECN data are available via the NERC Environmental Information Data Centre (DOI provided), highlighting continuity and potential for extended trend analyses beyond 1990.

## Relevance for monitoring frameworks
- Illustrates how long-term environmental health indicators can be built from standardized meteorological datasets across multiple sites.
- Demonstrates the importance of:
  - Standard procedures and documentation for data collection.
  - Clear data provenance, metadata, and data storage practices.
  - Addressing data gaps, site-specific staff responsibilities, and visibility of data ranges.
  - Potential barriers to data sharing and the need for ongoing data governance to ensure data remain usable and up-to-date.
- Provides a concrete example of integrating historical climate records into contemporary monitoring frameworks, with opportunities for data augmentation and continuity through ECN data.