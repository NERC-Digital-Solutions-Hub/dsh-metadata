# DATA HEADER INFORMATION for Site_description_Ankeniheny_Zahamena_forest_corridor_Madagascar.csv

## Overview
- Presents topographical characteristics for sampling sites within the Ankeniheny-Zahamena forest corridor, Madagascar.
- Associated with ESPA (Environmental Services Programme) and the P4GES project; DOI provided.
- Acknowledgement required for outputs derived from these data (Laboratoire des Radio Isotopes, Université d'Antananarivo).

## Variables and data types

- site_ID
  - Information: P4GES site code
  - Type: Text
  - Unit: None specified
  
- ZOI (Zone of Interest)
  - Information: Zone of Interest designation
  - Type: Categorical
  - Unit: ZOI1: Lakato / ZOI2: Andasibe / ZOI3: Anjahamana / ZOI4: Didy

- Location
  - Information: Name of the sampling point location
  - Type: Text
  - Unit: None specified

- LU (Land use type)
  - Information: Land use type
  - Type: Categorical
  - Unit: Closed Canopy / Tree Savoka / Shrub Savoka / Degraded Land

- Type
  - Information: Transect or Plot
  - Type: Categorical
  - Unit: Plot / Transect

- X
  - Information: Longitude (east)
  - Type: Numeric
  - Unit: Decimal degrees (WGS84)

- Y
  - Information: Latitude (south)
  - Type: Numeric
  - Unit: Decimal degrees (WGS84)

- Altitude
  - Information: Altitude of the sampling point
  - Type: Numeric
  - Unit: Meters

- Precision
  - Information: GPS precision
  - Type: Numeric
  - Unit: Meters

- slope_up
  - Information: Slope of the site upward measurement
  - Type: Numeric
  - Unit: Degrees

- slope_down
  - Information: Slope of the site downward measurement
  - Type: Numeric
  - Unit: Degrees

- topographic_position
  - Information: Position of the sampling point on the slope
  - Type: Text
  - Unit: Mid side / High side / Low side

- age_of_deforest
  - Information: Estimated age of deforestation based on field interviews
  - Type: Numeric
  - Unit: Years

- age_of_fallow
  - Information: Estimated age of fallows based on field interviews
  - Type: Numeric
  - Unit: Years

- Historic
  - Information: Historic of the site based on local people interviews
  - Type: Text
  - Unit: None specified

## Data provenance and access

- Programme: ESPA; Project: P4GES
- Data DOI provided
- Acknowledgement required for outputs
- Field resources referenced: botanist, local guides
- Data characteristics: topographical measurements at sampling points created for site descriptions in the forest corridor

## How to use the data

- Locational analysis: map sampling points using X/Y coordinates to examine spatial distribution across ZOI and land-use types.
- Topography and land-use relationships: explore associations among slope (slope_up, slope_down), altitude, land use, and topographic position.
- Deforestation history: analyze age_of_deforest and age_of_fallow in relation to historic notes and zone of interest.
- Data integration: combine with other environmental datasets (e.g., vegetation, hydrology) to support corridor management and conservation planning.
- Documentation and reproducibility: note the data provenance, units, and collection methods; share datasets with metadata for discoverability.

## Limitations and considerations

- The header information is focused on metadata and variable definitions; actual data values are not included here.
- Some fields (e.g., Historic) are qualitative and may require careful interpretation or coding for analyses.
- Spatial data scale and local specificity may limit extrapolation beyond surveyed sites.
- Data access and proper acknowledgment are required for use of outputs.