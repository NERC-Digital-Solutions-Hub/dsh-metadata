# Climatic data (Meteorological Office recordings) from four sites along an altitudinal gradient in Cumbria. 1952 - 1990

## Overview
- Climatic dataset collected at four sites along an altitude gradient in Cumbria, following standard Meteorological Office procedures.
- Data stored in a database described by Cuthbertson (1993); supporting documentation MM.pdf available.
- Intended to support environmental research and data-based insights; data provenance and structure documented for reuse.

## Site details
- Newton Rigg: Grid 349300 531000; Altitude 171 m; Data staff: Newton Rigg Agricultural College.
- Widdybank Fell: Grid 381700 529700; Altitude 527 m; Data staff: Ian Findlay.
- Moor House: Grid 375100 533400; Altitude 549 m; Data staff: Andy Millar.
- Great Dun Fell: Grid 371600 532100; Altitude 847 m; Data staff: Unknown.

## Recording locations and timeframes
- Data identified by DATID in the dataset.
- Moor House: earliest 01-MAY-1952 to 31-DEC-1979.
- Newton Rigg: earliest 01-JAN-1959 to 31-DEC-1990.
- Widdybank Fell: earliest 01-JUN-1974 to 31-DEC-1989.
- Great Dun Fell: earliest 01-JAN-1973 to 29-AUG-1975.

## Data structure and variables
- Core identifiers: DATID (dataset linkage), REC_DTE (date).
- Temperature: MAXTMP, MINTMP, MEANTMP, MINGRTMP, E10TMP, E20TMP, E30TMP, E100TMP, DRYTMP, WETTMP, DEWTMP.
- Other environment measures: HUMIDITY, VAPPRESS, SUNSHINE, WINDDIR, WINDVEL, HALFSNOW, SNOWDEPTH, NEWSNOW, CLOUD, VISIBILITY, VISCODE, WEATHDESC, THUNDER, GALE, FOG.
- Units and codes: most variables reported with specific units (e.g., °C for temperatures, hours for sunshine, knots for wind, %, etc.); VISCODE includes coded visibility descriptions; certain daily weather flags (THUNDER, GALE, FOG) indicate occurrences.
- Special notes: CLOUD uses an eight-point scale; VISCODE requires a code table for interpretation.

## Data provenance and references
- Data described as “Climatic data recorded for the Met Office” from multiple sites (Moor House enclosure noted).
- Data contribution and methodology aligned with Met Office observer handbook standards (4th ed., 1982).
- Additional context: UK Environmental Change Network continued Moor House monitoring post-1990 (Rennie et al., 2017); dataset references include Cuthbertson (1993) for database description and MM.pdf for supporting documentation.

## Access, usage, and caveats
- Dataset is suitable for cross-site climate analysis and altitudinal gradient studies, with long timeframes per site.
- Potential challenges include patchy data, variation in data formats, and multi-site data access requiring integration from multiple sources.
- Encouraged to consult the cited database description (Cuthbertson 1993) and supporting MM.pdf for data dictionary, unit conventions, and site-specific details.
- MO dataset context and continuity: Moor House data are part of a longer-term series, with ECN continuing monitoring beyond 1990.