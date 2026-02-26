# National Plant Monitoring Scheme survey data (2015-2018)

- The NPMS is a habitat-based plant monitoring scheme designed by BSBI, CEH, Plantlife and JNCC to provide annual indications of changes in plant abundance and diversity.
- Aims:
  - Detect change in the quality of priority habitats.
  - Understand drivers/pressures behind change.
  - Contribute data for the UK Biodiversity Indicator (C7 Plants of the wider countryside).
- Operated to monitor habitat health using volunteer plant recorders across the UK, Isle of Man and Channel Islands; data are compiled into an annually updated dataset held at CEH Wallingford.

## Data files and structure (overview)

- locations_2015to2018.csv: unique location_id, location_type (plot type).
- sampleInfo_2015to2018.csv: sampling events, linking to location_id, with survey_id, date_start, entered_sref, created_on, created_by_id, etc.
- sampleAttributes_2015to2018.csv: additional sample-level attributes linked to sampleInfo via sample_id.
- occurrences_2015to2018.csv: species occurrences per sample, with taxon data, dominance (domin) values, record_status, and sensitivity information.
- npmsHabitatLookup.csv: static lookup between NPMS broad and fine habitat categories.
- The NPMS data are supported by an Evidence Quality Assurance (EQA) framework and related methodological documents.

## How NPMS works in practice

- Habitat scope:
  - 28 fine NPMS habitats, which can be grouped into 11 broad NPMS categories.
  - Habitats described to support habitat-specific species lists and indicators.
- Survey units:
  - Square plots: 5x5 meters (10x10 m in woodlands).
  - Linear plots: 1x25 meters.
  - Plots are placed within 1-km squares and align with targeted NPMS habitats.
- Species data:
  - Sample-level data capture plant communities and abundances using Domin-style cover values.
  - Up to 30 target species per habitat (when using fine habitat lists); optional additional records can be entered if target species are absent.
  - Occurrences include taxon keys, preferred taxon names, and verification status (e.g., verified via iRecord).

## Field recording and guidance

- Field guidance covers:
  - Plot location marking, rel relocatability, and field sketching.
  - Photographing plots (up to 2 per plot) with orientation notes.
  - Use of GPS to improve location accuracy; not a replacement for sketches.
  - Data entry online via www.npms.org.uk; paper forms available for offline submission.
- Plot design and placement:
  - 3 plots per square (ideally) across different NPMS habitats; protocol supports self-selection (Protocol A) when pre-selected plots are inaccessible.
  - Preference for placing plots within the habitat’s typical area, avoiding obvious disturbances unless representative of the habitat.
  - Self-selected plots should be relocatable in future years using permanent features for reference.
- Special plot types:
  - Arable field margins: extend 1 m into the cultivated area from the edge.
  - Hedgerows, road verges, standing waters, rivers, streams, ponds, and springs: specify plot placement to capture representative habitat edges and margins.
  - Ponds/flushes: surveyed as linear plots if rare; attention to edge and habitat proportion within plots.
  - Rock outcrops and screes: vertical/horizontal adjustments recommended to minimize risk; focus on accessible sections.
- Recording in plots:
  - Record present species using the habitat-specific list.
  - Assess percent cover for each species (Domin scale); consider layered vegetation and understorey.
  - Optional additional data: vegetation height, woodedness, aspect, slope, and management.
  - Optional grazing categories (High/Moderate/Low) to capture disturbance regimes.
- Data submission and support:
  - Data entered online; support available at support@npms.org.uk.
  - Paper forms can be mailed to NPMS Volunteer Coordinator if online entry is not possible.

## Survey levels and sampling intensity

- Wildflower Level: fewer species recorded; subset of Indicator Level species.
- Indicator Level: full set of habitat indicator species; robust data collection.
- Inventory Level: Indicator Level plus recording all other vascular plants present in the plot.

## Plot relocation and documentation

- Importance of fixed plot locations to enable long-term trend detection.
- Tools to aid relocation:
  - Field sketches (including compass orientation and permanent features).
  - Photographs (limit of two per plot).
  - GPS coordinates (as a support tool, not a replacement for notes).
- Pre-selected plot locations within squares shown on the provided map; if unavailable, protocols allow self-selection or alternative plots (Protocol A).
- For malleable habitats or changes over time, maintain continuity by continuing with NPMS lists relevant to the habitat at each survey.

## Data quality assurance (EQA) and governance

- EQA framework references peer-reviewed and published sources:
  - Pescott et al. 2019 (design, launch, assessment of a volunteer-based plant monitoring scheme).
  - Pescott et al. 2015 (ecological monitoring with citizen science).
- QA processes:
  - Project Steering Group oversight.
  - External peer review for high-risk outputs.
  - Data verification via iRecord for specimen-level records; automated geographic range checks.
  - Outputs reviewed by science staff to ensure claims are evidence-based.
  - Uncertainty and bias addressed via robust statistical design and modelling.
  - Document tracking and version control per CEH Data Management Plan; archival and off-site backups; PRINCE2 project management standard.
  - Data and outputs publicly shareable; ongoing peer feedback encouraged.
- Uncertainty, limitations, and biases:
  - Clear communication of uncertainties in newsletters and reports.
  - Use of modelling to estimate uncertainties and ensure robust interpretations.
- Access, sharing and governance:
  - Data intended for public release to allow independent verification.
  - Data management and sharing governed to ensure metadata quality and dataset integrity.

## Habitat types (illustrative overview)

- 28 fine NPMS habitats described (with 11 broad categories), including:
  - Arable field margins
  - Bog and wet heath (blanket bog, raised bog, wet heath)
  - Broadleaved woodland, hedgerows, and wet woodland
  - Coastal habitats (saltmarsh, dunes, vegetated shingle, machair, maritime cliffs)
  - Freshwater (nutrient-poor and nutrient-rich lakes/ponds, rivers and streams)
  - Heathland (dry and montane variants)
  - Lowland grassland (dry acid, dry calcareous, neutral damp, neutral pastures and meadows)
  - Marsh and fen (acidic and base-rich fens, flushes, mires, springs)
  - Native pinewood and juniper scrub
  - Rock outcrops, cliffs and screes
  - Upland grassland (montane variants)
- Each habitat is associated with specific indicator species lists and recording guidance to reflect habitat quality and change.

## Data usage and access

- Primary purpose: provide annual feedback and robust data to policymakers, researchers, and the public.
- Data are designed to support analysis of habitat quality, species distributions, and long-term ecological changes across the UK.
- Public release and ongoing updates ensure transparency and independent evaluation.

## Health, safety, and access

- Survey participation requires personal safety precautions and adherence to country-specific access guidance.
- Users should secure permission for private land, follow local access codes, and avoid dangerous areas.
- Implement safety practices (buddy system, mobile phone where possible, first-aid kit, appropriate clothing).

## Appendix and guidance resources

- Appendix 1: Habitat type descriptions (detailed descriptions for each habitat type and subcategories).
- Domin Scale: detailed percent cover scale for recording species abundance (and guidance on translating cover to percentages for different plot sizes).
- Additional guidance and support materials are available on the NPMS website, including field guidance and species lists.

- The NPMS dataset provides a structured, quality-assured framework for monitoring plant communities and habitat condition, enabling policy-relevant insights and transparent reporting over time.