# National Plant Monitoring Scheme survey data (2015-2017)

## Overview and Aims
- A habitat-based plant monitoring scheme (NPMS) designed by BSBI, CEH, Plantlife, and JNCC to provide an annual indication of changes in plant abundance and diversity.
- Supports volunteer plant recorders to monitor plants and habitat attributes using fixed plots (square or linear) across the UK, Isle of Man, and Channel Islands.
- Objectives: detect change in priority habitats, understand drivers/pressures behind change, and contribute data to the UK Biodiversity Indicator C7 (plants of the wider countryside).
- Data produced are annually updated and intended for public reporting and independent review.

## Data Architecture and Files
- Four main CSV files (2015–2017) with relational links:
  - locations_2015to2017.csv: unique location_id and location_type; links to sampling events.
  - sampleInfo_2015to2017.csv: sampling events per location_id; includes survey_id, date_start, entered_sref, created_on, created_by_id.
  - sampleAttributes_2015to2017.csv: additional attributes per sample (linked by sample_id).
  - occurrences_2015to2017.csv: species occurrences linked to samples (sample_ID); includes taxonversionkey, preferred_taxon, domin (cover), record_status, sensitivity_precision.
- Key relationships:
  - location_id ties locations to sampling events (sampleInfo).
  - sample_id ties sampleAttributes to samples in sampleInfo.
  - taxondata in occurrences uses NBN taxon keys and accepted names; some records may be sensitive (blurred coordinates).
- Public data access and recorder identities: recorder name information is anonymised; unique recorder IDs are used.

## Data Collection, Metadata, and Submission
- Field structure:
  - Plots: square plots (5x5 m; woodland 10x10 m) and linear plots (1x25 m). Post-2015 design supports relocation and repeat sampling.
  - Habitat coverage: 28 fine NPMS habitats (grouped into 11 broad NPMS categories); species lists tailored to habitat type.
  - Sampling events: multiple samples per location; survey_id indicates type (87 Wildflower, 154 Inventory, 155 Indicator, 281 Extra species).
  - Spatial references: entered_sref and entered_sref_system specify grid references (OSGB, Irish Grid, WGS84).
  - Tracking: created_on and created_by_id identify data creation; plots are intended to be relocatable via sketches, photos, and maps.
- Data submission:
  - Primarily online via npms.org.uk; options to mail paper forms if online submission is not possible.
  - Support contact: support@npms.org.uk.

## Sampling Design and Habitat Classification
- Habitat framework:
  - 28 fine NPMS habitats, aggregated into 11 broad categories; use fine habitat lists when possible, otherwise use broad category lists.
  - Appendix 1 provides detailed definitions for each habitat category (e.g., Arable field margins, Bog and wet heath, Broadleaved woodland, Coast, Fresh water, Heathland, Lowland grassland, Marsh and Fen, Native pinewood and juniper scrub, Rock outcrops, Upland grassland).
- Plot layout and placement:
  - Square plots: 5x5 m (10x10 m in woodlands); priority is placement within pre-selected plot locations aligned to NPMS habitat.
  - Linear plots: 1x25 m to sample linear habitats (e.g., hedgerows, field margins, riversides); may start at feature intersections with gridlines.
  - Protocol A: self-selected plots allowed when pre-selected locations are inaccessible; emphasis on representative habitat, relocation clarity, and avoiding biased “hotspots.”
- Plot relocation and re-drawing:
  - Detailed guidance (Table 2) on sketch maps, compass directions, photographs, and permanent features to aid future relocation.

## Recording in Plots: Methods and Domin Scale
- Recording process:
  - Use habitat-appropriate species lists; search plots intensively to record all present species.
  - Abundance is recorded as percent cover using the Domin scale (1–10) with explicit guidance on interpreting 1% cover, clumps, and multi-square coverage.
  - Optional extra data: vegetation height classes, woodedness, aspect, slope, management signs (grazing, cutting, etc.), with definitions and intensity levels.
- Data components per plot:
  - Species presence and percent cover (Domin scale).
  - Bare ground, litter, bare rock/gravel, and moss/lichen cover percentages.
  - Optional attributes: vegetation height, woodedness, aspect, slope, and management indicators.
- Special habitat notes:
  - Aquatic and riparian plots recorded from banks; water-body plots include marginal and submergent vegetation; avoid deep water.
  - Special instructions for ponds, springs, flushes, and montane habitats (safety-focused plotting in some cases).

## Data Quality Assurance and Governance
- Evidence Quality Assurance (EQA) framework:
  - EQA is supported by peer-reviewed papers, internal project reports, and a data management plan.
  - Data input uses structured online forms, a species dictionary, calendar date entry, map-based locations, and controlled terms; automated geographic range checks are applied.
  - Verification via iRecord (BSBI-affiliated experts) for higher-level taxonomic checks; data will be publicly available for independent review.
- QA process details:
  - Project governance via a Steering Group; external peer review for high-risk outputs.
  - Uncertainty and bias handling through robust statistical design and modeling; uncertainty estimations to be reported with outputs.
  - Versioning, document tracking, and off-site backups per CEH Data Management Plan and PRINCE2 standards.
- Reporting and outputs:
  - Results will be disseminated via NPMS newsletters and peer-reviewed publications; outputs reviewed by scientists to ensure claims are evidence-based.

## Access, Rights, Health, and Safety
- Access and rights:
  - Guidance aligns with UK-wide access codes (England/Wales: Countryside Code; Scotland: Outdoor Access Code; Northern Ireland guidance).
  - Landowner introductions available via downloadable NPMS letters; sampling on private land requires permission.
- Health and safety:
  - Surveyors responsible for their own safety; guidance to assess weather, risk factors (e.g., cliffs, water bodies), and to work in pairs when possible.
  - Mandatory safety precautions: mobile phone, first-aid kit, appropriate clothing/footwear; contingency planning for inaccessible plots.

## Data Lifecycle, Usage, and Outputs
- Data lifecycle:
  - Data collected across multiple years with emphasis on repeat visits to plots to monitor habitat change.
  - If a plot shifts habitat type over time, continue using the appropriate habitat list for recording; if a plot falls outside NPMS, continue surveying as long as possible.
- Outputs and dissemination:
  - Data published publicly; analysis conducted by quantitative ecologists using R scripts.
  - Annual reporting and dissemination through newsletters and peer-reviewed journals.
- What to do with data:
  - Enter data online at npms.org.uk after registering; if online submission is not possible, post forms to NPMS Volunteer Coordinator, Plantlife.

##Appendix and Habitat Details
- Appendix 1 enumerates the 28 fine NPMS habitats and 11 broad categories with detailed definitions and typical species associations.
- Domin Scale: guidance on translating cover percentages to Domin scores (1–10) and practical examples for 10x10 m and 5x5 m plots.