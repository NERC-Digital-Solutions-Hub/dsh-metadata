# Final Report for LCM2007 - the new UK land cover map

- A UK-wide, parcel-based land cover map (LCM2007) designed to map land cover to Broad Habitats and enable habitat monitoring, policy support, and change detection.
- Comparison with Countryside Survey (CS) 2007 reveals variable agreement across Broad Habitats, with grassland categories being the main area of discrepancy.
- Data products include a vector of ~10 million parcels and raster products at 25 m and 1 km resolutions; extensive metadata and knowledge-based enhancements accompany the classification.

## Key findings from comparisons with Countryside Survey (CS) 2007

- Very similar area estimates (within CS 95% confidence limits in every country) for:
  - Coniferous Woodland
  - Freshwater
  - Built-up Areas and Gardens
  - Calcareous Grassland
- Similar area estimates (within CS UK 95% confidence limits) for:
  - Broadleaved Woodland
  - Acid Grassland
  - Inland Rock
- Dissimilar area estimates (beyond CS UK 95% confidence limits) for:
  - Arable and Horticulture
  - Improved Grassland
  - Neutral Grassland
  - Dwarf Shrub Heath
  - Bog
  - Montane Habitats
  - Coastal habitats
- Explanations for differences:
  - Differences in how “Arable and Horticulture” is defined, spectral confusion, and inclusion of boundary/linear features in LCM2007.
  - Grassland classifications show substantial spectral variability and a one-to-many relationship with Broad Habitats; this drove the Broad Habitat Association (BHA) rules.
  - Fen, Marsh and Swamp areas are complex mosaics; CS often records small patches below MMU, leading to large disparities with LCM2007.
  - Montane, bog, upland and coastal categories exhibit substantial differences due to CS sampling limitations and spectral/contextual classification dynamics.
  - Field surveys (CS) and LCM2007 have different spatial structures (1 km CS squares vs UK parcel framework), affecting comparisons.

- Validation context:
  - Ground reference validation reported roughly 9,127 points with an overall accuracy around 83% for LCM2007.
  - Class-level accuracies vary; grasslands, uplands, and boundary features contribute to misclassifications.

## UK Land Cover distribution and trends (LCM2007 vs CS)

- Overall UK distribution:
  - Over 50% of the UK is either Arable and Horticulture or Improved Grassland, or Built-up Areas and Gardens.
  - Woodlands account for about 12% (split between Broadleaved and Coniferous).
  - The remainder is semi-natural or natural with coastal, semi-natural grasslands, and mountain/habitat types.
- Country-level patterns:
  - England: highest share of intensive land use (about 76%).
  - Scotland: largest share of Coniferous Woodland and the most extensive montane/semi-natural habitat presence.
  - Northern Ireland and Wales: intermediate shares of intensive land use; notable regional habitat variations reflect local management and geomorphology.
- Temporal/spatial context:
  - LCM2007 uses a generalised cartographic framework with segment-based processing and knowledge-based enhancements to improve consistency across the UK, enabling coast-to-coast comparisons and national-scale change assessment.

## Data products, access, and usage

- Vector product:
  - Parcel-based polygons with 10 attributes and detailed metadata, including Construct, ProbList, and KBE (Knowledge-Based Enhancement) history.
  - 23 LCM2007 land cover classes mapped to Broad Habitats (BH) with a 0.5 ha minimum mapping unit.
- Raster products:
  - 25 m resolution raster: 23 LCM2007 classes.
  - 1 km resolution raster: UK-wide summaries using either percentage cover per class or dominant class per pixel.
- Access:
  - 1 km rasters available via the CEH Information Gateway.
  - Full vector and 25 m rasters available by license on request from CEH (potential fees apply).

## Practical takeaways for analysts

- LCM2007 provides a consistent, coast-to-coast UK land cover framework aligned to Broad Habitats, with robust vector metadata facilitating traceability and validation.
- Expect varying accuracy by class; grassland and upland habitats pose the greatest spectral and interpretive challenges.
- Knowledge-Based Enhancements (KBEs) improve thematic resolution but require careful validation, particularly in complex or transitional habitats.
- When comparing LCM2007 to Countryside Survey results, consider aggregating grassland types or using Broad Habitat Association links to improve comparability.
- Data access may involve licensing; plan for metadata-driven validation and reproducibility in analyses.

## Example areas and visualization

- LCM2007 examples cover upland areas, calcareous grasslands, urban landscapes, and fenland–arable mosaics, illustrating how different habitats appear under the parcel-based framework and how KBEs influence classification in mixed landscapes.

## Chapter 6: Discussion highlights (LCM2007 context)

- LCM2007 delivers the first continuous parcel-based UK land cover map with compatible vector and raster products, enabling broad environmental applications and policy support.
- Advantages over earlier CEH maps include integration with high-resolution national cartography (MasterMap, LPS) and a reusable spatial framework for future change detection.
- Change detection is complex due to methodological differences across LCM generations; a unified spatial structure (real-world land units) is considered the optimal path for future monitoring.
- LCM2007 complements CS field surveys by providing comprehensive nationwide coverage and enabling integration with other data sources (soil, hydrology, climate, LiDAR, etc.) for enhanced policy-relevant analyses.

## Data foundations and external links

- LCM2007 data underpin broader environmental policy areas such as biodiversity assessment, habitat connectivity, ecosystem services, and catchment management.
- European links: UK component of Corine Land Cover 2006 is derived from LCM2007; LCM2007 also relates to European datasets (e.g., IMAGE2006) used for pan-European monitoring.

## Appendices and methodological context (high-level)

- Bespoke validation: outlines that “fit for purpose” validation requires careful, location-specific quality assessment using parcel-level metadata and KBE histories.
- Broad Habitat Association (BHA): explains the rationale for cross-walk rules between LCM2007 classes and CS Broad Habitats to improve comparability in ambiguous or transitional cases.
- KBEs and metadata: LCM2007 parcels retain detailed processing history (KBE sequences, probabilities, and core pixels) to support user-driven validation and reproducibility.
- Chapter-level synthesis emphasizes the complexity of reconciling LCM2007 with CS data and the value of using a common spatial framework for future national-scale land surface mapping.

## Access and usage notes

- CEH Information Gateway provides 1 km rasters; full vector and 25 m rasters require a license from CEH.
- The report and datasets are intended to support a wide range of policy-relevant analyses in biodiversity, landscape planning, and environmental monitoring.