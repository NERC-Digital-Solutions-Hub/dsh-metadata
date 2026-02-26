# Final Report for LCM2007 - the new UK land cover map

- Overview
  - LCM2007 is the UK Land Cover Map for 2007, the third in the LCM series, produced by CEH (NERC) with Countryside Survey 2007 data and partners.
  - Provides a consistent, policy-relevant base for environmental monitoring, biodiversity, ecosystem services, landscape planning, and catchment management.
  - Maps land cover (not land use) against UK Biodiversity Action Plan Broad Habitats; delivers a continuous UK-wide vector framework with almost 10 million land parcels.

- Data and outputs
  - Data types:
    - Vector parcels with extensive metadata (area, source images, Broad Habitat, processing history, KBE).
    - 25 m raster with 23 LCM2007 classes.
    - 1 km raster products (two formats: percentage cover per class and dominant class per 1 km cell).
  - Spatial framework:
    - UK-wide parcel-based framework, GB and NI databases, MMU 0.5 ha, MFW 20 m.
    - Generalised boundaries based on OS MasterMap for GB and related data for NI; segmentation across multi-date composites.
  - Classification and enhancements:
    - Parcel-based supervised maximum likelihood classification using 37 composites and 21 single-date images.
    - Knowledge-based enhancements (seven automated rules) to reduce spectral confusion and refine habitat mapping.
  - Accessibility:
    - 1 km rasters via CEH Information Gateway.
    - Full vector and 25 m rasters available on license via CEH data portal; licensing and fees may apply.

- Accuracy, validation, and validation relationships
  - Ground reference validation: 9127 points; overall accuracy around 83% across LCM2007 classes.
  - Class-level variability: some classes show high accuracy, others are weaker due to spectral ambiguity and KBEs limitations (notably certain upland, montane, fen, and coastal types).
  - Comparisons with Countryside Survey (CS 2007):
    - 591 field squares used for comparison.
    - Broad Habitat (BH) correspondence roughly 62% at BH level; about 76% at Broad Habitat Association (BHA) level; ~67–70% at aggregate level depending on metric.
    - Grassland classes are problematic due to one-to-many relationships between observed land cover and BH classifications.
    - Coniferous Woodland shows strong correspondence; Broadleaved woodland and Arable/Horticulture generally align with some misclassifications (e.g., improved vs neutral grassland, woodland boundaries).
    - Fen, Marsh and Swamp is challenging spectrally; Montane habitats show relatively higher correspondence in BH/BHA.

- Dissimilar area estimates (4.3.2)
  - Dissimilar area (CS upper/lower 95% limits) observed for: Arable and Horticulture, Improved Grassland, Neutral Grassland, Dwarf Shrub Heath, Bog, Montane Habitats, and coastal habitats.
  - Key drivers:
    - Classification differences and what is included in Arable and Horticulture (e.g., boundary and linear features). LCM2007 may include boundary features within this class, inflating area.
    - Spectral confusion due to crop diversity, growth stages, and multiple-year image composites.
    - Differences in how grassland types are classified (Improved vs Neutral) and soil information limitations.
    - Fen, Marsh and Swamp areas are mosaics; CS often records small parcels that are below LCM MMU, causing large discrepancies.
    - Coastal and montane classifications affected by coastal proximity, terrain, and validation datasets.

- Discussion (4.3.3)
  - CS 2007 estimates are national extrapolations from field surveys; scaling and ITE Land Classes can influence comparisons with LCM2007.
  - Temporal range of imagery (multi-year composites) can cause fields to change class between seasons, affecting arable/grassland delineation.
  - Patch size and spatial structure differences (CS parcels often smaller than LCM MMU) influence area estimates for several habitats.
  - Fen, Marsh and Swamp differences are particularly sensitive to patch size and the mosaic nature of fen environments.

- UK Land Cover distribution and country variation (4.4)
  - UK-wide: over 50% of land in intensive agriculture (Arable and Horticulture + Improved Grassland) or Built-up Areas; forests cover about 12% (split roughly equally between Broadleaved and Coniferous).
  - Semi-natural and natural areas constitute about 30% of the UK; freshwater and mountain/heath/bog occupy smaller shares.
  - Country-level patterns:
    - England has the highest proportion of intensive land use (~76%: 40% Arable, 27% Improved Grassland, 9% Built-up).
    - Scotland has the largest share of Coniferous Woodland and the most semi-natural land (mountain/heath/bog and semi-natural grassland).
    - NI and Wales show intermediate levels of intensive land use.
  - Comparisons with LCM2000 indicate changes in Arable and semi-natural grassland shares; the spatial framework changes complicate direct temporal comparisons.

- Summary and discussion (4.5)
  - LCM2007 delivers a first continuous parcel-based UK-wide land cover dataset aligned with Broad Habitats, enabling long-term monitoring and policy evaluation.
  - Strong improvements from multi-date imagery and KBEs, notably for habitat-related mapping, but certain grassland, upland, and fen/marsh classes remain spectrally challenging.
  - Validation confirms solid overall accuracy, with class-dependent performance variability; comparison with CS provides useful, but imperfect, cross-validation for policy evaluation.
  - The integration with national cartography and a stable spatial framework supports future change detection, though methodological differences between LCM generations necessitate careful interpretation of changes.

- Change detection and methodological context
  - CEH highlights the complexity of cross-product change detection (LCM1990, LCM2000, LCM2007) due to differing spatial structures and classification schemes.
  - Suggests that future work may re-organise earlier CEH maps into a common spatial framework based on real-world land units to better support change detection.

- Example areas (5.1)
  - A set of illustrative areas across upland, calcareous grassland, urban, and fenland landscapes demonstrates LCM2007 performance in diverse habitat types and geographies (with references to figures illustrating each example).

- Access and contact
  - 1 km raster data: CEH Information Gateway.
  - Full vector and 25 m rasters: available on request via CEH data portal; licensing may apply.
  - Contact: spatialdata@ceh.ac.uk.

- Practical takeaways for analysts monitoring the environment
  - LCM2007 provides a detailed, UK-wide, cartography-based land cover resource aligned with Broad Habitats, suitable for long-term monitoring and policy analysis.
  - Multi-date image hardening and KBEs improve habitat mapping, but some grassland, upland, and fen/marsh classes remain spectrally ambiguous.
  - Validation shows robust overall accuracy with notable class-level differences; CS comparisons are informative but reveal limitations in fully reconciling products.
  - The dataset’s robust spatial framework and rich parcel-level metadata enable flexible quality assessment, reproducibility, and potential recalibration for specific study areas.
  - For change detection and policy evaluation, prefer aggregated class perspectives or reorganised cross-version comparisons to account for structural differences between LCM generations.