# National Plant Monitoring Scheme (NPMS)

## Overview and aims
- A habitat-based plant monitoring scheme designed by BSBI, CEH, Plantlife and JNCC to collect data annually on changes in plant abundance and diversity.
- Supports volunteer plant recorders to monitor plants and habitat attributes across fixed plots (square or linear) in 28 fine NPMS habitats (11 broad categories) across the UK, Isle of Man, and Channel Islands.
- Objectives:
  - Detect change in the quality of priority habitats.
  - Understand drivers/pressures behind change.
  - Contribute data to the UK Biodiversity Indicator C7 (Plants of the wider countryside).
- Data and outputs are housed in an annually updated dataset held at CEH Wallingford; data are intended to be publicly available for independent review.

## Data structure and files
- locations_2015to2018.csv: unique location_id and location_type (square or linear); links to sampling events.
- sampleInfo_2015to2018.csv: sampling events with id, survey_id (87 Wildflower, 154 Inventory, 155 Indicator, 281 Extra species), date_start, location_id, spatial reference (entered_sref and entered_sref_system), created_on, created_by_id; recorder identities are anonymized publicly.
- sampleAttributes_2015to2018.csv: additional data about samples linked via sample_id; includes category, text_value.
- occurrences_2015to2018.csv: species observations linked to samples; fields include id, sample_id, taxonversionkey, preferred_taxon, domin (Domin scale), record_status (C/V/R), sensitivity_precision.
- npmsHabitatLookup.csv: mapping between NPMS broad habitats and fine-scale habitats.
- Evidence Quality Assurance (EQA) documentation and publications underpinning data quality, including peer-reviewed papers and internal reports; data publishing and access are supported by an explicit QA framework.

## How NPMS works (survey design and data collection)
- Habitats and sampling
  - 28 fine NPMS habitats organized into 11 broad categories; species lists tailored to habitat type.
  - Three survey levels: Wildflower, Indicator, and Inventory (higher levels record more species; Inventory includes all vascular plants).
- Plot layout and sampling
  - Minimum of 5 plots per kilometre square: typically 3 square plots (5x5 m; woodland plots are 10x10 m) and 2 linear plots (1x25 m).
  - Plots should be in different NPMS habitats where possible; pre-selected plot locations provided but flexibility exists to accommodate accessibility and safety.
  - Arable margins, road verges, hedgerows, standing waters, ponds, springs, etc., have specific sampling guidelines to ensure consistency and relocatability.
- Plot relocation and documentation
  - Emphasis on relocatability: sketches, photos, GPS when available; mark permanent features to aid future relocation.
  - For each plot, record position, orientation, and key features to enable future revisit.
- Data capture and submission
  - Data entered online at NPMS website; non-digital submission via posted forms is available.
  - Online data entry uses a species dictionary and controlled terms; dates and locations are standardized; iRecord verification used for higher-level identifications.
- Plot selection and flexibility
  - Protocol A (self-selected plots) allows placement in representative areas of habitat, avoiding obvious hotspots to prevent bias.
  - If fewer than 3 accessible pre-selected plots within an NPMS habitat, alternative strategies are allowed (e.g., include a flush, locate new plots, or increase linear plots).

## Recording methodology and data quality
- Domin scale and abundance
  - Record species presence and estimate relative abundance using the Domin percent cover scale; different plot sizes translate to percentage coverage (e.g., 1x1 m area for 10x10 m plots equals 1%).
  - Record bare ground, litter, bare rock/gravel, and moss/lichen coverage.
- Optional and ancillary data
  - Vegetation height classes, woodedness, aspect, slope, and management practices are optional but encouraged to aid interpretation.
  - Management descriptors include grazing intensity and activities like mowing, coppicing, hedge-cutting, etc.
- Verification and QA
  - Data input checks include geographic range checks; iRecord verification for expert-level records.
  - Outputs and claims are reviewed by scientists; uncertainties are addressed through statistical modeling and transparent communication.
  - Data management follows a documented Data Management Plan with off-site backups and version control (PRINCE2 framework); project Steering Group oversees work with occasional external peer review.

## Data access, governance, and stewardship
- Access and rights
  - NPMS data are intended to be publicly available; responsible access and use guided by national access codes (England/Wales, Scotland, Northern Ireland) and landowner considerations.
  - Recoding and privacy: recorder identities are represented by unique IDs; public dissemination does not reveal individual identities.
- Roles and governance
  - Project overseen by a Steering Group; external expert input is used when risk warrants it.
  - Documentation and outputs are version-controlled; design and output tracking are maintained via a Data Management Plan.
- Data publishing and dissemination
  - Results will be published in newsletters and peer-reviewed outputs; data are released publicly to enable independent validation and reuse.

## Health, safety, and access considerations
- Participants are responsible for personal safety; assess weather and site risk; avoid unsafe plots (e.g., cliff edges, unstable slopes).
- Use a buddy system, carry a mobile phone where possible, and bring a first-aid kit and appropriate clothing.
- Access constraints vary by jurisdiction; local guidance and landowner permissions are provided to volunteers.

## Appendix: Habitat types and Domin scale
- 28 fine NPMS habitats organized into 11 broad categories; guidance to select fine-scale habitats when possible; broad categories used when fine classification is uncertain.
- Domin scale provides a standardized method for estimating percent cover and counts; guidance covers how to translate coverage to 1–10 scale across different plot sizes (5x5 m, 10x10 m, 1x25 m).
- Example habitats include: Arable field margins; Bog and wet heath; Broadleaved woodland; Coast habitats; Freshwater habitats; Heathland; Lowland grassland; Marsh and Fen; Native pinewood and juniper scrub; Rock outcrops; Upland grassland; and more.

## Implications for data leadership and strategy
- End-to-end data lifecycle: from field data collection (standardized plots and species lists) to centralized spatial database and public data release; strong QA and verification workflows ensure data reliability.
- Standardization and discoverability: consistent use of habitat classifications, Domin scale, taxon keys, and geospatial references supports cross-site comparability and integration with other datasets.
- Governance and risk management: formal QA, external review, version control, and a steering structure mitigate risk and ensure ongoing data quality and transparency.
- Open data and use in policy: annual NPMS snapshots feed biodiversity indicators and inform government and policy discussions; clear documentation supports reuse by researchers, practitioners, and decision-makers.
- Practical considerations: acknowledges data gaps and biases (e.g., accessibility, safety constraints, habitat representativeness) and provides protocols to mitigate and document these issues.