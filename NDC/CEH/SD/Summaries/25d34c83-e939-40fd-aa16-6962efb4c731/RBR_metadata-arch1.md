# Water temperature measurements from Durleigh Reservoir 2018 - RBR SoloT

## Overview
- Temperature measurements from Durleigh Reservoir in 2018 using an RBR SoloT thermistor chain.
- Measurements collected from surface (0 m) to bottom (6 m) at 10-minute intervals.
- Time period: 22/02/2018 to 05/10/2018.
- Temperature unit: degrees Celsius (oC).

## Data details
- Location: latitude 51.1210, longitude -3.0403.
- Sensor configuration: thermistors positioned at depths of 0 m, 1 m, 2 m, 3 m, 4 m, 5 m, and 6 m.
- Time format: dd/mm/yyyy HH:MM.
- Data source/file type: temperature data and a separate temperature metadata file documenting deployment details.

## Data quality and gaps
- Missing data for the 1 m, 2 m, and 3 m depth intervals due to corrupted files on download from the thermistors.
- Overall data coverage is affected by these missing depths; 0 m, 4 m, 5 m, and 6 m data may be present but need confirmation from the accompanying metadata.

## Metadata and provenance
- Deployment personnel: Emily Slavin and Danielle Wain.
- Documentation: Slavin, E.I., Wain, D.J. 2018. Water temperature measurements from Durleigh Reservoir 2018.
- Metadata scope includes location coordinates, depth intervals, and time range; aims to support data discovery and reuse.

## Usage considerations for analysts
- When analysing temperature profiles, account for missing data at 1–3 m; plan for gap-filling or sensitivity analyses where depth-specific responses are required.
- Ensure temporal alignment across depths for correlation or heat-content analyses, given 10-minute sampling.
- Consider data provenance and versioning; reference the 2018 deployment record and metadata file for proper context.

## Access and notes
- Temperature data are accompanied by a metadata file; reported temperatures are in Celsius and timestamps follow the specified format.
- Data provenance indicates the study is part of a documented 2018 deployment by named researchers.