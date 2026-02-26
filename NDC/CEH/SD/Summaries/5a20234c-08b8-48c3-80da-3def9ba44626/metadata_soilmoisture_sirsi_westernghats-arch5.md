# Soil moisture data, Sirsi, Western Ghats

## Overview
- Dataset of soil moisture profiles near trees on a farm near Sirsi, Karnataka, Western Ghats, India.
- Collection period: January 2020 – January 2022.
- Depths measured: 10 cm, 25 cm, 50 cm, 110 cm.
- Sensor type: Campbell CS616 Water Content Reflectometers.
- Location context: gentle slope, ~500 m from local valley bottom; coordinates 14.49 N, 74.75 E; altitude 538 m.

## Collection and Method Details
- Measurements taken on a farm site; sensors installed on a slope.
- Distance to valley bottom: about 500 m.

## Data Structure and Variables
- Data stored in a CSV file; columns contain variables.
- Notation for missing data: NAN (Not A Number).
- Date format: DD/MM/YY; Time format: HH:MM:SS.
- Recorded variables:
  - SM_m3/m3_at10cm_depth: soil moisture at 10 cm depth
  - SM_m3/m3_at25cm_depth: soil moisture at 25 cm depth
  - SM_m3/m3_at50cm_depth: soil moisture at 50 cm depth
  - SM_m3/m3_at110cm_depth: soil moisture at 110 cm depth
- Units: cubic meters of water per cubic meter of soil (m3/m3).

## Quality Control and Validation
- Data quality checked by the project team.
- Not independently calibrated: sensors were not calibrated with site-specific soils.

## Location, Temporal Coverage, and Data Scope
- Temporal coverage: Jan 2020 – Jan 2022.
- Spatial scope: single farm site near Sirsi, Western Ghats.
- Depths covered: four specified soil moisture depths.

## Data Stewardship and Governance Considerations
- Metadata includes date/time, depth-specific soil moisture values, and units.
- Missing data indicated by NAN; no mention of data revisions or versioning.
- Noted limitation: lack of independent site-specific calibration, which may affect absolute moisture readings.
- Potential need for follow-up calibration, documentation of calibration status, and explicit sharing/licensing details if distributing datasets.

## Potential Uses and Recommendations
- Useful for understanding vertical soil moisture profiles and hydrological/agricultural dynamics in the Western Ghats region.
- Recommend documenting calibration status and any site-specific adjustments to improve interoperability and reuse.