# Floral Unit Metadata

- Overview
  - Metadata accompanying the Floral_unit_data.csv dataset.
  - Floral unit data collected across two field margins in the same field.
  - Species-specific collection timeline to align with aerial imagery: Silene dioica (May 2019) and Centaurea nigra (July 2019).

- Dataset Structure and Key Columns
  - Weather: Recorded for each floral unit multiple times on the day prior to data collection; logged in the spreadsheet for the relevant unit.
  - Date: Date of floral unit data collection.
  - Time: Data collection times for each floral unit; noted multiple times prior to data collection for the unit.
  - Species: Silene dioica or Centaurea nigra.
  - Unit: The survey floral unit; one capitulum for C. nigra or one/multiple flowers within the same pixel for S. dioica.
  - Orientation: Position relative to ground for each S. dioica flower/bud or for each C. nigra capitulum.
  - TB_width_cm: Width of the floral unit in centimetres along the travel direction.
  - LR_width_cm: Width of the floral unit in centimetres left-to-right across the travel direction.
  - Individual_flower: Relevant only for Silene dioica; Yes if there is a single flower within the floral unit, No if multiple flowers/buds are present.

- Data Collection Context
  - May 2019 data for Silene dioica to correspond with May aerial imagery.
  - July 2019 data for Centaurea nigra to correspond with July aerial imagery.

- Data Quality and Governance Considerations for Data Stewards
  - Ensure metadata completeness and consistency (definitions of Unit, Orientation, and measurement units in cm).
  - Align time/weather notes with the corresponding floral unit entries for traceability.
  - Maintain clear documentation of the two-species approach and how Units map to imagery pixels.
  - Clarify any data availability or update procedures if sharing beyond the internal dataset (no explicit embargo details provided).

- Use and Interoperability
  - Metadata supports integration with aerial imagery datasets for temporal alignment and pixel-level analysis.
  - Facilitates discovery and reuse by researchers studying floral units, morphology, or habitat structure.