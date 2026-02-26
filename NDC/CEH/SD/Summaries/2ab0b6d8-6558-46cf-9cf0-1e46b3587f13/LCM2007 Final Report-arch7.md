# Final Report for LCM2007 - the new UK land cover map

## Overview of key findings (4.3.x sections)

- Dissimilar area estimates (4.3.2)
  - Classes with dissimilar UK-area estimates beyond the Countryside Survey (CS) 95% confidence limits: Arable and Horticulture, Improved Grassland, Neutral Grassland, Dwarf Shrub Heath, Bog, Montane Habitats, and coastal habitats.
  - Main causes for discrepancies:
    - Differences in what CS vs LCM2007 classify as Arable and Horticulture (including boundary and linear features in LCM2007).
    - Spectral confusion due to the broad spectral variability of arable crops and growth stages.
    - Inclusion of boundaries/linear features in LCM2007’s Arable and Horticulture class, inflating area.
    - Temporal mismatch: LCM2007 images span multiple years, increasing fields that change between temporary grassland and arable across years.
    - Boundary/delineation differences between CS field maps and LCM2007 MMU framework.
    - Grassland confusion: Improved vs Neutral grassland; soil data have limited utility for distinguishing Neutral vs Improved grassland.
    - Dwarf Shrub Heath vs Bog, Montane Habitats vs upland differences, and Fen, Marsh, Swamp areas are particularly sensitive to classification approach.
- Discussion (4.3.3)
  - Agreement between LCM2007 and CS varies by Broad Habitat; grassland categories are especially challenging due to one-to-many relationships.
  - LCM2007 shows high correspondence with CS 2007 for 1 km squares in Arable and Horticulture, but overall Broad Habitat extents tend to be higher in LCM2007 for Arable and Horticulture.
  - Fen, Marsh and Swamp estimates differ by an order of magnitude due to mixed land-cover types, small patch sizes, and spectral limitations; many CS fen areas map to Rough Grassland or Acid Grassland in LCM2007.
  - Patch size effects: CS parcels below LCM2007 MMU can substantially influence comparisons for several habitats.
  - The report emphasizes the need for a common spatial framework and potential KBEs to allocate certain grassland areas to Fen, Marsh and Swamp in future work.
- UK Land Cover (4.4)
  - Overall UK distribution: More than 50% of the UK is intensive land use (Arable and Horticulture + Improved Grassland) or Built-up Areas; ~12% Broadleaved and Coniferous Woodland; ~30% semi-natural (including Mountain, Heath and Bog, and semi-natural grassland); minor coastal and freshwater shares.
  - Country differences:
    - England: ~76% intensive land-use (40% Arable and Horticulture, 27% Improved Grassland, 9% Built-up Areas and Gardens).
    - Scotland: largest share of Coniferous Woodland; highest semi-natural land (36% Mountain, Heath and Bog; 20% semi-natural grassland); lower overall intensive land-use (36%).
    - Northern Ireland and Wales: around 64% intensive land-use.
  - Temporal/spatial framework changes: LCM2007 and LCM2000 comparisons show increases in Arable (26% vs 23%) and slight shifts in semi-natural grassland; conifer woodland modestly increased; urban area slightly reduced; exact magnitudes depend on spatial framework changes.
  - LCM2007 vs CS 2007 comparisons (Tables 4.8–4.9): CS 2007 and LCM2007 show mixed agreement across Broad Habitats; some categories fall within CS 95% limits, others exceed or fall below; Fen and related water/grassland classes show notable discrepancies; Grassland categories are particularly sensitive to classification boundaries and MMU effects.
  - Important caveat: Countryside Survey uses field-based, multi-method approaches while LCM2007 relies on satellite imagery and knowledge-based enhancements; direct one-to-one area matches are hampered by methodological differences.
- Summary implications (4.5)
  - Agreement between LCM2007 and CS varies by habitat, with grassland being the most problematic class due to one-to-many mappings and spectral variability.
  - LCM2007 aligns well with CS for certain key classes (e.g., Arable and Horticulture in 1 km squares) but tends to overestimate some broad habitats when aggregating to UK-wide extents.
  - Fen, Marsh and Swamp show the largest divergences, highlighting the need for additional data or KBEs to better allocate mosaic habitats.
  - The UK-wide spatial framework of LCM2007 provides a common reference for national-scale monitoring, but users should apply caution when interpreting differences with field-based surveys, particularly for grasslands and upland habitats.

## Data and spatial framework implications for GIS practice

- Data structure and scales
  - LCM2007 provides 23 thematic classes mapped to Broad Habitats, with both vector parcels and raster products (25 m and 1 km).
  - MMU and MFU constraints influence when features are mapped; boundaries below MMU are often incorporated into surrounding polygons, affecting area estimates for some classes.
- Sources and alignment
  - Uses national cartography (OS MasterMap, LPS Large-scale Vector) for a continuous UK vector framework; supports integration with other national datasets and consistent change detection across the UK.
- Change detection and validation considerations
  - Direct comparison with field-based CS is complex due to methodological differences; aggregate or trajectory-based change analysis may be more robust than pixel-for-pixel comparison.
  - KBEs and knowledge-based enhancements improve thematic resolution but require careful validation, especially for grassland and mosaic habitats.
  - The presence of boundary and linear features in LCM2007’s Arable and Horticulture class can inflate areas and affect downstream analyses if not accounted for.
- Practical guidance for GIS workflows
  - When combining with field data or other national datasets, consider using the 1 km rasters for broad-scale modelling and the 25 m rasters or vector data for finer-scale mapping and inspection.
  - Be aware of differences in spectral signatures across growth stages, crop types, and phenology; use KBE histories and probability lists to inform uncertainty.
  - For grassland analyses and habitat-change monitoring, anticipate potential misclassifications between Improved, Neutral, and Calcareous/Acid Grasslands; consider supplementary KBEs or local calibration.

## Key data availability and access (relevant to GIS work)

- 1 km raster data (UK-wide) available via the CEH Information Gateway.
- Full vector product and 25 m raster product available on request under licence from CEH (fees may apply).
- For data queries: CEH Information Gateway, data licensing at www.ceh.ac.uk/data, and spatialdata@ceh.ac.uk.