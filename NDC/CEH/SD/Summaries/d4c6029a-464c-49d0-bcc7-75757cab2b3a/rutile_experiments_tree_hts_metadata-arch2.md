# Materials and methods for the dataset: Growth of five species of trees on experimental plots on sand tailings left after mining for rutile in Sierra Leone.

## Overview
- Objective: Document materials and methods for a dataset tracking tree growth on sand tailings from rutile mining in Sierra Leone, enabling environmental monitoring and assessment of rehabilitation performance over time.
- Context: Tailings are nutrient-poor (N ~0.0027%, C ~0.073%), with very low natural regeneration; rehabilitation plots test growth of five species under different planting and surface amendments.
- Data purpose: Provide a standardized dataset (growth and related environmental metrics) for scrutiny of environmental health and policy performance over time.

## Study site and environmental context
- Location: Lanti South, SRL mining concession, Sierra Leone, near a dredge pond (coordinates around 7°41' N, 12°17' W).
- Landform and substrate: Sand tailings with coarse quartz sand; tailings up to 5 m deep; natural regeneration virtually non-existent.
- Climate: Wet tropical; ~3 m annual rainfall; August peak (~900 mm); high humidity; temperatures typically above 25°C.
- Hydrology: Drainage toward ponds; seasonally flooded depressions between ridges.
- Site history: Rutile mining since the 1970s; restoration attempts elsewhere; plots planted in 1994 with rehabilitation commencing at Lanti South in 2007.

## Experimental design and treatments
- Plots: Eight plots total; four square (plots 1–4) and four rectangular (plots 5–8); each plot comprises four 25 m × 25 m compartments.
- Species: Five tree species per compartment in rows (one species per row):
  - Gmelina arborea (Gmelina)
  - Mangifera indica (mango)
  - Anacardium occidentale (cashew)
  - Citrus sinensis (sweet orange)
  - Anisophyllea laurina (monkey apple)
- Planting treatments (per compartment):
  - Compost (17 L)
  - Topsoil (17 L)
  - Mixed 50:50 compost/topsoil (17 L)
  - Control (no additional material)
- Surface treatments (applied to entire compartment per plot):
  - Compost surface (~2 cm)
  - Topsoil surface (~2 cm)
  - Mulch (~5 cm; mainly mattress grass)
  - Control (no surface treatment)
- Planting density and arrangement: Trees planted in rows 5 m apart, 5 m between rows; 5 species rows per compartment; same planting treatment applied across all trees within a compartment.
- Maintenance and inputs: Compost sourced from local communities; some within-plot weed/seed issues due to compost; limited irrigation during dry season with few records.

## Data collection and measurements
- Primary growth metric: Height of trees at two-and-a-half years after planting (June 2007 to November 2009).
- Additional monitoring: Invertebrates, birds, and ground flora were recorded in each compartment; soil samples collected before planting (June 2007) and again in January 2009 for Carbon and Nitrogen; 2009 soil analyses included heavy metals (e.g., lead, cadmium, strontium) plus Carbon and Nitrogen.
- Monitoring frequency: At least twice per year for growth and biodiversity indicators.
- Data collection tools: Tape measures for height; field notebooks for observations; standard recording protocols.

## Data file and metadata
- Data file: rutile_experiements_tree_hts.csv (CSV; ASCII text)
- Size and structure: Approximately 800 tree records; 8 columns described in metadata (there is a note in the document of 7 columns, but metadata lists 8 columns). Main variables include:
  - id: Unique tree identifier (integer; 1–800)
  - Plot: Plot number (integer; 1–8)
  - Planting: Planting treatment (string: compost, topsoil, ts_and_c, or control)
  - Surface: Surface treatment (string: topsoil_surf, nothing_surf, compost_surf, or mulch_surf)
  - position: Position along the row (integer; 1–5)
  - Species: Tree species (string; Mangifera, Gmelina, Anisophyllea, Anacardium, Citrus)
  - Height: Tree height in centimeters (integer; 0 for dead/missing)
  - (An additional column exists in the header metadata but is not described in the variable list)
- Data format and storage: Comma-delimited ASCII text; first line contains variable names; subsequent lines contain observations.
- Data provenance and handling: Data collected in the field with tape measures, transcribed to Excel; double-entry verification to ensure accuracy.

## Data acquisition and quality control
- Procedures: Two-person field teams (measurer and recorder) to ensure accuracy; measurements taken from ground to the highest apical bud; cross-checks against plot maps to verify planting and surface treatments.
- Quality considerations: Tall trees posed measurement challenges; some signboards disappeared or were relocated, complicating plot identification; occasional gaps in irrigation records; weed growth (from decentralized compost) affected certain compartments.

## Permits and access
- Access: Plots located on SRL land; permission required from SRL Health, Safety and the Environment department prior to travel.

## Relevance for environmental monitoring and policy performance
- Standardization: Demonstrates a standardised approach to documenting rehabilitation experiments on mine tailings, including plot design, treatments, species selection, and measurement protocols.
- Monitoring value: Enables assessment of revegetation strategies by comparing growth responses across planting and surface treatments, species, and plots over time.
- Data accessibility and reuse: Data are structured for integration with other environmental datasets (soil properties, biodiversity indicators) to enhance monitoring value and policy analysis; datasets can be uploaded to appropriate portals for wider access.
- Limitations and opportunities: Weed intrusion from local compost and data gaps (sign boards, irrigation records) highlight areas for improved quality control; potential exists to link tree growth with soil nutrient dynamics and heavy metal status to better understand rehabilitation outcomes.