# Final Report for LCM2007 - the new UK land cover map

## Overview of the section
- Compares LCM2007 with Countryside Survey (CS) 2007 to assess area estimates and agreement across Broad Habitats.
- Identifies where estimates are similar (within UK 95% confidence limits) and where they diverge (beyond those limits).
- Discusses methodological factors driving differences (classification definitions, spectral variability, temporal ranges, and the handling of boundaries/linear features).
- Highlights implications for data governance, validation, and change-detection workflows for Data Stewards.

## 4.3.2 Similar area estimates
- Similar area estimates occur for:
  - Broadleaved woodland
  - Acid Grassland
  - Inland Rock

## 4.3.2 Dissimilar area estimates
- Dissimilar area estimates occur for:
  - Arable and Horticulture
  - Improved Grassland
  - Neutral Grassland
  - Dwarf Shrub Heath
  - Bog
  - Montane Habitats
  - Coastal habitats

## Explanations for key differences (selected points)
- Arable and Horticulture
  - CS UK total ~46,574 km2; DEFRA 2007 figure ~63,840 km2 when including temporary grass and uncropped land.
  - LCM2007 estimates ~63,005 km2, suggesting inclusion of temporary grassland and uncropped land within the LCM category, and reliance on multi-year imagery.
  - Spectral variability of arable crops leads to misclassification and potential overestimation in some areas.
  - Boundary and Linear Features are treated differently between CS and LCM, causing field-size and area differences (CS uses boundaries that are often below MMU; LCM generalises features into fields).
- Improved Grassland and Neutral Grassland
  - LCM2007 estimates differ notably from CS; discrepancies largely reflect how each product handles Neutral Grassland and the spectral similarity between improved and neutral grassland.
  - Soil data limitations reduce the ability to distinguish species composition, affecting class allocation.
- Dwarf Shrub Heath and Bog
  - Differences arise from allocation decisions between these two habitats, similar to grassland issues.
  - Montane Habitats often replace other upland categories; height/altitude rules influence classifications.
- Fen, Marsh and Swamp
  - CS recorded a UK total around 4392 km2, while LCM2007 shows about 101 km2.
  - Fen is a mosaic of land-cover types; smaller patches are often mapped as Rough Grassland or Acid Grassland by LCM2007, leading to large discrepancies.
  - Patch size and spatial structure (MMU, segmentation) contribute to the divergence.
- Coastal and Montane habitats
  - CS underrepresentation in these strata leads to apparent dissimilarities with LCM2007 results.
- Boundary and temporal effects
  - Differences in what CS labels as arable or boundary features and what LCM2007 maps within the MMU contribute to systematic shifts between products.
  - LCM2007 requires images from multiple years, introducing additional spectral variability and field-change effects.

## 4.4 UK Land Cover (high-level synthesis)
- Across the UK, more than 50% of land cover is intensive (Arable and Horticulture plus Improved Grassland) or built-up.
- Woodlands account for about 12% (split roughly evenly between Broadleaved and Coniferous).
- The remaining area is semi-natural, with Scotland showing the largest share of Montane Habitats and Mountain/ heath types; coastal and freshwater distributions vary by country.

## 4.5 Summary and discussion (implications for Data Stewards)
- Agreement between LCM2007 and CS varies widely by Broad Habitat; grasslands are especially problematic due to a one-to-many mapping between observed land cover and habitat types.
- Broad Habitat Association (BHA) rules were developed to improve interpretability of cross-walks between LCM2007 and CS, adding a third level of thematic accuracy beyond Broad Habitat and Aggregate classes.
- LCM2007 shows strong correspondence with CS 1 km mapping for Arable and Horticulture at the square level but tends to overestimate this class when considering Broad Habitat extents.
- Fen, Marsh and Swamp exhibit large discrepancies due to the mosaic nature of Fen and the small patch sizes relative to the MMU; potential future work could use additional data to allocate some Fen areas to Fen/Marsh/Swamp.
- The comparison underscores the importance of:
  - Maintaining clear, traceable provenance and metadata for classifications and cross-walks.
  - Using knowledge-based enhancements (KBEs) and cross-domain data (soil, terrain, boundaries) to improve accuracy and interpretability.
  - Establishing robust validation frameworks that consider patch-size effects and differences in spatial frameworks.
  - Supporting change-detection efforts with a consistent spatial framework and agreed-upon cross-walk rules.
- For Data Stewards, key practical takeaways include the need for:
  - Rigorous documentation of classification rules, cross-walks, and provenance.
  - Ongoing validation against independent surveys (CS-like datasets) and transparency about uncertainties, especially for grassland, fen, montane, and coastal habitats.
  - Clear governance around handling of boundary features, temporal ranges, and multi-year imagery in classification workflows.
  - Maintaining flexibility to re-allocate or adjust classes via KBEs where spectral confusion persists, while preserving traceability to original spectral classifications.

## Practical implications for governance and data sharing
- The results emphasize transparent reporting of class- and product-level accuracies and uncertainties to support risk assessment and user decision-making.
- A structured, documented cross-walk (BH and BH-associated rules) is essential for consistent interpretation across datasets and users.
- The development and maintenance of a common spatial framework (as in LCM2007) facilitate future change-detection and policy-relevant analyses, but require careful handling of differences in input data, temporal coverage, and classification approaches.