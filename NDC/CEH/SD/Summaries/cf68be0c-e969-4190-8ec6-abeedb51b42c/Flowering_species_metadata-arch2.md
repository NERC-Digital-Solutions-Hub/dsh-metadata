# Flowering Species Metadata

## Overview
- Metadata accompanying the Table_flowering_species.csv file.
- Enables standardized tracking of flowering species for environmental monitoring, supporting assessment of pollinator resources and habitat diversity over time.
- Includes margin or hedgerow species and data linked to ground-truth observations.

## Spreadsheet columns and meanings
- Date of image acquisition: Dates images were captured each month at both 3 cm and 7 cm resolutions.
- Dates gathered ground-truth location data: Date range for ground-truth data collection for margin species; location data for individual floral units and floral unit measurements (see Floral_unit_data.csv).
- Location: Indicates whether the species is a margin or hedgerow species.
- Flowering plant species (common name): Both the Latin name and common name of each flowering plant species of interest; these are included as classification categories in training sets.
- Nectar sucrose secretion rate (µg): Nectar sugar secretion rate per floral unit per day (µg). Calculated as the mean nectar sugar per flower (Baude et al. 2015a) multiplied by the mean number of flowers per floral unit (Baude et al. 2015b). The term floral unit follows Carvell et al. (2007) and defines one unit as any flower or stem with multiple flowers that a bee can walk between (not fly).

## Nectar secretion rate calculation and floral unit definition
- Calculation: mean nectar sugar per flower × mean number of flowers per floral unit.
- Floral unit definition: per Carvell et al. (2007), a unit is a flower or stem with multiple flowers accessible to a bee by walking.

## Ground-truth data and imagery context
- Ground-truth data dates tie to margin species locations and measurements, with linkage to additional data in Floral_unit_data.csv.
- Imagery resolutions (3 cm and 7 cm) indicate the granularity at which images were acquired for temporal analysis.

## Classification and training context
- The species entries (Latin and common names) are intended for use as classification categories within training datasets, supporting standardized species recognition and downstream analyses.

## References
- Baude, M., Kunin, W.E. and Memmott, J. (2015a). Nectar sugar values of common British plant species [AgriLand]. NERC Environmental Information Data Centre. DOI: 10.5285/69402002-16764de9-a04e-d17e827db93c.
- Baude, M., Kunin, W.E., Memmott, J. (2015b). Flower density values of common British plant species [AgriLand]. NERC Environmental Information Data Centre. DOI: 10.5285/6c6d3844-e95a-4f84a12e-65be4731e934.
- Carvell, C., Meek, W.R., Pywell, R.F., Goulson, D. and Nowakowski, M. (2007). Comparing the efficacy of agri-environment schemes to enhance bumble bee abundance and diversity on arable field margins. Journal of Applied Ecology, 44(1), 29-40. DOI: 10.1111/j.1365-2664.2006.01249.x.