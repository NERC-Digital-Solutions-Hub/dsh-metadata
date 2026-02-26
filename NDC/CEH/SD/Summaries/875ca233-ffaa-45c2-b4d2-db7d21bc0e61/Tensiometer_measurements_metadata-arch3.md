# Tensiometer measurements from a field experiment in the Conwy valley, North Wales, UK (2013 - 2015)

## Overview
- Field-based measurements of soil water potential (SWP) conducted 2013–2015 in the Conwy valley, North Wales, UK.
- Data intended for environmental monitoring and informing decisions about soil water status.

## Experimental Design and Sampling
- Tensiometers inserted vertically into holes bored using a hand auger.
- Insertion locations are specified in Plot_locations.csv.

## Collection Methods and Instruments
- SWP measured with refillable Delta-T Devices SWT4R tensiometers.
- Tensiometers connected to a Delta-T logger for data collection.

## Calibration and Units
- Internal conversion to centimetres of water within the logger.
- Recorded values are in centimetres of water (cm water).

## Data Structure and Metadata
- Data file: Tensiometer_measurements.csv.
- Column structure:
  - DateTime: date and time of measurement.
  - SWP_4.1_12.5, SWP_4.1_42.5, SWP_4.2_12.5, SWP_4.2_42.5, SWP_4.3_12.5, SWP_4.3_42.5, SWP_4.4_12.5, SWP_4.4_42.5.
  - Each column represents a site location and depth (e.g., Site 4.1 at 12.5 cm).
  - Empty cells indicate no data.
- Site coordinates are provided in Plot_locations.csv.
- Plot_locations_metadata.rtf contains metadata for Plot_locations.csv.

## Quality Control
- Visual inspection of plotted time series used to assess data quality.

## Data Availability and Governance
- Metadata for the main dataset is provided; underlying data can be shared publicly where appropriate.
- Metadata about plot locations is documented separately (Plot_locations.csv and its metadata).
- Data handling implies clear provenance and potential data sharing, with attention to documentation of origin and structure.

## Additional Notes
- Data structure is explicit about site/depth coding through column names, facilitating traceability and reuse in monitoring analyses.