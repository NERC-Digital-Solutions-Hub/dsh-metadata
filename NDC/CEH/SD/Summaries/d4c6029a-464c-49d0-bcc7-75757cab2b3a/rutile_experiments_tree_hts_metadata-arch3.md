# Growth of five species of trees on experimental plots on sand tailings left after mining for rutile in Sierra Leone.

## Overview
- Long-term environmental rehabilitation study in Sierra Leone’s rutile mining area.
- Assess growth of five tree species under different planting and surface treatments on coarse sand tailings.
- Data collection spanned from June 2007 to November 2009, including tree height and broader ecological observations.

## Study site and context
- Location: Lanti South within the Sierra Rutile Ltd (SRL) concession, on sand tailings adjacent to dredge ponds; near Mattru Jong (coordinates provided in the report).
- Climate and soils: wet tropical with ~3 m/year rainfall; soils are coarse quartz sand with very low nitrogen (≈0.0027%) and carbon (≈0.073%), lacking silt/clay; natural regeneration is minimal.
- Previous land use: post-mining disturbance with largely degraded substrates; adjacent areas include a large mangrove forest.
- Management and permissions: plots established and maintained by SRL; travel requires permission from SRL’s Health, Safety, and Environment head.

## Experimental design
- Plots and planting setup:
  - Eight plots, each with four compartments (25 m x 25 m); four plots are square, four are rectangular.
  - Each compartment planted with one of five species: mango (Mangifera indica), Gmelina arborea, cashew (Anacardium occidentale), citrus (Citrus sinensis), monkey apple (Anisophyllea laurina).
  - Planting density: trees spaced 5 m apart in rows; five rows per compartment; one species per row.
  - Each plot compartment assigned to one planting treatment.
- Treatments:
  - Planting treatments per hole: compost (17 L), topsoil (17 L), mixed compost/topsoil (17 L total), or control (no addition).
  - Surface treatments per plot: compost (~2 cm), topsoil (~2 cm), mulch (~5 cm), or nothing.
- Data collection:
  - Growth: tree height measured in centimeters; plates maintained over time.
  - Additional observations: invertebrates, birds, and ground flora; soil samples for carbon and nitrogen (2007 baseline; 2009 follow-up) and, in 2009, heavy metals (Pb, Cd, Sr, etc.).
- Data collection cadence: plots monitored at least twice per year.

## Data set and metadata
- Primary data file: rutile_experiements_tree_hts.csv (42 KB; about 8 columns and 800 rows; note: header mentions seven data columns; description lists eight with an identifier for rows).
- Key variables (as described):
  - id: unique tree identifier (integer, 1–800; no missing data).
  - Plot: plot number (1–8).
  - Planting: planting treatment applied to the hole (compost, topsoil, ts_and_c, or control).
  - Surface: surface treatment (topsoil_surf, nothing_surf, compost_surf, mulch_surf).
  - position: position along the row (1–5).
  - Species: tree species (Mangifera, Gmelina, Anisophyllea, Anacardium, Citrus).
  - Height: tree height in centimeters (integer; 0 indicates dead or missing plants).
- Data format and documentation:
  - File is a comma-delimited ASCII text; first line contains variable names; subsequent lines contain data.
  - Variable metadata provided in accompanying descriptions (Table 1 and Table 3 in the document): data types, units, allowable values, and notes on missing data.
- Data acquisition and QA:
  - Collection method: field tape measures; data recorded on paper and transcribed to Excel; double-entry verification.
  - Quality control: two-person teams (measurer and recorder); cross-checks against plot maps; measurement challenges noted for tall trees; plot signage has degraded over time.

## Considerations for monitoring and governance
- Data quality and completeness:
  - Potential measurement error for tall trees and signs of mislabeling due to degraded signage.
  - Height data allows dead/missing trees to be coded as zero, which affects growth analyses.
- Metadata and data sharing:
  - Comprehensive metadata is provided (data dictionary, variable descriptions); some inconsistencies in documentation (8 vs. 7 columns) should be clarified for reuse.
  - Data resides in a clearly described dataset with explicit data provenance and collection methods, aiding reproducibility and governance.
- Data applicability for policy monitoring:
  - Enables assessment of how planting and surface treatments influence tree growth on degraded, nutrient-poor sand tailings.
  - Supports evaluation of rehabilitation strategies’ effectiveness under tropical climate and poor substrate conditions.
  - Provides a baseline for environmental health monitoring in post-mining landscapes, including soil nutrient status changes (C and N) and potential heavy metal presence.

## Limitations and notes
- Weathering and management variables (e.g., irrigation details) are not comprehensively recorded beyond a note of some watering during the first dry season.
- Weed seed contamination from compost affected undergrowth in some plots, potentially impacting performance of jungle crops (monkey apple and citrus).
- Data rights and accessibility depend on the SRL concession and associated permissions for external use.