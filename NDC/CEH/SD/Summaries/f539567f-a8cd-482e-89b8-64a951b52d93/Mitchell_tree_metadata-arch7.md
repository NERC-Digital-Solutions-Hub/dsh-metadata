# Functional and epiphytic biodiversity differences between nine tree species in the UK.

## Overview
- A UK-wide study comparing functional and epiphytic biodiversity (bryophytes and lichens) across nine tree species, including disease-threatened Quercus petraea, Q. robur, and Fraxinus excelsior.
- Data collected across six sites with 230 trees to assess how tree species identity influences biodiversity, soil properties, bark characteristics, and decomposition processes.
- Aims to support GIS-based exploration of spatial patterns and species-level biodiversity functions.

## Study design and spatial scope
- Six sites across the UK: Knightshayes Court (England), Bodnant (Wales), Dinefwr (Wales), Westonbirt (England), Crathes (Scotland), Mount Stuart (Scotland).
- Sites chosen to include multiple individuals of target species and varied habitats (semi-natural woodland, parkland, gardens).
- Each site includes 35–40 trees; 230 trees in total, with species and site-level metadata (climate data, soil type, elevation, etc.).
- Spatial identifiers include GPS and British National Grid coordinates (X-cord, Y-cord) for each tree.

## Data collected per tree and site
- Tree data: species, tree tag numbers, GPS/BNG coordinates, slope, aspect, height, DBH; habitat around tree (semi-natural woodland, garden, parkland); four cardinal sectors around the tree; distance to nearest tree.
- Bark and chemistry: bark samples for pH, water holding capacity, and conductivity; bark pattern and physical characteristics (pattern type, fissures, ridges, bark hardness); bark sampled at multiple heights.
- Lichen and bryophytes: presence/absence data for taxa on trunk (ground level to 1.75 m) and, where possible, branches and twigs.
- Decomposition: litterbag experiments (filter papers) placed near trees to measure decomposition rates over time; temperature and decomposition-related measurements recorded.
- Soil analyses: eight soil samples per tree for mineralized N, total C and N, pH in water and CaCl2, LOI, and bulk properties; FTIR spectral measurements on processed soil; soil sample data linked to each tree.
- Canopy and microhabitat: percent canopy cover estimates around each tree on north, east, south, and west aspects.
- Additional measurements: iButton soil temperature loggers placed near each tree; date and collector metadata; notes on collection and relocation (where applicable).

## Data model and access
- Data organized as a relational dataset designed for a database (central Trees table linking to related data files).
- Related tables/files include: Habitats_structure, Decomposition, Temperature, Soil, FTIR, Bark_chemistry, Bark_plot, Bryophytes, Lichens, plus lookup tables Bryophyte_names and Lichen_names.
- Key linking field: ANS_Tree_code (primary key for trees) with cross-links to all other tables.
- Access format specified as a relational database (Microsoft Access) for integrated querying and GIS-ready joins.
- Metadata and table descriptions provided for each file (Tables 1–14 detail site data, tree data, habitat structure, decomposition, temperature, soil, FTIR, bark chemistry, bark plot, bryophyte and lichen data).

## Implications for GIS and data products
- Enables creation of map-based visuals: distribution of tree species, DBH/total height, bark characteristics, canopy cover, and lichen/bryophyte presence across sites.
- Spatial analysis opportunities: correlation of biodiversity indicators with tree species, site climate, soil properties, and bark traits; potential hotspot mapping for epiphytic communities.
- Time- and condition-aware mapping possible through date fields and decomposition/temperature measurements; integration with soil chemistry layers and FTIR-related spatial patterns.
- Supports multi-layer GIS products by joining central Trees table with Habitat_structure, Canopy, and species-specific biodiversity records.

## Data quality, challenges, and usage notes
- Data synthesized from multiple sources and resolutions; QA, cleaning, and data transformation are essential steps prior to GIS use.
- Some limitations: lichen/bryophyte sampling restricted to accessible parts of trees; not all trees had functioning iButtons; some data (e.g., branches) limited by reach.
- The dataset is designed for relational querying to support robust spatial analyses and reproducible maps.

## How to use in a GIS workflow
- Import the relational dataset and join tables via ANS_Tree_code to build a unified feature set per tree.
- Map core GIS-ready fields: site, species, DBH/Height, coordinates (BNG), canopy cover by direction, habitat type, bark pattern/texture, and lichen/bryophyte presence.
- Create thematic layers: biodiversity indicators by species, habitat-structure effects, soil chemistry distributions, and decomposition metrics over time.
- Integrate soil temperature data (iButton) and FTIR/ bark chemistry results as auxiliary raster or tabular layers linked to tree positions for advanced analysis.
- Leverage metadata tables to understand variable definitions and unit scales for accurate visualization and analysis.

## Summary of key outputs and references
- Primary dataset supports comparative analyses of functional and epiphytic biodiversity among nine tree species across six UK sites.
- Data descriptions, site details, and variable metadata are comprehensively documented (Tables 1–14) to facilitate data reuse and GIS integration.
- Funded by Defra through PuRpOsE (BB/N022831/1) with additional Scottish Government support.