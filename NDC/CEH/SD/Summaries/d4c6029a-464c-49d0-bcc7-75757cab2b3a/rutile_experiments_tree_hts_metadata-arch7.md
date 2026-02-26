# Materials and methods for the dataset: Growth of five species of trees on experimental plots on sand tailings left after mining for rutile in Sierra Leone.

## Overview
- Dataset documents growth of five tree species on eight experimental plots (four compartments per plot) established on rutile sand tailings near Lanti South, Sierra Leone.
- Trees were planted in June 2007 and growth measured up to November 2009 (about 2.5 years).
- Measured variable in the dataset: tree height in centimetres for 800 trees across eight plots and seven variables.
- Experimental factors include planting treatments (compost, topsoil, 50:50 mix, or control) and surface treatments (compost, topsoil, mulch, or nothing).
- Data quality notes: some undergrowth from weed seeds in compost; some markers moved; tall-tree measurement challenges; data entered via double-entry process.

## Location and Site Context (GIS relevance)
- Site: Lanti South within Sierra Rutile Ltd (SRL) concession; adjacent to active dredge ponds; two main ridges of sand tailings.
- Geography: coarse white quartz sand substrate, with very low natural regeneration; drainage toward ponds; climate with ~3 m annual rainfall, heavy August rains.
- Plot coordinates: approximate plot centers provided (GPS coordinates in WGS 84) for plots 1–8, enabling geospatial placement of plots within a GIS.
- Environmental background: soils deficient in nitrogen (~0.0027%) and carbon (~0.073%); tailings resemble sand dunes with minimal silt/clay.

## Experimental Design and Plot Layout
- 8 plots total; each plot comprises four 25 m × 25 m compartments (some plots are square, others rectangular).
- Each compartment contains five rows of trees, one species per row:
  - Gmelina arborea (Gmelina)
  - Mangifera indica (mango)
  - Anacardium occidentale (cashew)
  - Citrus sinensis (sweet orange; some varieties may vary)
  - Anisophyllea laurina (monkey apple)
- Spacing: 5 m between trees and 5 m between rows.
- Planting treatments (per compartment): 17 L of compost, 17 L of topsoil, 17 L of a 50:50 compost/topsoil mix, or control (none).
- Surface treatments (per plot; applied uniformly across all four compartments of a plot): ~2 cm compost surface, ~2 cm topsoil surface, ~5 cm mulch (mattress grass), or nothing.
- Plot management: planting and maintenance conducted by SRL with local labor; compost produced by local communities (decentralized model).
- Data collection: tree height measured for each tree; additional monitoring of invertebrates, birds, ground flora; soil samples collected before planting (June 2007) and January 2009; some 2009 soil tests for heavy metals and nutrient content.

## Data Collected and Variables (CSV details)
- Data file: rutile_experiements_tree_hts.csv (note: spelling variations appear in the document; for reference: rutile_experiements_tree_hts.csv).
- Size/format: approximately 42 KB; 8 columns reported, 800 rows (one per tree); first line contains column names.
- Core variables (Table 3 descriptions):
  - id: Unique tree identifier (integer; values 1–800; no missing data).
  - Plot: Plot number (integer; values 1–8).
  - Planting: Planting treatment applied to the hole (string; values include 'compost', 'topsoil', 'ts_and_c' for 50:50 mix, 'control' for none).
  - Surface: Surface treatment applied to the plot (string; values include 'topsoil_surf', 'nothing_surf', 'compost_surf', 'mulch_surf').
  - position: Position along the row (integer; values 1–5; indicates location within the compartment).
  - Species: Tree species (string; 'Mangifera' = mango, 'Gmelina' = Gmelina arborea, 'Anisophyllea' = monkey apple, 'Anacardium' = cashew, 'Citrus' = sweet orange).
  - Height: Tree height in centimetres (integer; range 0–404; 0 indicates dead or missing trees).
- Notes:
  - No missing data reported for the key fields; zeros in Height indicate dead or missing trees.
  - Height measurements taken from ground to the highest apical bud; measurement challenges noted for tall trees.
  - Data entry performed via double-entry in Excel.

## Data Acquisition and Quality Assurance
- Field methods: measurements taken with tape measures; two-person teams (measurer and recorder).
- Verification: recorder cross-checks measurements, ensures all trees are accounted for; plot markers have sometimes disappeared or been relocated; planting treatments cross-checked against maps.
- Limitations/considerations: tall trees posed measurement difficulties; weed seeds from compost may have influenced undergrowth in some plots (notably plots 3 and 7).

## Access, Permissions, and Usage Notes
- Location within SRL mining concession; travel requires permission from the Head of Health and Safety and the Environment at SRL.
- Dataset provides a geospatially relevant basis for mapping tree growth by species and treatment across plots, enabling analyses of spatial patterns of growth under different substrate and surface amendments.
- Temporal scope: height data covers up to 2.5 years post-planting (June 2007 to November 2009); soil and environmental context captured via additional soil sampling data from 2007 and 2009.

## GIS Application Guidance
- Use plot center coordinates to place plots in a GIS and assign each compartment a location within its plot for spatial visualization.
- Join height data to plot-level attributes (Plot, Planting, Surface, Species) to create choropleth or symbol maps showing growth by species and treatment.
- Consider integrating soil and environmental context (Nitrogen, Carbon, heavy metals where available) to analyze correlations with tree growth.
- Note data constraints: single height measurement timeframe (2.5-year snapshot); potential non-uniform undergrowth and measurement challenges in tall trees.