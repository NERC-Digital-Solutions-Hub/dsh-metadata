# Butterfly Protocol

- The ECN Butterfly Monitoring Protocol documents how butterfly data are collected and organized for environmental monitoring and policy evaluation.
- It supports standardized, comparable outputs to assess environmental health over time.

## Overview and Purpose

- Data originate from the UK Environmental Change Network (ECN) Data Centre, with data providers including a consortium of UK government departments and agencies.
- Aims to demonstrate environmental condition in a consistent format and enable scrutiny of environmental health and policy performance over time.
- Acknowledgement of data use is requested, including sending one reprint of any publication citing the data.

## Protocol Details

- Butterfly monitoring follows the national Butterfly Monitoring Scheme managed by the Biological Records Centre (within the CEH).
- Transects are divided into up to 15 sections; butterflies seen flying within or passing through a 5m x 5m x 5m imaginary box are counted.
- Transects are walked weekly from 1 April to 29 September, at an even pace.
- Weather and conditions: air temperature between 13-17°C and at least 60% sunshine.
- Quality information should accompany data usage.

## Data Structure

- Core data fields:
  - SITECODE: Unique ECN site code
  - LCODE: Location ID
  - SDATE: Date of data recording
  - SECTION: Transect section ID
  - FIELDNAME: Species code
  - VALUE: Measured value (count)

## Site Codes (ECN Sites)

- T01 Drayton — Location: 52°11'37.95" N, 1°45'51.95"W; Date range: 14-Apr-1993 to 19-Dec-2012
- T02 Glensaugh — Location: 56°54'33.36" N, 2°33'12.14"W; Date range: 14-Oct-1993 to 26-Dec-2012
- T03 Hillsborough — Location: 54°27'12.24" N, 6°4'41.26"W; Date range: 02-Feb-1994 to 27-Dec-2012
- T04 Moor House - Upper Teesdale — Location: 54°41'42.15" N, 2°23'16.26"W; Date range: 06-Oct-1992 to 24-Dec-2012
- T05 North Wyke — Location: 50°46'54.96" N, 3°55'4.10"W; Date range: 29-Sep-1993 to 26-Dec-2012
- T06 Rothamsted — Location: 51°48'12.33" N, 0°22'21.66"W; Date range: 02-Feb-1994 to 12-Dec-2012
- T07 Sourhope — Location: 55°29'23.47" N, 2°12'43.32"W; Date range: 08-Dec-1993 to 26-Dec-2012
- T08 Wytham — Location: 51°46'52.86" N, 1°20'9.81"W; Date range: 09-Jun-1993 to 12-Dec-2012
- T09 Alice Holt — Location: 51°9'16.46" N, 0°51'47.58"W; Date range: 27-Apr-1994 to 12-Dec-2012
- T10 Porton Down — Location: 51°7'37.83" N, 1°38'23.46"W; Date range: 17-Jan-1996 to 26-Jan-2000
- T11 Y Wyddfa - Snowdon — Location: 53°4'28.38" N, 4°2'0.64"W; Date range: 02-Jul-1997 to 27-Dec-2012
- T12 Cairngorms — Location: 57°6'58.84" N, 3°49'46.98"W; Date range: 06-Oct-1999 to 26-Dec-2012

## Species List

- A coded list maps numeric codes to Latin and common butterfly names (e.g., 2 = Aglais urticae, Small tortoiseshell; 4 = Anthocharis cardamines, Orange tip; 98 = Pieris brassicae, Large white; 120 = Thymelicus sylvestris, Small skipper; XX = No butterflies present; etc.).
- The dataset includes a broad spectrum of UK butterfly species; full mapping is provided with the data (ECN_IB files).

## Additional Information and Quality

- Additional information is provided in ECN_IB2.csv (sampling details: SITECODE, LCODE, SDATE, SHOUR, SMINS, RECORDER, RECCODE, TEMP, SUNPERC, WSPEEDB, WEEK).
- Quality information is provided in ECN_IB_qtext.csv (location, variable, date ranges, data type, continuing issues, and detailed descriptions of quality concerns).
- The quality framework includes codes for date ranges and flags indicating whether issues are ongoing.

## Data Use and Outputs

- Data are intended to be transformed and cleaned to produce outputs such as reports, maps, and charts.
- Datasets are stored and uploaded to appropriate portals to support dissemination and reuse.
- The protocol emphasizes ensuring data quality, standardization, and accessibility for others to use underlying data.

## Relevance for Analysts Monitoring the Environment

- Provides a standardized, time-series dataset of butterfly populations across multiple UK sites, enabling environmental health monitoring and policy assessment.
- Facilitates cross-site comparisons and trend analyses through consistent transect methodology and data structure.
- Supports linkage with other environmental data to enhance dataset value and improve accessibility of underlying data.
- Includes clear provenance, quality metadata, and usage acknowledgments to support reproducibility and stakeholder trust.