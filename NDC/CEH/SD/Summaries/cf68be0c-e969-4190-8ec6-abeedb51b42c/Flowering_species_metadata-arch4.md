# Flowering Species Metadata

## Purpose
- Metadata accompanying the Table_flowering_species.csv file, outlining the data structure and definitions for key ecological and classification variables.

## Columns and Meanings
- Date of image acquisition: Dates when imagery was acquired each month at both 3 cm and 7 cm resolutions.
- Dates gathered ground-truth location data: Date range during which ground-truth location data for margin species were collected (location data for individual floral units and floral unit measurements; references Floral_unit_data.csv).
- Location: Indicates whether the species is a margin or hedgerow species.
- Flowering plant species (common name): Includes both the Latin name and common name of each flowering plant species; these are used as classification categories within classification training sets.
- Nectar sucrose secretion rate (µg): Nectar sucrose secretion rate per floral unit per day (in micrograms). Calculated as the mean nectar sugar per flower from Baude et al. (2015a) multiplied by the mean number of flowers per floral unit from Baude et al. (2015b). The term floral 'unit' follows Carvell et al. (2007), where a unit is any flower or stem with multiple flowers that a bee can walk to (not fly between).

## Data provenance and references
- Baude, M., Kunin, W.E. and Memmott, J. (2015a). 'Nectar sugar values of common British plant species [AgriLand]'. NERC Environmental Information Data Centre. DOI: 10.5285/69402002-16764de9-a04e-d17e827db93c.
- Baude, M., Kunin, W.E., Memmott, J. (2015b). 'Flower density values of common British plant species [AgriLand]'. NERC Environmental Information Data Centre. DOI: 10.5285/6c6d3844-e95a-4f84a12e-65be4731e934.
- Carvell, C., Meek, W.R., Pywell, R.F., Goulson, D. and Nowakowski, M. (2007). 'Comparing the efficacy of agri-environment schemes to enhance bumble bee abundance and diversity on arable field margins', Journal of Applied Ecology, 44(1), 29-40. DOI: 10.1111/j.1365-2664.2006.01249.x.

## Implications for data governance and quality
- Enables traceability and reproducibility through explicit definitions, sources, and cross-references (e.g., ground-truth data and Floral_unit_data.csv).
- Supports discoverability of species classifications and ecological measurements for training data and analyses.
- Highlights data quality considerations such as granularity (ground-truth location data), consistency of taxonomy (Latin and common names), and reliance on external reference sources for nectar rates.
- Provides a clear linkage between image data, ground-truth location data, and ecological measurements for coherent data integration.

## Usage, interoperability, and workflow
- Designed to support classification training sets and ecological modelling by standardizing species identifiers and associated nectar metrics.
- Facilitates integration with related datasets (e.g., Floral_unit_data.csv) and image acquisition records to support end-to-end workflows from data collection to model development.
- Encourages transparent metadata practices to aid collaboration across research teams and data communities studying pollinator-plant interactions.