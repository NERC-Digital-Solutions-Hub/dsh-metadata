# Project: Historical lake sediment metal concentrations from Greater Glasgow File Uploaded to EIDC: hydroscape_glasgow_core_metadata.csv

## Overview
- Metadata for historical lake sediment metal concentration project in Greater Glasgow.
- File uploaded to EIDC named hydroscape_glasgow_core_metadata.csv; supports linking core data to lake and sampling context within the Hydroscape region.

## Key fields and definitions
- WBID: Waterbody Identification number; unique ID linking to lakes index.
- Hydroscape: Name of the Hydroscape region used for the cores.
- Name: Lake name.
- General location of core: Core placement category (deep, littoral, or intermediate).
- OSGB36_E / OSGB36_N: Easting and Northing coordinates in OSGB36 datum.
- Water depth at core site (m): Water depth from surface to sediment surface at the core site.
- Secchi disc depth (m): Water clarity measurement prior to coring.
- Core length and type: Core length in metres and description of core type.
- Corer types: Cores collected using specified corers (e.g., Tapper; reference to methodologies).
- Date core collected: Field collection date (dd/mm/yyyy).
- UCL_Code: Internal University College London code used on bags/database.
- UCL Sample ID: Internal unique ID for the entire sample core.
- 210 Pb-dated (Y/N) for Hydroscape: Indicates whether the core was dated using 210Pb during the project.

## Data provenance and context
- Collected as part of the Historical lake sediment metal concentrations project within the Greater Glasgow area.
- Metadata supports linking physical core context (location, depth, coring method) with analytical results.
- Uses OSGB36 coordinates for spatial accuracy and consistency with UK datasets.

## Usability and data quality considerations
- Enables spatial mapping and cross-referencing of core locations with lake characteristics.
- Facilitates quality checks by matching core IDs with UCL codes and sample IDs.
- Potential data quality considerations: some fields may be missing or require cross-referencing with the lakes index or related publications; dating status (210Pb) informs chronology reliability.

## Access and usage guidance
- Access via EIDC using the hydroscape_glasgow_core_metadata.csv dataset.
- Use to join core context with metal concentration results, enabling self-serve exploration of spatial and temporal patterns.
- Map core locations, assess relationships between core depth, water depth, and sampling date; examine dating status across Hydroscape cores.

## Suggested data products and analyses (Data Support perspective)
- Dashboards mapping core locations and metadata (depth, core length, dating status).
- Pivot/joined tables linking WBID with core metadata and metal concentration results.
- Dashboards highlighting differences by Hydroscape region, core type, and dating method to support interpretation of historical metal records.