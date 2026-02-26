# Soil moisture data, Sirsi, Western Ghats

## Overview
- Dataset of soil moisture profiles near trees on a farm in Sirsi, Karnataka, Western Ghats, India (lat 14.49 N, lon 74.75 E; altitude 538 m).
- Measurements collected from January 2020 to January 2022.
- Depths: 10 cm, 25 cm, 50 cm, and 110 cm.

## Collection and Location
- Collected on a gentle slope approximately 500 m from the local valley bottom.
- Soil moisture measured with Campbell CS616 Water Content Reflectometers.

## Data Structure and Variables
- Data stored in a CSV file with variables arranged in columns.
- Date format: DD/MM/YY; Time format: HH:MM:SS.
- Key variables:
  - SM_m3/m3_at10cm_depth (soil moisture at 10 cm)
  - SM_m3/m3_at25cm_depth (soil moisture at 25 cm)
  - SM_m3/m3_at50cm_depth (soil moisture at 50 cm)
  - SM_m3/m3_at110cm_depth (soil moisture at 110 cm)
- Missing data indicated as NaN (Not A Number).

## Measurements and Units
- Depth-specific soil moisture expressed as m3/m3.
- Temporal resolution not specified beyond measurement period (Jan 2020–Jan 2022).

## Quality Control and Limitations
- Data quality checked by the project team.
- Sensors were not independently calibrated using soils from the site, which may affect calibration-specific accuracy.

## Relevance for Environmental Monitoring
- Provides standardized soil moisture profiles across multiple depths for a specific site, suitable for temporal analysis of soil moisture dynamics.
- Aligns with typical monitoring workflows: data verification, standardised outputs, and potential integration with broader environmental datasets.

## Data Access and Use Considerations
- Dataset presented as a CSV with a clear, columnar structure; explicit portal storage or data access mechanisms are not detailed in the document.
- Consider linking with other datasets to enhance value and enable broader accessibility of underlying data.