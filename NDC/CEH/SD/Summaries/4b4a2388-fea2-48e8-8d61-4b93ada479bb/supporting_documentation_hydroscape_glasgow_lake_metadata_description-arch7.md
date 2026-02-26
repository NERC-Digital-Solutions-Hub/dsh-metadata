# Project: Historical lake sediment metal concentrations from Greater Glasgow

## Overview
- Describes a dataset uploaded to EIDC as hydroscape_glasgow_core_metadata.csv.
- Contains metadata and field-level descriptions for lake sediment cores used to study historical metal concentrations.

## Data structure and fields
- WBID (Waterbody Identification number): identifier for water bodies (linked to CEH Lakes app).
- Hydroscape: name of the Hydroscape region.
- Name: lake name.
- General location of core: core position types (deep, littoral, intermediate) within the lake.
- OSGB36_E / OSGB36_N: UK Ordnance Survey coordinates (Easting/Northing) in OSGB36 datum for GIS mapping.
- Water depth at core site (m): depth from water surface to sediment surface at the core site.
- Secchi disc depth (m): water clarity measurement prior to coring.
- Core length and type: length of the core in metres and its type.
- Corer types: e.g., Tapper; reference to methodology by Tapper, Chambers, and Cameron (2001).
- Date core collected: field collection date (dd/mm/yyyy).
- UCL_Code: internal UCL code used on bags/database.
- UCL Sample ID: internal unique ID for the entire sample core (Amphora code).
- 210 Pb-dated (Y/N) for Hydroscape: whether the core was dated using lead-210.

## Spatial information
- Coordinates (OSGB36_E, OSGB36_N) enable precise plotting of core locations in GIS and can be transformed to other coordinate systems as needed.

## Sampling metadata and provenance
- Source: UK Centre for Ecology & Hydrology (CEH) Hydroscape project; core data associated with Greater Glasgow lakes.
- UCL coding: internal labeling for samples and bags, facilitating data tracking and integration with other datasets.

## Data quality and integration considerations
- Data may come from multiple sources and locations; ensure consistent standards when integrating.
- Potential gaps or varying resolutions across fields; careful cleaning and harmonisation recommended.
- Large or complex datasets may require packaging into manageable units for GIS workflows.

## GIS applications and use cases
- Map core locations with OSGB36 coordinates to visualise spatial distribution of sediment cores.
- Combine core metadata with metal concentration data (from related datasets) to analyse spatial and temporal trends.
- Use core position categories (deep, littoral, intermediate) to examine within-lake spatial variability.
- Leverage 210Pb dating information where available to align age models and create time-based maps or time series.

## Access and references
- EIDC upload: hydroscape_glasgow_core_metadata.csv.
- Related references: CEH Lakes, Hydroscape region details, and the corer methodology reference (Tapper, Chambers, and Cameron, 2001).