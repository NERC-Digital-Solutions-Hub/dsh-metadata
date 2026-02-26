# Climatic data (Meteorological Office recordings) from four sites along an altitudinal gradient in Cumbria. 1952 - 1990

## Overview
- Climatic data collected from four sites along an altitudinal gradient in Cumbria, covering 1952–1990.
- Data gathered following standard Meteorological Office procedures (Observer's Handbook, 4th ed., 1982).
- Stored in a database described in Cuthbertson (1993); a summary is available in MM.pdf.
- Site metadata includes grid references, altitudes, and responsible staff.

## Data provenance and collection methods
- Data collected according to established Meteorological Office methods.
- Provenance documented via a referenced database and supporting documentation (MM.pdf).
- Data are linked to a dataset description (DATID) and include recording dates for traceability.

## Site metadata
- Newton Rigg: Grid 349300 531000; Altitude 171 m; Staff: Newton Rigg Agricultural College.
- Widdybank Fell: Grid 381700 529700; Altitude 527 m; Staff: Ian Findlay.
- Moor House: Grid 375100 533400; Altitude 549 m; Staff: Andy Millar.
- Great Dun Fell: Grid 371600 532100; Altitude 847 m; Staff: Unknown.
- Recording locations identified in dataset via DATID with dataset descriptions corresponding to each site.
- Earliest and latest dates per site vary (e.g., Moor House: 01-May-1952 to 31-Dec-1979; Newton Rigg: 01-Jan-1959 to 31-Dec-1990; Widdybank Fell: 01-Jun-1974 to 31-Dec-1989; Great Dun Fell: 01-Jan-1973 to 29-Aug-1975).

## Data structure and variables
- Core identifiers: DATID (dataset-identified), REC_DTE (record date).
- Temperature variables: MAXTMP, MINTMP, MEANTMP, MINGRTMP; soil temperatures: E10TMP, E20TMP, E30TMP, E100TMP; other temperature measures: DRYTMP, WETTMP, DEWTMP.
- Humidity, precipitation, and related measures: HUMIDITY, VAPPRESS, SUNSHINE, WINDDIR, WINDVEL, HALFSNOW, SNOWDEPTH, NEWSNOW, CLOUD, VISIBILITY, VISCODE, WEATHDESC, THUNDER, GALE, FOG.
- Units and descriptions are specified for many variables; some units are listed as missing or ambiguous in the summary (e.g., HUMIDITY and some TEMP fields note potential unit inconsistencies).
- VISCODE provides a coded table for visibility categories (1–9 with increasing clarity).
- WEATHDESC, THUNDER, GALE, FOG indicate daily weather events or conditions.

## Data availability and continuity
- Primary data span across 1952–1990, with site-specific date ranges noted.
- The note mentions continuity of meteorological monitoring at Moor House via the UK Environmental Change Network (ECN) from 1991–2015 (Rennie et al. 2017) with a DOI reference.
- The dataset has documented metadata and references to the broader environmental data program, enabling reuse and cross-linking to related datasets.

## Practical considerations for data stewardship and reuse
- Standard procedures and metadata are documented, supporting discoverability and reuse.
- Data provenance through staff at each site and clear recording dates facilitate data quality assessment and lineage tracking.
- For updated or extended analyses, consider the ECN continuation data for Moor House and check related publications for indicators of compatibility and interoperability.
- Potential challenges include ensuring consistent metadata interpretation across sites (e.g., unit specifications) and aligning historical formats with modern data portals.

## Key takeaways for Data Stewards
- This dataset exemplifies rigorous governance: adherence to MO procedures, detailed site and variable metadata, and clear provenance.
- It provides a structured foundation for long-term climatic analyses and serves as a model for documenting historical environmental data, including future integration with ongoing ECN records.