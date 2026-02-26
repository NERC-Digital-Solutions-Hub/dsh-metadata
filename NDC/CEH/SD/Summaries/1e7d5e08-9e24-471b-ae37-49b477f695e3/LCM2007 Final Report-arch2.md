# Final Report for LCM2007 - the new UK land cover map

## Overview for environmental analysts
- Provides a continuous UK-wide land cover map (LCM2007) with 23 land cover classes, mapped to 17 Broad Habitats, plus vector and raster data at 25 m and 1 km resolutions.
- Built to support habitat monitoring, biodiversity assessment, landscape planning, and ecosystem services analysis; designed as a baseline for long-term policy evaluation and change detection.
- Combines multi-temporal satellite imagery (70+ images forming 34 composites) with a national cartographic spatial framework (OS MasterMap and LPS) and knowledge-based enhancements.
- Output formats include a detailed vector parcel dataset (with 10 processing attributes and Broad Habitat sub-classes), 25 m rasters (23 classes), and 1 km summary rasters (percent cover or dominant class). Access via CEH gateway or by licence on request.

## Data, methods and spatial framework
- Data and processing
  - Parcel-based land cover map produced by supervised classification on 34 composites plus single-date images; 9% from single-date imagery; 0.5% manually filled.
  - 9,127 ground reference points used for training/validation; knowledge-based enhancements (KBEs) applied post-classification (affecting ~20% of parcels) to improve spectral coherence and boundary delineation.
  - Spatial framework anchored to national cartography with a minimum mappable unit of 0.5 ha and minimum feature width of 20 m (GB); NI data integrated where available.
- Outputs and access
  - Vector product: 23 land cover classes linked to 17 Broad Habitats; includes 10 attributes documenting processing steps (Construct, ProbList, KBE, etc.).
  - Raster products: 25 m resolution with 23 classes; 1 km rasters summarise cover by either percentage or dominant class.
  - Access specifics: 1 km rasters via CEH gateway; full vector and 25 m data available on licence by request (licence fees may apply).

## Dissimilar area estimates: comparison with Countryside Survey (CS) 2007 (Chapter 4.3.2)
- Defined dissimilar areas (differences beyond UK CS 95% confidence limits) occur for:
  - Arable and Horticulture
  - Improved Grassland
  - Neutral Grassland
  - Dwarf Shrub Heath
  - Bog
  - Montane Habitats
  - Coastal habitats
- Key factors driving dissimilarities
  - Classification definitions: differences in what CS vs. LCM2007 include in each class (e.g., inclusion of boundary/linear features in LCM2007’s Arable and Horticulture).
  - Spectral confusion: high spectral variability for grassland and arable types due to multiple crops, growth stages, and multi-year imagery; misclassification risk where signatures are underrepresented in training data.
  - Boundary and MMU differences: CS maps include many features below LCM MMU; LCM2007 integrates boundary features into field polygons, affecting area estimates.
  - Temporal range: LCM2007 requires multi-year imagery; fields changing between temporary grass and arable across years can bias arable estimates.
  - Habitat-specific issues: Neutral vs Improved Grassland classifications; Dwarf Shrub Heath vs Bog allocations; Fen, Marsh and Swamp reconstruction challenges due to mosaic nature and small patches.
- Illustrative UK-wide results (examples)
  - Arable and Horticulture: CS UK area ~46,574 km2; DEFRA 2007 ~46,090 km2 for arable plus horticulture; CS upper limit ~51,276 km2; LCM2007 ~63,005 km2 (likely due to temporary grass, uncropped land, and boundary features, plus multi-year image requirements).
  - Temporary grass and uncropped land contributions likely inflated LCM2007’s Arable and Horticulture class.
  - Spectral variability in arable crops leads to overestimation in some regions where arable signatures dominate.
  - Boundary/linear features often split differently, increasing field sizes in LCM2007 relative to CS.
  - Fen, Marsh and Swamp estimates differ by an order of magnitude; CS maps mosaics often recorded as Rough Grassland or other grassland types in LCM2007, reflecting classification complexity.
  - Montane, intertidal and coastal habitats show substantial differences given divergent field surveys and coastal/montane data structures.
- 4.3.3 Discussion highlights
  - Agreement between LCM2007 and CS varies by Broad Habitat; grassland mapping is particularly challenging due to one-to-many relationships.
  - KBEs and the BH association framework help, but do not fully align satellite-based classifications with field-based Broad Habitats.
  - LCM2007 aligns well with CS 1 km squares for Arable and Horticulture, but Broad Habitat extents can diverge due to thematic aggregation and spatial structure differences.
  - Fen, Marsh and Swamp show large UK-scale differences due to mosaic nature and patch size; potential future work could use additional data to allocate some of these areas to Fen via KBEs.

