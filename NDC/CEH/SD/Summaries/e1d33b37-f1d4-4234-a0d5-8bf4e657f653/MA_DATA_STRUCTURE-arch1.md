# UK Environmental Change Network (ECN) meteorology data: 1992-2012

## Overview
- A meteorology dataset from the UK Environmental Change Network (ECN) covering 1992–2012.
- Originated by the ECN Data Centre and sponsored by a consortium of UK government departments and agencies.
- Data usage acknowledged by ECN; request for one reprint of any publication citing the data.

## Data content and scope
- Data comprise hourly summaries derived from 5-second samplings collected by Automatic Weather Stations (AWS).
- Many ECN sites operated more than one AWS at the same location (replacement AWSs may run concurrently for cross-checking); the AWS is identified by AWSNo.
- Users should consult accompanying quality information when using the data.
- Protocol reference for data reuse is MA.pdf, available in the ECN/EIDC Hub data holdings.

## Data structure and schema
- Data tables are organized with clear field definitions and codes, including:
  - Site (site codes and metadata)
  - AWS (individual AWS at a location; AWSNo)
  - SDAT (sampling date and time)
  - SHOU (sampling hour)
  - FIELD (field name and description)
  - VALU (value)
- Site Codes section provides
  - Site code (e.g., T01…T12)
  - Site name and coordinates
  - AWS1 and AWS2 date ranges per site (periods when each AWS operated)
- Fields (examples of variables and units)
  - ALBGRD: Albedo Ground (average), W m-2
  - ALBSKY: Albedo Sky (average), W m-2
  - DRYTMP: Dry bulb temperature (average), °C
  - DRTYMP_R: Dry bulb temperature within the RH sensor (average), °C
  - NETRAD: Net Radiation (average), W m-2
  - RAIN: Rainfall (total), mm
  - RH: Relative humidity (average), %
  - SOLAR: Solar Radiation (average), W m-2
  - STMP10: Soil temperature at 10 cm (average), °C
  - STMP30: Soil temperature at 30 cm (average), °C
  - SURWET: Surface wetness (minutes per hour the surface is wet), minutes
  - SWATER: Soil moisture (gypsum block, average), arbitrary units
  - SWATER_T: Soil moisture - theta probe at 20 cm (average), %
  - SWATER_V: Soil moisture - volumetric water content at 20 cm, m3/m3
  - WDIR: Wind direction (average), degrees
  - WSPEED: Wind speed (average), m s-1
  - WETTMP: Wet bulb temperature (average), °C
- Each field includes a name, description, units, and notes as part of the dataset metadata.

## Sites and coverage
- The ECN meteorology network includes multiple sites with precise coordinates and site-specific AWS histories, for example:
  - T01 Drayton
  - T02 Glensaugh
  - T03 Hillsborough
  - T04 Moor House - Upper Teesdale
  - T05 North Wyke
  - T06 Rothamsted
  - T07 Sourhope
  - T08 Wytham
  - T09 Alice Holt
  - T10 Porton Down
  - T11 Y Wyddfa - Snowdon
  - T12 Cairngorms
- For each site, AWS1 and AWS2 date ranges are provided, indicating periods of operation and enabling reconstruction of data availability over time.

## Data quality and usage notes
- Use the accompanying quality information to assess data suitability.
- When two AWSs operated concurrently at the same site, identify the correct series via the AWSNo field.
- Data are organized to support cross-site comparisons and longitudinal analyses, but users may need to address gaps or non-uniform coverage due to site- and period-specific AWS histories.

## Access, governance, and citations
- Data governance: ECN program funded by a consortium of UK government departments and agencies; data sharing encourages acknowledgement and citation.
- Acknowledgement: Users should acknowledge the ECN data and send one reprint of any publication that cites the dataset.
- Protocols and additional assistance: The MA.pdf protocol document is available in the EIDC Hub data holdings page; additional metadata and data access information are maintained by the ECN Data Centre (data.ecn.ac.uk). Contact: ecn@ceh.ac.uk.