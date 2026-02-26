# Introduction The National Plant Monitoring Scheme (NPMS) is a habitat-based plant monitoring scheme designed by BSBI, UK CEH, Plantlife and JNCC.

## Overview
- A volunteer-based plant monitoring program across the UK, Isle of Man and Channel Islands to track annual changes in plant abundance and habitat attributes.
- Aims to detect habitat quality changes, understand drivers/pressures, and contribute to the UK Biodiversity Indicator (C7 Plants of the wider countryside).
- Data are stored in the NPMS database at UKCEH Wallingford and released as an annually updated dataset.
- Field guidance and survey resources are available (Survey Guidance notes and related documents).

## Data files provided (structure and GIS relevance)
- locations_2015to2022.csv (177 kb)
  - Unique location_id and location_type (survey plot type; square or linear) to link to sampling events.
- sampleInfoWithLatLong_2015to2022.csv (3,206 kb)
  - Sample-level records: id, survey_id (type of NPMS survey), date_start, location_id, entered_sref and system, lat/long, monad and monadCRS, country, created_on, created_by_id.
  - Includes spatial context (lat/long, 1 km monad grid) for GIS mapping.
- sampleAttributes_2015to2022.csv (9,645 kb)
  - Attributes linked by sample_id (caption and text_value). Useful to extract habitat attributes (e.g., NPMS Habitat).
- occurrences_2015to2022.csv (16,796 kb)
  - Species observations per sample: id, sample_id, taxonversionkey, preferred_taxon, domin (Domin score), record_status (C = not reviewed, V = verified, R = rejected), sensitivity_precision (10000 = record is sensitive and blurred).
- npmsHabitatLookup.csv (2 kb)
  - Mapping between NPMS broad habitat and fine-scale habitat categories.
- dominScores.csv (1 kb)
  - Harmonised Domin score mappings and mid-point interpretations.
- Note: Example workflow provided for accessing habitat info by joining sampleInfoWithLatLong with sampleAttributes where caption = 'NPMS Habitat'.

## Spatial data and GIS considerations
- Spatial references and units
  - Coordinates include LATITUDE/LONGITUDE, monad (1 km square), and monadCRS (OSGB, OSIE, UTM30) with appropriate CRS identifiers.
- Location and sampling linkages
  - location_id links locations_2015to2022.csv to multiple sampling events in sampleInfoWithLatLong_2015to2022.csv.
- Data sensitivity and privacy
  - sensitivity_precision indicates records that are spatially blurred to 10 km if marked as sensitive (value 10000).
- Data quality and verification
  - Occurrence records have verification status (V = verified, C = not reviewed, R = rejected) and may be blurred for sensitive records.
- Temporal coverage
  - Data span 2015–2022, with ongoing annual updates.

## Accessing and integrating NPMS data
- Retrieve habitat information per sample by joining sampleInfoWithLatLong_2015to2022.csv with sampleAttributes_2015to2022.csv on sample_id and filtering caption = 'NPMS Habitat'.
- Example workflows
  - R: merge samples with habitat attributes to attach habitat information to each sample.
  - SQL: perform LEFT JOIN between sampleInfoWithLatLong_2015to2022 and sampleAttributes_2015to2022 with WHERE caption = 'NPMS Habitat'.
- Taxonomic and abundance data
  - Occurrences provide taxon information (preferred_taxon) and Domin abundance category (domin), enabling map-based visualization of plant communities.
- Habitat categorization
  - Use npmsHabitatLookup.csv to translate between broad and fine-scale habitat classifications for GIS thematic mapping.
- Data harmonisation
  - dominScores.csv provides a harmonised interpretation of Domin values across survey types (Wildflower, Indicator, Inventory).

## Evidence Quality Assurance (EQA) and governance
- EQA foundations and references
  - Publications supporting EQA: design and assessment of NPMS, citizen science ecological monitoring, and statistical treatment of interval-censored plant cover data.
  - Additional reports and technical reviews outlining NPMS design, data use, and methodological choices.
- QA process and risk management
  - Project overseen by a Steering Group; external peer review conducted where risk is higher.
  - Uncertainty and limitations are communicated in outputs; results are checked by scientists before publication.
- Data management and documentation
  - Robust documentation and version control; design work and outputs archived and backed up off-site per a UK CEH Data Management Plan using PRINCE2 standards.
  - Outputs (newsletters, reports) are designed for transparent communication of methods, uncertainty, and assumptions.
- Quality control questions (summary)
  - How methods and publications were peer reviewed and who was involved.
  - Appropriate review levels for different processes/outputs based on risk.
  - Clear communication of uncertainty, quality, and limitations.
  - Measures to avoid biases in statistics.
  - Document tracking and version control practices.

## Implications for GIS specialists
- Rich, GIS-ready spatial and attribute data for habitat mapping and change detection analyses.
- Ability to create map-based indicators of plant community changes across habitats and over time.
- Opportunities to integrate with broader habitat classifications and standardized Domin-based abundance metrics.
- Important data quality flags (verification status, sensitivity) to filter or annotate maps.
- Public availability of data with transparent QA processes and supporting methodological literature.

## Access and resources
- NPMS website for data access and documentation.
- Survey Guidance notes and additional survey resources available via NPMS content pages and links provided in the dataset description.