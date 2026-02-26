# Flowering Species Metadata

## Overview
- Metadata document accompanying the Table_flowering_species.csv.
- Describes fields that capture imagery, ground-truth data, species identification, and nectar secretion rates for margin/hedgerow flowering plants.
- Links to related data: references to Floral_unit_data.csv for floral unit measurements.

## Data schema and key fields
- Date of image acquisition
  - Date acquired imagery for each month at both 3 cm and 7 cm resolutions.
- Dates gathered ground-truth location data
  - Date range for ground-truth data collection for margin species, i.e., location data for individual floral units and floral unit measurements (see Floral_unit_data.csv).
- Location
  - Indicates whether the specimen is a margin or hedgerow species.
- Flowering plant species (common name)
  - Includes both Latin (scientific) name and common name; used as a classification category within training sets.
- Nectar sucrose secretion rate (µg)
  - Per floral unit per day; calculated as the mean nectar sugar per flower (Baude et al. 2015a) multiplied by the mean number of flowers per floral unit (Baude et al. 2015b).
  - The term “floral unit” follows Carvell et al. (2007) definition: one unit equals a flower or stem with multiple flowers that a bee can walk between.

## Data provenance and references
- Baude, M., Kunin, W.E. and Memmott, J. (2015a). Nectar sugar values of common British plant species [AgriLand]. NERC EIDC. DOI: 10.5285/69402002-16764de9-a04e-d17e827db93c.
- Baude, M., Kunin, W.E., Memmott, J. (2015b). Flower density values of common British plant species [AgriLand]. NERC EIDC. DOI: 10.5285/6c6d3844-e95a-4f84a12e-65be4731e934.
- Carvell, C., Meek, W.R., Pywell, R.F., Goulson, D. and Nowakowski, M. (2007). Comparing the efficacy of agri-environment schemes to enhance bumble bee abundance and diversity on arable field margins. Journal of Applied Ecology, 44(1), 29-40. DOI: 10.1111/j.1365-2664.2006.01249.x.

## Data quality, governance, and stewardship considerations
- Standardization
  - Ensure consistent use of plant nomenclature (Latin and common names) and alignment with training set classifications.
- Metadata completeness
  - Validate that image acquisition dates, resolutions, and ground-truth date ranges are complete and match related datasets (e.g., Floral_unit_data.csv).
- Provenance and traceability
  - Maintain clear linkage to source publications for nectar and density values; preserve DOIs for auditability.
- Access and sharing
  - Assess any sharing restrictions tied to ground-truth location data or proprietary measurements; document data availability and embargoes if applicable.
- Interoperability
  - Align units and definitions (e.g., floral unit concept per Carvell 2007) to support cross-dataset integration.
- Update and maintenance
  - Establish a process to update nectar rate calculations and species classifications as new literature or measurements become available.

## Relevance to Data Stewards aims
- Supports readiness of datasets for discovery and reuse by ensuring metadata is comprehensive, standardized, and linked to related data (e.g., Floral_unit_data.csv).
- Documents data standards (taxonomy, measurement units, definitions), enabling accurate data sharing and governance across large datasets.
- Facilitates data provenance and traceability through explicit references and data field definitions.
- Identifies dependencies and potential sharing constraints to manage data availability and updates responsibly.

## Practical notes for implementation
- When uploading, ensure the Table_flowering_species.csv metadata is harmonized with the metadata of related files (e.g., Floral_unit_data.csv) for seamless discovery.
- Clearly record any deviations from standard definitions and cite sources (Carvell 2007; Baude et al. 2015a,b) to maintain data integrity.