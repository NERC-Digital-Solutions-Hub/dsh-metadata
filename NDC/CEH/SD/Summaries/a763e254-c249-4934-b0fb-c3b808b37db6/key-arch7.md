# Type and Condition Codes

## Overview
- Defines two code tables for feature attributes used in GIS datasets: one for road/path characteristics and another for settlement/land-use characteristics.
- Each feature type uses a pair of attributes: Type and Condition, with integer codes to facilitate validation and mapping.

## Road/Path features
- Type codes:
  - 1 - Major (paved)
  - 2 - Major (unpaved)
  - 3 - Minor (paved)
  - 4 - Minor (unpaved)
  - 5 - Track (unpaved)
- Condition codes:
  - 1 - Intact
  - 2 - Obstructed/damaged

## Settlement/Land-Use features
- Type codes:
  - 1 - Residential (permanent)
  - 2 - Residential (informal/temporary) [note: original shows a typo "Resdiential"]
  - 3 - Industrial i.e. hydropower
  - 4 - Municipal
- Condition codes:
  - 1 - Intact
  - 2 - Obstructed/damaged

## Data quality and practical notes
- Typographical inconsistency: "Resdiential" should be corrected to "Residential" for consistency.
- Codes are suitable for defining enumerated domains in GIS (e.g., validating attribute values, enabling consistent symbology and querying).
- When integrating datasets from multiple sources, align coding schemes and document any deviations to maintain data standards.

## GIS workflow considerations
- Implement domains/domains tables in GIS software to enforce allowed values.
- Use the codes to drive map styling (e.g., road type and condition) and to filter datasets by condition or category.
- Plan for data cleaning and transformation steps to harmonize inputs from varied sources.