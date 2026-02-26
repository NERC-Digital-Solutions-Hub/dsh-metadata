# DATA HEADER INFORMATION for Site_description_Ankeniheny_Zahamena_forest_corridor_Madagascar.csv

## Overview
- Provides topographical and site-characteristics data for sites within the Ankeniheny-Zahamena forest corridor, Madagascar.
- Associated with ESPA Programme and the P4GES project; DOI provided.
- Acknowledgement required for products derived from these data: Laboratoire des Radio Isotopes, Université d'Antananarivo.

## Data provenance and scope
- Programme and project: ESPA (Environmental Science for a Changing World) and P4GES.
- Dataset focuses on site-level topography and observational context to support environmental health monitoring.
- Zone of Interest (ZOI) categories: ZOI1 Lakato, ZOI2 Andasibe, ZOI3 Anjahamana, ZOI4 Didy.
- Field resources noted: botanist; local guides; data collection tools include GPS devices and a compass/clinometer.

## Key variables and measurements
- site_ID
  - Type: Text string
  - Description: P4GES site code
- ZOI
  - Type: Categorical
  - Description: Zone of Interest (Lakato/Andasibe/Anjahamana/Didy)
- Location
  - Type: Text string
  - Description: Name of the sampling point location
- LU (Land Use)
  - Type: Categorical
  - Description: Land use type (Closed Canopy, Tree Savoka, Shrub Savoka, Degraded Land)
- Type
  - Type: Categorical
  - Description: Transect or Plot (Transect for WP4 site; Plot for common site with other workpackages)
- X
  - Type: Numeric
  - Description: Longitude (decimal degree, WGS84)
- Y
  - Type: Numeric
  - Description: Latitude (decimal degree, WGS84)
- Altitude
  - Type: Numeric
  - Description: Altitude of sampling point (meters)
- Precision
  - Type: Numeric
  - Description: GPS precision (meters)
- slope_up
  - Type: Numeric
  - Description: Slope upward (degrees)
- slope_down
  - Type: Numeric
  - Description: Slope downward (degrees)
- topographic_position
  - Type: Text string
  - Description: Position on slope (Mid side, High side, Low side)
- age_of_deforest
  - Type: Numeric
  - Description: Estimated age of deforestation (years)
- age_of_fallow
  - Type: Numeric
  - Description: Estimated age of fallows (years)
- Historic
  - Type: Text string
  - Description: Historical context of the site based on local interviews

## Data collection details and resources
- Field resources documented: local botanists and guides; GPS devices (GPS eTrex 30 Garmin); Sunnto MC-2 compass and Mirror Clinometer for slope measurements.
- Metadata and provenance notes indicate source is field-based, with emphasis on local knowledge for historical context.

## Data governance, quality, and access considerations
- Data sharing and open data considerations implied by field resources and project requirements; acknowledgment clause indicates formal provenance.
- Metadata completeness and clarity are important for verifying data suitability (some fields mention the need for adequate metadata and clear transformation steps).
- Data governance practices referenced include ensuring traceability of measurements and clear presentation of findings (through notes, charts, or dashboards) and sharing underlying data where appropriate.