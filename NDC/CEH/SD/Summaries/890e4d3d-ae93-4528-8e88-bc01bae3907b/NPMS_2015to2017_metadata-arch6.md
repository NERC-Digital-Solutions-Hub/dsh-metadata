# National Plant Monitoring Scheme survey data (2015-2017)

## Purpose and scope
- A volunteer-based plant monitoring scheme designed to track changes in plant abundance and habitat condition across 28 fine NPMS habitats (11 broad categories) in the UK.
- Aims include detecting change in priority habitats, understanding drivers of change, and contributing to UK biodiversity indicators.
- Provides an annually updated snapshot of NPMS data held at CEH Wallingford and aims to publish data publicly for independent review.

## Files provided and what they contain
- locations_2015to2017.csv: location-level identifiers (location_id) and location type; links to sampling events.
- sampleInfo_2015to2017.csv: sampling-level records (id) with survey_id, date_start, location_id, entered_sref, created_on, created_by_id; ties samples to locations and recorders.
- sampleAttributes_2015to2017.csv: additional attributes about samples linked by sample_id; includes attribute category (caption) and text_value.
- occurrences_2015to2017.csv: species observations linked to samples via sample_id; includes taxon keys, preferred_taxon, domin (dominance/abundance), record_status (verification), and sensitivity_precision (for blurred records).
- Each file is designed to be joined via location_id, id (sample_id), and related keys; recorder names are anonymized to unique IDs.

## How the data are structured and linked
- Location layer: locations_2015to2017.csv defines unique locations and their plot type (square or linear) and links to samples via location_id.
- Sample layer: sampleInfo_2015to2017.csv contains individual sampling events per location, with timing, spatial reference, and creator.
- Attribute layer: sampleAttributes_2015to2017.csv provides descriptive attributes for each sample (via sample_id).
- Observation layer: occurrences_2015to2017.csv records species-level observations per sample, with taxonomic keys, abundance (domin), and verification status.
- Data quality: record_status indicates review status (C, V, R); sensitivity_precision flags spatially blurred records; automated checks and iRecord verification support data quality.

## Evidence quality assurance (EQA) and governance
- EQA is supported by:
  - Peer-reviewed publications and internal reports detailing NPMS design, monitoring approaches, and data handling.
  - A project Steering Group with external peer review as needed; design and risk assessments inform QA levels.
  - Data is published with uncertainty communication, supported by review teams and ongoing feedback from the wider monitoring science community.
  - Version control and archival of design outputs per CEH Data Management Plan; PRINCE2 project management standards.
- Outputs are checked by scientists to ensure claims are evidence-based; data may be shared for wider scientific scrutiny.

## How the survey works (field methodology)
- Habitat scope: 28 fine NPMS habitats, grouped into 11 broad categories; observers use fine or broad habitat lists to identify target species.
- Plot types:
  - Square plots: 5x5 m (woodlands 10x10 m); intended to be relocatable using sketches, GPS, and photographs.
  - Linear plots: 1x25 m, used for specific linear habitats (e.g., hedgerows, margins, streams); ponds/flushes surveyed as linear plots.
- Plot selection:
  - Prefer pre-selected plot locations aligned to habitat types; Protocol A allows self-selected plots in representative areas if needed.
  - At least 5 plots per kilometre square (3 square plots and 2 linear plots preferred); plots should be within a single habitat type.
  - If plots are unsafe or inaccessible, skip or substitute using guidelines (safety first).
- Recording levels:
  - Wildflower Level, Indicator Level, and Inventory Level, with guidance to progress to Indicator Level where possible.
- Data submission:
  - Data entered online at npms.org.uk; if online submission is not possible, forms can be posted.

## What to record in each plot
- Species presence: use the relevant NPMS species list for the habitat; record all species observed.
- Abundance: estimate percentage cover for each species using the Domin scale (percent cover semantics explained in the guidance).
- Additional information (optional but encouraged):
  - Vegetation height class and score
  - Woodedness (dense/ scattered/ hedgerow/ none)
  - Optional: aspect, slope, management (e.g., grazing, mowing, hedge management), and grazing intensity (high/ moderate/ low) with standardized categories.
- Plot relocation aids:
  - Sketch maps, compass direction, photographs (up to 2 per plot), and GPS coordinates to aid future re-location.

## Data recording and submission workflow
- Use a dedicated survey form per plot; one form can cover two visits if feasible.
- Online entry preferred for efficient data management; alternatively, post forms to NPMS Volunteer Coordinator.
- Ensure accurate location data (grid reference or GPS) and preserve relocation features for year-on-year comparisons.
- Photographs, sketches, and notes are valuable aids for future re-location and interpretation.

## Access, rights, and safety
- Surveying should respect land access rights and countryside codes; obtain permission where necessary.
- Health and safety emphasized; assess risks, survey with a buddy when possible, and avoid dangerous locations (steep slopes, cliffs, etc.).
- Users responsible for their own safety; carry basic safety equipment and contact information.

## Use and dissemination of NPMS data
- Data support UK biodiversity indicators and habitat change assessments.
- Outputs (newsletters, reports, and peer-reviewed publications) communicate results and uncertainties; data are available for external review.
- Data sharing and public availability aim to enable independent verification and broad use by researchers, policymakers, and the public.

## Appendix and habitat guidance
- Appendix 1 provides habitat types (28 fine habitats, 11 broad categories) with detailed descriptions and species lists to guide recording.
- Domin Scale guidance (percent cover) and examples to help standardize abundance scoring across plots.
- Habitat-specific notes cover arable margins, bogs, woodlands, coast, freshwater, heathland, grasslands, marshes, pinewood/juniper, rock outcrops, and upland grasslands, including special considerations for each habitat type.