# Floral Unit Metadata

## Overview
- Metadata that accompanies the Floral_unit_data.csv file.
- Data were collected across two field margins within the same field.
- Species and timing details:
  - Silene dioica data gathered in May 2019 to correspond with May aerial imagery.
  - Centaurea nigra data gathered in July 2019 to correspond with July aerial imagery.

## Data collection and structure
- Weather: Recorded for each floral unit multiple times throughout the day prior to data gathering; entries noted in the spreadsheet for the relevant floral unit.
- Date: Date on which floral unit data were collected.
- Time: Time(s) recorded for each floral unit, noted multiple times during the day prior to collection.
- Species: Silene dioica or Centaurea nigra.
- Unit: The survey floral unit; for Centaurea nigra, one capitulum; for Silene dioica, one or multiple flowers within the same pixel space (e.g., flowers on one central main stalk).
- Orientation: Position relative to the ground of each flower/bud (S. dioica) or capitulum (C. nigra).
- TB_width_cm: Width of each floral unit in centimetres along the direction of travel of the margin.
- LR_width_cm: Width of each floral unit in centimetres left-to-right when facing the unit in the direction of travel.
- Individual_flower: Only relevant for Silene dioica. 'Yes' indicates a single flower within the floral unit; 'No' indicates multiple flowers/buds within the unit.

## Data semantics and alignment with imagery
- The measurements are aligned with aerial imagery timing:
  - May imagery for Silene dioica data.
  - July imagery for Centaurea nigra data.

## Data governance implications for Data Leaders
- Clear, field-specific metadata supports data discoverability, provenance, and correct interpretation across datasets.
- Definitions differentiate how units are counted and measured by species, aiding consistency and reuse.
- Documentation links data collection practices to the corresponding remote-sensing data (aerial imagery), facilitating integrated analyses and cross-referencing within data ecosystems.