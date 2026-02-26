# Macroinvertebrates of the Conwy catchment

## Overview
- Dataset describing macroinvertebrate communities from the Conwy catchment, Wales, UK.
- Collected over three years: 2008–2010.
- Includes species-level descriptions plus supporting habitat and geographical data.

## Data Content
- Taxon dataset: Macroinvertebrates of the Conwy catchment - taxon data.csv
  - Columns include: Site code, Year, Sample date, Taxon code, Taxon name, Life stage, Abundance.
- Environmental variables dataset: Macroinvertebrates of the Conwy catchment - environmental variables.csv
  - Variables include: Site code, Year, Wetted width, Water depth, Velocity, % cover of rock pavement, % cover by substrate types (rocky to fine), % cover by macrophytes.
- Supporting information: Macroinvertebrates of the Conwy catchment - supporting information.csv
  - Site-level metadata: Easting, Northing, Grid reference, Distance from source, Altitude, Slope, Stream Strahler order, Catchment area, and site names.
- Sample identifiers: Defined by a unique combination of site code and project year; a key to site codes is provided in the supporting information.

## Methods
- Study area: Tributary streams of the Conwy, Wales, UK.
- Sampling dates: November 2008, 2009, and 2010.
- Field protocol: 1 mm kick net sampling following RIvPACS procedure; record site variables (depth, width, velocity, substrate cover, macrophyte cover).
- Sample handling: Samples preserved in 4% formaldehyde in the field, later washed through a 500 μm sieve; macroinvertebrates picked and identified to the lowest taxonomic level possible (usually species).
- Taxonomy: Valid names and unique taxon codes follow Davies & Edwards (2011).
- Data validation: Data entry validated by cross-checking printouts with laboratory sheets.
- Spatial data: Map variables derived using Intelligent River Network (Version 17); methodology described by Dawson et al. (2002).

## Data Quality and Validation
- Taxonomic names and codes standardized to a published code list (Davies & Edwards, 2011).
- Cross-checks between laboratory sheets and data printouts ensure accuracy of entries.
- Data entry follows a consistent, traceable process to support reliability in monitoring outputs.

## Spatial Design and Source Data
- Location: Conwy catchment streams; coordinates and site details provided in supporting information.
- Site metadata include exact easting/northing, grid references, distance from source, altitude, slope, stream order, and catchment area.

## Data Structure and Key Fields
- Taxon data
  - Site code, Year, Sample date, Taxon code, Taxon name, Life stage, Abundance.
- Environmental data
  - Site code, Year, Wetted width, Water depth, Velocity, % cover of rock pavement, % cover by boulders/cobbles, pebble/gravel, sand/clay, % cover by macrophytes.
- Supporting information
  - Site code, Site name, Easting, Northing, Grid reference, Distance from source, Altitude, Slope, Stream order, Catchment area.
- Sample identifiers are documented with a site-code–year scheme; a site-code key is provided in the supporting information.

## Data Access, Reuse, and Stewardship
- Designed to provide standardized outputs suitable for environmental health assessment and policy performance monitoring over time.
- Acknowledges challenges common to monitoring data use:
  - Increasing the value of datasets by combining with other relevant data.
  - Facilitating access to the underlying data behind final outputs.
- Datasets are prepared for storage and upload to appropriate data portals, aligning with monitoring responsibilities and data stewardship practices.

## Version and Contributors
- Version: 1.0, date 28/06/16; description: created; author: F. Edwards.
- Contributors:
  - Sample collection: Gearóid Webb, Peter Scarlett, John Davy-Bowker
  - Laboratory analysis: Gearóid Webb, Helen Vincent, François Edwards
  - Supporting information: Peter Scarlett, Gearóid Webb, François Edwards
  - Planning and Management: François Edwards, David Cooper