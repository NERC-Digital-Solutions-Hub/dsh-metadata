# Flowering Species Metadata

- This document provides metadata to accompany the table Table_flowering_species.csv, detailing imagery, ground-truth data, and plant characteristics used for GIS analyses and map-based visualisations.

## Columns and Meaning

- Date of image acquisition: Date the imagery was acquired for each month at both 3 cm and 7 cm resolutions.
- Dates gathered ground-truth location data: Date range during which ground-truth data for margin species were collected, including location data for individual floral units and floral unit measurements (refer to Floral_unit_data.csv).
- Location: Indicates whether the data pertain to margin or hedgerow species.
- Flowering plant species (common name): Includes both the Latin name and common name; used as a classification category within training sets.
- Nectar sucrose secretion rate (µg): Nectar sucrose secretion rate per floral unit per day (µg). Calculated as the mean nectar sucrose per flower from Baude et al. (2015a) multiplied by the mean number of flowers per floral unit from Baude et al. (2015b). A floral 'unit' is defined per Carvell et al. (2007) as any flower or stem with multiple flowers that a bee can walk between (not fly).

## Data provenance and references

- Baude, M., Kunin, W.E. and Memmott, J. (2015a). Nectar sugar values of common British plant species [AgriLand]. NERC Environmental Information Data Centre. DOI: 10.5285/69402002-16764de9-a04e-d17e827db93c.
- Baude, M., Kunin, W.E., Memmott, J. (2015b). Flower density values of common British plant species [AgriLand]. NERC Environmental Information Data Centre. DOI: 10.5285/6c6d3844-e95a-4f84a12e-65be4731e934.
- Carvell, C., Meek, W.R., Pywell, R.F., Goulson, D. and Nowakowski, M. (2007). Comparing the efficacy of agri-environment schemes to enhance bumble bee abundance and diversity on arable field margins. Journal of Applied Ecology, 44(1), 29-40. DOI: 10.1111/j.1365-2664.2006.01249.x.

## GIS use and data integration

- Data can be joined with Floral_unit_data.csv to align margin/hedgerow species with observed floral units.
- Temporal alignment: use Date of image acquisition and ground-truth date ranges to synchronize imagery with field measurements.
- Spatial considerations: classify features as margin or hedgerow as indicated in Location.
- Classification and mapping: use Flowering plant species (common name) as categorical attributes for choropleth or symbol-based maps.
- Quantitative attribute: Nectar sucrose secretion rate (µg) can be mapped as a per-unit numeric layer or aggregated to floral units or plant species.

## Calculations and definitions

- Nectar secretion rate is derived from published values (Baude et al. 2015a,b) and scaled by the mean number of flowers per floral unit (Baude et al. 2015b).
- Floral unit definition follows Carvell et al. (2007): a unit comprises flowers/stems with multiple flowers that a bee can traverse on foot.

## Data quality and considerations

- Data are sourced from multiple references and may require harmonisation during integration.
- Ground-truth data are linked via Floral_unit_data.csv, so ensure consistent identifiers when combining datasets.
- Be aware of resolution differences (3 cm vs 7 cm imagery) when analysing spatial features.