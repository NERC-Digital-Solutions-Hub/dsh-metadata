# The National Plant Monitoring Scheme (NPMS)

## Overview
- A habitat-based plant monitoring scheme in the UK, Isle of Man, and Channel Islands designed by BSBI, UKCEH, Plantlife, and JNCC.
- Aims to provide an annual indication of changes in plant abundance and diversity; supports volunteer recorders to monitor plants and habitat attributes in small plots using a structured methodology.
- Objectives:
  - Detect change in the quality of priority habitats.
  - Understand drivers/pressures behind change.
  - Contribute data for UK Biodiversity Indicator C7 by measuring plant community change across important habitats.
- The dataset is an annually updated snapshot of the NPMS database held at UKCEH Wallingford, with guidance and resources available on the NPMS site.

## Data structure and contents
- Core data files (2015–2021) and brief descriptions:
  - locations_2015to2021.csv: unique location_id and location_type (e.g., square or linear plots); links to sampling events via location_id.
  - sampleInfoWithLatLong_2015to2021.csv: per-sample information including id, survey_id (sample type), date_start, location_id, entered_sref and CRS, created_on/by, LATITUDE, LONGITUDE, monad and monadCRS, country.
  - sampleAttributes_2015to2021.csv: sample_attribute_id, sample_id, caption, text_value; supports linking attributes like habitat information to samples.
  - occurrences_2015to2021.csv: records of species occurrences with id, sample_id, taxonversionkey, preferred_taxon, domin (Domin score), record_status (C, V, R), sensitivity_precision (blur indication).
  - npmsHabitatLookup.csv: mapping between NPMS broad habitats and fine-scale habitats.
  - dominScores.csv: harmonized Domin scales; includes dominIndex and midPoint for cover-abundance categories.
- These files enable linking locations, samples, habitats, and species occurrences for GIS mapping and analyses.

## Accessing habitat information (example)
- To obtain habitat data for each sample, join sampleInfoWithLatLong_2015to2021.csv with sampleAttributes_2015to2021.csv where caption equals 'NPMS Habitat'. Example workflow provided in R and SQL.

## Data quality, evidence, and QA (EQA)
- EQA supported by a range of publications (journal articles, reports) and guidance materials.
- Key QA elements:
  - Design and review: sample stratification, grid/linear plot design, habitat definitions, and target species indicators developed with expert input; field recording designed for volunteer engagement.
  - Data input and verification: online capture with a species dictionary, date-calendar, map-based locations, controlled terms; automated checks; iRecord verification by botanical experts for certain records.
  - Transparency: data published publicly to allow independent review.
  - Analysis and reporting: conducted by experienced ecologists using R; dissemination via NPMS newsletters and peer-reviewed outlets.
- Uncertainty and bias handling:
  - Robust statistical design allows uncertainty to be modeled; outputs communicate uncertainty, limitations, and assumptions.
- Governance and version control:
  - Steering Group oversight; external peer review where necessary; data and design documents tracked and versioned under a Data Management Plan; backups follow PRINCE2 standards.

## Practical considerations for GIS use
- Spatial references and geography:
  - entered_sref and entered_sref_system indicate the coordinate reference system used for samples.
  - monad (1 km square) and monadCRS specify the spatial unit and its CRS (OSGB 27700, OSIE 29902, UTM30 32630).
  - country field clarifies territorial context (Britain, Channel Islands, Northern Ireland).
- Data harmonization and labeling:
  - Domin scores are harmonized via dominScores.csv to a consistent DominIndex for cross-survey comparability.
  - npmsHabitatLookup.csv provides a bridge between broad and fine habitat categories for mapping.
- Data quality indicators:
  - record_status shows verification state (C = not reviewed, V = verified, R = rejected).
  - sensitivity_precision flags records that are spatially blurred (e.g., 10000 indicates 10 km blur).

## Usage and publication
- Data are suitable for map-based visualization and public/peer review; can be analyzed in R or SQL with the provided relational links among location, sample, habitat, and occurrence data.
- Supports monitoring outputs and biodiversity indicators, such as UK Biodiversity Indicator C7.

## References and further resources
- NPMS survey guidance and related resources available via the NPMS website.
- Publications and reports documenting design, QA, analysis methods, and applications of NPMS data.