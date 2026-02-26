# Atmospheric Chemistry: Nitrogen Dioxide (AN)

## Overview
- A monitoring dataset from the UK Environmental Change Network (ECN) measuring NO2 using passive diffusion tubes.
- Dataset originator: ECN Data Centre; dataset owners include a consortium of UK government departments and agencies funding site monitoring and network coordination.
- Sponsors include: Agri-Food and Biosciences Institute, BBSRC, Natural Resources Wales, DSTL, Defra, Environment Agency, Forestry Commission, Welsh Government, Natural England, NERC, SEPA, Scottish Government, Scottish Environment Protection Agency, and others.
- ECN requests acknowledgement of data use and asks for one reprint of any publication citing the data.
- Protocol reference provided; quality information should accompany data usage.

## Data collection protocol and quality
- Passive diffusion tubes measure NO2 concentration; tubes left out for two weeks.
- Quality assurance includes transport of blank tubes to sites, unexposed on arrival, and laboratory analysis alongside exposed tubes.
- Data usage should reference accompanying quality information.
- A quality-flagging system (Q1–Q8) records multiple quality codes per measurement; unusual events can be described with code 999 and accompanying text.

## Data structure and metadata
- Core data structure:
  - D1AN_xxx tables (one per site) store measurement data:
    - Fields: SITECODE, SDATE (sampling date), TUBEID (sample type: E for Experimental, B for Blank), FIELDNAME (data type), VALUE (numeric value).
  - D2AN_xxx tables contain sample-collection information for the same sites:
    - Deployment dates and times (DEPDATE, DEPHOUR) and sampling date/time components (SDATE, SHOUR, SMINS).
  - Core metadata tables (referenced by each dataset field) provide descriptions and units.
- Fieldnames and data:
  - WEIGHTNO2: weight of NO2 on mesh (µg)
  - NO2: NO2 concentration (µg/m3)
  - NO2PPB: NO2 concentration (ppb)
  - TDIFF: exposure time (minutes)
  - Q1–Q8: quality codes (integers) indicating data quality or issues
- Quality metadata:
  - Codes are drawn from a standard ECN list; a range covers common data issues (e.g., sample loss, equipment problems, environmental interferences) and extended notes for codes like 999 (unusual event).
  - A separate quality text may accompany codes to describe non-standard issues.

## Site network and coverage
- 12 ECN sites with names and coordinates:
  - T01 Drayton (52°11'37.95"N 1°45'51.95"W), date range 20-Jan-1993 to 26-Dec-2012
  - T02 Glensaugh (56°54'33.36"N 2°33'12.14"W), 12-May-1993 to 12-Dec-2012
  - T03 Hillsborough (54°27'12.24"N 6°4'41.26"W), 02-Feb-1994 to 19-Dec-2012
  - T04 Moor House - Upper Teesdale (54°41'42.15"N 2°23'16.26"W), 03-Feb-1993 to 24-Dec-2012
  - T05 North Wyke (50°46'54.96"N 3°55'4.10"W), 21-Jul-1993 to 26-Dec-2012
  - T06 Rothamsted (51°48'12.33"N 0°22'21.66"W), 03-Feb-1993 to 12-Dec-2012
  - T07 Sourhope (55°29'23.47"N 2°12'43.32"W), 09-Jun-1993 to 26-Dec-2012
  - T08 Wytham (51°46'52.86"N 1°20'9.81"W), 03-Feb-1993 to 19-Dec-2012
  - T09 Alice Holt (51° 9'16.46"N 0°51'47.58"W), 11-May-1994 to 27-Dec-2012
  - T10 Porton Down (51° 7'37.83"N 1°38'23.46"W), 06-Jul-1994 to 12-Dec-2012
  - T11 Y Wyddfa - Snowdon (53° 4'28.38"N 4° 2'0.64"W), 26-Mar-1997 to 27-Dec-2012
  - T12 Cairngorms (57° 6'58.84"N 3°49'46.98"W), 10-Nov-1999 to 12-Dec-2012

## Data availability and governance
- Data are stored in a centralized Oracle database, with site-specific tables to support dataset organization.
- Data owners are a consortium of public sector organisations; governance, data sharing, and metadata standards are emphasized.
- Users are urged to ensure proper attribution and to follow the accompanying quality metadata when using the data.

## Relevance to monitoring framework design
- Demonstrates a multi-site environmental health monitoring program with:
  - Standardized measurement protocol (diffusion tubes) and QA procedures (blanks, quality information).
  - Structured metadata and data provenance across multiple sites.
  - A robust quality-code system to capture data reliability and field/lab issues.
  - Explicit data governance expectations (acknowledgement, publication reprints).
  - Challenges highlighted by the data design, including data integration across sites, metadata availability, and translating complex QA flags into clear interpretation for policy and decision-making.

## Key considerations for authors of monitoring frameworks (lessons from this dataset)
- Ensure explicit, extensible QA protocols and accompanying metadata to enable transparency and reproducibility.
- Design data schemas that separate measurement data from collection and contextual metadata; provide clear field definitions and units.
- Implement a comprehensive, standardized quality-coding system with documentation to facilitate data vetting and interpretation.
- Plan for data governance: sharing norms, attribution requirements, and mechanisms to communicate data limitations to users.
- Anticipate data access barriers (e.g., cross-site data integration, legacy formats) and provide strategies to mitigate silos and transform data for policy use.