# Floral Unit Metadata

## Purpose
- Metadata to accompany the Floral_unit_data.csv dataset.
- Data were collected across two field margins within the same field.
- Species-specific data collection timing: Silene dioica in May 2019 to align with May aerial imagery; Centaurea nigra in July 2019 to align with July aerial imagery.

## Data Collected and Context
- Weather: Weather for each floral unit was recorded multiple times throughout the day prior to data gathering and noted for the relevant floral unit.
- Date: Date on which the floral unit data were gathered.
- Time: Times noted multiple times during the day prior to data gathering for the relevant floral unit.
- Field alignment: Data collected to correspond with aerial imagery captured in May (S. dioica) or July (C. nigra).

## Columns / Fields
- Species: Silene dioica or Centaurea nigra.
- Unit: The survey floral unit. For Centaurea nigra, one capitulum; for Silene dioica, one or multiple flowers within the same pixel space (e.g., on one central stalk).
- Orientation: The position relative to the ground of each flower/bud (S. dioica) or each capitulum (C. nigra).
- TB_width_cm: The width of the floral unit in the direction of travel (centimetres).
- LR_width_cm: The width of the floral unit from left to right when facing the unit in the direction of travel (centimetres).
- Individual_flower: Only relevant for Silene dioica. Yes indicates a single flower within the floral unit; No indicates multiple flowers/buds.

## Measurement Details
- Measurements are recorded in centimetres for width-related fields.
- Data are collected in a sequential order, with weather and time snapshots preceding the data gathering for each unit.

## Use for Analysis and Data Products
- Enables integration with aerial imagery for time-mynced analyses (May and July imagery alignment).
- Supports quality assurance, provenance, and context when creating dashboards, pivot analyses, or self-serve data tools.
- Facilitates data cleaning and combination with other datasets by providing explicit units, orientation, and unit definitions.
- Aids in understanding spatial layout and sampling within pixel spaces for comparative studies between the two species.