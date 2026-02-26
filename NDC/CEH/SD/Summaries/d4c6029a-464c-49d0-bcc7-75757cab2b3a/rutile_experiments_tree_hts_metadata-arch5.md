# Materials and methods for the dataset: Growth of five species of trees on experimental plots on sand tailings left after mining for rutile in Sierra Leone

## Overview
- Describes a dataset documenting tree growth (height in cm) for five species grown on sand tailings rehabilitated after rutile mining in Sierra Leone.
- Study location: Lanti South SRL concession, Sierra Leone; eight experimental plots with four 25 m x 25 m compartments each.
- Planting and surface treatments: four planting treatments (compost, topsoil, 50:50 mix, or control) and four surface treatments (compost, topsoil, mulch, or control).
- Species: mango (Mangifera indica), Gmelina arborea, cashew (Anacardium occidentale), citrus sinensis (sweet orange), and monkey apple (Anisophyllea laurina).
- Time frame: growth data collected over 2.5 years (June 2007 to November 2009).
- Substrate and site context: coarse quartz sand with very low N (0.0027%) and C (0.073%); high rainfall (~3 m/yr); natural regeneration is minimal; plots arranged on two ridges of sand tailings with a nearby mangrove forest.

## Dataset Structure and Contents
- Dataset file: rutile_experiements_tree_hts.csv
- Size and format: 42 kb; 8 columns (file says 8 columns, 801 rows; data rows described as 800 trees with seven columns; header present on first line).
- Data organization: each row corresponds to a tree; data captured per tree across columns.
- Variables (as described in Table 3/Table 1):
  - id: integer, 1–800; unique tree identifier
  - Plot: integer, 1–8; plot number
  - Planting: string; planting treatment in the hole (compost, control, ts_and_c which is 50:50 mix, topsoil)
  - Surface: string; surface treatment per plot (topsoil_surf, nothing_surf, compost_surf, mulch_surf)
  - position: integer; position along the row (1–5)
  - Species: string; tree species (Mangifera, Gmelina, Anisophyllea, Anacardium, Citrus)
  - Height: integer; tree height in cm (0 for dead or missing)
  - Note: an eighth column is implied but not described in the text; described variables total seven, indicating a possible additional column not detailed
- Data collection and documentation:
  - Header line with variable names; subsequent lines contain data
  - Version includes notes on possible minor inconsistencies between column counts and described variables

## Experimental Design and Context
- Plot design: eight plots, each with four 25 m x 25 m compartments; compartments contain one species per row; four planting treatments applied per compartment; four plot-wide surface treatments
- Species arrangement: each compartment contains one species; rows spaced 5 m apart; trees planted 5 m between rows
- Planting materials: standard bucket of 17 L used for compost, topsoil, or mix; control had no added material
- Surface treatments: approximately 2 cm of topsoil or compost, ~5 cm mulch, or no surface treatment
- Maintenance: planting and initial compost supplied by Sierra Rutile Ltd. and local communities; observed undergrowth issues in plots with local compost containing weed/vegetable seeds; some early watering noted but not quantified

## Data Collection, Measurement, and Methods
- Data collection: tree heights measured; in addition, monitoring of invertebrates, birds, and ground flora; soil samples collected before planting (June 2007) and again in January 2009; 2009 soil tests included carbon, nitrogen, and heavy metals (Pb, Cd, Sr, etc.)
- Instrumentation: tape measures for height and spread
- Data recording: measurements recorded on paper in the field and transcribed into Excel; double-entry verification (two-person teams: measurer and recorder)
- Taxonomy and labeling: species names standardized to common usage; citrus classified as sweet orange (with possible variation)
- Permits/ethics: plots located on SRL land; travel requires permission from SRL Health, Safety and Environment leader

## Data Quality Assurance and Control
- Data integrity: two-person verification to reduce measurement and transcription errors; cross-checking against plot maps to ensure planting treatments align with plot locations
- Potential challenges noted:
  - Some sign boards disappeared or were relocated, complicating plot identification
  - Taller trees near 2009 measurement could be difficult to measure accurately with a simple tape
  - Compost plots produced unintended thick undergrowth due to weed seeds, potentially affecting target species growth (e.g., Monkey apple and Citrus)
  - Planting treatment verification sometimes required field cross-checks against maps

## Access, Use, and Limitations
- Access constraints: fieldwork conducted within a mining concession; permission required from SRL leadership to travel to the site
- Temporal and contextual details available: precise GPS coordinates for plot centers; climate and site history context included to support interpretation and reuse
- Data limitations and considerations for reuse:
  - Height data coded with 0 for dead/missing trees; users should distinguish zero values as living zero-height measurements or dead/missing
  - Possible inconsistency in column count (8 columns vs. 7 described variables) requires careful interpretation of the dataset structure
  - Understory competition and weed-seed in compost may have introduced biases affecting growth
  - Some data capture gaps exist (e.g., exact timing/quantity of watering not recorded)

## Metadata and Provenance
- Metadata elements included or referenced:
  - Site description, plot layout, species composition, planting and surface treatment details
  - Experimental design and measurements cadence
  - Data collection methods and QA processes
  - File-level metadata: filename, data type, and column descriptions; documented variable definitions and units
- Provenance notes emphasize field origin (SRL site), methods (tape measurements, field notes, Excel transcription), and QA workflow (two-person teams, cross-checks)

## Practical Guidance for Data Stewards
- Maintain clear linkage between plots, compartments, and treatments to preserve interpretability
- Preserve documentation on signboard removals and cross-check procedures to aid future data quality improvements
- Ensure consistent coding for Planting and Surface treatments; consider adding a separate column to capture any anomalies or additional treatment notes
- Document measurement challenges (e.g., tall trees near measurement limits) and any adjustments made during data collection
- Provide explicit licensing/usage terms and data access notes for researchers wishing to reuse the dataset, given the concession-based access constraints