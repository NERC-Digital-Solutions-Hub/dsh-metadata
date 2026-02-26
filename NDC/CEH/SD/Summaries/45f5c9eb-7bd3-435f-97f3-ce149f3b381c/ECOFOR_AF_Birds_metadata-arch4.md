# BirdSpecies.csv

## Data overview
- Bird survey dataset from 441 sampling locations in the Atlantic Forest of Brazil.
- Four temporal replicates per point conducted between December 2015 and February 2017.
- Part of the ECOFOR project, under the NERC HumanModified Tropical Forest programme.

## Sampling design
- 441 points across Vale do Paraíba and Serra do Mar, São Paulo, Brazil.
- Evenly spread across 49 landscapes using a nine-point regular grid with 75 m spacing (where feasible).
- 15 landscapes are controls with a single predominant land-use type (native forest, Eucalyptus plantation, or pasture).
- 34 landscapes are native forest fragments embedded in other land-use types.
- For fragmented landscapes: three points in native forest fragment, three at the fragment edge, and three in the surrounding matrix.
- Two matrix types surveyed: 15 fragments border plantation and 19 border pasture.

## Data collection techniques
- Point counts of 15 minutes per survey, recording all bird species within a 25 m radius.
- Four temporal replicates, evenly split between dry and wet seasons.

## Data structure
- Data stored in a single CSV file: BirdSpecies.csv.
- Each row represents a single sampling point.

## Column headings and meanings
- Species columns (1–267): identity of species detected, following BirdLife International taxonomy (BirdLife International 2017). Values indicate the number of temporal replicates in which the species was detected.
- LandscapeID: numerical reference to the landscape containing the sample point.
- HabitatType: I = native forest interior, E = native forest edge, M = matrix.
- MatrixType: P = pasture, E = plantation, CF = control forest landscape, CP = control pasture landscape, CE = control plantation landscape.
- X and Y: coordinates in SAD 1969 UTM 23S, rounded to the nearest kilometre to protect exact locations of rare/ threatened species.

## Data provenance and references
- Taxonomy: BirdLife International (2017) Handbook of the Birds of the World and BirdLife International digital checklist (Version 9.1).

## Data governance and stewardship (Data Leaders perspective)
- Provenance is well-documented through ECOFOR/NERC program affiliation.
- Standardized data structure supports discoverability and reuse (single CSV; clear column definitions; BirdLife taxonomy).
- Spatial data are masked to protect sensitive species locations (coordinate rounding).
- Metadata elements (LandscapeID, HabitatType, MatrixType, coordinates) enable reproducibility and cross-study integration.
- Suitable for evaluating habitat effects, fragmentation, and community composition across landscapes, with potential for cross-partner data sharing within a collaborative data system.