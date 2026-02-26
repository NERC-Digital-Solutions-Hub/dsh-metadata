# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

## Overview
- Dataset from the UK Environmental Change Network (ECN) focusing on bird data collected using the Common Birds Census (CBC) methodology.
- National-scale, site-based data intended for understanding environmental change relationships, best used alongside broader monitoring data (e.g., BTO).
- CBC protocol used until 1999, after which Breeding Bird Survey (BBS) became standard; some sites continued CBC for comparison. Date ranges vary by site.

## Data scope and coverage
- Sites (with codes): Drayton (T01), Hillsborough (T03), North Wyke (T05), Rothamsted (T06), Wytham (T08), Alice Holt (T09), Porton Down (T10).
- Site details include location coordinates and BTO site class (e.g., Farmland, Woodland, Special).
- Site-specific time ranges:
  - Alice Holt: 1994–2007
  - Drayton: 1993–1999
  - Hillsborough: 1993–2001
  - North Wyke: 1993–2002
  - Porton Down: 1994–1998
  - Rothamsted: 1991–1997
  - Wytham: 1971–2003
- Data files describe sampling years and species-specific observations per site.

## Data collection and protocol
- CBC method: multiple visits to all parts of a defined plot during the breeding season; birds recorded by sight or sound on large-scale maps.
- Outcomes include estimates of territories (CLUST) and, for some species, nest counts (NEST) or combined measures.
- Protocol emphasizes comparability across sites; accompanying quality information should be consulted when using the data.
- Historical context: CBC was standard at lowland ECN sites until 1999; BBS implemented thereafter.

## Data structure and fields
- Data download fields include:
  - SITECODE: site code
  - SYEAR: sampling year
  - BI_SPEC: bird species code
  - CLUST: number of territories (clusters)
  - NEST: number of nests
- Supporting file ECN_cbc_qtext.csv provides issue descriptions by SITECODE, SYEAR, BI_SPEC.

## Site information
- Explanatory information lists the seven ECN sites with names, coordinates, and BTO classifications.
- Additional site details available via CEH catalog linked in the documentation.

## Species information
- Bird species are coded with two-letter codes and full common names (e.g., AC = Arctic Skua, BT = Blue Tit, etc.).
- A comprehensive mapping between BI_SPEC codes and species names is provided in the accompanying documentation.

## Data quality and supporting documentation
- Quality notes are provided in ECN_cbc_qtext.csv to document issues affecting data.
- Users are advised to consult accompanying quality information to understand limitations and data context.

## Usage and attribution
- ECN requests acknowledgement of data use and one reprint of any publication citing ECN data.
- Data are best used in conjunction with broader monitoring data (e.g., BTO) to better interpret relationships with environmental change.

## Access and further information
- Supporting documentation and data access are described; further information is available via the CEH data catalogue (link provided in the document).