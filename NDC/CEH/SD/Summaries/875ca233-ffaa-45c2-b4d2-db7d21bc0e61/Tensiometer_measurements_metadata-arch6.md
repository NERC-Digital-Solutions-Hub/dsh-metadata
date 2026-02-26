# Tensiometer measurements from a field experiment in the Conwy valley, North Wales, UK (2013 - 2015)

## Overview
- Field experiment conducted in the Conwy valley, North Wales, UK, during 2013–2015.
- Measurements capture soil water potential using tensiometers.
- Measurements are recorded in centimetres of water (cm H2O).

## Experimental design and sampling
- Tensiometers inserted vertically into holes bored with a hand auger at locations specified in Plot_locations.csv.
- Site locations and depths include SWP measurements at 12.5 cm and 42.5 cm depth for sites 4.1, 4.2, 4.3, and 4.4.

## Collection methods
- Equipment: Delta-T Devices SWT4R tensiometers connected to a Delta-T logger.
- Internal data conversion to centimetres of water performed within the logger.

## Calibration
- Data values are converted internally to centimetres of water (cm H2O) by the logger.

## Nature and units of recorded values
- Recorded values: soil water potential (SWP) in centimetres of water.
- Column names follow the pattern SWP_<site>_<depth> (e.g., SWP_4.1_12.5).

## Data structure (schema)
- DateTime: date and time of measurement.
- SWP_4.1_12.5
- SWP_4.1_42.5
- SWP_4.2_12.5
- SWP_4.2_42.5
- SWP_4.3_12.5
- SWP_4.3_42.5
- SWP_4.4_12.5
- SWP_4.4_42.5
- Empty cells indicate no data.

## Quality control
- Visual inspection of plotted time series used for data quality assessment.

## Related metadata and files
- Plot_locations.csv contains site coordinates.
- Plot_locations_metadata.rtf contains metadata for Plot_locations.csv.