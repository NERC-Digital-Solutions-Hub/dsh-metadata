# Floral Unit Metadata

## Overview
- Metadata accompanying Floral_unit_data.csv, capturing floral units from two field margins within the same field.
- Species-specific data collection aligned with aerial imagery: Silene dioica collected in May 2019; Centaurea nigra collected in July 2019.

## Data collection context
- Two field margins within the same field were surveyed.
- Data collection timing matched imagery: May for S. dioica and July for C. nigra.

## Spreadsheet columns and data captured
- Weather: Weather notes recorded multiple times across the day before data collection for each floral unit; included in the spreadsheet.
- Date: Date on which floral unit data were gathered.
- Time: Time(s) data were gathered for each floral unit, logged in order; multiple time entries may precede data collection for a unit.
- Species: Silene dioica or Centaurea nigra.
- Unit: The survey floral unit; for C. nigra, one capitulum; for S. dioica, one floral unit may comprise one or multiple flowers within the same pixel space.
- Orientation: Ground relative position of each flower/bud (S. dioica) or each capitulum (C. nigra).
- TB_width_cm: Width of the floral unit measured in the direction of travel along the field margin (in cm).
- LR_width_cm: Width of the floral unit measured from left to right when facing the unit, in the direction of travel (in cm).
- Individual_flower: Only relevant for S. dioica. 'Yes' if the floral unit contains a single flower; 'No' if multiple flowers/buds are present.

## Measurement details
- Widths (TB_width_cm and LR_width_cm) are measured in specified travel and orientation directions along the margin.

## Species-specific unit definitions
- Silene dioica: a floral unit may consist of a single flower or multiple flowers within the same pixel area; Individual_flower clarifies if only one flower is present.
- Centaurea nigra: a floral unit is typically one capitulum.

## Data quality and workflow notes
- Data collected in consecutive order with contemporaneous weather and time records.
- Weather and time annotations occur repeatedly to contextualize each floral unit observation.
- Clear linkage to imagery collection periods enhances potential for integrated analyses.

## Potential uses and accessibility
- Metadata enables reproducible analyses of floral unit morphology and spatial patterns.
- Dataset designed for integration with aerial imagery, facilitating cross-referencing by date, plant species, and measured dimensions.