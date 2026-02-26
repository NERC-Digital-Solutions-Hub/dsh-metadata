# BirdSpecies.csv

## Data overview
- Bird survey data from 441 sample locations in the Atlantic Forest of Brazil (Vale do Paraíba and Serra do Mar, São Paulo).
- Four surveys per location between December 2015 and February 2017.
- Part of the ECOFOR project under the NERC HumanModified Tropical Forest programme.
- Data stored in a single CSV file; each row represents one sampling point.

## Sampling design
- 441 sampling points spread across 49 landscapes using a nine-point regular grid with 75 m spacing (where feasible).
- 15 landscapes are controls with a single predominant land-use type, evenly split among native forest, Eucalyptus plantation, and pasture.
- 34 landscapes are fragmented native forest fragments embedded in other land-uses.
- Fragmented landscapes sampled with 3 points in the fragment, 3 at the edge, and 3 in the surrounding matrix; two matrix types (15 fragments border plantation, 19 border pasture).

## Data collection techniques
- Point counts lasting 15 minutes per session; all bird species detected within a 25 m radius recorded.
- Four temporal replicates per sampling point, distributed across dry and wet seasons.

## Data structure
- Data contained in BirdSpecies.csv; each row is a sampling point.

## Column headings
- Species columns (1–267): counts indicating the number of temporal replicates in which each species was detected; taxonomy follows BirdLife International (2017).
- LandscapeID: numerical reference to the landscape containing the sample point.
- HabitatType: I = native forest interior, E = native forest edge, M = matrix.
- MatrixType: P = pasture, E = plantation, CF = control forest landscape, CP = control pasture landscape, CE = control plantation landscape.
- X and Y: coordinates in SAD 1969 UTM 23S, rounded to the nearest kilometre to protect rare/threatened species.

## References
- BirdLife International. 2017. Handbook of the Birds of the World and BirdLife International digital checklist of the birds of the world. Version 9.1. Available at: http://datazone.birdlife.org/species/taxonomy

## Practical notes for GIS use
- The dataset is wide (one column per species). Consider transforming to long format for species-by-point analyses or use as a multi-attribute layer if preferred.
- Join to landscape attributes via LandscapeID to enrich spatial analysis (land-use type, matrix context).
- Use the X, Y coordinates to map sampling points; the grid structure and landscape-level context (Habit Type, Matrix Type) support spatial comparisons of species detection/density across habitats and matrices.
- Seasonal replicates enable temporal analyses (dry vs. wet seasons) of detection patterns.
- Be aware of coordinate rounding limits precision at fine scales, particularly when mapping rare species.