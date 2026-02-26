# Introduction

- The National Plant Monitoring Scheme (NPMS) is a habitat-based plant monitoring scheme designed by BSBI, UKCEH, Plantlife and JNCC to provide annual indicators of changes in plant abundance and diversity.
- Volunteers collect data on plants and habitat attributes in small plots across the UK, Isle of Man, and Channel Islands using a structured sampling approach.
- Objectives:
  - Detect change in the quality of priority habitats.
  - Understand drivers and pressures behind change.
  - Contribute data to the UK Biodiversity Indicator "C7 Plants of the wider countryside" by measuring plant community changes across important habitats.
- Data snapshot and documentation are maintained by the NPMS database at UKCEH Wallingford; field recording guidance and related resources are available via the NPMS website.

## NPMS data scope and structure

- The NPMS data are organized into several CSV files that interrelate to describe locations, samples, attributes, and species observations:
  - locationTypes_2015to2020.csv: links each sampling location_id to a location_type (survey plot type).
  - sampleInfoWithLatLong_2015to2020.csv: details for each sample (id), survey_id, date_start, location_id, spatial reference, created_on, created_by_id, latitude, longitude, monad, country, and related geographic metadata.
  - sampleAttributes_2015to2020.csv: additional attributes for samples (sample_attribute_id, sample_id, caption, text_value).
  - occurrences_2015to2020.csv: species occurrences with id, sample_id, taxonversionkey, preferred_taxon, domin (domin score), record_status (verification), sensitivity_precision (records may be blurred for sensitive taxa).
  - npmsHabitatLookup.csv: mapping between NPMS broad habitats and fine-scale habitats.
  - dominScores.csv: harmonized domin category and mapping to a unified dominIndex and midPoint for cover estimates.
- These files together enable reconstruction of where, when, and what plant communities were observed, plus habitat context and data quality controls.

## Accessing habitat information (example)

- Habitat information for samples can be obtained by joining sampleInfoWithLatLong_2015to2020.csv with sampleAttributes_2015to2020.csv on sample_id where caption equals 'NPMS Habitat' (example in R and SQL shown in the document).

## Evidence Quality Assurance (EQA) and governance

- EQA basis:
  - NPMS evidence quality is supported by listed journal articles, other publications, and technical/research reports.
  - Publications cover design, statistical methods for plant cover data, and monitoring scheme implementation.
  - Various reports document design development, data use, and methodological advances.
- Quality management questions (Q1–Q5) addressed in NPMS documentation:
  - Q1: Partnership governance, design and expert involvement; evidence-based survey design and field testing; diverse expertise in the project team.
  - Q2: Review level and risk-based QA; steering group oversight with external peer review as needed (e.g., survey design workshop).
  - Q3: Communication of uncertainty, quality, assumptions, and limitations; outputs reviewed by scientists and open to external feedback.
  - Q4: Bias avoidance via robust statistical design enabling uncertainty estimation in models.
  - Q5: Version control and document tracking; design work archived and backed up off-site under a Data Management Plan with PRINCE2 standards.
- Data publication and accessibility:
  - Data from NPMS are intended to be publicly available to allow independent review of results.
  - Analysis is performed by experienced ecologists; results disseminated through NPMS newsletters and peer-reviewed publications.

## Data collection, verification, and metadata

- Field recording relies on volunteers with varying botanical expertise, offering tiered participation and comprehensive guidance and training.
- Data input uses structured online capture with:
  - A species dictionary, calendar dates, map-based locations, controlled habitat terms, and standardized sample information (e.g., vegetation height, Domin scores).
  - Automated checks (e.g., geographic range) and a separate verification step via iRecord for expert review when needed.
- Analysis and reporting are conducted by a team with botany, statistics, and science communication expertise, ensuring alignment with project aims and audiences.