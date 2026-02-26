# Habitat samples dataset

- Purpose and scope
  - NPMS is a habitat-based plant monitoring scheme in the UK, Isle of Man, and Channel Islands designed to track changes in plant abundance and diversity annually.
  - Objectives include detecting changes in priority habitats, understanding drivers, and contributing to the UK Biodiversity Indicator for plants in the wider countryside.
  - The dataset consolidates NPMS samples with recorded surveyor habitat, adding NPMS habitat classifications and change indicators to support training and validation of Earth Observation–based products.

- Data content and structure
  - Core file: npmsHabitatSamples_2015to2022.csv (approximately 4287 kb).
  - Each row represents a plant community sample at a fixed plot over time, linked via sample_id and survey_id.
  - Key fields and concepts:
    - Spatial and temporal: entered_sref, entered_sref_system (OSGB, Irish Grid, WGS84), LATITUDE, LONGITUDE, monad (1 km square), monadCRS.
    - Plot and survey identifiers: sample_id, survey_id, created_on, created_by_id (anonymized recorder IDs).
    - Habitat information: surveyorHabitat (fine or broad NPMS habitat), NPMS_hab_type (fine/broad), NPMS_broad_habitat, multipleHabs (change or not between samples).
    - Metadata and provenance: country, entered_sref System, recorder identifiers, and data entry timestamps.
  - Dataset is pre-joined with habitat classifications and includes changes in surveyed habitats over time for each plot location.
  - Designed to support training and validation of Earth Observation–based data products.

- Metadata, standards and data quality controls
  - Habitat classification and recording follow NPMS guidelines; surveyors may provide fine- or broad-scale habitat assignments.
  - Data capture uses a structured spatial database with:
    - Species dictionary, calendarized dates, map-based locations, and controlled terms for habitats and sample attributes (e.g., vegetation height, cover values).
  - Automated data quality checks (geographic range checks); validation through the BSBI–affiliated iRecord system for expert review of exceptional records.
  - Documentation and guidance available on the NPMS website; explicit attention to unit and coordinate reference system consistency (OSGB, Irish Grid, WGS84).
  - Evidence Quality Assurance (EQA) references underpin data quality, with supporting publications listed (journal articles, reports). EQA considerations address design, uncertainty, bias avoidance, and review processes.

- Governance, review and risk management
  - Oversight by a project Steering Group; external peer review used when risk warrants it (e.g., survey design workshop).
  - Uncertainty and limitations are communicated in outputs (newsletters, reports) and checked by scientists to ensure claims are evidence-based.
  - Document tracking and version control aligned with a UK CEH Data Management Plan; backups off-site; adherence to PRINCE2 project management standards.
  - Outputs and analyses are conducted by experienced quantitative ecologists; results disseminated via NPMS newsletters and peer-reviewed publications.

- Access, publication and usage
  - Data from the NPMS is intended to be publicly available to enable independent review of results.
  - Data products (datasets, indicators, and analyses) are designed to be transparent, with clear communication of uncertainties, assumptions, and limitations.
  - Training materials, field guides, and surveyor resources support consistent data collection and interpretation.

- Practical implications for Data Stewards
  - Ensure alignment of dataset with overarching NPMS governance, metadata standards, and versioning.
  - Maintain data dictionaries and controlled vocabularies (habitat types, monitoring codes) to support interoperability.
  - Monitor data timeliness and completeness from volunteer inputs; implement processes to chase up data where needed.
  - Manage data sharing while preserving provenance and enabling public access with appropriate documentation of limitations.
  - Continuously integrate quality assurance findings (EQA publications, review outcomes) into data management practices.
  - Preserve traceability through robust data management plans, off-site backups, and documented revisions.