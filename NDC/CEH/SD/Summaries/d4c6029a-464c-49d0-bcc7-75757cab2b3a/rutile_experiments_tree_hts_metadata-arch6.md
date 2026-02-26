# Materials and methods for the dataset: Growth of five species of trees on experimental plots on sand tailings left after mining for rutile in Sierra Leone

## Purpose and scope
- Documents the dataset on tree height growth for five species after 2.5 years (June 2007–November 2009) on eight experimental plots of rutile-sand tailings near Lanti South, Sierra Leone.
- Aims to support understanding of how planting and surface treatments influence tree growth on degraded, nutrient-poor sand tailings and to enable data-driven restoration planning.

## Experimental design and treatments
- Plots and layout
  - Eight plots (plots 1–8), each with four compartments (25 m × 25 m).
  - Each compartment planted with five species, arranged in rows 5 m apart and 5 m between rows; one species per row.
  - Species: mango (Mangifera indica), Gmelina arborea, cashew (Anacardium occidentale), citrus (Citrus sinensis), and monkey apple (Anisophyllea laurina).
  - Trees planted in 2007; plots include both square (1–4) and rectangular (5–8) configurations.
- Planting treatments (per compartment)
  - 17 L compost
  - 17 L topsoil
  - 17 L of a 50:50 mix of compost and topsoil (ts_and_c)
  - Control (no added material)
- Surface treatments (applied to all trees in a compartment)
  - ~2 cm surface compost
  - ~2 cm surface topsoil
  - ~5 cm mulch (mostly mattress grass)
  - Control (no surface treatment)
- Measurements and data scope
  - Height of each tree recorded in centimeters; 800 trees across 32 compartments.
  - Tree survival is indicated by height = 0 (dead/missing).
  - Additional measurements during the project include invertebrates, birds, ground flora, and soil samples (C, N, and later heavy metals) but the dataset described here focuses on tree height.
- Data collection timeline
  - Planting began June 2007; monitoring occurred at least twice yearly through 2009.

## Data content and structure
- Dataset file: rutile_experiements_tree_hts.csv
- Size and format
  - Approximately 42 KB; CSV with 8 columns and 801 rows (800 trees plus header).
- Core variables (as described in the data dictionary)
  - id: Unique tree identifier (integer; 1–800)
  - Plot: Plot number (integer; 1–8)
  - Planting: Planting treatment in the hole (string; compost, topsoil, ts_and_c, or control)
  - Surface: Surface treatment applied to the compartment (string; topsoil_surf, nothing_surf, compost_surf, mulch_surf)
  - position: Position along the row (integer; 1–5)
  - Species: Tree species (string; Mangifera, Gmelina, Anisophyllea, Anacardium, Citrus)
  - Height: Tree height in centimeters (integer; 0 indicates dead or missing)
  - Note: Height measurements range up to 404 cm; missing/dead trees coded as zero
- Data provenance
  - Data collected in-field with tape measures, recorded on paper, then transcribed into Excel; double-entry verification performed.

## Data collection, entry, and quality control
- Procedures
  - Measurements taken by two-person teams (measurer and recorder) to ensure accuracy; height measured from ground to the highest apical bud.
  - Regular checks to ensure all trees were measured and accounted for; plots/compartments marked, though some signs disappeared or were relocated over time.
- Quality considerations
  - In 2009, very tall trees challenged measurement accuracy with standard tapes.
  - Some undergrowth due to seed bank in compost provided by local communities affected certain compartments (notably plots 3 and 7) and may influence growth observations.
  - Cross-checks between planting treatments and plot maps performed to verify treatments; signage and plot delineation could introduce some confusion.

## Site context and environment
- Location and geography
  - Lanti South area within a Sierra Rutile Ltd (SRL) concession.
  - Sand tailings from rutile dredging; soils are coarse quartz sand with very low silt/clay and extremely low nutrients (N ~0.0027%, C ~0.073%).
  - Natural regeneration is virtually non-existent on tailings; plots lie on two main sand-tailings ridges separated by a low-lying, seasonally flooded area.
- Climate and hydrology
  - Wet tropical climate; ~3 meters of rainfall per year; August is particularly wet (~900 mm).
  - Soils leach readily; drainage to nearby ponds; no significant natural watersheds within plot area.
- Ground conditions
  - Substrate is coarse sand up to several meters deep; tailings show poor soil structure and low fertility, with pre-disturbance soil N ~0.12% and C ~4%.

## Data access, usage, and governance
- Data and permissions
  - Data collected on SRL concession land; travel and data access require permission from SRL’s Head of Health, Safety and Environment.
- Data dictionary and documentation
  - Variable descriptions and data types are provided (Table 1 and Table 3 in the documentation) to support interpretation and integration with other datasets.
- Related data opportunities
  - The project also collected soil C/N and heavy metals, invertebrate/bird/ground flora data; these can be integrated with height data for richer analyses on growth drivers and ecological restoration potential.
  - Potential data products include self-serve dashboards and reports by plot, species, and treatment to compare growth trajectories and survival across treatments.
  
## Potential data products and analyses (Data Support perspective)
- Descriptive analytics
  - Growth summaries by species, planting treatment, and surface treatment.
  - Survival rates by species and treatment combinations (using height = 0 as dead).
- Comparative analyses
  - Interaction effects between planting and surface treatments on height growth.
  - Species-specific responses to nutrient amendments in planting holes.
- Spatial and plot-level insights
  - Per-plot growth curves and compartment-level comparisons.
  - Correlations with soil measurements (C, N) and any available heavy metals data from 2009.
- Data products for end users
  - Dashboards displaying height over time (2.5-year window) by species and treatment.
  - Filterable views by plot, treatment, and position along row.
  - Data dictionaries and provenance trails to support reproducibility and re-use in local restoration planning or policy discussions.