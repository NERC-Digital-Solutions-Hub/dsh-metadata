# Table 1. Broad Habitats and their relation to LCM2000 Target classes, Subclasses and Variants (the Suclasses are shown in their map display colours).

- The document provides a cross-walk between Broad Habitats and the LCM2000 Target Classes, Subclasses, and Variants, with Suclasses indicated by map colours.
- It includes numerous rows linking habitat types (e.g., inshore sublittoral, standing water, littoral/seabed habitats, various woodland and grassland types, urban and coastal interfaces) to the LCM2000 Target Class, Subclass, and Variant codes, including variants such as rock, mud, algae, saltmarsh, bog, montane habitats, arable, horticultural, and built-up categories.

## Purpose and scope (context for data work)

- Enables consistent mapping between broad habitats and the LCM2000 taxonomy to support data integration, analysis, and product creation across UK regions.
- Assists in understanding how LCM2000 data align with field classifications and where discrepancies may arise (e.g., coastal, urban, montane, and patchy data areas).

## Data sources and methodologies used (context for data practitioners)

- Basis: LCM2000 (Land Cover Map 2000) with cross-walk to CS2000 field survey concepts.
- Data granularity and basis: 25 m grid for LCM2000 statistics; field survey statistics (FS) referenced in footnotes (Haines-Young et al. 2000).
- Regional coverage: England, Wales, Scotland, Northern Ireland, and GB as aggregated units.
- Notes on quality and comparability: differences between LCM2000 and FS statistics are explained in the text; coastal coverage varies due to tidal states and offshore area inclusion.

## Key tables and what they show (data products and validation)

- Table 5: Coverage (km2) of Subclasses from LCM2000 and of Aggregate classes from LCM2000 and field survey (FS) in the UK and constituent countries.
  - Provides UK- and country-level area figures for major classes (e.g., Broad-leaved/mixed woodland, Coniferous woodland, Arable cereals, Arable & Horticultural, Improved grassland, Neutral/Calcareous/Acid grasslands, Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog, Standing open water, Built up areas, etc.).
  - Illustrative examples:
    - Broad-leaved/mixed woodland: UK LCM2000 15,600 km2; UK FS 15,220 km2 (England ~10,963; England FS ~11,710; Scotland ~2,687; Scotland FS ~3,000; NI ~341; NI FS ~510).
    - Arable & Horticultural: UK LCM2000 ~57,630 km2; UK FS ~53,070 km2 (England & Wales ~49,296; FS ~46,090; Scotland ~7,342; NI ~992).
    - Improved grassland: UK LCM2000 ~59,073 km2; UK FS ~60,500 km2 (England ~31,983; Scotland ~10,326; NI ~9,049; Wales ~7,738).
  - Indicates that LCM2000 and FS provide complementary area estimates with regional variation and some differences in totals.

- Table 6: LCM2000 cover (uncalibrated) for BHs (Broad Habitats) by England, Wales, Scotland, Northern Ireland and GB, compared with field survey estimates at 95% confidence (i.e. +/- 2 standard errors).
  - Presents UK-wide and country-level LCM2000 values alongside FS lower and upper bounds for major habitats (e.g., Broadleaved/mixed and yew woodland; Coniferous woodland; Arable and horticulture; Improved grassland; Neutral/Calcareous/Acid grasslands; Bracken; Dwarf shrub heath; Fen/marsh/swamp; Bog; Montane habitats; Inland rock; Built up areas and gardens; Supralittoral and Littoral categories; etc.).
  - Example GB figures:
    - Broadleaved/mixed and yew woodland: LCM2000 15,259; FS Low 12,750; FS High 16,670.
    - Coniferous woodland: LCM2000 12,879; FS Low 10,672; FS High 16,808.
    - Arable & Horticulture: LCM2000 56,638; FS Low 47,944; FS High 57,036.
    - Improved grassland: LCM2000 50,024; FS Low 50,936; FS High 59,104.
    - Neutral grassland: LCM2000 10,770; FS Low 5,046; FS High 7,214.
  - Notes: FS estimates include regional confidence intervals; coastal and urban generalisation issues are highlighted; differences between LCM2000 and FS are discussed in the accompanying text.

- Table 8, Table 9, Table 10: Summary correspondence matrices (results expressed per 1000 in GB; England & Wales; Scotland) comparing LCM2000 with CS2000 field survey squares.
  - Show correspondences between LCM2000 broad habitats, target classes, and aggregate classes with CS2000 classifications.
  - Indicate patterns of agreement and misalignment across major habitat groups, including how urban/generalised urban classes map to suburban/urban CS2000 equivalents and where cross-walking is more ambiguous (e.g., montane, inland rock, supralittoral categories).
  - Useful for data quality assessment and for designing data products that rely on cross-dataset compatibility.

- Footnotes and caveats (relevant for data modelling and QA):
  - LCM2000 statistics based on a full count of cover on a 25 m grid; FS statistics from Haines-Young et al. 2000.
  - Some figures labeled as n/a (not available); differences between LCM2000 and FS are explained in the text.
  - Coastal coverage is variable due to tidal states and offshore-intertidal inclusion/exclusion.
  - NI-specific BHs may be excluded from survey in certain totals.
  - Generalisation of urban areas is noted in cross-dataset correspondences.

## Practical implications for Data Support work

- Data integration and product design
  - Use the cross-walk (Table 1) to align LCM2000 outputs with other data sources and with CS2000 field classifications.
  - Leverage Table 5 and Table 6 to validate, calibrate, and QA regional and national land-cover estimates; build dashboards showing country-level comparisons and uncertainty bands.
  - Use Tables 8–10 to understand where LCM2000 and CS2000 agree or diverge, informing data fusion strategies and uncertainty modeling.

- Data quality and uncertainty management
  - Acknowledge coastal complexities and urban generalisation when merging LCM2000 with field data; apply region-specific adjustments or explain discrepancies in any data product.
  - Incorporate 95% confidence intervals (Table 6) into reports and dashboards to communicate reliability to end users.

- Data product ideas for end users
  - Interactive maps showing LCM2000 target classes with links to corresponding Broad Habitats and Variants.
  - Dashboards comparing LCM2000 vs FS/CS2000 by habitat type, country, and region, with uncertainty ranges.
  - Reports highlighting major alignment and misalignment areas to guide data interpretation and decision-making.

- Data preparation and reproducibility
  - When reproducing analyses, reference the 25 m grid basis for LCM2000 statistics and the bootstrapping approach used for CS2000 comparisons.
  - Document coastal definitions and urban generalisation rules used in cross-dataset mappings.

## Summary takeaway for a Data Support perspective

- The document provides a comprehensive cross-walk between Broad Habitats and LCM2000 taxonomies, along with extensive UK-wide and country-level area statistics and validation against field survey data (CS2000/FS).
- It supports data integration, quality assessment, and the development of user-facing data products by clarifying how habitats map to LCM2000 targets, how well LCM2000 aligns with field data, and where uncertainty and methodological differences lie.
- Practical use includes guiding dashboards, validation workflows, and transparent communication of data reliability to stakeholders.