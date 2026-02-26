# Climatic data (Meteorological Office recordings) from four sites along an altitudinal gradient in Cumbria. 1952 - 1990

## Overview
- Climatic data from four sites along an altitudinal gradient in Cumbria, collected according to standard Meteorological Office procedures (1952–1990).
- Data stored in a database described by Cuthbertson (1993); summary available in MM.pdf.
- Dataset covers a range of meteorological and environmental variables suitable for analyses of temperature, humidity, precipitation, wind, soil temperature at depth, snow, cloud, and visibility.

## Sites and recording locations
- Newton Rigg: grid 349300 531000; altitude 171 m; data collection by Newton Rigg Agricultural College staff; earliest 1959-01-01 to 1990-12-31.
- Widdybank Fell: grid 381700 529700; altitude 527 m; staff Ian Findlay; earliest 1974-01-01 to 1989-12-31.
- Moor House: grid 375100 533400; altitude 549 m; staff Andy Millar; earliest 1952-05-01 to 1979-12-31.
- Great Dun Fell: grid 371600 532100; altitude 847 m; staff unknown; earliest 1973-01-01 to 1975-08-29.
- Recording locations are indicated in the dataset via DATID.

## Recording locations and data description
- Each DATID entry describes the data: e.g., “Climatic data recorded for the Met Office. Moor House Meteorological enclosure.”
- Site date ranges vary by location (as listed above).

## Variables and data structure
- Core identifiers: DATID, REC_DTE (date).
- Temperature and related measurements: MAXTMP, MINTMP, MEANTMP, MINGRTMP; soil temperatures E10TMP, E20TMP, E30TMP, E100TMP; DRYTMP, WETTMP, DEWTMP.
- Humidity, precipitation, and atmospheric variables: HUMIDITY, VAPPRESS, SUNSHINE (hours), WINDDIR, WINDVEL, CLOUD, VISIBILITY, VISCODE, WEATHDESC.
- Snow and related conditions: HALFSNOW, SNOWDEPTH, NEWSNOW.
- Other indicators: THUNDER, GALE, FOG (flags).
- Visibility codes provide qualitative descriptions (e.g., Thick fog, Moderate fog, Very good, Excellent).

## Data quality and integration considerations
- Gaps exist in both temporal and site coverage (different earliest/latest dates per site).
- Data originate from standard Met Office procedures, enabling potential harmonization, but multi-site integration requires careful alignment of variables and timing.
- Some metadata gaps (e.g., staff for Great Dun Fell) and relatively short sidereal spans for certain sites (e.g., Great Dun Fell 1973–1975).
- The UK Environmental Change Network has continued monitoring at Moor House from 1991–2015, providing a longer continuity beyond this dataset.

## References and data access
- Cuthbertson, M. (1993). A database for environmental research programmes. Journal of Environmental Management, 37(4), 291-300.
- Summary documentation: MM.pdf.
- ECN continuation: Rennie et al. (2017). UK Environmental Change Network meteorology data: 1991–2015. NERC Environmental Information Data Centre. https://doi.org/10.5285/fc9bcd1c-e3fc-4c5a-b5692fe62d40f2f5