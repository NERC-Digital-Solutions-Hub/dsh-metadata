# UK Environmental Change Network (http://www.ecn.ac.uk) Frogs (BF)

## Overview
- Phenology-based frog spawning data used as an environmental health indicator, complemented by laboratory analysis of pool water.
- Collected and managed under the UK Environmental Change Network (ECN) framework to support scrutiny of policy, evaluation of environmental health, and informing future decisions.
- Data span multiple ECN sites with site-specific monitoring and spelling out data provenance, quality, and governance requirements.

## Data Origin, Ownership, and Access
- Originator: ECN Data Centre; Data hosting: ECN data infrastructure (Oracle database with site tables).
- Owners: ECN programme sponsored by a consortium of UK government departments and agencies (e.g., Defra, Natural England, Environment Agency, Scottish/Northern Ireland equivalents, NERC, etc.).
- Usage expectations: Acknowledge ECN data usage and provide one reprint of any publication citing the data.
- Protocol reference: Phenology-based methodology for monitoring spawning in selected pools/ditches; accompanying quality information provided.
- Data sharing: Emphasis on metadata quality and openness; potential barriers noted (e.g., public sharing requirements, metadata gaps).

## Protocol and Measurements
- Primary indicator: Spawning health inferred from counts of frog egg masses; spawning in pools/ditches as a health proxy.
- Supporting analyses: Laboratory analyses of water samples from observed pools; accompanying metadata informs data quality.
- Quality information: Use of accompanying quality metadata to assess data suitability and limitations.

## Data Structure and Metadata
- Core data storage: 10 site-specific tables for core frog data (D1BF_xxx) and 10 site-specific tables for lab analyses (D2BF_xxx) in an Oracle database.
- Core data fields (examples): SITECODE (site code), LCODE (location code), SDATE (sampling date), FROMDATE (date last recorded), FIELDNAME (measurement name), VALUE (measurement value), plus various metadata fields.
- Lab data fields (examples): SDATE (sampling date), PHDATE/PHHOUR/PHMINS (pH measurements), FILTDATE/COMPDATE (processing dates), and a range of chemical and physical parameters (ALKY, CALCIUM, NO3N, TOTALN, etc.).
- Field naming and description: Field names correspond to environmental and water-quality parameters (e.g., ALKY, NO3N, PO4P, TEMP metrics, SPAWNDATE, PERCDEAD, etc.).
- Site metadata: Site codes and names (e.g., T01 Drayton; T02 Glensaugh; T03 Hillsborough; T04 Moor House - Upper Teesdale; T05 North Wyke; T06 Rothamsted; T08 Wytham; T09 Alice Holt; T10 Porton Down; T11 Snowdon), including coordinates and dataset date ranges (e.g., 1994–2012 for several sites; some ranges vary by site).

## Site Details
- T01: Drayton (52°11'37.95"N, 1°45'51.95"W); date range 01-JAN-1994 to 22-FEB-2012.
- T02: Glensaugh (56°54'33.36"N, 2°33'12.14"W); date range 01-JAN-1994 to 19-JUN-2012.
- T03: Hillsborough (54°27'12.24"N, 6°04'41.26"W); date range 01-JAN-1994 to 25-FEB-2011.
- T04: Moor House - Upper Teesdale (54°41'42.15"N, 2°23'16.26"W); date range 01-JAN-1994 to 10-OCT-2012.
- T05: North Wyke (50°46'54.96"N, 3°55'4.10"W); date range 05-JAN-1994 to 28-MAR-2012.
- T06: Rothamsted (51°48'12.33"N, 0°22'21.66"W); date range 17-FEB-1994 to 14-JUL-2010.
- T08: Wytham (51°46'52.86"N, 1°20'9.81"W); date range 01-JAN-1994 to 17-JUN-1994.
- T09: Alice Holt (51°9'16.46"N, 0°51'47.58"W); date range 28-FEB-1995 to 14-MAR-2001.
- T10: Porton Down (51°7'37.83"N, 1°38'23.46"W); date range 14-FEB-2001 to 07-APR-2010.
- T11: Y Wyddfa - Snowdon (53°4'28.38"N, 4°2'0.64"W); date range 31-DEC-1995 to 30-MAY-2012.

## Quality Codes and Data Quality
- ECN quality codes: Assigned by site managers to indicate data quality factors; codes drawn from a standard list with 999 reserved for unusual events (textual notes accompany such cases).
- Examples of standard QC codes include: 100 No information available; 101 No sample/reading taken; 102 Sample lost; 103 Partial loss; 104 Sample frozen; 105–189 various field/handling conditions; 200–241 adverse conditions affecting sampling, etc.; 501–513 laboratory-related and calculation-related caveats; 999 Unusual event (see quality text).
- Quality codes are designed to aid users in assessing data reliability and to provide context for any data limitations.

## Data Use, Governance, and Policy Relevance
- Data governance: Metadata documentation exists and point to core metadata tables; data management practices include data quality assurance, cleaning, transformation, analysis, and clear presentation in reports, charts, or dashboards.
- Outputs dissemination: Outputs are shared with stakeholders; underlying data should be shared appropriately; governance processes are implemented to maintain data standards and currency.
- Policy relevance: Framework supports evaluation of environmental change impacts and informs future policy decisions through standardized, quality-controlled environmental health indicators.

## Challenges and Barriers (relevant to Monitoring Framework Authors)
- Common monitoring framework challenges reflected:
  - Lack of data or data at insufficient quality for some indicators.
  - Limited or delayed access to data; data silos within or between organisations.
  - Requirements to publicly share datasets can hinder use of some data.
  - Metadata gaps hinder quick verification of data suitability.
  - Data often require transformation to be usable in analyses.
  - Communicating complex findings clearly to stakeholders.
  - Establishing and maintaining data governance to ensure datasets meet standards and remain up to date.