# Tensiometer measurements from a field experiment in the Conwy valley, North Wales, UK (2013 - 2015)

## Overview
- Field measurements of soil water potential using tensiometers in Conwy valley, North Wales (2013–2015).
- Data file: Tensiometer_measurements.csv.
- Supporting metadata and locations are provided via Plot_locations.csv and Plot_locations_metadata.rtf.

## Experimental design and collection methods
- Tensiometers inserted vertically into holes bored with a hand auger at locations specified in Plot_locations.csv.
- Soil water potential measured with refillable Delta-T Devices SWT4R tensiometers connected to a Delta-T logger.
- Calibration involves internal conversion to centimetres of water within the logger.
- Fieldwork and instrumentation details reference the above methods.

## Data structure and content
- Recorded values are in centimetres of water (cm water).
- Columns include:
  - DateTime: date and time of measurement.
  - SWP_4.1_12.5, SWP_4.1_42.5, SWP_4.2_12.5, SWP_4.2_42.5, SWP_4.3_12.5, SWP_4.3_42.5, SWP_4.4_12.5, SWP_4.4_42.5
  - Each column represents soil water potential for a site (4.1 to 4.4) at a specific depth (12.5 cm or 42.5 cm).
- Empty cells indicate no data for that site/depth at a given time.

## Quality control and supporting metadata
- Quality control performed via visual inspection of plotted time series.
- Site coordinates and related metadata are provided in Plot_locations.csv and Plot_locations_metadata.rtf, respectively.

## Supporting documents and data governance
- Plot_locations.csv contains site locations; Plot_locations_metadata.rtf contains metadata for those locations.
- Data is structured to allow cross-referencing between measurement timestamps, site identifiers, and depths.

## Data quality considerations and caveats
- Some data rows contain empty cells, indicating missing measurements.
- Metadata notes clarify units, site/depth labeling, and data provenance (instrumentation and calibration steps).

## Data stewardship considerations
- Ensure consistent units (cm of water) and labeling across sites and depths.
- Maintain alignment between Tensiometer_measurements.csv and Plot_locations.csv for site-location context.
- Document any data updates or additions to support ongoing discoverability and usability.
- Monitor data completeness and fill gaps as needed to support time-series analyses.
- Preserve and reference supporting metadata (Plot_locations_metadata.rtf) to maintain dataset provenance.