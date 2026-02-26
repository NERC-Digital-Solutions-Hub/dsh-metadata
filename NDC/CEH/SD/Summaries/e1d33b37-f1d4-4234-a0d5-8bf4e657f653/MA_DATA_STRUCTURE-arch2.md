# UK Environmental Change Network (ECN) meteorology data: 1992-2012

## Overview
- Long-term meteorology dataset from the UK Environmental Change Network (ECN), comprising hourly summaries derived from 5-second sampling by automatic weather stations (AWS).
- Spans 1992–2012 across multiple ECN sites, with some sites operating more than one AWS at the same location for cross-checking.
- Data are prepared for standardised analysis and presentation (e.g., charts, maps, reports); accompanying quality information is essential for correct use.

## Data Origin and Ownership
- Originator: ECN Data Centre (Centre for Ecology and Hydrology); data available via the ECN portal (data.ecn.ac.uk).
- Dataset Owners: ECN programme funded by a consortium of UK government departments and agencies (e.g., Defra, BEIS, Natural England, Scottish and Welsh administrations, and others).
- Usage acknowledgement: ECN requests acknowledgment of data use and one reprint of any publication that cites the data.

## Protocols and Access
- Protocol Reference: See the Protocol document (MA.pdf) in the ECN data holdings to assist data reuse.
- Data access and reuse: Data are stored and uploaded to appropriate portals; users should consult the accompanying quality information and the AWS-specific notes when using the data.

## Data Content, Structure, and Coverage
- Data content: Hourly summaries derived from 5-second AWS samplings; includes quality checks and, where applicable, cross-checks from concurrent AWS units.
- AWS details: Some sites operated multiple AWS units (identified by AWSNo); replacement AWS units are noted to aid correct data interpretation.
- Site coverage (T01–T12) with coordinates and AWS periods:
  - T01 Drayton, 52°11'37.95"N 1°45'51.95"W; AWS1: 1993-01-01 to 2008-12-31; AWS2: 2010-09-29 to 2012-12-31
  - T02 Glensaugh, 56°54'33.36"N 2°33'12.14"W; AWS1: 1994-07-07 to 2007-01-01; AWS2: 2004-07-08 to 2012-12-31
  - T03 Hillsborough, 54°27'12.24"N 6°04'41.26"W; AWS1: 1993-10-13 to 2009-12-16; AWS2: 2010-03-22 to 2012-12-31
  - T04 Moor House - Upper Teesdale, 54°41'42.15"N 2°23'16.26"W; AWS1: 1991-05-28 to 2009-12-31; AWS2: 2007-07-04 to 2012-12-31
  - T05 North Wyke, 50°46'54.96"N 3°55'04.10"W; AWS1: 1995-05-01 to 2009-03-24; AWS2: 2009-03-24 to 2012-12-31
  - T06 Rothamsted, 51°48'12.33"N 0°22'21.66"W; AWS1: 1993-03-29 to 2012-12-31
  - T07 Sourhope, 55°29'23.47"N 2°12'43.32"W; AWS1: 1993-11-01 to 2007-04-01; AWS2: 2004-07-07 to 2012-12-31
  - T08 Wytham, 51°46'52.86"N 1°20'09.81"W; AWS1: 1992-03-13 to 2007-12-31; AWS2: 2006-09-15 to 2012-12-31
  - T09 Alice Holt, 51°09'16.46"N 0°51'47.58"W; AWS1: 1994-01-09 to 2012-12-31
  - T10 Porton Down, 51°07'37.83"N 1°38'23.46"W; AWS1: 1994-11-09 to 1998-04-08; AWS2: 2007-09-18 to 2012-12-31
  - T11 Y Wyddfa - Snowdon, 53°04'28.38"N 4°02'00.64"W; AWS1: 1995-05-01 to 2012-12-31
  - T12 Cairngorms, 57°06'58.84"N 3°49'46.98"W; AWS1: 1999-06-28 to 2007-07-17; AWS2: 2007-09-12 to 2012-12-31
- Data table structure (representative fields):
  - Site, AWS, Sampling date/time (E), Sampling hour (R), Field name (NAME), Value (VALU)
  - Examples of fields (variables) and units: 
    - ALBGRD (Albedo Ground, average) 
    - ALBSKY (Albedo Sky, average)
    - DRYTMP (Dry bulb temperature, average) in °C
    - NETRAD (Net Radiation, average) in W/m^2
    - RAIN (Rainfall, total) in mm
    - RH (Relative humidity, average) in %
    - SOLAR (Solar Radiation, average) in W/m^2
    - STMP10 / STMP30 (Soil temperature at 10 cm / 30 cm) in °C
    - SURWET (Surface wetness) in minutes with wet surface
    - SWATER / SWATER_T / SWATER_V (Soil moisture measurements at different depths) in their respective units
    - WDIR (Wind direction) in degrees
    - WSPEED (Wind speed) in m/s
    - WETTMP (Wet bulb temperature) in °C
- Data quality and usage notes:
  - Use the accompanying quality information for proper interpretation.
  - Be aware of AWS replacements and concurrent operation at a site when aggregating data.
  - Standardised methods are applied to derive outputs suitable for policy monitoring and environmental health assessment.

## Usage Guidance for Analysts
- Leverage standardized outputs (reports, maps, charts) to compare environmental health and policy performance over time.
- Integrate ECN meteorology data with other relevant datasets to increase analytical value and enable broader insights.
- Ensure data access for stakeholders by following ECN data sharing practices and citing the data properly.

## Acknowledgments and Licensing
- Data use acknowledgement requested; publication citing the ECN data should be accompanied by a reprint if possible. 
- Protocol MA.pdf provides the reuse guidance; data stewardship includes storage and portal submission for reuse.