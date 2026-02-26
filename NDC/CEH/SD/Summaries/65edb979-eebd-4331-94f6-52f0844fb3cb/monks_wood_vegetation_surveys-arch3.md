# Two vegetation surveys of the 160 ha Monks Wood National Nature Reserve (NNR) in 2005 and 2006

- Purpose and scope
  - Data derived from two vegetation surveys of Monks Wood NNR (2005 and 2006) to assess habitat structure.
  - Although designed around Marsh Tit territories, the sampling distributed transects across the whole wood to provide representative coverage.

- Survey design and methods
  - Transect layout
    - Each year used 100 m long transects, 10 m wide.
    - Transects centered on Marsh Tit territory centroids and on centroids of unoccupied wood blocks; minimum spacing ~15 m, maximum ~159 m, mean ~75 m.
  - Year 2005 (February)
    - 35 sampling locations across Monks Wood.
    - Records for all shrubs >30 cm tall and trees >1 m tall.
    - Trees categorized by DBH (<5 cm, 5–30 cm, >30 cm); shrubs not size-classified.
  - Year 2006 (June–July)
    - 34 sampling locations (based on Marsh Tit territories and unoccupied areas).
    - Similar recording of shrubs and trees with updated DBH (categories: <10 cm, 10–30 cm, >30 cm).
    - Deadwood recorded: fallen (10–30 cm and >30 cm) and standing snags (>10 cm), plus large dead branches; differentiated by whether in transect and by form.
  - Data capture nuances
    - Some categories marked as no_data when not counted.
    - Transect center coordinates and bearings recorded for each 50 m section.

- Data structure and fields
  - Core identifiers: Transect_ID, Year, Transect_ID_Annual, description fields.
  - Spatial data: X_coordinate_centroid, Y_coordinate_centroid, transect bearings.
  - Vegetation data: species-by-DBH class counts for major genera (e.g., Ash, Aspen, Elm, Oak, Birch, etc.) and totals; tree/shrub tallies; deadwood categories (fallen and standing by size).
  - Documentation fields: notes on data presence/absence, data quality, and data lineage.
  - A field recording sheet example and reference methodology are provided in the documentation.

- Quality control and data management
  - Records were checked and cleaned; missing values labeled as no_data.
  - Metadata clarity is emphasized, with a need to ensure data provenance and transformation steps are traceable.

- Context and references
  - Grounded in Marsh Tit Territories in a British Broadleaved Wood (Broughton et al., 2006).
  - An example field recording sheet is provided to illustrate data capture format.

- Relevance for monitoring frameworks
  - Demonstrates a structured, repeatable monitoring approach across years to detect vegetation change.
  - Highlights challenges relevant to monitoring governance:
    - Ensuring metadata completeness and consistency across years.
    - Maintaining data accessibility while documenting data transformations.
    - Balancing data sharing with practical constraints (e.g., dataset completeness, standardization).
  - Provides a data schema that could inform standardization of environmental health indicators (species counts by size class, deadwood components, transect-based sampling) and governance considerations (data provenance, quality assurance, and harmonization).