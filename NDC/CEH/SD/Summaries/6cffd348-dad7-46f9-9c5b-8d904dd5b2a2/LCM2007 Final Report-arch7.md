# Final Report for LCM2007 - the new UK land cover map

- Reports dissimilar area estimates between LCM2007 and Countryside Survey (CS) 2007 across several broad habitat classes, driven by classification definitions, spectral variability, boundary feature handling, and spatial structure differences.
- Highlights key numeric contrasts:
  - Arable and Horticulture: CS GB area ~46,574 km2; DEFRA/CS comparisons around 46,090 km2 vs CS upper/lower limits; LCM2007 ~63,005 km2, with overestimation linked to temporal image range, spectral variability, and inclusion of boundary/linear features in LCM2007.
  - Improved Grassland and Neutral Grassland: LCM2007 shows ~10,000 km2 more Improved Grassland and ~10,000 km2 less Neutral Grassland than CS, largely due to how neutral vs improved grassland are spectrally distinguished and soil information limitations.
  - Dwarf Shrub Heath and Bog: differences arise from allocation between habitats; montane representations affect counts.
  - Fen, Marsh and Swamp: CS 2007 estimates are far higher than LCM2007 (CS ~4,392 km2 UK vs LCM2007 ~101 km2) due to mosaic nature of fen areas and spectral/scale handling; many CS fen areas map to Rough Grassland or Acid Grassland in LCM2007.
- Discussion on CS comparison:
  - Grassland categories cause the largest variability because grass is present in multiple Broad Habitats; Broad Habitat Association (BHA) rules were developed to quantify correspondences beyond the Broad Habitat level.
  - LCM2007 shows strong correspondence with CS 2007 for 1 km squares in Arable and Horticulture, but overall Broad Habitat extents are broader in LCM2007, suggesting substantial differences in how areas are classified at different scales and schemes.
- UK Land Cover distribution (summary for the UK and country-level variation):
  - More than 50% of the UK across Arable and Horticulture plus Improved Grassland or Built-up Areas and Gardens; roughly 12% Broadleaved and Coniferous Woodlands combined; around 30% semi-natural across various habitats.
  - England shows the highest share of intensive land use; Scotland has the largest share of Coniferous Woodland and the greatest extent of Mountain/Heath habitats; Northern Ireland has montane and intertidal representations that differ from the other nations.
- Data products and access (Section 4.4):
  - 1 km raster products: percentage cover and dominant class (UK, GB, England, Scotland, Wales, Northern Ireland).
  - Full vector and 25 m raster products: available on request under licence; license fees may apply.
  - Vector product includes 23 LCM2007 classes with extensive metadata and processing history; 25 m raster provides equivalent land cover detail; 1 km rasters derived from 25 m with either percentage or dominant-class summaries.
- Heritage and context (brief):
  - LCM2007 is the third CEH land cover map in the series, adopting a cartography-derived spatial framework to enable improved change detection and cross-map comparisons with LCM1990 and LCM2000.
- Relevance for GIS work:
  - LCM2007 provides UK-wide parcel-based (vector) land cover with a robust 0.5 ha MMU and rich polygon metadata, plus 25 m and 1 km raster products for scalable GIS analyses, data fusion, and change detection.
  - Knowledge-based enhancements (KBEs) and Broad Habitat sub-classes offer refined thematic resolution with an auditable history for each polygon.
  - A continuous UK-wide vector framework reduces boundary inconsistencies and supports consistent GIS analyses and policy support.

- Accessing data (practical steps for GIS users):
  - 1 km raster products (percent cover and dominant class) accessible via the CEH Information Gateway.
  - Full vector and 25 m raster products available on request under licence from CEH; licensing fees may apply.
  - Contact: spatialdata@ceh.ac.uk or CEH data portal (gateway.ceh.ac.uk).

- Discussion: change detection and methodological considerations (Chapter 6):
  - LCM2007’s distinct spatial structure from previous maps necessitates sophisticated change-detection approaches to separate real change from methodological differences.
  - A common spatial framework facilitates future national monitoring, but cross-map change assessment remains challenging without re-organising earlier CEH maps into a common framework.
  - LCM2007 and CS complement each other: CS provides field-based validation and habitat quality context; LCM2007 offers coast-to-coast coverage and temporal stock distributions ideal for policy, planning, and large-scale modelling.

- Bespoke validation and interpretation (Appendix 4):
  - Emphasises fit-for-purpose accuracy rather than absolute truth.
  - Parcel-level metadata enables users to inspect KBE histories and top spectral variants; suggests informal Bayesian-style validation using high-resolution imagery to assess plausibility.
  - Recommends reporting results with two-part categories (e.g., plausible, probably) to quantify uncertainty.

- Broad Habitat Association (Appendix 5):
  - Provides rules for cross-walk between LCM2007 classes and CS Broad Habitats (BH) to interpret correspondences at multiple thematic levels.
  - Highlights complexities in matching mosaic and transitional habitats (e.g., Bog, Dwarf Shrub Heath, Montane Habitats) and the non-reciprocal nature of some correspondences.
  - Recognises challenges with Fen, Marsh and Swamp due to mosaics and scale, and outlines RBAs for water and boundary features.

- Additional notes and context (selected points from the appendices):
  - Notes on class definitions and special-case mappings (e.g., Rough Grassland, Boundary and Linear Features, temporary grassland, Coastal vs. Inland water) influencing CS vs. LCM2007 comparisons.
  - The report underscores the importance of integrating multiple data sets (soil, topography, urban contexts, coastal proximity) to achieve robust thematic separation and improved change detection.