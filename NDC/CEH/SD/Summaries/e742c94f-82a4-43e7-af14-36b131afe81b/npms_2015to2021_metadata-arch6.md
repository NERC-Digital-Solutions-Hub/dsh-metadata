# National Plant Monitoring Scheme (NPMS)

- The NPMS is a habitat-based plant monitoring scheme designed by BSBI, UKCEH, Plantlife and JNCC to provide annual indications of changes in plant abundance and diversity.
- The dataset described provides a snapshot of the NPMS database held at UKCEH Wallingford and includes files that capture locations, samples, attributes, species occurrences, habitat mappings, and domin scores.
- The scheme uses volunteer recorders to monitor plants and habitat attributes across the UK, Isle of Man, and Channel Islands, with data managed and quality-assured through established processes.

## Objectives and scope

- Detect changes in the quality of priority habitats.
- Understand drivers and pressures behind observed changes.
- Contribute data for the UK Biodiversity Indicator 'C7 Plants of the wider countryside' by measuring changes in plant communities across important habitats.
- Data are periodically updated and publicly available for independent review.

## Provided data files (2015–2021)

- locations_2015to2021.csv: Unique location_id and location_type (plot type: square or linear).
- sampleInfoWithLatLong_2015to2021.csv: Sampling events with id, survey_id, date_start, location_id, spatial reference, created_on, created_by_id, lat/long, monad, monadCRS, country.
- sampleAttributes_2015to2021.csv: Additional attributes linked to samples (sample_attribute_id, sample_id, caption, text_value).
- occurrences_2015to2021.csv: Species occurrences with id, sample_id, taxonversionkey, preferred_taxon, domin (Domin score), record_status (C, V, R), sensitivity_precision.
- npmsHabitatLookup.csv: Mapping between NPMS broad habitats and fine-scale habitats.
- dominScores.csv: Harmonised Domin categories and mid-point values for abundance interpretation.

## Data relationships and how to use

- location_id in locations_2015to2021.csv links to sampleInfoWithLatLong_2015to2021.csv to relate sampling events to locations.
- sampleInfoWithLatLong_2015to2021.csv provides id (sample_id) and survey_id to identify the type of NPMS survey (wildflower, inventory, indicator).
- sampleAttributes_2015to2021.csv links via sample_id to provide contextual attributes (e.g., habitat information via captions like NPMS Habitat).
- occurrences_2015to2021.csv ties observations to samples (via sample_id) and provides taxon names, abundance (domin), and verification status.
- Spatial data include entered_sref and entered_sref_system (OSGB, OSIE, 4326), with monad and monadCRS describing 1 km squares and their coordinate systems.

## Practical example (data integration)

- To access habitat information for each sample, you can join sampleInfoWithLatLong_2015to2021.csv with sampleAttributes_2015to2021.csv on the sample_id field and filter for attributes where caption equals NPMS Habitat.
- The accompanying guidance demonstrates how to perform such a join in R or SQL to produce a combined dataset of samples with habitat attributes.

## Evidence Quality Assurance (EQA) and quality control

- EQA materials and methodologies are supported by multiple publications (journal articles, reports) detailing design, analysis, and validation of NPMS data.
- Key processes include:
  - Robust study design and sampling strategy (grid-based square plots and linear plots for habitat coverage).
  - Habitat definitions developed via peer review; target species lists reviewed for purpose and engagement.
  - Data input via online capture with a structured spatial database, using controlled vocabularies, calendars, and georeferenced locations.
  - Automated validation checks (geographic range) and iRecord verification for expert review when necessary.
  - Public data publishing with review by project scientists; analysis by experienced ecologists using R.
  - Dissemination through NPMS newsletters and peer-reviewed publications.
- Quality control questions (Q1–Q5) cover:
  - Peer review and stakeholder involvement in methods.
  - Appropriate review levels for different outputs based on risk.
  - Clear communication of uncertainty, quality, and limitations.
  - Bias avoidance through robust statistical design.
  - Document tracking and version control via data management plans and PRINCE2 standards.

## Data usage, access, and publication

- Outputs are intended to be publicly available to enable independent review and use by researchers, volunteers, policy-makers, and the public.
- The project employs a Data Management Plan and version control to ensure traceability and reproducibility.
- Analysis and reporting are carried out by a multidisciplinary team with expertise in botany, statistics, and science communication.

## Considerations for data users

- The dataset reflects volunteer-collected observations and may include uncertainties and variances typical of citizen science data.
- EQA materials and methodological references should be consulted to understand design choices, limitations, and interpretation of results.
- Uncertainty can be quantified through the models and methods described in the cited literature and project documentation.

## Accessing and further information

- Core NPMS resources and survey guidance documents are available through the NPMS website, including field recording guidance, species lists, and indicators.
- References and external publications provide additional context for methods, validation, and applications of NPMS data.