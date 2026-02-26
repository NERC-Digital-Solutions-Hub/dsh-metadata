# Flowering Species Metadata

## Overview
- Metadata accompanying the Table_flowering_species.csv dataset.
- Captures temporal, spatial, taxonomic, and nectar-production details for margin/hedgerow plant species used in classification training and ecological analyses.

## Spreadsheet columns (key fields)
- Date of image acquisition: monthly imagery at two resolutions (3 cm and 7 cm).
- Dates gathered ground-truth location data: date range for when field location data for margin species were collected.
- Location: indicates whether the species is a margin or hedgerow plant.
- Flowering plant species (common name): includes both Latin name and common name; used as a classification category in training sets.
- Nectar sucrose secretion rate (µg): mean nectar sucrose secretion per floral unit per day.
  - Derived as: mean nectar per flower (Baude et al. 2015a) × mean number of flowers per floral unit (Baude et al. 2015b).
  - Floral unit definition (Carvell et al. 2007): any flower or stem with multiple flowers that a bee can walk between (not necessarily fly).

## Data sources and references
- Baude, M., Kunin, W.E., and Memmott, J. (2015a). Nectar sugar values of common British plant species [AgriLand]. NERC EIDC. DOI: 10.5285/69402002-16764de9-a04e-d17e827db93c.
- Baude, M., Kunin, W.E., Memmott, J. (2015b). Flower density values of common British plant species [AgriLand]. NERC EIDC. DOI: 10.5285/6c6d3844-e95a-4f84a12e-65be4731e934.
- Carvell, C., Meek, W.R., Pywell, R.F., Goulson, D. and Nowakowski, M. (2007). Comparing the efficacy of agri-environment schemes to enhance bumble bee abundance and diversity on arable field margins. Journal of Applied Ecology, 44(1), 29-40. DOI: 10.1111/j.1365-2664.2006.01249.x.

## Usage considerations for analysts
- Use image acquisition dates and ground-truth timing to align nectar data with field observations.
- Leverage the nectar secretion rate to estimate nectar provisioning per floral unit across sites and times, applying the Carvell (2007) floral unit definition.
- Ensure consistency between species names (common/Latin) used in classifications and those in nectar/value calculations.
- Reference the primary sources for any methodological details or unit interpretations.