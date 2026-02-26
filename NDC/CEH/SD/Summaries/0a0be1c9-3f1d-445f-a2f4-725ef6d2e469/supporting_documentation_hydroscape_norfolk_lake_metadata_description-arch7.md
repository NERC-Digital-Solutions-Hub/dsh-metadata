# File Uploaded to EIDC: hydroscape_norfolk_core_metadata.csv

## Overview
- Metadata for a CSV file uploaded to EIDC detailing hydroscape core data from Norfolk lakes.
- Captures spatial, temporal, and sample metadata to support GIS-based visualization and analysis of lake cores.

## Key fields and their meanings
- EIDC File Name: File name uploaded to EIDC (CSV).
- WBID: Waterbody Identification number (link to lake database).
- Hydroscape: Name of the Hydroscape region used.
- Name: Lake name.
- General location of core: Cores collected from the central (often deepest) area of the lake.
- OSGB36_E: UK Ordnance Survey Easting (OSGB36 Datum).
- OSGB36_N: UK Ordnance Survey Northing (OSGB36 Datum).
- Water depth at core site (m): Water surface to sediment surface depth at the core site.
- Core length and type: Core length in metres and core type.
- Corer types: References for corers used (Big Ben and Livingstone; with corresponding literature).
  - Big Ben: Patmore et al. 2014 (wide-bore piston corer for multi-proxy palaeolimnology).
  - Livingstone: Livingstone 1955 (lightweight piston sampler for lake deposits).
- Date core collected: Date of fieldwork and core collection (dd/mm/yyyy); year only shown if the precise date is unknown.
- UCL_Code: Internal UCL code used on bags/database.
- UCL Sample ID: Internal (Amphora) code for the entire sample core (unique ID).
- 210 Pb-dated (Y/N) for: Indicates whether the core was dated using 210Pb dating.
- Hydroscape: (Field exists; description truncated in the provided text).

## GIS implications
- Coordinates provided as OSGB36_E and OSGB36_N allow precise plotting of core locations on UK maps.
- Enables spatial analysis of core distribution within and across Hydroscape regions.
- Supports joins with lake-level attributes (WBID, Lake name, Hydroscape) for enriched map pop-ups and thematic maps.

## Data quality and provenance considerations
- Date formats include full dd/mm/yyyy or just year when exact date is unknown.
- Some fields reference external manuals/references (corer types) that may require domain knowledge to interpret.
- Data may originate from multiple sources; standardization (units, coordinate system) should be verified for GIS workflows.
- OSGB36 coordinates may require transformation for cross-compatibility with other projections.

## Practical usage notes
- Import into GIS as point features using OSGB36_E/N for geometry.
- Join attribute table with related datasets using WBID or UCL Sample IDs for richer context.
- Use 210Pb-dated flag to filter cores with radiometric dating for chronological analyses.
- Visualize by Hydroscape region to compare sampling density, depth distributions, and core lengths across lakes.