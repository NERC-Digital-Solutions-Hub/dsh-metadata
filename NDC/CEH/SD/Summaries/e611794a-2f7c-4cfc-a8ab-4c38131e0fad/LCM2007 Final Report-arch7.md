# Final Report for LCM2007 - the new UK land cover map

- A UK-wide, parcel-based land cover map (LCM2007) with continuous vector coverage and derived raster products (25 m and 1 km resolutions), aligned with Broad Habitats for biodiversity planning.
- Provides coastal-to-coastal coverage and supports change detection, habitat monitoring, and policy-relevant GIS analyses.

## Data and spatial framework

- Data sources
  - Satellite imagery: Landsat TM5, LISS-3, SPOT-4/5; AWIFS as backup; 20–30 m resolution; multi-date composites (summer/winter).
  - External vector/cartography: OS MasterMap (GB), OSNI/LPS (NI); agricultural boundaries; urban area datasets; soils and terrain data.
- Spatial framework
  - UK-wide framework built on generalised national cartography (MasterMap/LPS) integrated with image segmentation to delineate homogeneous spectral regions and real-world land parcels.
  - Minimum mapping unit (MMU) of 0.5 ha; polygons generalised to fit MMU constraints.
  - NI and GB internal generalisations optimised for integration with image segments.

## Image processing and segmentation

- Pre-processing
  - Cloud/cloud-shadow masking, atmospheric correction, geo-registration, topographic correction; traceability via logs.
- Segmentation and classification
  - Segment-based approach using multi-date composites; parcel-level refinement via supervised classification (initial spectral classes) and iterative KBEs.
  - Core pixels and segment-level statistics used to derive training and classification results.
- Knowledge-based enhancements (KBE)
  - Seven automated KBEs applied post-classification to resolve spectral confusion and improve thematic resolution.
  - KBEs incorporate terrain, soils, coastal context, urban influence, and other ancillary data.
  - About 20% of parcels affected by KBEs; detailed provenance stored in vector attributes.

## Knowledge base data and algorithms

- Contextual data used by KBEs
  - Urban boundaries, coastal outlines, terrain (DEM), soils, and related generalized layers.
- KBE algorithms
  - Seven automated rules addressing Terrain, Soil, Coastal/Offshore, Urban context, Within/Outside Urban boundaries, and Water-related adjustments (plus montane/shoreline adjustments).
- Output
  - KBEs modify initial spectral classifications to improve thematic resolution and provide traceable processing history.

## Products and access

- Vector product
  - Parcels with attributes: area, source images, Broad Habitat (BH), KBEs applied, ProbList (top 5 spectral variants with probabilities), and construction history.
  - Broad Habitat Sub-classes (BHSub) provide additional detail but are not as rigorously QA’d as the main 23 LCM2007 classes.
- Raster products
  - 25 m raster: 23 LCM2007 classes.
  - 1 km raster: UK-wide, with either percent cover per 1 km pixel per class or a dominant class per pixel.
- Access and licensing
  - 1 km rasters: via CEH Information Gateway.
  - Full vector and 25 m rasters: available by license on request from CEH (licence fees may apply).

## Change mapping and limitations

- Change detection
  - Attempting to map changes between LCM1990, LCM2000, and LCM2007 is complex due to differing spatial structures and class definitions.
  - Emphasis on stable spatial objects (cartography-derived boundaries) to support repeatable change detection.
- Comparison with Countryside Survey (CS)
  - CS and LCM2007 show varying levels of agreement across Broad Habitats; grasslands are particularly challenging due to differences in field vs. spectral mapping and boundary delineation.
  - Fen, Marsh and Swamp show large discrepancies due to mosaic nature and small patch sizes; some CS-recorded fen areas are mapped as Rough Grassland or other classes in LCM2007.
  - Boundary/Linear Features in CS often fall below LCMU thresholds and are incorporated differently, influencing area estimates.
- Practical limitations for GIS users
  - MMU exclusions lead to fragmentation of some habitat mosaics and potential underestimation of small but relevant features.
  - Spectral variability, especially for Arable and Horticulture, can cause misclassification due to crop types, phenology, and multi-year image requirements.
  - Differences in spatial framework across LCM editions complicate direct change comparisons; KBEs mitigate but do not eliminate discrepancies.

## Quality assurance, accuracy, and interpretation

- Validation
  - Ground reference data and CS-based comparisons used to assess accuracy; producer’s and user’s accuracies broken down by class.
  - Overall accuracy around 83% for LCM2007, with varying class-level performance.
- Interpretive notes for GIS users
  - The vector product includes rich metadata and KBE histories, enabling provenance tracing and expert quality checks.
  - For analyses, consider using the 1 km raster for broad UK-scale modelling or the 25 m rasters when finer spatial detail is necessary; use vector data when parcel-level accuracy and processing provenance are critical.
  - When comparing with CS or performing change detection, be mindful of boundary definitions, MMU effects, and potential misalignments between spectral classes and field-based habitat definitions.

## UK land cover distribution and temporal context

- Summary distribution (Broad Habitats)
  - Arable and Horticulture + Improved Grassland dominate, with significant semi-natural components (e.g., woodlands ~12% total; balanced Broadleaved and Coniferous).
  - Distribution varies by country due to land-use patterns (England typically higher intensive land use; Scotland higher woodland and montane components).
- Temporal and methodological notes
  - LCM2007 uses a UK-wide approach based on multi-temporal imagery and KBEs, aiming for consistency and reusability in future monitoring.
  - The spatial framework is designed to be reusable, facilitating future national-scale land cover monitoring and change detection.

## Example datasets and data formats

- Data formats
  - Vector: land parcels with attributes and metadata, including KBE history and ProbList.
  - 25 m raster: 23-class land cover rasters with associated metadata.
  - 1 km raster: two formats—percent cover per 1 km pixel per class and dominant class per pixel.
- Documentation and figures
  - Figures and tables illustrate product types, metadata structure, and regional results; detailed metadata available in accompanying tables (Tables 5.1–5.3 and related figures).

## Implications for GIS practice

- Practical benefits
  - A pan-UK, parcel-based land cover map aligned to national cartography, enabling integrated GIS analyses with other national data layers.
  - Rich provenance and KBEs support reproducibility, auditability, and targeted quality checks in GIS workflows.
- Recommended usage
  - Use the vector product for analyses requiring boundary accuracy and detailed parcel-level history.
  - Use the 25 m raster for detailed spatial analyses where boundaries are less critical or for overlay with other high-resolution layers.
  - Use the 1 km raster for national-scale modelling, trend analysis, or integration with climate, hydrology, or biodiversity datasets.
- Future potential
  - The established spatial framework and KBEs enable integration with additional datasets (soil, climate, biodiversity surrogates) to support evidence-based policy and ecosystem-service assessments.

## Access, references, and governance

- Data access
  - CEH Information Gateway for 1 km rasters; licenced access for vector and 25 m rasters.
- Governance and context
  - LCM2007 sits within Countryside Survey collaborations and aligns with UK Biodiversity Action Plan Broad Habitats.
  - The methodology emphasizes repeatable, policy-relevant national land cover monitoring and the potential for cross-country comparability.