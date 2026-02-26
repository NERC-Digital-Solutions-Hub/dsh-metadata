# hydroscape_lakedistrict_core_metadata.csv

## Overview
- Metadata for a CSV file containing lake sediment core information in the Hydroscape Lake District.
- Includes identifiers, spatial coordinates, core positions, measurement values, core collection details, and dating status.
- Data linked to the UK Centre for Ecology & Hydrology and the Hydroscape region.

## Spatial context
- Hydroscape region designation used to contextualize each lake/core site.
- Geographic fields:
  - OSGB36_E (Easting)
  - OSGB36_N (Northing)
- Core locations are linked to specific lakes (lake names) and can be mapped in OSGB36; enable reprojection to other CRS (e.g., WGS84) for web GIS.

## Key fields and meanings
- WBID: Waterbody Identification number
- Hydroscape: Hydroscape region name
- Name: Lake name
- General_location_of_core: Core position within the lake (deep/central deep, littoral near vegetation margin, intermediate mid-depth)
- OSGB36_E / OSGB36_N: UK Ordnance Survey coordinates (Easting/Northing)
- Water_depth_at_core_site_(m): Water surface to sediment surface depth at the core site; measured with a hand-held echo sounder from a boat
- Secchi_disc_depth_(m): Mean water clarity (Secchi depth) at deepest position of the lake; derived from three measurements
- Core_length_and_type: Core length in metres and corer type used (Tapper, Big Ben, Livingstone, Renberg) with bibliographic references
- Date_core_collected: Fieldwork date (dd/mm/yyyy)
- UCL_Code: Internal UCL code used on bags/database
- UCL_Sample_ID: Internal Amphora code for the entire sample core (unique ID)
- 210 Pb-dated_Y_N_for_Hydroscape: Indicates if core was dated by 210Pb (Yes/No)

## Data collection methods
- Water depth: measured with a hand-held echo sounder; littoral depth confirmed by Secchi disc reaching sediment surface
- Secchi depth: three measurements taken; mean calculated; taken at the deepest lake position
- Core collection: multiple corer types referenced (Tapper, Big Ben, Livingstone, Renberg) with corresponding methodological sources

## GIS considerations
- Suitable for map-based visualization of lake cores, core depths, water clarity, and dating status
- Coordinate system: OSGB36; plan to transform to WGS84 or other CRS for standard GIS/WEB mapping
- Data may be integrated with other hydrological or limnological datasets; ensure consistent identifiers (WBID, UCL codes)

## Data quality and integration challenges
- Data may be dispersed across multiple sources; plan for data harmonization
- Potential gaps in resolution or missing values (e.g., dating status, exact coordinates)
- Variability in data standards and documentation across core datasets
- Large/complex datasets may require chunking by lake or core for processing

## Usage and context notes
- Includes a link to the Lakes index for broader context: https://eip.ceh.ac.uk/apps/lakes/index.html
- Enables GIS analysts to explore spatial patterns of core sites, their depth characteristics, and dating information within the Hydroscape Lake District