# Common Birds Census (CBC) Data from the UK Environmental Change Network (ECN)

## Overview
- Dataset originates from the ECN Data Centre (Centre for Ecology and Hydrology) and is part of the UK Environmental Change Network (ECN) program.
- Dataset owners are a consortium including DEFRA, NE, NERC, and other UK government bodies; they fund site monitoring or network coordination.
- Users are asked to acknowledge data use and to send one reprint of any publication that cites ECN data.

## Data provenance and governance
- ECN provides standard operating procedures to ensure data comparability across sites; bc.pdf explains data collection methods.
- Usage notes reference the Common Birds Census (CBC) methodology and how data are collected and interpreted (territory counts CLUST; nest counts NEST).
- The CBC is designed as a national-scale survey; site-based data have limited detail on precise links between populations and environmental change; users are advised to combine ECN CBC data with broader datasets (e.g., BTO data) to mitigate limitations.
- Since 1999, CBC at lowland ECN sites was largely replaced by the Breeding Bird Survey (BBS); some sites continued CBC for comparison. Historical data (pre-ECN) exist for certain sites (e.g., Wytham). Date ranges vary by site.

## Data content and structure
- Data download fields:
  - SITECODE: Unique ECN site code
  - SYEAR: Sampling year
  - BI_SPEC: Bird species code
  - CLUST: Number of territories (clusters)
  - NEST: Number of nests
- Supporting documentation: ECN_cbc_qtext.csv, containing site- and issue-related descriptions for data quality notes.
- Explanatory information includes details on site codes, bird species codes, and site metadata.

## Site codes and locations
- T01 Drayton (52°11'37.95"N, 1°45'51.95"W) – Farmland
- T03 Hillsborough (54°27'12.24"N, 6°4'41.26"W) – Woodland
- T05 North Wyke (50°46'54.96"N, 3°55'4.10"W) – Woodland
- T06 Rothamsted (51°48'12.33"N, 0°22'21.66"W) – Farmland
- T08 Wytham (51°46'52.86"N, 1°20'9.81"W) – Woodland
- T09 Alice Holt (51°9'16.46"N, 0°51'47.58"W) – Woodland
- T10 Porton Down (51°7'37.83"N, 1°38'23.46"W) – Special
- Additional historical data and site information available via the CEH catalogue (link provided).

## Bird species codes
- A comprehensive mapping of two-letter species codes to full scientific/common names is provided, covering a wide range of birds from Arctic Skua (AE) to Yellowhammer (YW) and beyond.
- The dataset uses BI_SPEC as the species code, with accompanying descriptions for each code in the provided mapping.

## Data coverage and time range
- Site-specific date ranges vary by location:
  - Alice Holt: 1994–2007
  - Drayton: 1993–1999
  - Hillsborough: 1993–2001
  - North Wyke: 1993–2002
  - Porton Down: 1994–1998
  - Rothamsted: 1991–1997
  - Wytham: 1971–2003
- Overall, the ECN CBC data span multiple decades with site-specific coverage; data include territory (CLUST) and nest (NEST) counts for bird species.

## Data access, quality, and usage guidance
- Use the accompanying quality information when using the data; be mindful of data quality notes and site-specific issues.
- Recognize data limitations due to site-specific sampling, changing protocols (CBC to BBS), and the national-scale nature of the CBC.
- For robust analyses of population-environment relationships, supplement ECN CBC data with data from broader monitoring programs (e.g., BTO).

## Supporting information and references
- Supporting documentation file: ECN_cbc_qtext.csv (descriptions of issues affecting data)
- Explanatory information includes detailed site codes and bird species code mappings.
- Additional site information and broader dataset context available at the CEH catalogue (external link provided).
- A published reference is Rennie et al. 2017: UK Environmental Change Network (ECN) bird data: 1995–2015 (doi provided) for context and integration with other datasets.