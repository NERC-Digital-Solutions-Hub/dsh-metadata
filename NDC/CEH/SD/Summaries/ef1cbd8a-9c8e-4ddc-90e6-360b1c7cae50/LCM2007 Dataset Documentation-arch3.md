# LAND COVER MAP 2007 DATASET DOCUMENTATION

## Overview
- Provides a range of data products to support UK land cover monitoring, replacing LCM2000 with key improvements.
- Land cover classification for the UK using 23 classes based on Broad Habitats; created from summer–winter satellite composites at 20–30 m pixels.
- Clarifies that LCM2007 maps land cover (not directly land use) and uses a 0.5 ha minimum mappable area (parcels smaller than 0.5 ha or very short linear features are dissolved).
- Built upon generalised OS mapping frameworks, improving compatibility with GIS datasets.

## Data Products and Structure
- Vector Data Set
  - 8.6 million polygons for Great Britain; 0.9 million for Northern Ireland.
  - 10 attributes per polygon, including Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (class code for display), KBE (processing history), ProbList (top 5 spectral-class probabilities), CorePixels, Construct, TotPixels.
  - Unique Parcel_ID retained for clear communication between users.
  - Broad Habitat sub-classes provide additional detail but are not guaranteed to have the same accuracy as LCM2007 classes.
- Raster Data Sets
  - 25 m and 1 km rasters derived from the vector data.
  - Great Britain and Northern Ireland provided separately with their respective projections.
  - 23-class 25 m raster; 1 km rasters include Dominant Cover, Aggregate-class summaries, and Percentage Cover for both LCM2007 and Aggregate classes.
- Classifications and mappings
  - 23 LCM2007 classes derived from Broad Habitats (Table 1; Appendix 2 shows relationships with Broad Habitat sub-classes; Appendix 3 provides color mappings).
  - LCM2007 classes are aligned with Broad Habitats; some Broad Habitat sub-classes may require user validation due to differing accuracy/consistency.

## Data Quality and Validation
- Ground-reference validation against polygons at equivalent spatial and thematic resolution.
- Average accuracy around 83% across the validation dataset; local discrepancies possible.
- Sub-classes (Broad Habitat sub-classes) are included primarily for ProbList context and are not part of the QA-verified LCM2007 class accuracy.

## Metadata and Data Governance
- Rich metadata for vector polygons, including data sources, processing history (KBE), and spectral-class probabilities (ProbList).
- Parcel_ID and field codes included; FieldCode usage is recommended only with caution and user validation.
- Documentation emphasizes understanding production methodology, metadata, and inherent limitations for appropriate use.

## Access, Licensing, and Data Management
- Data Access
  - 1 km raster data available via CEH Information Gateway.
  - Full vector and 25 m raster products available under licence on request from CEH; online application process or direct contact provided.
- Licensing
  - Licence fees may apply for some users and applications.
- Data Management Considerations
  - Vector data are large (nearly 10 million polygons); plan storage and processing accordingly.
  - Cross-border data (GB vs NI) have separate datasets and projections; NI moving toward ITM projection in progress.
- Projections
  - GB: British National Grid (OSGB 1936).
  - NI: Irish National Grid (and transitioning toward ITM).

## Practical Usage and Considerations for Monitoring Frameworks
- LCM2007 is designed to support diverse monitoring applications, including integration with other datasets via a common spatial framework.
- Important distinctions for policy monitoring:
  - Do not assume land cover equals land use; interpret accordingly.
  - Use the QA-validated LCM2007 class (INTCODE) for display and primary analyses; treat Broad Habitat sub-classes as supplementary.
  - When using sub-classes or ProbList outputs, perform your own validation to confirm suitability for decision-making.
- Data products enable multi-resolution analysis:
  - 25 m vector and raster products provide detailed, object-based information.
  - 1 km rasters enable broad national-scale analyses and integration with other national datasets.

## Appendices and Colour Mapping
- Appendix 1: Detailed 23 LCM2007 classes and Broad Habitat definitions (with notes on mapping challenges such as grasslands, bogs, montane habitats, and aquatic systems).
- Appendix 2: Relationships between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (including specific class-number mappings).
- Appendix 3: Standard colour mappings for the 23 LCM2007 classes (for visualization in final reports and maps).

## Acknowledgements and Further Information
- Acknowledges data sources and cartographic partners (Landsat, SPOT, AVNIR, OS data, etc.).
- References to the Final Report for LCM2007 (Morton et al., 2011) and Jackson (2000) for broader habitat classifications.
- For more information and detailed methodology, consult Morton et al. (2011) Final Report and related Countryside Survey documentation (www.countrysidesurvey.org.uk).