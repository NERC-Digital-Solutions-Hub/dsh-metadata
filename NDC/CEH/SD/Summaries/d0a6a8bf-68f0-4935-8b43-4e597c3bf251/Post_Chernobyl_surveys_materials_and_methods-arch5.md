# Metadata for datasets available from Chaplow et al. (2015): Chaplow, J.S., Beresford, N.A., Barnett, C.L. (2015). Post Chernobyl surveys of radiocaesium in soil, vegetation, wildlife and fungi in Great Britain. NERC Environmental Information Data Centre. http://doi.org/10.5285/d0a6a8bf-68f0-4935-8b434e597c3bf251

## Overview
- Compilation of datasets resulting from post-Chernobyl radiocaesium surveys across Great Britain.
- Datasets cover radiocaesium in soil, vegetation (graminaceous), wildlife, and fungi.
- Data originate from five CSV files describing different sampling periods and components.
- Data are stored at the NERC Environmental Information Data Centre (EIDC) and associated with CEH/ITE metadata and project codes.

## Datasets included
- 1_Post_Chernobyl_survey_data_radiocaesium_in_soil_vegetation_wildlife_1986_and_1987.csv
  - Surveys of Chernobyl fallout in graminaceous vegetation across GB; sampling in 1986 (May–June; October) and spring 1987; includes soil, vegetation, and wildlife samples.
- 2_Post_Chernobyl_survey_data_radiocaesium_in_vegetation_1986_1987_1988.csv
  - Radiocaesium in vegetation from Cumbria (1986), north Wales (1987), and north Yorkshire (1988).
- 3_Post_Chernobyl_survey_data_radiocaesium_in_soil_and_vegetation_1989_and_1990.csv
  - Soil and vegetation sampling at three sites in Cumbria (1989/1990).
- 4_Post_Chernobyl_survey_data_radiocaesium_in_soil_and_vegetation_1992.csv
  - Soil and vegetation results from three upland sheep-flock grazing areas in Cumbria (1992).
- 5_Post_Chernobyl_survey_data radiocaesium in fungi 1994 to 1997.csv
  - Fungi and associated soil sampled across GB (autumn 1994–spring 1997).

## Data collection and processing
- Sample types and targets
  - Vegetation: grassy/graminaceous plants (including sedges and rushes); sampling prioritized plants important in grazing.
  - Wildlife: various species (rabbit, hare, fox, red deer, woodcock, grouse); includes samples of ingested food (rumen, stomach, crop contents) and tissues (flesh, GI contents).
  - Soil: soil layers (lower and upper), litter layers, and horizons where present.
  - Fungi: fungal species with corresponding soil contexts.
- Sampling and handling
  - Sites selected away from roadsides and overhanging vegetation to reduce contamination biases.
  - Samples weighed, frozen, thawed before gamma analysis.
  - Vegetation: clipped from 1 m2 plots, oven-dried, ground, and weighed into sample containers.
  - Soils: collected as 20 x 20 x 15 cm blocks; litter separated; cores divided by horizon when present.
- Laboratory analysis
  - Gamma spectrometry using high-purity Ge detectors (Ge or Ge-Li) with 20–25% relative efficiency; acquisition times ranging from 25k to 80k seconds.
  - Detectors calibrated with British Calibration Service standards; accuracy checked against international standards.
  - Analyte suite includes Cs-134, Cs-137 (primary radiocaesium targets), K-40, Pu-238/239/240, Ru-103/Ru-106, among others.
- Units and corrections
  - Primary units: Bq/kg dry weight (Bq/kg DM) for tissues/soil; Bq/m2 for deposits.
  - All results decay-corrected to the sampling date.
- Metadata and structure
  - Extensive accompanying metadata fields for site, sampling date, habitat, soil characteristics (pH, texture, LOI), bulk density, depth, and sampling details.
  - Variables include LEADING fields such as CEH_Code, Site_name, Sample_nu mber, ITE_Land_Classification, Latitude, Longitude, Location, Restriction_status, Habitat, Sampling_date_yyyymmdd, Soil_classification, Soil_pH, Soil_texture_lower/upper, Upper_bulk_density, etc.
  - Radiocaesium and related measurements organized with specific column naming conventions (e.g., Cs134_bqkg_DM_lower soil, Cs137_bqkg_veg, Cs137_Deposit_Bqm2), plus related soil/vegetation biomass metrics (Dry matter, Fresh weight, LOI, etc.).
- Data quality cues
  - Some entries use MDA thresholds or “n/a” indicators.
  - Notes fields indicate samples not analysed or not present; some column headers reflect typographical/formatting artifacts from archival sources.

## Data schema and fields (highlights)
- Core measurements
  - 134Cs and 137Cs activity concentrations in soil (top and below 4 cm), vegetation, and dry/fresh tissue; deposition per square metre; bulk density; soil depth.
  - Additional radionuclides included in the dataset (e.g., K-40, Pu isotopes, Ru isotopes) with corresponding activity concentrations.
- Sample and site metadata
  - CEH/ITE identifiers, site codes, site names, location coordinates, latitude/longitude, sampling date, habitat type, land classification, and restriction status.
- Soil and vegetation context
  - Soil classification (e.g., clay/silt/sand/organic/loam, as per Avery 1980), pH, LOI, texture, bulk densities (mineral and organic layers), peat content, and organic/mineral layer distinctions.
  - Vegetation metrics including dry matter mass, fresh weight, and habitat associations.
- Data provenance and project references
  - Data tied to CEH/ITE projects and site codes; dataset compilation documented in Chaplow et al. (2015) with ripcording to NERC EIDC.

## Provenance, access, and reuse
- Source: Chaplow et al. (2015) post-Chernobyl radiocaesium surveys; datasets curated for public access via the NERC Environmental Information Data Centre (EIDC).
- Data stewardship
  - Original sample IDs, site codes, project IDs, and cataloging fields preserved to support traceability and reproducibility.
  - Metadata-intensive dataset intended to support distribution analyses, uptake studies in wildlife and ecosystems, and environmental radiological risk assessments.

## Quality, limitations, and standardization considerations
- Notes on data quality
  - Presence of non-analysed samples and missing values (e.g., MDA entries, n/a fields) requiring careful handling during reuse.
  - Some metadata fields may reflect archival transcription with occasional formatting inconsistencies; users should cross-check with Chaplow et al. 2015 documentation where possible.
- Standardization needs for reuse
  - Harmonization of units (e.g., Bq/kg DM vs. Bq/kg wet weight) and depths across datasets.
  - Alignment of location identifiers, soil classifications, and habitat terminology with current ontologies and schemas.
  - Clear data dictionary and field-level definitions to facilitate integration with contemporary data platforms.

## Stewardship considerations for reuse
- Actions for data stewards
  - Create or update a concise data dictionary linking column names to definitions, units, and calculation methods (e.g., decay correction references).
  - Normalize units and document conversion rules (e.g., DM definitions, moisture corrections).
  - Map site and soil classifications to current standards; document any deviations or historical conventions (e.g., Avery 1980 soil typology).
  - Ensure coordinate reference system is explicit (decimal degrees) and preserve sampling date formats (YYYY-MM-DD) for temporal analyses.
  - Maintain provenance: link each data slice to its original CSV file and to Chaplow et al. (2015) narrative for methodological context.
  - Flag and document missing data and non-analysed entries to support transparent data quality assessment.
  - Consider retention of legacy column order for traceability, while providing a modern data view that is easier to query.