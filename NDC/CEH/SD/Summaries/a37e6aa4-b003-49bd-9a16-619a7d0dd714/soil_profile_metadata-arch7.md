# soil_profile_data.csv

## Overview
- A soil profile data sheet for the Siksik catchment in the North West Territories, Canada.
- Data collected in September 2014 along a transect; includes 64 samples and 10 soil profiles (P1–P10) with dominant plant community names.
- Geographic scope and elevation provided: Longitude 133°26'26"W, Latitude 68°44'17"N, Elevation 85 m.
- Fields capture sampling location, depths, pH, bulk density, and spatial coordinates for GIS mapping.

## Data schema and fields
- sample: Sample identification number (1 to 64).
- location: Soil profile identification; notes that 14C indicates 14C analysis; names refer to the dominant plant community.
- depth_1: Upper depth of the sampling depth (cm).
- depth_2: Lower depth of the sampling depth (cm).
- ph: pH value obtained via a 1:5 soil:water suspension method.
- Bulk_density_gcm3: Bulk density in g/cm3.
- longitude: Location of sampling within the Siksik catchment; coordinates provided in a DMS-like format (no explicit CRS stated in excerpt).
- latitude: Location of sampling within the Siksik catchment; coordinates provided similarly.
- elevation: Elevation of sampling location (m) provided in the header.
- Column_heading / Units: The sheet includes column headings and their units (as part of the data sheet description).

## Sampling and methods
- Soil samples collected along a transect in September 2014, Siksik catchment, NW Territories, Canada.
- Recording of sampling depth, location (latitude/longitude) for each sample.
- Bulk density measured according to Blake and Hartge (1986).
- pH determined using the 1:5 soil:water suspension method.
- References in the data sheet point to established soil analysis methods for reproducibility.

## Spatial and contextual notes
- Names in the dataset refer to dominant plant communities.
- P1 to P10 indicate soil profiles along the transect.
- Data is structured to support map-based visualization of soil properties across a transect, including vertical (depth_1 to depth_2) and horizontal (location coordinates) dimensions.

## References
- Blake, G., Hartge, K. (1986). Bulk density. In Klute, A. (Ed.), Methods of Soil Analysis: Part 1. Physical and Mineralogical Methods. SSSA, Madison, WI, pp. 383–411.
- pH method reference: 1:5 soil:water suspension method (linked to NSW soil test methods PDF).

## GIS considerations
- Coordinate data are provided as longitude and latitude in a DMS-like format; verify and convert to a standard CRS (e.g., WGS84) for GIS work.
- Depth_1 and depth_2 enable analysis of soil properties at multiple depths; data can be visualized as vertical profiles on maps or per-profile cross-sections.
- Keep in mind the transect layout (P1–P10) when aggregating across profiles for spatial analyses or when joining with other layers (e.g., vegetation, elevation).