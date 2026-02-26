# BirdSpecies.csv

## Overview
- Bird survey data from 441 sample locations in the Atlantic Forest of Brazil, collected as part of the ECOFOR project under the NERC HumanModified Tropical Forest programme.
- Four temporal replicates per point collected between December 2015 and February 2017.
- Data designed to support analyses of biodiversity and ecosystem functioning in degraded and recovering forests.

## Sampling design
- 441 sampling points across Vale do Paraíba and Serra do Mar, São Paulo, Brazil.
- Points arranged on a nine-point regular grid with 75 m spacing, spanning 49 landscapes.
- 15 landscapes are controls with a single predominant land-use type (native forest, Eucalyptus plantation, or pasture), split equally among the three types.
- 34 landscapes are native forest fragments embedded within other land-use types.
- Fragmented landscapes: three points in native forest fragment, three at fragment edge, three in surrounding matrix.
- Two matrix types surveyed: pasture border and plantation border; additional controls include CF (control forest landscape), CP (control pasture landscape), CE (control plantation landscape).
- Fragmented landscapes chosen to represent a range of patch sizes and connectivity.

## Data collection techniques
- Point count surveys: 15 minutes per sample, recording all bird species detected within a 25 m radius.
- Four temporal replicates per point, distributed across dry and wet seasons.

## Data structure
- Data stored in a single CSV file (BirdSpecies.csv).
- Each row corresponds to a single sampling point.

## Columns (key fields)
- Species names (columns 1–267): counts of temporal replicates per species, using BirdLife International taxonomy (BirdLife International 2017).
- LandscapeID: numeric reference to the landscape containing the sampling point.
- HabitatType: I = native forest interior, E = native forest edge, M = matrix; control landscapes indicate transect aggregation.
- MatrixType: P = pasture, E = plantation, CF = control forest landscape, CP = control pasture landscape, CE = control plantation landscape.
- X, Y: coordinates in SAD 1969 UTM 23S; rounded to the nearest kilometre to protect rare/threatened species locations.

## References
- BirdLife International. 2017. Handbook of the Birds of the World and BirdLife International digital checklist of the birds of the world. Version 9.1. Available at: http://datazone.birdlife.org/species/taxonomy

## Potential analyses for data-driven insights
- Compare species richness and community composition across habitatTypes (interior vs edge vs matrix) and MatrixTypes (pasture vs plantation) to assess fragmentation and land-use effects.
- Assess species-specific responses to landscape context and fragment connectivity.
- Explore seasonal (dry vs wet) effects on detections using the four temporal replicates.
- Build predictive models of species detectability and occupancy across landscapes with varying patch sizes and connectivity.
- Integrate with spatial metadata (LandscapeID, coordinates) to map biodiversity patterns and identify hotspots or at-risk habitats.