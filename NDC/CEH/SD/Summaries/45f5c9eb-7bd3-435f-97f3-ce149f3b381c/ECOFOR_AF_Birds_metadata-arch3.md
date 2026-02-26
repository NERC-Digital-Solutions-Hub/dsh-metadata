# BirdSpecies.csv

## Overview
- Bird survey data from 441 sampling points in the Atlantic Forest of Brazil (Vale do Paraíba and Serra do Mar, São Paulo).
- Four temporal replicates per point between December 2015 and February 2017.
- Part of the ECOFOR project (Biodiversity and Ecosystem Functioning in Degraded and Recovering Forests) within the NERC Human Modified Tropical Forest programme.

## Sampling Design
- 441 points across 49 landscapes, using a nine-point regular grid with 75 m spacing where possible.
- 15 landscapes with a single predominant land-use type (controls): native forest, Eucalyptus plantation, or pasture; evenly split.
- 34 landscapes are fragmented native forest embedded within other land-use types.
  - For fragments: three points in native forest fragment, three at the edge, three in the surrounding matrix.
  - Two matrix types surveyed: 15 fragments bordering plantation and 19 bordering pasture.
- Fragmented landscapes chosen to represent a range of patch sizes and connectivity.

## Data Collection Techniques
- Point counts of 15 minutes per sampling event; all bird species within a 25 m radius recorded.
- Four temporal replicates distributed across the dry and wet seasons.

## Data Structure and Variables
- Data stored in a single CSV file (BirdSpecies.csv); each row corresponds to one sampling point.
- Columns include:
  - Species columns (267 total): for each species, the value indicates the number of temporal replicates in which the species was detected.
  - LandscapeID: numeric reference to the landscape containing the sample point.
  - HabitatType: I = native forest interior, E = native forest edge, M = matrix.
  - MatrixType: P = pasture, E = plantation, CF = control forest landscape, CP = control pasture landscape, CE = control plantation landscape.
  - X and Y: coordinates in SAD 1969 UTM 23S, rounded to the nearest kilometre to protect exact locations of rare/threatened species.
- Taxonomy follows BirdLife International (2017).

## Provenance and Context
- Data originate from the ECOFOR project within the NERC HMTF programme.
- Reference for taxonomy: BirdLife International 2017 Handbook of the Birds of the World and BirdLife International digital checklist (Version 9.1).

## Relevance for Monitoring Frameworks
- Provides baseline biodiversity data across native forest, plantation, pasture, and fragmentation contexts to assess impacts of land-use change and matrix effects.
- Supports indicators of species incidence/occurrence, habitat associations, and temporal biodiversity responses to seasonal variation.
- Highlights data governance considerations for monitoring frameworks:
  - Data are centralized in a single CSV, with explicit metadata on sampling design and variable definitions.
  - Taxonomy aligned to a standard reference (BirdLife International).
  - Location data are spatially coarse (rounded coordinates) to protect sensitive species, illustrating a balance between data accessibility and privacy.
  - Metadata completeness is embedded in the data description; no explicit external metadata schema noted beyond column definitions.