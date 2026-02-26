# Final Report for LCM2007 - the new UK land cover map

- Aims and scope
  - Delivers the first continuous parcel-based UK land cover map (LCM2007) with 23 Broad Habitat classes, plus 1 km summaries and a suite of raster products.
  - Supports policy, biodiversity, ecosystem services, and landscape planning with UK-wide, comparable data.
  - Builds on Countryside Survey (CS) data, enabling comparisons and integration with other data sources.

- Data framework and spatial structure
  - Spatial framework derived from detailed national cartography:
    - Great Britain: Ordnance Survey MasterMap (OSMM) topography layer.
    - Northern Ireland: Large-scale Vector data (LPS).
  - Boundaries supplemented with agricultural census data and urban boundary datasets to improve delineation.
  - Minimum Mapping Unit (MMU) of 0.5 ha; minimum feature width of 20 m.
  - Northern Ireland used a slightly different integration process; boundaries not embedded the same way as GB but segmentation and LPS data refined delineation.

- Data preparation and processing workflow
  - Global multi-date satellite composites used to maximize land-cover separability:
    - Primary sensors: Landsat-TM5, IRS-LISS3, SPOT-4/5 (20–30 m); AWIFS (60 m) as backup.
    - Target year: 2007; season chosen to capture phenological extremes.
  - Pre-processing steps: cloud masking, atmospheric correction (FLAASH), georeferencing (RMSE < 0.3 px), topographic correction, and image compositing.
  - Image segmentation used for GB and NI inputs, then integrated with cartography to create a unified spatial framework.
  - 91% of UK mapped from composites; remainder from single-date imagery.

- Classification and outputs
  - Parcel-based supervised maximum likelihood classification using 37 composites and 21 single-date images.
  - Training data from ground reference (2006–2008); iterative refinement; manual edits for rare classes and shadow effects; hole-filling with Landsat-7 ETM+ as needed.
  - Outputs include:
    - Vector product: land parcels with 10+ attributes (including processing history, ProbList, and KBE status).
    - Raster product: 25 m resolution with 23 LCM2007 classes.
    - 1 km products: class percentages and dominant classes, plus 10 Aggregate classes.
  - Knowledge-Based Enhancements (KBEs) applied post-classification to resolve spectral confusion and raise thematic resolution; KBEs are re-runnable and adjustable.

- Knowledge-Based Enhancements (KBEs)
  - Seven automated KBEs used in sequence (e.g., terrain, soil, urban context, coastal proximity, within/outside urban boundaries, water classification).
  - Aimed to disambiguate semi-natural habitats and improve class accuracy by incorporating contextual data.
  - Affected roughly 20% of parcels; preserved original spectral data for traceability.
  - KBEs designed to be reversible or adjustable by users to examine alternative classifications.

- Data products and metadata
  - Vector product: parcel-based polygons with attributes such as area, source images, Broad Habitat, and KBE history.
  - 25 m raster: 23 LCM2007 classes.
  - 1 km raster: two summary modes per class—percent cover and dominant class.
  - Rich metadata supports traceability of processing decisions, KBE history, and outputs; users can enable/disable KBEs as needed.

- Access, licensing, and distribution
  - 1 km raster data available via the CEH Information Gateway.
  - Full vector and 25 m raster available under license from CEH; licensing fees may apply.
  - Access details and contact information provided by CEH.

- Quality assurance, validation, and limitations
  - Ground reference validation: 9,127 points (2006–2008); overall accuracy about 83%.
  - Class-level accuracies vary; some grassland and mosaic habitats show spectral ambiguity and mapping challenges.
  - Validation emphasizes differences between field surveys and remote sensing outputs; CS comparison provides additional context.
  - Bespoke validation Appendix discusses confidence assessment, parcel-level metadata, and an informal Bayesian-style approach to gauge plausibility against high-resolution imagery.

- Comparison with Countryside Survey (CS)
  - LCM2007 vs CS 2007: broad agreement varies by habitat; grassland is particularly challenging due to one-to-many relationships with Broad Habitats.
  - Overall correspondence is higher for some aggregated levels (e.g., Arable and Horticulture) but can differ for Broad Habitat extents due to spatial structure, MMU, and spectral/contextual differences.
  - Fen, Marsh and Swamp shows large discrepancies due to complex mosaics and small patch sizes; many CS-recorded fen areas map to Rough Grassland or Acid Grassland in LCM2007.
  - Section highlights that LCM2007 provides coast-to-coast coverage with a different spatial framework, complicating direct comparisons but enabling integrated analyses.

- Change mapping and longitudinal considerations
  - Change detection across LCM1990, LCM2000, and LCM2007 is complex due to shifts in class definitions and spatial structure.
  - Distinguishing real change from classification error requires careful methodological work; aggregation or alignment with common spatial units is suggested.

- Practical implications for data support
  - LCM2007 provides a robust, transportable UK-wide land-cover dataset suitable for habitat monitoring, biodiversity policy, ecosystem services assessment, landscape planning, and catchment management when used with other data sources.
  - KBEs and detailed metadata enhance usability and enable end users to understand or adjust classification decisions.
  - The continuous vector framework supports scalable analyses and change detection, with caveats about class-level accuracy and MMU.
  - Users should consider discrepancies with field surveys (CS) and differences in spatial structure when integrating LCM2007 with CS or other datasets.

- Related context and future integration
  - European links: LCM2007 data underpin Corine Land Cover mapping (2006) via transformation and generalisation.
  - Data architecture is designed to support future monitoring by reusing the generalised spatial framework for efficient change detection and nationwide monitoring.

- Examples and dissemination notes
  - The report includes example areas illustrating LCM2007’s representation across upland, calcareous, urban, arable, and fenland contexts.
  - Data users are encouraged to utilize parcel-level KBEs and validation guidance to tailor usage to their specific study area.

- Summary takeaway for data support
  - LCM2007 represents a significant advancement in UK land-cover mapping, delivering coast-to-coast, parcel-based data with rich metadata and knowledge-based enhancements that improve usability and traceability.
  - While offering valuable national-scale products, users should be mindful of class-specific accuracies, MMU implications, and differences relative to field-based surveys when applying the data for policy, planning, or change-detection analyses.