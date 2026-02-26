# Metadata for datasets available from Chaplow et al. (2015): Chaplow, J.S., Beresford, N.A., Barnett, C.L. (2015). Post Chernobyl surveys of radiocaesium in soil, vegetation, wildlife and fungi in Great Britain. NERC Environmental Information Data Centre. http://doi.org/10.5285/d0a6a8bf-68f0-4935-8b434e597c3bf251

## Overview
- Purpose: Metadata and dataset descriptors for post-Chernobyl radiocaesium surveys in Great Britain.
- Datasets cover radiocaesium (Cs-134 and Cs-137) in soil, vegetation, wildlife, and fungi.
- Timeframe and scope: GB-wide surveys conducted from 1986 through 1997 (with multiple years in some datasets).
- Data format and provenance: Five CSV datasets prepared by CEH/ITE; linked to CEH codes, site names, and sampling metadata.
- Access: Data described and archived in the NERC Environmental Information Data Centre (with a DOI).

## Datasets Included
- 1_Post_Chernobyl_survey_data_radiocaesium_in_soil_vegetation_wildlife_1986_and_1987.csv
  - Survey of Chernobyl fallout in graminaceous vegetation across GB; sampling in May–June 1986, October 1986, spring 1987.
  - Includes samples of soil, vegetation types, and wildlife.
- 2_Post_Chernobyl_survey_data_radiocaesium_in_vegetation_1986_1987_1988.csv
  - Radiocaesium in vegetation at sites in Cumbria (1986), north Wales (1987), north Yorkshire (1988).
- 3_Post_Chernobyl_survey_data_radiocaesium_in_soil_and_vegetation_1989_and_1990.csv
  - Soil and vegetation surveys at three Cumbria sites (1989/1990).
- 4_Post_Chernobyl_survey_data_radiocaesium_in_soil_and_vegetation_1992.csv
  - Soil and vegetation results over grazing areas of three upland sheep flocks in Cumbria (1992).
- 5_Post_Chernobyl_survey_data radiocaesium in fungi 1994 to 1997.csv
  - Fungi and associated soil sampled across GB (autumn 1994–spring 1997).

## Materials and Methods (Data Generation)

- Vegetation sampling
  - Graminaceous vegetation clipped from 1 m^2 plots to 1 cm of soil; samples oven-dried (85°C, 24 h), weighed, ground, and prepared for analysis.
- Soil sampling
  - 20 x 20 x 15 cm plots; litter layer separated; horizons noted; soil stored cold; pH measured; texture classified; soil sieved; <2 mm fraction gamma analyzed.
- Wildlife sampling
  - Species include rabbit, hare, fox, red deer, woodcock, grouse; tissue and gastrointestinal contents collected to assess uptake.
- Gamma analysis
  - High-resolution gamma spectroscopy with Ge detectors (20–25% efficiency; 25k–80k s counting times).
  - Calibration with British Calibration Service standards; decay correction to sampling date; QA with international standards.
- Measurements and units
  - Radiocaesium expressed as activity concentrations (Bq/kg dry matter or fresh weight) and deposition (Bq/m^2).
  - Cs-134 and Cs-137 reported for soil, vegetation, and animal/gut contents; additional metrics include 0–4 cm soil layers, whole soil deposits, and vegetation deposits.
- Data notes
  - Some fields include qualifiers (e.g., MDA, n/a); internal sample and site codes (CEH/ITE) linked to project IDs.
  - Metadata includes sampling dates, locations (latitude/longitude), habitat type, and sample_type (e.g., grass, bracken, fungi, animal species).

## Data Schema and Key Variables

- Core identifiers and location
  - CEH_code_Site_name, CEH_Code_Farm, CEH_code_Sample_number, Site_name, Location, Latitude, Longitude, Sampling_date_yyyymmdd.
- Biological and sample characteristics
  - Sample_type (vegetation, grass, heather, fungi, etc.), Habitat (Open ground/Woodland), Age_of_wildlife (A = adult, C = calf), Sex, Species_name.
- Soil and environmental context
  - Soil_classification, Soil_pH, Soil_texture (Clay, Silt, Sand, Loam, Organic; various combinations), LOI (loss on ignition), Upper/Lower_bulk_density, Bulk_density_kgm3 (and per m^2), Depth_lower_soil, Depth_upper_soil_layer, Soil_bulk_density_0-4cm, Soil_depth_cm, Peat.
- Radiocaesium measurements
  - Cs134_bqkg_DM_lower, Cs134_bqkg_DM_upper, Cs134_bqkg_DM_veg, Cs134_bqkg_dry_gut_contents, Cs137_bqkg_DM_lower, Cs137_bqkg_DM_upper, Cs137_bqkg_DM_veg, Cs137_bqkg_dry_gut_contents, Cs134_0-4cm_soil_bqkg, Cs137_0-4cm_soil_bqkg, Cs134_Deposit_Bqm2, Cs137_Deposit_Bqm2, Cs134_Veg_Bqm2, Cs137_Veg_Bqm2, Cs137_in_below_4cm_soil_m, Cs134_in_below_4cm_soil_m, etc.
- Other analytical descriptors
  - K40_bqkg_DM_lower, K40_bqkg_DM_upper, LOI_upper_soil_layer, NaNH4, NH4, PH, Location_details, Replicate_number, Replicate_info, Replicate notes.
- Data quality and provenance fields
  - CEH_code_Sample_ID, Project_ID, Note fields, n/a/MDA indicators, method_instrument, Local QA references.

## Data Quality, Provenance, and Access

- Provenance
  - Datasets produced by CEH and ITE; referenced with CEH/ITE project identifiers and site codes.
- Methods and QA
  - Standardized field and lab protocols; calibration against international standards; decay corrections to sampling date; QA via Ge detectors and well-documented instrument configurations.
- Data availability and citation
  - Archived in the NERC Environmental Information Data Centre; DOI and dataset descriptions provided in metadata.
- Data completeness and caveats
  - Some fields contain qualifiers (e.g., not applicable, not analysed, MDA); some samples recorded as “No sample” or “Not analysed”; variability across sites and years; potential gaps due to sampling scope or missing layers.

## Considerations for Data Leaders

- Integration and harmonization
  - Large, multi-entity dataset with consistent site and sample identifiers but diverse matrices (soil, vegetation, wildlife, fungi) and years; requires careful harmonization of units, depth conventions, and metabolite naming.
- Metadata richness
  - Rich data dictionary supports downstream analyses but necessitates robust data governance to preserve mappings between CEH/ITE codes, site metadata, and sample records.
- Data quality and lineage
  - Strong QA/QA steps (calibration, decay correction, standard references) enable reliable cross-dataset comparisons but attention needed for MDA flags and incomplete fields.
- Access and governance
  - Data-centre hosting (NERC EIDC) provides discoverability; ensure proper citation and preservation of internal IDs, sampling dates, and instrument details for reproducibility.
- Practical actions
  - Align with organisational needs for a data system that supports cross-domain radiation exposure analyses; consider adopting standardized metadata schemas and cross-referencing with contemporary datasets to maintain interoperability.