# Final Report for LCM2007 - the new UK land cover map

- Overview
  - First continuous parcel-based (polygon) UK land cover map (LCM2007) with derived raster products.
  - Multi-resolution data framework: vector parcels and 25 m raster with 23 LCM2007 classes; 1 km raster products (percentage cover and dominant class).
  - Spatial framework anchored to detailed national cartography (Ordnance Survey MasterMap and Large-scale Vector) for UK-wide integration and consistent change detection.
  - Outputs support biodiversity assessment, landscape planning, ecosystem services, and policy development; designed for reuse with rich metadata and traceability.
  - Broad Habitat alignment and knowledge-based enhancements (KBEs) improve thematic resolution and cross-dataset interpretability.

- Data sources and spatial framework
  - Multi-sensor imagery and references:
    - Core satellite data: Landsat TM/ETM+, SPOT-4/5, LISS-III (IRS), AWIFS; multiple dates to build 2-date composites.
    - Ground reference and validation: CEH ground points; Countryside Survey (CS) 2007 data for GB comparison.
  - Spatial framework and granularity:
    - UK-wide coverage with nine regional chunks; parcel-based vector framework generalised from OS MasterMap and agricultural boundaries.
    - Minimum Mappable Unit: 0.5 ha; minimum feature width: 20 m.
    - Parcel-level metadata includes processing history and KBEs applied.
  - Outputs alignment:
    - Vector: 23 classes with 10-attribute processing history.
    - Rasters: 25 m (23 classes); 1 km (percent cover and dominant class).

- Processing workflow and segmentation
  - Image pre-processing:
    - Cloud/cloud-shadow masking; atmospheric correction; geo-registration (RMSE < 0.3 pixel).
    - Topographic correction using NEXTMap NI DEM; winter shadow mitigation.
  - Segmentation and integration:
    - Segmentation of 101 images (summer-winter composites and singles); integration with OSMM and agricultural boundaries to form parcel-based units.
    - Northern Ireland treated with NI vector components; nine UK chunks stitched for continuity.
  - Data assembly:
    - 2-date composites to maximize spectral contrasts; nine-chunk UK strategy prioritised for consistent classifications.
    - Some areas classified from single-date scenes when composites were suboptimal.

- Classification and knowledge-based enhancements (KBEs)
  - Classification approach:
    - Parcel-based supervised maximum likelihood classification using 37 composite + 21 single-date images.
    - Training data drawn from ground reference points and OS maps; iterative refinement.
    - Per-parcel ProbList retains top five spectral-class candidates.
  - Knowledge-based enhancements (KBEs):
    - Seven automated KBEs applied in sequence to reclassify parcels using contextual data (urban proximity, coastal/terrain/soil layers, etc.).
    - About 20% of parcels affected; final attributes document KBEs with reversibility if needed.
  - Thematic resolution for grassland:
    - Grassland classes refined using spectral signals plus KBEs to allocate Neutral/Calcareous/Acid Grassland; montane adjustments via altitude data.

- Outputs and data products
  - Core products:
    - Vector dataset: 23 LCM2007 land cover classes with 10 attributes (processing stages, spectral results, KBEs).
    - Raster dataset: 25 m resolution with 23 classes.
  - Aggregated products:
    - 1 km rasters providing percentage cover or dominant class for each 1 km cell (23 LCM2007 classes; 10 aggregates).
  - Metadata and access:
    - Rich metadata accompanying vector data for traceability; KBEs were recorded.
    - Access: 1 km rasters via CEH Information Gateway; full vector and 25 m rasters available on request under license from CEH (licensing fees may apply); NI data under dedicated NI frameworks.

- Quality assurance and validation
  - Ground truth validation:
    - 9,127 ground reference polygons; overall accuracy around 83% for LCM2007 classes.
    - Class- and habitat-specific accuracy reported; performance varies by habitat type.
  - Countryside Survey (CS) comparison:
    - UK-level CS 2007 vs LCM2007 shows varying agreement across Broad Habitats; grassland classifications especially complex due to one-to-many mappings.
    - Grassland aggregation into Broad Habitat Association (BHA) rules improves cross-dataset correspondence.
    - Fen, Marsh and Swamp exhibits large disparities due to complexity and small patch sizes; many CS “Fen” areas map to Rough Grassland or Acid Grassland in LCM2007.
  - Change mapping considerations:
    - Change detection across LCM1990/2000/2007 is challenging due to differing spatial structures and class definitions.
    - Spectral/classification errors (~20%) and structural differences complicate attribution of true habitat change.

- UK Land Cover findings and policy relevance
  - UK-wide distribution:
    - Over 50% of the UK in intensive land use (Arable and Horticulture + Improved Grassland) or Built-up Areas; ~12% in Broadleaved and Coniferous Woodland; remainder semi-natural or coastal/montane.
  - Country-level patterns:
    - England highest share of intensive land use; Scotland lowest but with significant conifer woodland and upland semi-natural habitat.
  - Historical comparison:
    - LCM2007 differs from LCM2000 in reported proportions for Arable and Semi-natural Grassland; spatial framework changes complicate direct comparisons.
  - Reuse and interpretation:
    - Aggregation of grassland types improves comparability with field survey inventories.
    - Broad Habitat Association (BHA) links assist in interpreting cross-dataset correspondences and uncertainty.

- Practical considerations for data support and use
  - Data availability and licensing:
    - 1 km raster data openly accessible via CEH gateway.
    - Full vector and 25 m raster data available under license; licensing fees may apply; NI data governed by NI frameworks.
  - Data structure and usage guidance:
    - Vector data include detailed polygon-level metadata and processing history; 25 m raster suitable for high-detail analyses; 1 km rasters suitable for national-scale modeling and integration with other datasets.
    - Nine-chunk UK coverage supports seamless UK-wide analysis but boundary handling requires care.
  - Limitations and caveats:
    - Spectral confusion persists for some habitat classes; KBEs mitigate but do not eliminate misclassification.
    - Grassland mapping depends on soil and altitude contexts; field conditions may differ from spectral signals.
    - Change detection requires careful interpretation due to class-definition shifts across years.
  - Reuse guidance:
    - For comparisons with field surveys, consider aggregating grassland types and using BHA links to interpret correspondences.
    - Use the 1 km raster products for broad-scale analyses; the 25 m and vector products for detailed, parcel-based studies with provenance.

- Key references and significance
  - LCM2007’s class set, KBEs, and Broad Habitat mappings linked to JNCC Broad Habitats.
  - Validation results: 83% overall accuracy; CS 2007 comparisons illustrating thematic correspondences.
  - Data access points: CEH Information Gateway; CEH data portal for licensing.
  - The project demonstrates robust integration of cartography, image segmentation, multi-sensor imagery, and knowledge-based enhancements, establishing a reusable framework for UK-wide land cover monitoring and change detection.