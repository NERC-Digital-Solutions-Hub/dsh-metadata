# National Plant Monitoring Scheme

- A habitat-based plant monitoring program designed by BSBI, CEH, Plantlife and JNCC to provide an annual indication of changes in plant abundance and diversity.
- Supports volunteer plant recorders to monitor plants and habitat attributes in small plots chosen via a structured UK-wide methodology (including Isle of Man and Channel Islands).
- Objectives:
  - Detect changes in the quality of priority habitats.
  - Understand why changes occur (pressures and drivers).
  - Contribute data to the UK Biodiversity Indicator “C7 Plants of the wider countryside” by measuring changes in plant communities across key habitats.
- The dataset is updated annually and stored at CEH Wallingford, with ongoing reference to survey guidance and related resources.

## Data collection framework and scope

- Plots are selected on a regular grid for square plots and a gridline approach for linear plots to ensure randomization with respect to the landscape.
- Survey types include Wildflower surveys, Inventory surveys, and Indicator surveys (example codes: 87, 154, 155).
- Volunteers collect data on plant communities and habitat attributes at multiple time points at each location.
- Data coverage (2015–2019) underpin a public-facing, time-series dataset used to assess habitat condition and drivers of change.

## Data files and structure (2015–2019)

- locations_2015to2019.csv: unique location_id and location_type (plot type: square or linear); links to sampling events.
- sampleInfoWithLatLong_2015to2019.csv: sample_id, survey_id, date_start, location_id, spatial references, created_on, created_by_id, LAT/LONG, monad, monadCRS, country.
- sampleAttributes_2015to2019.csv: sample_attribute_id, sample_id, caption, text_value (e.g., habitat attributes).
- occurrences_2015to2019.csv: occurrence_id, sample_id, taxonversionkey, preferred_taxon, domin (Domin score), record_status (C/V/R), sensitivity_precision (blurred records).
- npmsHabitatLookup.csv: mapping between NPMS broad and fine-scale habitats.
- dominScores.csv: harmonized Domin category mappings and midpoint values for cover-abundance interpretation.
- These files enable linking locations to samples, habitats, and species observations with quality indicators and spatial context.

## Data access and examples of use

- Example workflow (R): merge sampleInfoWithLatLong with sampleAttributes filtered for NPMS Habitat to obtain habitat information per sample.
- Data are designed for public sharing to allow independent review of results and methods, with clear provenance and metadata.

## Evidence Quality Assurance (EQA) and governance

- EQA framework supported by peer-reviewed publications and internal reports.
- Key design elements validated via expert workshops:
  - Sample stratification and survey design (grid-based plots; random with respect to landscape).
  - Habitat definitions peer-reviewed by habitat experts.
  - Target species list selected to minimize bias and maintain volunteer engagement.
- Field recording relies on volunteers with varying botanical expertise; three participation levels and comprehensive guidance/training.
- Data input includes: species dictionary, date calendars, map-based locations, controlled terms; automated geographic checks; verification via iRecord for expert review.
- Data analysis performed by experienced ecologists using R; results published in newsletters and peer-reviewed outlets.
- Reporting and dissemination managed by a project team with botany, statistics, and communication expertise.

## Quality assurance, review, and documentation (Q1–Q5)

- Q1: Partnership oversight via a Steering Group; external peer review where risk warrants; design workshops used to inform methods.
- Q2: Risk-based QA with external review when needed; emphasis on robust survey design.
- Q3: Uncertainty, quality, and assumptions are clearly communicated; outputs are reviewed to ensure evidence support.
- Q4: Bias avoidance through robust statistical design and transparent uncertainty modeling.
- Q5: Version control and documentation tracked under a CEH Data Management Plan and PRINCE2 practices; designs and outputs archived and backed up off-site.

## Operational implications for analysts

- Provides a standardized, auditable pipeline from field collection to data products and public outputs.
- Facilitates monitoring of environmental health and policy performance through consistent time-series data across habitats.
- Enables combination with other data sources to enhance dataset value while maintaining data provenance and quality.
- Ensures transparency and reproducibility via public data access, explicit QA procedures, and versioned documentation.

## Resources and further information

- Survey guidance and supporting documents available on the NPMS website.
- References include design, validation, and occupancy/abundance modeling work relevant to NPMS data and interpretation.