# Introduction

- The National Plant Monitoring Scheme (NPMS) is a habitat-based plant monitoring program in the UK designed by BSBI, UKCEH, Plantlife and JNCC to track annual changes in plant abundance and diversity.
- It supports volunteer recorders to monitor plants and habitat attributes in structured plots across the UK, Isle of Man, and Channel Islands.
- Primary objectives:
  - Detect change in the quality of priority habitats.
  - Understand drivers/pressures behind change.
  - Contribute data for the UK Biodiversity Indicator C7 by measuring plant community change in important habitats.
- The dataset described is an annually updated snapshot of the NPMS database held at UKCEH Wallingford, with accompanying evidence quality assurance (EQA) documentation and survey guidance for field operatives.

## Data Structure and Key Files (2015–2020)

- locationTypes_2015to2020.csv: links a unique location_id to the survey plot type (square or linear) and habitat type context.
- sampleInfoWithLatLong_2015to2020.csv: records sampling events at a location, including id, survey_id, date_start, location_id, spatial reference (entered_sref and entered_sref_system), creation metadata, recorder, and coordinates (LATITUDE, LONGITUDE), monad and monadCRS, and country.
- sampleAttributes_2015to2020.csv: additional sample-level attributes linked to samples (sample_attribute_id, sample_id, caption, text_value).
- occurrences_2015to2020.csv: species occurrences per sample, with id, sample_id, taxonversionkey, preferred_taxon, domin (Domin score), record_status (verification), and sensitivity_precision (blurring of sensitive records).
- npmsHabitatLookup.csv: mapping between NPMS broad and fine habitat categories.
- dominScores.csv: harmonises Domin scores across survey types (domin, dominIndex, midPoint).
- Example of how files relate: location_id links locationTypes to sampleInfoWithLatLong via location_id; sampleAttributes can provide habitat information for each sample; occurrences tie taxa to samples.

## Key Data Elements for Analysis

- Spatial data: latitude/longitude, monad (1 km grid) and monadCRS (OSGB, OSIE, UTM) for spatial analyses; country context.
- Temporal data: sample dates (date_start) and created_on timestamps; multiple samples per location (time series potential).
- Taxonomic data: taxonversionkey and preferred_taxon for species-level analyses; Domin scores capture cover-abundance.
- Data quality flags: record_status (C not reviewed, V verified, R rejected) and sensitivity_precision (records may be blurred if sensitive).
- Habitat context: NPMS habitat classifications (broad and fine) via npmsHabitatLookup.
- Data harmonisation: dominScores and related midPoints to support comparable abundance/cover across survey types.

## Accessing Habitat Information (Example)

- Practical approach to obtain habitat data for samples:
  - Load sampleInfoWithLatLong and sampleAttributes; filter sampleAttributes where caption equals NPMS Habitat; merge on sample_id to attach habitat attributes to samples.
- This enables self-serve data exploration and dashboarding for habitat-focused analyses.

## Evidence Quality Assurance (EQA) and Governance

- EQA is supported by a body of publications and internal guidance, aligning data use with quality standards.
- Design and oversight:
  - Project Steering Group provides governance; external peer review used where risk requires it (e.g., survey design workshops).
  - Habitat definitions and target species list developed with expert review; field recording designed for volunteer participation with multiple contribution levels and training.
  - Data input/verification includes structured online capture, a species dictionary, date standardisation, map-based locations, controlled vocabularies, automated range checks, and iRecord verification for expert review.
- Data publication:
  - NPMS data are publicly available for independent review and reuse.
  - Analysis conducted by experienced ecologists using R; dissemination via NPMS newsletters and peer-reviewed publications.
- Documentation and version control:
  - All design outputs tracked and archived; project data management plan and PRINCE2 standards guide version control and off-site backups.

## Outputs, Reuse and Data Products

- The NPMS dataset is designed to enable end users to self-serve analyses, dashboards, or reports to monitor habitat change and plant community dynamics.
- Outputs are intended to be transparent about uncertainty and limitations, with QA checks ensuring claims are evidence-based.
- Outputs are disseminated through newsletters and peer-reviewed outlets, promoting broad access and external critique.

## Uncertainties, Biases and Limitations

- Data quality and coverage challenges:
  - Patchy data availability and varying survey types across locations and years.
  - Differences in data formats and systems requiring harmonisation.
  - Potential biases in field recording and sampling design, though mitigated by robust statistical design and verification processes.
  - Sensitive records may be blurred in spatial data (sensitivity_precision), limiting precise geolocation for some observations.
- Communication of uncertainty:
  - Outputs are reviewed by scientists to ensure claims are supported; formal uncertainty quantification is incorporated via modelling where appropriate.

## Practical Considerations for Data Support

- Opportunities for building data products:
  - Combine NPMS habitat data with other datasets to support policy, conservation planning, or public-facing dashboards.
  - Create self-serve dashboards showing habitat change over time by location, habitat type, or survey type.
  - Provide guidance on data access patterns, joins (e.g., location_id and sample_id relationships), and best practices for summarising Domin scores.
- Data stewardship and support:
  - Emphasise clear data dictionaries, robust version control, and accessible documentation.
  - Be prepared to facilitate SQL or R-based integrations and provide example queries or workflows similar to the habitat-access example.

## Q&A Summary (Q1–Q5)

- Q1: How were methods and outputs peer-reviewed?
  - Design and outputs benefited from expert workshops, collaboration with statisticians and habitat specialists, and project team reviews; external peer review used when necessary.
- Q2: How is quality assurance level determined for processes/outputs?
  - Managed by a project Steering Group with risk-based external peer reviews; critical design elements (e.g., survey design) involved expert input.
- Q3: How are uncertainty, quality, assumptions, and limitations communicated?
  - Claims are checked by scientists; data and outputs are openly shared and subject to external scrutiny; uncertainty is considered in analyses.
- Q4: How are biases avoided in statistics and outputs?
  - Robust statistical design and modelling are used to account for uncertainty and minimise bias.
- Q5: Is there proper document tracking and version control?
  - Yes: outputs are versioned, archived, backed up off-site per the Data Management Plan; PRINCE2 governs project management and documentation.