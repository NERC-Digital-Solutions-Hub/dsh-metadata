# UK Environmental Change Network (http://www.ecn.ac.uk) Frogs (BF)

## Overview and aim
- Phenology-based protocol for monitoring Common Frog spawning as an indicator of population health.
- Laboratory analyses of water from observed pools/ditches accompany field observations.
- Data are intended to support analysis of environmental change effects on frog populations and water quality; accompany quality information is essential when using the data.

## Data origin, owners, and use conditions
- Originator: ECN Data Centre (Centre for Ecology and Hydrology).
- Dataset owners: UK Environmental Change Network programme, sponsored by a consortium of UK government departments and agencies.
- Usage acknowledgement: Users are asked to acknowledge ECN data and to send one reprint of any publication that cites the dataset.

## Protocol and data provenance
- Methodology: Spawning is monitored phenologically by counting egg masses as a health indicator for frog populations; accompanying laboratory water analyses are conducted.
- Quality information: Use the accompanying quality information when using the data; quality codes accompany data entries.

## Data structure and access
- Storage: Oracle database with site-specific tables.
- Field data: 10 tables named D1BF_xxx (one per site) containing field observations.
- Laboratory data: 10 tables named D2BF_xxx (one per site) containing lab analysis results.
- Common structure elements:
  - SITECODE (site code), LCODE (location code), SDATE (sampling date), VALUE (numeric measurement), FIELDNAME (description of the measured field), and other metadata fields.
  - For field data (D1BF_xxx): includes sampling date, field name, value, and related descriptors.
  - For lab data (D2BF_xxx): includes sampling date, pH-related fields (PHDATE, PHHOUR, PHMINS), filter/complete dates (FILTDATE, COMPDATE), and corresponding values.
- Metadata reference: Core metadata tables exist; see ECN metadata documentation for full structure.

## Sites covered (codes, names, and date ranges)
- T01 — Drayton: 01-JAN-1994 to 22-FEB-2012
- T02 — Glensaugh: 01-JAN-1994 to 19-JUN-2012
- T03 — Hillsborough: 01-JAN-1994 to 25-FEB-2011
- T04 — Moor House - Upper Teesdale: 01-JAN-1994 to 10-OCT-2012
- T05 — North Wyke: 05-JAN-1994 to 28-MAR-2012
- T06 — Rothamsted: 17-FEB-1994 to 14-JUL-2010
- T08 — Wytham: 01-JAN-1994 to 17-JUN-1994
- T09 — Alice Holt: 28-FEB-1995 to 14-MAR-2001
- T10 — Porton Down: 14-FEB-2001 to 07-APR-2010
- T11 — Y Wyddfa - Snowdon: 31-DEC-1995 to 30-MAY-2012
- Site details include site name, precise location coordinates, and site-specific data range.

## Key data fields and types (highlights)
- Common field data fields: SITE CODE, LOCATION CODE, SAMPLING DATE, FIELD NAME, VALUE.
- Selected laboratory-related fields (D2BF_xxx): SAMPLING DATE, pH date/time fields (PHDATE, PHHOUR, PHMINS), FILTRATION and ANALYSIS completion fields (FILTDATE, COMPDATE), and associated measurements.
- Fieldnames cover a wide range of chemical, physical, and biological indicators (examples include alkalinity, various ions/metals, nutrients, pH measurements, temperature, spawn-related dates, counts of spawn masses, and related quality codes).

## Quality codes and data quality guidance
- Quality codes are assigned by ECN site managers from a standardized list; a code 999 indicates an unusual event (with accompanying text available in quality metadata).
- Example quality codes span categories such as sample availability issues, laboratory issues, environmental disturbances, data edits, and measurement uncertainties (ranging from 100 to 513, plus 999 for unusual events).
- It is essential to consult the accompanying quality information to interpret any data points properly.

## How this data can be used
- Cross-site comparisons of frog spawning phenology and associated environmental measurements.
- Time-series analyses examining environmental change effects on frog populations across multiple ECN sites.
- Data integration for dashboards or self-serve analyses, with attention to site-specific date ranges and quality codes.
- Reuse in policy-supporting analyses or public communication about environmental change indicators.

## References and protocol details
- Protocol Reference: http://www.ecn.ac.uk/measurements/terrestrial/b/bf
- Metadata documentation provides the full structure of core metadata tables and additional dataset-specific details.

## Notes for users
- Ensure you apply the accompanying quality codes and notes when interpreting results.
- Acknowledge ECN data usage and consider sharing reprints of publications that cite the dataset.
- Be mindful of patchy data and site-specific date ranges; cross-check site codes and data availability before aggregating across sites.