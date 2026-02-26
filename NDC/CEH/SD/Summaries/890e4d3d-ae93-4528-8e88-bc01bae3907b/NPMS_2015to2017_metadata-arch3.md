# National Plant Monitoring Scheme survey data (2015-2017)

## Overview and Aims
- NPMS is a habitat-based plant monitoring scheme designed to provide annual indications of changes in plant abundance and diversity.
- Partners: BSBI, CEH, JNCC, Plantlife.
- Objectives: detect change in priority habitats, understand drivers/pressures, contribute data for UK Biodiversity Indicators, and provide annual feedback to volunteers.
- Data are maintained in a centralized NPMS database at CEH Wallingford and are intended for public sharing and independent review.

## Data Structure and Files Provided
- locations_2015to2017.csv: unique location_id, location_type; links to sampling events via location_id.
- sampleInfo_2015to2017.csv: sampling events for each location_id; fields include id, survey_id (type of NPMS survey), date_start, entered_sref, created_on, created_by_id; recorder information is anonymized to unique IDs.
- sampleAttributes_2015to2017.csv: additional data linked to sample_id (from sampleInfo); includes attribute category and text_value.
- occurrences_2015to2017.csv: species occurrences recorded during sampling; fields include id, sample_ID, taxonversionkey, preferred_taxon, domin (domin scale), record_status (verification), sensitivity_precision (if blurred for privacy).
- key survey_id codes: 87 = Wildflower, 154 = Inventory, 155 = Indicator, 281 = Extra species.
- The dataset is curated to enable linking of occurrences to samples and locations, with verification through the iRecord system where applicable.

## Evidence Quality Assurance (EQA) and Governance
- EQA framework is supported by peer-reviewed publications and internal project reports; outputs are checked by scientists to ensure claims are evidence-based.
- Data governance includes a project Steering Group, external peer review as needed, and version control with archived report versions backed up off-site per CEH Data Management Plan and PRINCE2 standards.
- Data publishing: NPMS intends to publish data publicly to enable independent review; uncertainty and assumptions are disclosed in outputs.
- Data verification: online data capture uses a species dictionary, controlled terms, calendar dates, and geographic range checks; iRecord review provides subject-matter verification for certain records.
- Note: Formal quality assessment of field recording is not currently part of NPMS but is contemplated for the future.

## Survey Design and Methodology
- Habitat focus: 28 fine NPMS habitats grouped into 11 broad NPMS categories; target species are indicator taxa chosen to reflect habitat quality and tractability for volunteers.
- Grid-based sampling: plots are selected on a regular grid to ensure randomization with respect to landscapes; plots must remain within a single habitat type.
- Three survey levels to accommodate participant expertise:
  - Wildflower Level: fewer species recorded.
  - Indicator Level: all habitat-indicator species recorded (preferred for robustness).
  - Inventory Level: Indicator Level plus all other vascular plants recorded.
- Plot selection and relocation: emphasis on fixed plots to track change over years; relocation aids include sketches, photographs, GPS, and permanent features.

## Plot Layout and Field Protocol
- Square plots: 5x5 m (woodland plots are 10x10 m). Minimum of 3 square plots per kilometre square in different fine habitats; up to 5 plots recommended per square.
- Linear plots: 1x25 m, used for arable margins, waters, rock, scree, road verges, hedgerows; start at feature intersection with gridlines.
- Ponds and flushes: treated as linear plots; survey prioritizes accessibility.
- Pre-selected plot locations: provided to guide placement, but flexibility via Protocol A (self-selected plots) if necessary, ensuring plots are representative and relocatable.
- Plot placement considerations: avoid disturbance, use representative habitat areas, and ensure plots can be relocated in future years.

## Data Recording in Plots
- Recording process: use the relevant habitat-specific NPMS species lists; search plots thoroughly to record all observed species.
- Abundance scoring: percent cover estimated for each species using the Domin scale (1-10 for percent cover; 1-10 for abundance where applicable).
- Additional data (optional but recommended): vegetation height classes, woodedness, aspect, slope, and management signals (e.g., grazing, ditch clearance). Grazing intensity is categorized (high, moderate, low) with corresponding vegetation indicators.
- Recording form and media: use NPMS forms, sketch maps, and up to two photos per plot to aid relocation and interpretation; GPS coordinates can be used to improve accuracy.
- Data submission: online data entry through www.npms.org.uk; if online entry is not possible, forms can be mailed.

## Data Use, Access, and Responsibilities
- Data submission and access: data are intended to be publicly available for transparency and independent review; volunteers and landowners should be respected; safety and access rights vary by country (England/Wales, Scotland, Northern Ireland).
- Health and safety: contributors are responsible for their own safety; guidance includes weather checks, risk assessment, buddy systems, mobile phones, first aid, and suitable clothing.
- Withdrawals and multiple squares: participants may withdraw; plots may be reallocated; if surveying multiple squares, intervals are defined to ensure at least one square is surveyed each year.

## Appendix 1: Habitat Types and Domin Scale
- Habitat types: 11 broad NPMS categories with detailed descriptions and examples (e.g., Arable field margins; Bog and wet heath; Broadleaved woodland; Coast; Fresh water; Heathland; Lowland grassland; Marsh and Fen; Native pinewood and juniper scrub; Rock outcrops; Upland grassland).
- Domin Scale: detailed scoring system for percent cover and plant abundance (1-10) to standardize abundance estimates across plots and years.
- Guidance for plotting and data interpretation: specific instructions on how to handle complex habitats (e.g., flushes, montane communities) and how to score partial plots or irregular features.