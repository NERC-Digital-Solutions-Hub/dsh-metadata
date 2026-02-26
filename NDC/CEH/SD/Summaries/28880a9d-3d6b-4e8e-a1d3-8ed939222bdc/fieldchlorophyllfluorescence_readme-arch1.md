# Data collected on Mt Etna during the field transplant in 2017

## Overview of the experiment
- Five genotypes per species were randomly selected for each of two Senecio species (AE = S. aethnensis; CH = S. chrysanthemifolius).
- For each genotype, four cuttings were taken and measured at each transplant elevation.
- Four leaves per plant were measured.
- To account for weather and measurement time, the measurements were repeated on a second day.
- On each plant, light-response measurements were recorded after 30 minutes of dark adaptation using an IMAGING-PAM M-series chlorophyll fluorometer.

## Variables and data structure
- Species: AE (S. aethnensis) and CH (S. chrysanthemifolius)
- Genotype: genotype ID from individuals grown in the glasshouse; cuttings sourced from these
- TGSite: elevation of the transplant sites
- TGBlock: replicate experimental blocks in the field
- Grid: grid location of plants within each block; genotype randomized to different grid locations
- Day: day on which measurements were taken
- Fluorometer outputs: Columns 7–22; analysis focuses on PI(total), representing the total photosynthetic capacity

## Measurements and protocol
- Measurements: light response data collected after dark adaptation
- Quantity used for analysis: PI(total) from the fluorometer output (total photosynthetic capacity)

## Data considerations for analysis
- The design is hierarchical and factorial (species × genotype × elevation × block × grid), enabling mixed-effects modeling to assess species or genotype effects across elevations.
- Repeated measures on a second day provide a handle on temporal variation (weather/time of day) and enhance robustness.
- The dataset supports examining how PI(total) responds to transplant elevation within and between species and genotypes, accounting for block and grid-level random effects.