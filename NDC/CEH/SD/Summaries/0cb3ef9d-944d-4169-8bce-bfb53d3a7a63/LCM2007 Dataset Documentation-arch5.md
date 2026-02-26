# Land Cover Map 2007 Dataset Documentation

- Purpose and scope
  - Parcel-based classification of UK land cover using 23 classes based on Broad Habitats.
  - Uses 20–30 m satellite imagery; maps land cover (not land use); ao update from LCM2000.
  - Minimum mappable unit: >0.5 ha; parcels <0.5 ha and linear features <20 m dissolved into surrounding landscape.
  - Product range supports diverse user needs; final report Morton et al. (2011) recommended for comprehensive methodology.

- Data products and structure
  - Vector Data Set
    - Polygons with 10 attributes; ~8.6 million polygons in GB and ~0.9 million in NI.
    - Key attributes: Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE, KBE (processing history), ProbList (top 5 spectral class probabilities), CorePixels, Construct, TotPixels.
    - Unique Parcel_ID enables unambiguous communication; retain for traceability.
  - Raster Data Sets
    - 25 m and 1 km products derived from the vector dataset.
    - 23 LCM2007 classes for 25 m; 1 km products include Dominant cover, Percentage cover for LCM2007 classes, and Aggregated (Broad Habitat) classes.
    - GB and NI provided separately due to different projections.
  - Class relationships and mapping
    - Appendix 2 documents relationships between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
    - Appendix 3 provides standard colour mapping for visualization.
  - Data formats and sizes
    - Vector (Shapefile) at 100 km × 100 km: GB ~4.13 GB; NI ~433 MB.
    - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
    - Raster 1 km: global sizes range from 21 MB to 49 KB.
  - Data access
    - 1 km raster data via CEH Information Gateway.
    - Full vector and 25 m raster data available on request under licence (fees may apply).

- Quality, metadata, and validation
  - Rich metadata for polygons; KA (Knowledge-Based Enhancements) history recorded per polygon; ProbList shows top spectral matches.
  - Validation against ground reference data: average accuracy ~83% across 9,127 polygons; variability exists by location.
  - The 23-class thematic resolution is the recommended usage level; Broad Habitat sub-classes are included but not consistently validated against QA.

- Methodology and caveats
  - Constructed from summer-winter composite images; aligned with generalised OS Master Map frameworks for GB and NI; polygons represent real-world objects (fields, woodland blocks).
  - Distinctions between land cover and land use are not always clear; caution when inferring land use from cover (e.g., arable crops vs usage).
  - KBE rules applied to refine classifications (e.g., soil corrections, altitude corrections); some sub-classes may require users to perform their own validation before use.
  - Montane, inland rock, freshwater, littoral, and coastal classifications include specific caveats (e.g., montane boundaries based on altitude, peat depth informing bog vs heath).

- Geographic coverage and projections
  - Great Britain: British National Grid (OSGB 1936); Northern Ireland: Irish National Grid (NI newline); NI moving toward ITM projection.
  - Users should reproject as needed for compatibility with other datasets.

- Usage guidance for data stewards
  - Governance and interoperability
    - Maintain Parcel_ID and full metadata lineage to support data provenance and reuse.
    - Track KBE and ProbList histories for audit trails of classification decisions.
  - Data management and storage
    - Prepare for large file sizes, especially vector datasets; plan storage and processing resources accordingly.
  - Standards and validation
    - Use the 23-class LCM2007 catalog as the primary thematic resolution; validate Broad Habitat sub-classes if used for detailed analyses.
  - Access and licensing
    - Explore CEH gateway for 1 km rasters; obtain licences for vector and 25 m rasters as required; anticipate potential licensing fees.

- Appendices and references
  - Appendix 1: LCM2007 class descriptions and Broad Habitat interpretations.
  - Appendix 2: Detailed mapping between Broad Habitats, LCM2007 classes, and Sub-classes.
  - Appendix 3: Standard LCM2007 colour mapping.
  - Acknowledgements and references to Morton et al. (2011) Final Report and Jackson (2000) for classification definitions.