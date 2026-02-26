# pasture fed livestock farms across Great Britain, 2019

## Overview
- Dataset from a UK Centre of Ecology & Hydrology project funded by BBSRC to evidence how pasture-fed livestock practices affect grassland parameters (sward composition and soil qualities).
- Covers grazing landscapes across Britain conceptualized into four Broad Habitat grassland types; highlights the Pasture Fed Livestock Association (PFLA) certification standards and their relevance to biodiversity, animal and soil health.
- Focuses on practices such as mob grazing and, to a lesser extent, herbal leys, using data from 17 PFLA farms collected in 2019 (second year of sampling).

## Data Collection and Content

- Study design
  - 17 farms across Great Britain, members of PFLA; 10 fully certified and 7 with near-term certification plans.
  - Farms sampled May–September 2019; paired-field sampling where possible to compare mob-grazed vs set-stocked fields or fields under species-rich vs traditional leys.
  - Anonymised farm and field identifiers to protect landowner confidentiality.
- Data collected
  - Vegetation: species presence, cover (percent), flowering status, vegetation height, wormcasts, soil surface indicators; biomass samples for dry weight by plant group (grass, dicot, cereal).
  - Soils: 3-depth soil sampling with a W-shaped transect (0–5 cm, 5–15 cm, 15–30 cm) plus a soil core per field; bulked samples across the field; soil chemistry and physical properties.
  - Farm management: on-site interview data regarding sward longevity, grazing type and intensity, inputs, and specific field management practices via a dedicated questionnaire.
  - Data structure: 7 CSV data tables (see Data Structure) with anonymised farm/field references.
  - Additional data: data-derived soil DNA (eDNA) sub-samples submitted to European Nucleotide Archive under PRJEB46195.
- Data structure (7 CSV tables)
  - SEEGSLIP_PLOTS_2019.csv: plot-level vegetation attributes and plot metadata.
  - SEEGSLIP_SPECIES_2019.csv: species-level vegetation data per plot (plant names, cover, flowering, etc.).
  - SEEGSLIP_BIOMASS_2019.csv: dried biomass weights by plant group (grass, dicot, cereal) per field/plot.
  - SEEGSLIP_SOIL_2019.csv: soil chemistry and physical properties by depth and field (pH, conductivity, moisture, LOI, bulk density, textures, carbon/nitrogen, phosphorus, Olsen P, CaCO3, totals, etc.).
  - SEEGSLIP_FARMDATA_2019.csv: farm- and field-level management data (grazing type, stocking, rest periods, fertiliser use, costs, etc.).
  - SEEGSLIP_FIELDS_2019.csv: field-level management characteristics (control vs managed, field size, shade, rest practices, etc.).
  - SEEGSLIP_STOCK_2019.csv: stocking information (supplementary feeding, bale practices, livestock types).
- Anonymisation
  - Farms anonymised with IDs; landowner confidentiality preserved.

## Methods, Quality Assurance, and Provenance

- Laboratory and analytical methods
  - Soil analyses aligned with Countryside Survey (CS) protocols and UK CEH SOPs (SOC, TOTC/TOTN, LOI, pH, Olsen P, CaCO3, conductivity, moisture, bulk density, particle size, aggregate stability).
  - Loss-on-ignition (LOI) measurements with quality control using internal standards; repeat if QC criteria exceeded.
  - SOC and total nitrogen measured with inorganic carbon removal, using elemental analysis (VarioEL).
  - Total phosphorus and Olsen P measured via colorimetric and flow-injection techniques with standard QC (duplicates, blanks, matrix-matched references).
  - pH measured in water and CaCl2 suspensions with internal standard QC.
  - Electrical conductivity measured on field-moist soil suspensions with QC.
  - Bulk density and particle size distribution derived using standard methods (laser diffraction with calibration standards; cross-checks with sand standards).
  - Aggregate stability tested with wet sieving and NaOH treatment to derive stability metric.
- Data quality controls
  - Multiple internal QC standards per batch; duplicates and cross-checks across batches; calibration against standards; instrument-specific QC procedures.
  - eDNA sub-samples processed and deposited with ENA; data traceability to primary samples.
- Provenance and references
  - Data produced by CEH within the CS framework; references provided for laboratory methods (Emmett et al., Bunce et al., Gee & Or, Lebron et al., Stace, etc.).
  - Further reading includes studies on soil microbiomes, mob grazing, and related management implications.

## Data Access and Reuse

- Data availability
  - CSV data tables described above (SEEGSLIP_2019 series) with field- and farm-level anonymisation.
  - eDNA sequences deposited in European Nucleotide Archive under accession PRJEB46195.
- Documentation and metadata
  - Table-level and field-level descriptions provided within the data descriptor, including variable definitions, units, and data types for each CSV.
  - Explicit notes on field sampling design (paired-field comparisons) and the year of data collection (2019).
- Reuse considerations
  - Suitable for research on pasture-based livestock systems, soil-plant-microbial interactions, and farm management practices.
  - Data can be integrated with other grassland or soil datasets, subject to anonymisation and metadata alignment.
  - Users should cite the original dataset and related publications; consider cross-referencing with the listed methodological references.

## Governance, Stewardship, and Stewardship Considerations for Data Stewards

- Data governance alignment
  - Anonymised farm identifiers and ethical handling of field data align with responsible data stewardship.
  - Comprehensive metadata and explicit data structure documentation support discoverability and reuse by data users.
- Standards and interoperability
  - Use of established CS soil methods and clear variable definitions facilitates interoperability with other soil/grassland datasets.
  - The presence of detailed QC procedures and instrument calibration records supports data quality assessments.
- Data lifecycle and maintenance
  - Clear data structure enables integration with future datasets (e.g., additional years or related projects).
  - Potential for updates or expansion (e.g., additional fields, longitudinal follow-up) while maintaining consistent schema.
- Challenges to address
  - Ensuring timeliness and completeness of metadata across all tables; maintaining consistent units and coding across future releases.
  - Handling heterogeneity inherent in field-based ecological data (e.g., missing values, field-level variations).
- Privacy and data licensing
  - Anonymisation safeguards owner confidentiality; licensing terms should be clarified in the metadata for downstream users.

## Summary of Key Points for Data Stewards

- The dataset provides a richly detailed, anonymised, year-specific snapshot (2019) of pasture-fed livestock farms across Britain, including vegetation, soil properties, and farm management data, with eDNA supplementary data.
- It uses robust, QC-backed methodologies aligned with established soil and ecosystem assessment protocols, enabling high-quality data curation and potential cross-study integration.
- The data are organized into seven well-documented CSV tables, with clear variable definitions, units, and provenance notes to support discovery, validation, and reuse.
- Data stewardship opportunities include maintaining metadata quality, ensuring interoperability with similar datasets, and supporting future expansions or longitudinal studies while preserving anonymisation and data integrity.