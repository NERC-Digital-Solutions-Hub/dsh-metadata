# Final Report for LCM2007 - the new UK land cover map

- The project delivers the first continuous parcel-based UK land cover map (LCM2007) with UK-wide coverage, aligned with Broad Habitats for policy monitoring and change detection, building on prior CEH maps and enabling integrated environmental assessment.

## Dissimilar area estimates (4.3.2)

- Dissimilarity defined as land-cover classes outside Countryside Survey (CS) 95% confidence limits for the UK.
- Major dissimilarities occur for: Arable and Horticulture, Improved Grassland, Neutral Grassland, Dwarf Shrub Heath, Bog, Montane Habitats, and coastal habitats.
- Key causes:
  - Classification differences: CS vs LCM2007 definitions differ, e.g., temporary grass and uncropped land may be included in Arable and Horticulture in LCM2007.
  - Spectral confusion due to wide spectral variability in Arable and Horticulture across crops and seasons.
  - Boundary and Linear Features: CS maps many boundaries below LCM MMU; LCM often aggregates these into adjacent fields, inflating apparent field size.
  - Grasslands: Improved vs Neutral grassland split varies; spectral similarity and soil data limitations complicate discrimination.
  - Fen, Marsh and Swamp: CS tends to record mosaics; LCM often maps as Rough Grassland or Acid Grassland; patch size and spatial structure influence results.
  - Montane and coastal habitats: CS underrepresents these, amplifying differences.
  - Fen-related differences: CS and LCM2007 differ in polygon size and structure; most Fen polygons are below LCM MMU, impacting area estimates.

## Discussion (4.3.3)

- Agreement between LCM2007 and CS varies widely across Broad Habitats; grassland classifications are particularly problematic due to one-to-many mappings.
- Broad Habitat Association (BHA) rules improve alignment by addressing one-to-many grassland mappings between CS and LCM2007.
- LCM2007 shows high correspondence with CS 2007 for Arable and Horticulture at 1 km scale, but UK-wide Broad Habitat extents are often higher in LCM2007.
- Fen, Marsh and Swamp estimates differ by an order of magnitude due to mosaic nature and small patch sizes; many CS Fen areas map to Rough Grassland or Acid Grassland in LCM2007.
- Validation and accuracy:
  - Ground reference validation: 9127 points; overall LCM2007 accuracy about 83%.
  - Class-level accuracies vary (e.g., Bog ~93% Producer’s; Improved Grassland ~89% Producer’s, 83% User’s; Neutral Grassland ~16% Producer’s).
  - KBEs and external data can reduce accuracy for some specialized classes; results are dataset/context dependent.
- Practical interpretation:
  - Use aggregated grassland categories for better field-data correspondence.
  - Apply Broad Habitat Associations for nuanced CS-LCM comparisons.
  - Consider spatial scale and MMU when comparing with finer-scale CS data (CS MMU smaller than LCM MMU of 0.5 ha).
  - KBEs offer user-adjustable outputs, but validate with ground data.

## UK Land Cover (4.4)

- Summary: UK land cover is dominated by intensive use (Arable and Horticulture and Improved Grassland together ~50%), with ~16% Coniferous/ Broadleaved woodland, and ~30% semi-natural (including Mountain, Heath and Bog; semi-natural grassland; coastal components).
- Country differences:
  - England: highest intensive land use ~76% (40% Arable and 27% Improved Grassland, 9% Built-up).
  - Scotland: largest share of Coniferous Woodland; substantial semi-natural grassland and Mountain habitats.
  - Northern Ireland and Wales: substantial intensive land use, with variations in grassland and woodland patterns.
- Comparisons with LCM2000 show changes in Arable and Semi-natural Grassland proportions; spatial framework changes contribute to observed differences.
- Directional note: LCM2007 provides coast-to-coast, consistent Broad Habitat framework, but some differences with CS reflect methodological and spatial-structural differences.

## Summary and discussion (4.5)

- LCM2007 provides a continuous UK-wide spatial framework aligned to Broad Habitats, enabling consistent monitoring and policy evaluation, while recognizing several challenges:
  - Grassland classes pose the largest comparability challenge due to one-to-many mappings with CS and mosaic habitat structures.
  - Fen, Marsh and Swamp areas are difficult to map spectrally and are sensitive to polygon size and spatial structure.
  - Spatial framework changes mean direct one-to-one change mapping across versions (LCM1990, LCM2000, LCM2007) is complex; aggregated approaches or reformatting to a common framework may improve change detection.
- The generalised spatial framework from LCM2007 is reusable and enhances future monitoring efficiency and cross-country comparability.
- LCM2007 data and CS data are complementary: CS provides ground-truthing and habitat quality insights; LCM2007 delivers nationwide coverage and change-tracking capabilities.
- European links: UK component of Corine Land Cover 2006 is derived from LCM2007 vector via geometric generalisation and thematic transformations, supporting pan-European assessments.

## Example areas (5.1)

- A range of geographic examples demonstrates LCM2007 performance across uplands, calcareous grasslands, urban areas, and arable/fenland mosaics, illustrating how different Broad Habitats manifest in the vector and raster outputs.

## Vector and raster products (5.2)

- Vector: Parcel-based polygons with attributes such as area, source images, Broad Habitat, processing history (Construct, KBEs), ProbList (top five spectral variants), and core pixels.
- Raster products:
  - 25 m resolution with 23 LCM2007 classes.
  - 1 km raster summaries: (A) Percent cover per class; (B) Dominant class per pixel.
- Access:
  - 1 km rasters via CEH Information Gateway.
  - Full vector and 25 m rasters licensed on request from CEH (licensing fees may apply).

## Practical considerations for analysts

- For field data comparisons, use aggregated grassland classes and apply Broad Habitat Associations to improve correspondences.
- Be mindful of scale: CS operates at finer MMU than LCM2007; adjust analysis accordingly.
- Leverage KBEs to refine classifications in context-rich zones but validate against ground data where possible.
- Use the 1 km raster outputs for national-scale modeling, or combine with higher-resolution data (e.g., meteorology, species distributions) for integrated analyses.

## Data access and synthesis (Chapter reflections)

- LCM2007's parcel-based vector framework (with stable boundaries) enables robust change detection and interoperability with other cartographic products, while the 25 m and 1 km raster products provide scalable outputs for diverse applications.
- The project emphasizes the need for integrating multiple data sources (satellite, field surveys, soils, topography) to enhance classification accuracy and habitat interpretation.

## High-level takeaway

- LCM2007 delivers a robust, harmonised UK-wide land cover product aligned with Broad Habitats for consistent environmental monitoring and policy evaluation, while acknowledging challenges in discriminating spectrally similar habitats and reconciling with field-based surveys.