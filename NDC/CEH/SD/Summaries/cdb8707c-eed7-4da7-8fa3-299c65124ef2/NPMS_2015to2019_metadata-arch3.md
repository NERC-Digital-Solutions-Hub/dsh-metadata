# The National Plant Monitoring Scheme (NPMS)

## Purpose and scope
- A habitat-based plant monitoring scheme designed by BSBI, CEH, Plantlife and JNCC.
- Aims to provide an annual indication of changes in plant abundance and diversity.
- Objectives:
  - Detect change in the quality of priority habitats.
  - Understand drivers and pressures causing change.
  - Contribute data for the UK Biodiversity Indicator 'C7 Plants of the wider countryside' by measuring changes in plant communities across key habitats.
- Method: engages volunteer plant recorders to monitor plants and habitat attributes in small plots selected across the UK, Isle of Man, and Channel Islands.
- Outputs: an annually updated dataset stored at CEH Wallingford, designed to be publicly accessible and suitable for policy and research use.

## Data and outputs
- Snapshot: NPMS database as of 2015–2019.
- Provided file suite and purpose:
  - locations_2015to2019.csv: unique location_id and location_type (plot type: square or linear).
  - sampleInfoWithLatLong_2015to2019.csv: sampling events with id, survey_id, date_start, location_id, entered_sref, entered_sref_system, created_on, created_by_id, LATITUDE, LONGITUDE, monad, monadCRS, country; links to locations_2015to2019.csv.
  - sampleAttributes_2015to2019.csv: additional sample data linked to samples via sample_id; includes caption and text_value describing attribute category and value.
  - occurrences_2015to2019.csv: species observations with id, sample_id, taxonversionkey, preferred_taxon, domin (Domin score), record_status, sensitivity_precision; includes verification via iRecord when applicable.
  - npmsHabitatLookup.csv: mapping between NPMS broad and fine-scale habitats.
  - dominScores.csv: harmonized Domin categories and mid-point interpretations for cross-scheme consistency.
- Data accessibility and quality:
  - Records include verification status (C, V, R) and sensitivity handling (blur to 10 km for sensitive records).
  - Data are designed for integration with GIS and statistical analysis; example R workflow is provided to access habitat information.

## Data collection and field protocols
- Field design:
  - Regular grid of square plots and gridlines for linear plots to ensure random sampling with respect to landscape.
  - Habitat definitions and target species lists developed and peer-reviewed; field recording involves volunteers with varying botanical expertise.
- Data collection and entry:
  - Online data capture with structured fields and a species dictionary; maps for locations; controlled terms for habitats and sample information.
  - Dates and geographical coordinates recorded; multiple sampling events per location.
- Quality assurance at collection:
  - Data input uses validation checks (geographic range checks; standardized fields).
  - Verification carried out via iRecord for botanical experts when needed.
- Data processing and analysis:
  - Analysis prepared by experienced quantitative ecologists using R; results disseminated via newsletters and peer-reviewed publications.

## Evidence Quality Assurance (EQA)
- Publications supporting EQA:
  - Journal articles (design and assessment of NPMS; models for interval-censored plant data; citizen science in ecological monitoring).
  - Additional articles and reports describing NPMS development, design choices, and implications.
- EQA framework and governance:
  - A project Steering Group oversees work; external peer review conducted for high-risk or critical components (e.g., survey design).
  - Uncertainty, quality, assumptions, and limitations are communicated through outputs reviewed by scientists; data and results are exposed to external scrutiny.
  - Robust statistical design used to manage bias and enable uncertainty estimation via models.
  - Document tracking and version control are maintained; design outputs are archived and backed up off-site; a Data Management Plan aligned with PRINCE2 governs processes and versioning.

## Data sharing, metadata and governance
- Data are publicly available to enable independent review and reuse.
- Metadata, field definitions, and data dictionaries accompany the data; cross-references between files allow reconstruction of habitat information and plant occurrences.
- Data provenance and governance are supported by explicit links between sample-level data, attributes, and occurrences; the system supports data transparency and reproducibility.

## Example: accessing NPMS habitat information
- A practical workflow is provided for combining sample records with habitat attributes:
  - Load sampleInfoWithLatLong_2015to2019.csv and sampleAttributes_2015to2019.csv
  - Filter sampleAttributes for NPMS Habitat
  - Merge with samples on the sample_id to obtain habitat information for each sample

## Considerations for monitoring framework authors
- Design choices that support policy relevance:
  - Structured, traceable workflow from field collection to public outputs.
  - Clear documentation of sampling design, habitat definitions, and target species criteria.
  - Public data release with validation mechanisms to ensure credibility and fitness for governance.
- Data governance and openness:
  - Data management plans, version control, and off-site backups improve reproducibility and accountability.
  - Data are openly shareable while respecting sensitive data restrictions and verification standards.
- Managing challenges (as per NPMS context):
  - Collaborative, multi-stakeholder development and peer review reduce risk of bias and improve methodological robustness.
  - Comprehensive QA processes balance openness with data integrity and reliability.
  - Ongoing evaluation of field recording quality and potential expansion of formal QA for field data collection in the future.

## Enduring value for policy and monitoring practice
- NPMS demonstrates a transparent, volunteer-based monitoring framework with rigorous QA, open data commitments, and governance structures suitable for informing policy and biodiversity indicators.
- The documented data architecture and QA approach offer a blueprint for other environmental monitoring programs seeking robust, transparent, and participatory data ecosystems.