# Macroinvertebrates of the Conwy catchment - taxon data.csv

## Overview
- Dataset describing macroinvertebrate communities from the Conwy catchment, Wales, UK.
- Sampled over three years: 2008, 2009, and 2010.
- Includes supporting habitat and geographical data to contextualise biological observations.

## Data Files Included
- Macroinvertebrates of the Conwy catchment - taxon data.csv
  - Species-level descriptions of macroinvertebrate communities.
  - Abundances per sample, taxon codes, life stage, and sample identifiers.
- Macroinvertebrates of the Conwy catchment - environmental variables.csv
  - Site-level environmental measurements (width, depth, velocity, substrate, macrophyte cover, etc.).
- Macroinvertebrates of the Conwy catchment - supporting information.csv
  - Site metadata (site code, site name, coordinates, distance from source, altitude, slope, stream order, catchment area, etc.).

## Contributors and Roles
- Sample collection: Gearóid Webb, Peter Scarlett, John Davy-Bowker
- Laboratory analysis: Gearóid Webb, Helen Vincent, François Edwards
- Supporting information: Peter Scarlett, Gearóid Webb, François Edwards
- Planning and management: François Edwards, David Cooper

## Methods and Data Collection
- Study focus: tributary streams of the Conwy, Wales, UK.
- Sampling times: November 2008, 2009, and 2010.
- Biological sampling: 1 mm kick net following the RIvPACS protocol; collected macroinvertebrates preserved in 4% formaldehyde in the field.
- Laboratory processing: samples washed through a 500 μm sieve; macroinvertebrates identified to the lowest taxonomic level possible (usually species).
- Taxonomic references: valid taxon names and codes per Davies, Edwards (2011) Code list for recording freshwater macroinvertebrates in the British Isles.
- Data validation: data entry validated by cross-checking printouts with laboratory sheets.
- Geospatial data: map variables derived using Intelligent River Network (Version 17); methodology described by Dawson et al. (2002).

## Data Structure and Sample Identification
- Samples defined by a unique combination of site code and year.
- A site-code to site-name mapping is provided in the supporting information.
- Taxon dataset columns:
  - A: Site code
  - B: Year
  - C: Sample date
  - D: Taxon code (per Davies and Edwards 2011)
  - E: Taxon name (per Davies and Edwards 2011)
  - F: Life stage (L = larva/nymph, P = pupa, A = adult, U = life stage not relevant)
  - G: Abundance in sample
- Supporting information columns:
  - A: Site code
  - B: Site name
  - C: Easting
  - D: Northing
  - E: OS grid reference
  - F: Distance from source (km)
  - G: Altitude (m)
  - H: Slope (m per km)
  - I: Stream Strahler order
  - J: Upstream catchment area
- Environmental variables columns:
  - A: Site code
  - B: Year
  - C: Wetted width (m)
  - D–G: Depth (cm), Velocity (m/s)
  - H–K: Percent cover of rock pavement, boulders/cobbles, pebble/gravel, sand/clay (sums to 100%)
  - M: Percent cover by macrophytes

## Data Quality and Provenance
- Taxon coding aligned with Davies & Edwards (2011) taxonomy codes.
- Data entry validated against laboratory records to ensure accuracy.
- Map-derived environmental variables created with a documented pipeline (Intelligent River Network, Version 17).

## Reuse, Access, and Context
- The dataset combines biological observations with rich site-level metadata to support cross-site comparisons and broader ecological analyses.
- Useful for river health assessments, biodiversity studies, and data integration with RIvPACS-based frameworks.
- Access is structured around three interconnected files (taxon data, environmental variables, and supporting information) that can be joined via site code and year.

## Version and Contact
- Version 1.0, date 28/06/16
- Authors: F. Edwards (primary), with listed contributors for data collection, lab analysis, and planning/management.