## UK-wide land cover: summary and country-level differences (Chapter 4.4)
- National distribution (UK)
  - More than 50% of the UK is intensive land use (Arable and Horticulture + Improved Grassland) or Built-up Areas and Gardens.
  - Woodlands ~12% (split between Broadleaved and Coniferous).
  - Remainder is semi-natural (including Mountain, Heath and Bog; semi-natural grassland) and small fractions of Coastal and Freshwater.
- Country patterns
  - England: highest intensive land use (~76%; ~40% Arable and Horticulture, ~27% Improved Grassland, ~9% Built-up).
  - Scotland: largest share of Coniferous Woodland; substantial semi-natural areas (36% Mountain, Heath and Bog; 20% semi-natural grassland).
  - Wales and Northern Ireland: high proportions of intensive land use compared with Scotland; NI includes montane/habitat variations and separate montane sub-strata.
  - Freshwater share differs (Wales ~1%, England ~4%, Scotland ~2%, NI ~4%) due to hydrogeography (e.g., Lough Neagh).
- Comparisons with LCM2000
  - LCM2007 shows 26% Arable and 13% semi-natural grassland vs LCM2000’s 23% and 17%, respectively; conifer woodland modestly increases; urban share slightly lower than LCM2000.
- Data interpretation notes
  - Spatial framework changes and data sources complicate direct change detection across versions; careful methodological alignment is required for trend analyses.

## Product scope, purpose and use for monitoring
- Core outputs for monitoring
  - Stock estimates and distributions of Broad Habitats for the UK, GB, four countries, and NI.
  - Availability of both high-resolution (25 m) and coarse-scale (1 km) rasters for modelling and policy evaluation.
  - Vector data with detailed metadata enabling traceability of processing steps, plus a cross-walk to Countryside Survey.
- Practical use for analysts
  - Baseline for habitat extent, fragmentation, and land-cover change over time.
  - Contextual base map for higher-resolution habitat mapping, ecological connectivity analyses, and policy planning (e.g., woodland expansion, Natura targets).
  - Comparable framework with CS data, including guidance on harmonisation approaches (e.g., aggregating grassland classes).

## Validation, validation tools and quality assurance
- Bespoke validation approach (Appendix 4)
  - Acknowledges there is no absolute truth in geography; “fit for purpose” assessment is essential.
  - Parcel-level metadata enables inspection of knowledge-based enhancements and spectral variant probabilities for target classes.
  - Recommends qualitative validation using high-resolution imagery (e.g., Google Earth) to assess consistency with LCM2007 at parcel level.
  - Encourages a two-part assessment: high-probability and moderate-probability parcels; suggests fuzzy categorisation (plausible, probably, possibly) to derive upper/lower accuracy estimates.
- Broad Habitat Association (BHA) rules (Appendix 5)
  - Documents how LCM2007 classes correspond to CS Broad Habitats and how certain mosaics (e.g., Fen, Marsh and Swamp, Montane vs. grasslands) are reconciled at BH adjacency and other levels.
  - Provides reciprocal rules and caveats to support cross-walks and interpretability when comparing datasets.

## Accessibility and data licensing
- Access points
  - 1 km raster datasets via CEH Information Gateway.
  - Full vector and 25 m raster products available on licence by applying through CEH; some applications may incur licence fees.
- Data formats
  - Vector: land parcels with attributes including BH, sub-classes, KBE history, ProbList, etc.
  - Raster: 25 m (23 LCM2007 classes) and 1 km rasters (percentage or dominant class).

## Practical implications for policy and monitoring
- LCM2007 provides a robust, repeatable UK-wide land cover baseline suitable for long-term environmental health assessment, habitat monitoring, and landscape planning.
- KBEs and the strengthened spatial framework improve interpretability and applicability for habitat monitoring, ecological connectivity, and catchment management.
- Users should be mindful of uncertainties arising from spectral variability (notably grasslands and arable crops), boundary feature handling, and differences in spatial structure when comparing with Countryside Survey or previous CEH maps.
- For change detection, consider aggregating to BHAs or broader aggregates, and be prepared to account for methodological differences across LCM releases; integrating LCM2007 with CS or other data sources enhances interpretation.

## Endnotes and recommendations for analysts
- When comparing LCM2007 to CS, use broad Habitat associations or aggregated classes to improve comparability; be cautious with grassland classes due to one-to-many relationships.
- For Fen, Marsh and Swamp, expect major differences; consider applying KBEs or auxiliary data to reallocate mosaic areas to Fen where appropriate.
- Use the parcel-level metadata and ProbList to assess the plausibility of classifications in location-specific monitoring studies.
- In long-term monitoring, align spatial frameworks and class definitions across time to facilitate reliable change detection and policy evaluation.