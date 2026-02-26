# Kākāpō Egg Fertility 2019: Documentation

## Overview
- Dataset describing origin, fertility, and physical characteristics of kākāpō eggs laid in New Zealand during the 2018/19 breeding season.
- Eggs were laid in natural nests, then artificially incubated as part of the Kākāpō Recovery Programme; undeveloped eggs were preserved, transported to the University of Sheffield, and analyzed to determine fertilization status and early embryo mortality.
- Key findings include that 252 eggs were laid, with 129 failing to develop; analyses included counting sperm on the perivitelline layer (PVL) and fluorescence microscopy of yolk samples.

## Datasets Included
- Kakapo_egg_fertility_2019-1_all_eggs: 252 rows, 10 columns; data on all eggs laid in the season.
- Kakapo_egg_fertility_2019-2_undeveloped_eggs: 129 rows, 15 columns; data on undeveloped eggs/ yolk samples transported to Sheffield.
- Both datasets share egg_id as a key field for merging.

## Key Fields and Data Structure
- File 1: kakapo_egg_fertility_2019-1_all_eggs
  - egg_id, island, mother, clutch, developed, early_EM, fertile, examined, female_multiple_males, female_AI
- File 2: kakapo_egg_fertility_2019-2_undeveloped_eggs
  - egg_id, egg_number, fertilized, PVL_sperm, PVL_holes, PVL_area_mm, mean_sperm_mm, note, length, width, preserve_weight, fresh_weight, alb_weight, yolk_weight, shell_weight
- Key linking field: egg_id (enables merging the two files if needed)

## Spatial Context and GIS Relevance
- Spatial units are the two breeding islands: Anchor Island and Whenua Hou (Codfish Island).
- Geographic coordinates for the study population are provided for context; egg-level spatial positions are not included, enabling GIS users to join eggs to island-level polygons or broader habitat layers.
- Potential GIS uses: map fertility status by island, visualize egg distribution across nests, join with habitat or ecological layers (food abundance, predator presence), and analyze spatial patterns in relation to management actions.

## Data Collection & Analysis Methods
- Daily candling during artificial incubation to identify embryos; undeveloped eggs opened, yolks preserved in formalin, shipped to Sheffield.
- In Sheffield: yolks examined for embryonic cells; PVL inspected for sperm presence; PVL_sperm, PVL_holes, PVL_area_mm recorded; fertilization status inferred.
- Additional egg metrics collected: dimensions (length, width) and weights (preserve, fresh, albumen, yolk, shell).

## Provenance and Governance
- Funded by Natural Environment Research Council Urgency Grant (NE/T00200X/1).
- Principal Investigator: Dr Nicola Hemmings; Researcher Co-Investigator: Dr James Savage.
- Kiwi programme leads: Dr Jodie Crane and Kākāpō Recovery Team; broader KRT staff contributed.
- NZ Department of Conservation maintains additional population and management data beyond these files.

## Data Quality and Limitations
- Data include binary and numeric fields with some missing values (e.g., fertilized status can be NA in undeveloped eggs).
- 98% of undeveloped eggs associated with samples; dataset captures both complete egg data and detailed undeveloped-egg analyses.
- Some fields reflect observational notes (note) and may require careful interpretation during analysis.

## Usage and Integration Guidance for GIS Specialists
- Use egg_id to join the two datasets when integrating fertility results with physical egg characteristics.
- Align island values with spatial boundaries for Anchor and Whenua Hou; consider linking to island shapefiles for choropleth or point-density mapping at nest-level proxies.
- Leverage fields such as developed, fertilized, and PVL-based fertilization status to create thematic maps of fertility outcomes by nest or island.
- Validate consistent naming conventions for islands (anchor, whenua_hou) when merging with external spatial datasets.
- Potential to integrate with broader population and management data from the NZ Department of Conservation for multi-layer analyses over multiple seasons.