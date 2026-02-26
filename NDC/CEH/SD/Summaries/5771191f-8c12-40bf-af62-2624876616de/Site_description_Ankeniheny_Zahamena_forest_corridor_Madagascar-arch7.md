# DATA HEADER INFORMATION for Site_description_Ankeniheny_Zahamena_forest_corridor_Madagascar.csv

## Overview
- Metadata header for a CSV dataset detailing the topographical characteristics of sampling sites in the Ankeniheny-Zahamena forest corridor, Madagascar.
- Associated with ESPA programme and the P4GES project; DOI provided for dataset access.
- Acknowledgement of the Laboratoire des Radio Isotopes, Université d'Antananarivo is required for products derived from these data.

## Data content and structure (key fields)
- site_ID: P4GES site code; text string.
- ZOI (Zone of Interest): Categorical; values include Lakato, Andasibe, Anjahamana, Didy.
- Location: Name of the sampling point location; text string.
- LU (Land use type): Categorical; values include Closed Canopy, Tree Savoka, Shrub Savoka, Degraded Land.
- Type: Categorical; indicates whether the site is a Plot or a Transect.
- X: Longitude in decimal degrees (WGS84); numeric; measured with GPS eTrex 30 Garmin.
- Y: Latitude in decimal degrees (WGS84); numeric; measured with GPS eTrex 30 Garmin.
- Altitude: Elevation in meters; numeric; GPS eTrex 30 Garmin.
- Precision: GPS precision in meters; numeric; GPS eTrex 30 Garmin.
- slope_up: Upward slope at the site; numeric; measured in degrees.
- slope_down: Downward slope at the site; numeric; measured in degrees.
- topographic_position: Position on the slope (Top sequence) described as Mid side, High side, or Low side.
- age_of_deforest: Estimated age of deforestation; numeric; years; based on field interviews with locals.
- age_of_fallow: Estimated age of fallows; numeric; years; based on field interviews with locals.
- Historic: Historical context of the site; text string; based on local interviews.

## Data collection methods and resources
- Coordinates (X, Y) and altitude obtained in the field using GPS equipment (GPS eTrex 30 Garmin).
- Slope measurements (slope_up, slope_down) obtained with a Sunnto MC-2 compass and Mirror Clinometer.
- Topographic positioning (topographic_position) recorded relative to slope orientation (top/mid/bottom) with qualitative descriptors.
- Age of deforestation and fallows, as well as historic context, derived from local interviews and input from local guides.

## Data use, standards, and provenance
- Dataset adheres to WGS84 geographic coordinates; units: decimal degrees for X/Y, meters for altitude/precision, degrees for slope variables.
- Clear linkage to the ESPA/P4GES program metadata and DOI for citation.
- Data providers note the requirement to acknowledge the Laboratoire des Radio Isotopes when using these data.

## Practical GIS implications for analysts
- Suitable for creating map-based topographical visualizations of site conditions across Zone of Interest.
- Enables integration with other spatial datasets (e.g., land use, elevation models) for landscape-level analyses.
- Useful for documenting site-specific characteristics (e.g., slope, position on slope, deforestation age) in spatial dashboards or thematic maps.