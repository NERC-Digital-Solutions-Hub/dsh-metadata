# National Plant Monitoring Scheme (NPMS)

## Purpose and scope
- A habitat-based plant monitoring scheme designed by BSBI, CEH, Plantlife and JNCC to provide annual indicators of changes in plant abundance and diversity.
- Supports volunteer recorders to monitor plants and habitat attributes across the UK, Isle of Man and Channel Islands.
- Objectives: detect changes in priority habitats, understand pressures/drivers, contribute to UK Biodiversity Indicator C7 (plants of the wider countryside).
- Aims to deliver a consistently updated dataset stored with CEH, enabling scrutiny of environmental health and policy performance over time.

## Data structure and files (provided datasets)
- locations_2015to2018.csv: unique location_id and location_type (square or linear plots).
- sampleInfo_2015to2018.csv: sampling events with sample_id, survey_id, date_start, location_id, spatial reference, created_on/by, etc.
- sampleAttributes_2015to2018.csv: additional attributes linked to samples (sample_attribute_id, sample_id, text_value, caption).
- occurrences_2015to2018.csv: species occurrences with id, sample_id, taxon keys, preferred_taxon, domin (Domin scale), record_status, sensitivity_precision.
- npmsHabitatLookup.csv: mapping between NPMS broad habitats and fine-scale habitats.
- Usage: data are designed for cross-year, standardized analyses of habitat condition and plant community change.

## How the NPMS works (survey design and data capture)
- Habitat coverage: 28 fine NPMS habitats, aggregated into 11 broad categories.
- Species lists: up to 30 indicator species per habitat; inventories may record all vascular plants (Inventory Level).
- Plots:
  - Square plots: 5x5 m (10x10 m in woodlands), placed within pre-selected locations; aim for 3 plots in different fine habitats per square where possible.
  - Linear plots: 1x25 m for linear habitats (e.g., arable margins, hedgerows, streams).
- Survey levels:
  - Wildflower Level: subset of species.
  - Indicator Level: full set of habitat-indicator species.
  - Inventory Level: Indicator Level plus all other vascular plants.
- Sampling frequency: two visits per year (late spring/early summer and late summer); in year 1, a reconnaissance visit may be used to locate plots.
- Plot relocation: emphasis on fixed plot locations with field sketches, photos, grid coordinates, and permanent features to aid future relocation.
- Data capture: online entry preferred; standardized fields, species dictionary, dates, coordinates, and controlled habitat terms; automated geographic checks; iRecord used for expert verification where needed.

## Field methods and data recording
- Recording protocol:
  - Identify species present and estimate abundance as percent cover using the Domin scale.
  - Record bare ground, litter, bare rock/gravel, and moss/lichen covers.
  - Optional attributes: vegetation height, woodedness, aspect, slope, and management (with prescribed categories and guidance).
- Plot layout and relocation aids:
  - Sketch maps, compass directions, photographs (up to 2 per plot), and GPS as a supplementary tool.
  - Protocols for square plots, linear plots, rock outcrops, screes, ponds and flushes, with habitat-specific guidance.
- Special considerations:
  - Arable margins, road verges, hedgerows, and standing waters have explicit sampling rules (e.g., margins extend 1 m into cultivated area; ponds surveyed from the bank).
  - Ponds and streams may require careful handling due to water levels; survey from the edge when possible.
  - If a plot falls outside NPMS habitat definitions over time, continue surveying with the appropriate NPMS species list if feasible.

## Evidence Quality Assurance (EQA) and governance
- EQA supported by peer-reviewed publications, project design reports, and ongoing methodological reviews.
- Core QA elements:
  - Robust sampling design (grid-based square plots and gridlines for linear plots) and habitat definitions validated by experts.
  - Clear target species lists aligned with habitat indicators; objective selection criteria with project team review.
  - Data input verification via online systems, species dictionaries, calendar dates, map-based locations, and controlled terms; iRecord verification for expert review.
  - Data analysis by experienced ecologists using R; results reviewed by a dedicated project team.
  - Transparency on uncertainty, limitations, and assumptions; outputs checked by scientists before publication.
  - Document tracking and version control via a Data Management Plan and PRINCE2 project management standards.
- Governance:
  - NPMS Steering Group oversees work; external peer review conducted where risk warrants it.
  - Outputs (newsletters, reports) reviewed for evidence-based claims; data made publicly available for independent review.
  - Ongoing engagement with CEH Monitoring science to foster feedback and critique.

## Data use, outputs, and accessibility
- Data are intended to support annual reporting on habitat condition and plant community changes; contribute to biodiversity indicators and policy discussions.
- Outputs include newsletters, reports and peer-reviewed publications; data published publicly to enable independent verification.
- Field survey results provide feedback to volunteers and stakeholders; methodology and uncertainties are communicated alongside outputs.

## Access, rights, and safety
- Volunteers must respect countryside access rights, safety, and landowner permissions; guidance varies across the UK nations.
- Health and safety emphasized: check weather, avoid unsafe sites, work with a buddy if possible, carry a mobile phone and first-aid kit, and wear appropriate gear.

## Appendix: Habitat types and measurement details
- 28 fine NPMS habitats organized into 11 broad categories (e.g., Arable field margins, Bog and wet heath, Broadleaved woodland, Coast, Fresh water, Heathland, Lowland grassland, Marsh and fen, Native pinewood and juniper scrub, Rock outcrops, upland grassland).
- Domin Scale explained (percentage cover and abundance scoring) and guidance for translating plots into percent cover (e.g., 1% to 10% cover increments; 1–10 scale).
- Habitat descriptions provide context for habitat-specific species lists and survey emphasis.

## Key challenges and opportunities for analysts
- Increasing the value of NPMS datasets by integrating with other datasets to avoid single-use outputs.
- Improving access to underlying data for broader analyses and transparent scrutiny of results.