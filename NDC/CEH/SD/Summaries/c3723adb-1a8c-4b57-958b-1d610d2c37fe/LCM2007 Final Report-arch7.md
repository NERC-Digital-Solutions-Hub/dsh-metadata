# Final Report for LCM2007 - the new UK land cover map

- The report documents the creation of LCM2007, a UK-wide, parcel-based land cover map with accompanying 25 m raster and 1 km summary products, designed for GIS users and policy-relevant analyses.
- It introduces a robust spatial framework aligned with real-world land units, and applies knowledge-based enhancements to improve thematic resolution within a UK-wide context.

## Key data products and formats for GIS use

- Vector product: 23 LCM2007 classes mapped to 17 Broad Habitats, with 10 Aggregate classes for some analyses; polygons carry rich metadata on processing steps and history.
  - Attributes include: BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, ProbList, KBE history, Construct, CorePixels, and related processing notes.
- Raster products:
  - 25 m raster: 23 LCM2007 classes.
  - 1 km raster: two summaries per pixel for each class:
    - Percentage cover (for each LCM2007 class).
    - Dominant class per pixel.
- Minimum mapping unit and scaling:
  - Minimum mappable unit ~0.5 ha; segmentation and MMU design used to balance detail with manageability.
- Accessibility:
  - 1 km raster datasets available via CEH Information Gateway.
  - Full vector product and 25 m raster available on license from CEH (licensing may apply).

## Spatial framework and data sources

- Base cartography:
  - Great Britain: OS MasterMap topography generalized to MMU and feature width constraints; integration with agricultural boundaries and image segments.
  - Northern Ireland: NI LPS polygons generalised and integrated with image segments; segmentation supports urban/rural delineation.
- Spectral data and processing inputs:
  - Multi-date and multi-sensor composites (Landsat TM/ETM+, SPOT-4/5, and LISS-III/AWIFS) with cloud masking, atmospheric correction, and topographic corrections.
- Ancillary data:
  - Ground reference points, Countryside Survey extents, soils, DEMs (NEXTMap Britain/NI), urban extents, agricultural boundaries, and other thematic layers.

## Processing workflow and knowledge-based enhancements

- Pre-processing and segmentation:
  - Image import, cloud/shadow masking, atmospheric correction, geo-registration, topographic correction, and creation of spectral composites.
  - Image segmentation to form segments; integration with vector cartography and agricultural boundaries to improve delineation.
- Classification:
  - Parcel-based supervised maximum likelihood classification using 37 composites and 21 single-date images; training data from ground references.
- Knowledge-based enhancements (KBEs):
  - Contextual rules to resolve spectral ambiguities (terrain, soils, coastal proximity, urban context, etc.).
  - Refined classifications with approximately 20% of parcels reclassified via KBEs.
  - Original spectral classifications retained in ProbList to allow reversion if needed.
  - Grassland differentiation and coastal/urban context handling to improve thematic accuracy.
- Outputs and traceability:
  - Detailed metadata documenting processing steps, including KBE history and probability signatures.

## Change mapping and limitations

- Change mapping challenges:
  - Non-uniform class definitions and differing spatial structures across LCM1990, LCM2000, and LCM2007 complicate robust change detection.
  - Typical per-pixel classification error around 20%; period-to-period change in Broad Habitats is harder to detect robustly given these differences.
- Grassland and fen-related issues:
  - Grassland categories show notable discrepancies due to one-to-many relationships between observed land cover and Broad Habitats.
  - Fen, Marsh and Swamp areas show large UK-level differences due to spectral mixing, small patch sizes, and mosaic nature of fen habitats.
- Spatial structure implications:
  - Differences in spatial framework and MMU between CS (Countryside Survey) and LCM2007 can affect comparisons and integration, particularly for small patches and boundary features.

## Validation, accuracy, and Countryside Survey (CS) comparison

- Overall accuracy:
  - LCM2007 shows high-level correspondence with CS for certain Broad Habitats, but variability exists across classes (e.g., arable areas, various grassland types, bog, montane, fen-specific classes).
- CS comparison findings:
  - Arable and horticulture: LCM2007 often exceeds CS upper limits, influenced by boundary features, class definitions, and temporal image ranges.
  - Grasslands: substantial differences between Improved, Neutral, Calcareous, Acid grasslands due to spectral similarity and CS field conventions.
  - Fen, Marsh and Swamp: large discrepancies attributed to mosaic composition and small patch sizes; CS may record these differently than LCM2007.
  - Montane and coastal habitats: representation differences largely due to CS’s limited high-elevation data.
- Summary takeaway:
  - Agreement varies by Broad Habitat; grasslands are particularly challenging. The Broad Habitat Association (BHA) rules were developed to improve cross-walks and interpretability between datasets.

## UK-wide and country-level patterns

- UK distribution (LCM2007 vs CS 2007):
  - LCM2007 indicates a substantial share of intensive and semi-natural land covers, with country-level variations reflecting management intensity and habitat dominance.
  - England shows higher intensive land use; Scotland features more coniferous woodland and montane habitats; Northern Ireland emphasizes grassland and urban patterns; Wales shows a mix with notable arable and grassland areas.
- 2000 vs 2007 comparison:
  - LCM2007 broad habitat proportions show increases in arable and reductions in some grassland categories relative to LCM2000, with spatial framework changes complicating direct interpretation.

## Access, usage, and guidance for GIS specialists

- Data integration and workflow:
  - Use 1 km rasters for broad national-scale quantification and cross-country comparisons.
  - Use 25 m rasters and vector parcels for detailed mapping, change detection, habitat-network analyses, and policy-relevant mapping.
  - Leverage the detailed parcel-level metadata (KBE history, ProbList) to assess and QA classifications in local contexts.
- Cautions for integration:
  - Align spatial structures when combining CS and LCM2007 data; be mindful of MMU differences and class definitions.
  - When performing change detection, consider aggregating to robust, commonly mapped classes or applying trajectory-based methods to filter out implausible changes.
- Practical applications:
  - Habitat monitoring, ecosystem services, landscape planning, biodiversity surveillance, carbon accounting, and policy evaluation.
  - Use the BHA cross-walks (Appendix 5) to interpret correspondences between LCM2007 classes and CS field categories.

## Key figures, products, and access points

- Product scope:
  - 23 LCM2007 classes, 17 Broad Habitats, 10 Aggregate classes.
  - 25 m raster and 1 km raster products; vector parcels with definitive metadata.
- Access:
  - CEH Information Gateway for 1 km rasters.
  Full vector and 25 m raster available on license from CEH (online application and contact details provided in the report).

## Takeaways for implementers

- LCM2007 delivers a validated, high-resolution UK land cover dataset with a clear, re-usable spatial framework and transparent processing history.
- The Knowledge-Based Enhancements and rich metadata support reproducibility and targeted refinement in GIS workflows.
- For national to regional analyses, use 1 km rasters for quick quantification; for detailed mapping, change detection, and integration with other spatial datasets, use the 25 m vector/raster products.
- When comparing with Countryside Survey data, account for class-definition differences, MMU disparities, and the mosaic nature of certain habitats; consider harmonisation or aggregation to enable robust comparisons.
- The dataset is designed to be integrated with broader environmental datasets and policies, supporting habitat networks, ecosystem services analyses, and land-use change assessments.