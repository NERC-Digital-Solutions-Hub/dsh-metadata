# Tensiometer measurements from a field experiment in the Conwy valley, North Wales, UK (2013 - 2015)

## Dataset overview
- Field measurements of soil water potential (SWP) using tensiometers in Conwy valley, North Wales (2013–2015).
- Tensiometers inserted vertically into holes bored with a hand auger at locations specified in Plot_locations.csv.
- Data linked to Plot_locations.csv for site coordinates; Plot_locations_metadata.rtf contains metadata.

## Experimental design and sampling regime
- Measurements taken at multiple sites indicated in Plot_locations.csv.
- Tensiometers inserted vertically into pre-bored holes to record soil water potential over time.

## Collection methods and instrumentation
- Soil water potential measured with refillable Delta-T Devices SWT4R tensiometers.
- Tensiometers connected to a Delta-T logger for data capture.
- Internal conversion to centimetres of water within the logger.

## Calibration and data units
- Calibration: internal conversion to centimetres of water (cm water) within the logger.
- Recorded values expressed in centimetres of water (cm H2O).

## Data structure and fields
- DateTime: date and time of each measurement.
- SWP_4.1_12.5, SWP_4.1_42.5
- SWP_4.2_12.5, SWP_4.2_42.5
- SWP_4.3_12.5, SWP_4.3_42.5
- SWP_4.4_12.5, SWP_4.4_42.5
- Each SWP_* field corresponds to a site location (4.1–4.4) and depth (12.5 cm or 42.5 cm).
- Empty cells indicate no data.

## Quality control and supporting documentation
- Quality Control: visual inspection of plotted time series.
- Supporting documents:
  - Plot_locations.csv contains site coordinates.
  - Plot_locations_metadata.rtf contains metadata related to Plot_locations.csv.

## Spatial context and GIS relevance
- Data are geolocated via Plot_locations.csv, enabling spatial mapping of SWP across sites and depths.
- Suitable for GIS-based visualization of temporal changes in soil moisture potential by location and depth.

## Temporal scope
- Measurements collected during 2013–2015.