# Macroinvertebrates of two abstracted streams - taxon data.csv

## Overview
- Dataset of macroinvertebrate communities from two Lowther catchment streams (Heltondale Beck and Howes Beck) upstream and downstream of water abstraction points.
- Includes species-level taxon data and supporting habitat/geographic information to assess environmental health and the impact of abstractions.
- Date of sampling: 23–24 September 2010; locations fixed as ~100 m reaches around abstraction points.

## Data and contents
- Macroinvertebrate data
  - Taxon dataset with columns:
    - Sample identifier (coded as stream + position upstream/downstream + replicate)
    - Taxon name (per Davies & Edwards 2011)
    - Taxon code (per Davies & Edwards 2011)
    - Life stage (L, P, A, U)
    - Abundance per sample area (0.0625 m2)
- Supporting information (Table 1)
  - Habitat and site variables for each stream/reach, including:
    - Grid references, northings/eastings, altitude, slope, distance from source
    - Elevation at source, geology codes (BGS solid/drift; NCC)
    - Wetted width, water depth
    - Habitat Quality Assessment (HQA) and Habitat Modification Score (RHS)
    - RHS class (HMS class)
  - Data rows for Howes Beck (US/DS positions) and Heltondale Beck (US/DS positions) with detailed geolocation and environmental parameters

## Methods and data acquisition
- Study design
  - Two tributaries of the Lowther: Howes Beck (Cawdale Beck) and Heltondale Beck
  - Reaches selected ~100 m upstream and downstream of abstraction points; sampling includes 5 riffles per reach
- Field methods
  - Habitat assessment using River Habitat Survey (RHS) method
  - Water depth (cm) and wetted width (m) measured as triplicate means
  - GPS-based location, 100 m sampling reach defined (50 m upstream, 50 m downstream)
- Macroinvertebrate sampling
  - Surber sampling: 0.0625 m2 area, 250 μm mesh, approximately 5 cm depth
  - Five riffles per reach sampled; field samples preserved in 4% formaldehyde
  - In lab, samples washed through 250 μm sieve; macroinvertebrates identified to the lowest taxonomic level feasible (usually species)
  - Taxon nomenclature and unique codes from Davies & Edwards (2011) Code list; data entry validated against laboratory sheets
- Data processing
  - Taxon codes and names cross-checked with established code list; life stages recorded; abundance per sample area documented

## Data structure and sample coding
- Sample codes
  - Stream: HB Howes Beck or HDB Heltondale Beck
  - Position: US (upstream) or DS (downstream)
  - Replicate: 1–5
- Taxon dataset columns (A–E)
  - A: Sample identifier
  - B: Taxon name
  - C: Taxon code
  - D: Life stage (L, P, A, U)
  - E: Abundance in sample area (0.0625 m2)
- Supporting information columns (Table 1)
  - A–R cover stream name, position, grid coordinates, Northings/Eastings, Altitude, Slope, Dist_from_source, Height_of_source, Geology codes, Width, Depth, HQA, HMS, HMS class
  - Example rows provided for Howes Beck and Heltondale Beck with upstream/downstream positions and comprehensive environmental metadata

## Data quality and provenance
- Validation
  - Data entry cross-checked with laboratory records
  - Valid taxon names and codes provided by Davies & Edwards (2011)
- Documentation and accessibility
  - Supporting information enables contextual interpretation (habitat and geology) for environmental health assessments
  - Described as part of a monitored dataset with standardized methods for consistency over time

## Relevance to environmental monitoring
- Enables assessment of ecological health by linking macroinvertebrate communities to habitat conditions and geology
- Provides standardized, repeatable methods suitable for monitoring policy performance and environmental status over time
- Designed to value-add by enabling integration with other data sources (e.g., RHS, hydrology, geology) and supports data sharing through appropriate portals

## Contributors and version history
- Sample collection: François Edwards, Peter Scarlett, Gearóid Webb
- Laboratory analysis: Gearóid Webb, François Edwards, Helen Vincent
- Supporting information: Peter Scarlett, Gearóid Webb, François Edwards
- Version history
  - Version 1.0 — created (21/06/2016)
  - Version 2.0 — modified to support information (22/06/2016)

## Usage notes
- Useful for environmental health reporting, trend analysis, and impact assessments around water abstractions
- Data structure supports aggregation to community metrics (e.g., taxa richness, abundance) and linkage to habitat quality indicators
- Suitable for integration with other datasets to broaden utility beyond single-use analyses