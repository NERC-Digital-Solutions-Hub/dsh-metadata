# BirdSpecies.csv

## Data overview
- BirdSpecies.csv contains bird survey data from 441 sample locations in the Atlantic Forest of Brazil, with four surveys per location conducted between December 2015 and February 2017.
- Part of the ECOFOR project (Biodiversity and Ecosystem Functioning in Degraded and Recovering Amazonian and Atlantic Forests) under the NERC HumanModified Tropical Forest programme.

## Sampling design
- 441 sampling points across Vale do Paraíba and Serra do Mar, São Paulo, Brazil.
- Evenly spread across 49 landscapes using a nine-point regular grid with 75 m spacing (where possible).
- 15 landscapes designated as controls, with native forest, Eucalyptus plantation, and pasture types; 34 landscapes contain native forest fragments embedded within other land uses.
- Fragmented landscapes: three points in native forest fragments, three at the fragment edge, and three in the surrounding matrix per landscape.
- Two matrix types surveyed: 15 fragments bordering plantation and 19 fragments bordering pasture.
- Fragmented landscapes chosen to represent a range of patch sizes and connectivity.

## Data collection techniques
- Bird surveys conducted as 15-minute point counts, recording all bird species within a 25 m radius.
- Four temporal replicates between December 2015 and February 2017, with replicates evenly split between dry and wet seasons.

## Data structure
- Data stored in a single CSV file (BirdSpecies.csv); each row represents an individual sampling point.

## Column headings
- Species columns (1–267): species identities following BirdLife International taxonomy; values indicate the number of temporal replicates in which the species was detected.
- LandscapeID: numerical reference to the landscape containing the sample point.
- HabitatType: I = native forest interior, E = native forest edge, M = matrix (points within control landscapes aggregated into transects).
- MatrixType: P = pasture, E = plantation, CF = control forest landscape, CP = control pasture landscape, CE = control plantation landscape.
- X and Y: coordinates in SAD 1969 UTM 23S; values rounded to the nearest kilometre to protect locations of rare/threatened species.

## References
- BirdLife International. 2017. Handbook of the Birds of the World and BirdLife International digital checklist of the birds of the world. Version 9.1.