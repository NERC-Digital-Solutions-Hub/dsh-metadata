# Vegetation surveys of the Monks Wood National Nature Reserve (NNR) in 2005 and 2006

## Purpose and scope
- Two vegetation surveys of Monks Wood NNR (160 ha) conducted in 2005 and 2006 to inform habitat assessment for Marsh Tits.
- Transects were centered on Marsh Tit territories and similar-sized unoccupied woodland blocks, effectively sampling across the whole wood.
- Each year provides a representative, year-specific snapshot of vegetation structure and composition.

## Study area and sampling design
- Location: Monks Wood NNR, coordinates provided in British National Grid.
- Transects: 100 m long, 10 m wide; transect centers used as the sampling unit.
- Yearly sampling locations: 35 in 2005; 34 in 2006; centroids selected from Marsh Tit territories (n = 22 in 2005; n = 21 in 2006) plus unoccupied areas (n = 13 each year).
- Distance between transects: minimum 15 m; maximum 159 m; mean 75 m (SD 37 m).
- Transect bearing: recorded for two 50 m segments from the centroid.

## Methods and measurements
- 2005 (Feb 2005):
  - Record all shrubs (>30 cm) and trees (>1 m) within each transect.
  - Trees classified by DBH: <5 cm, 5–30 cm, >30 cm.
  - Shrubs not size-classified beyond height >30 cm.
  - Multi-stemmed species counted as separate individuals if >1 m apart; otherwise grouped.
  - Deadwood not surveyed in 2005.
- 2006 (Jun–Jul 2006):
  - Similar recording of shrubs and trees; added deadwood data.
  - Tree DBH classes: <10 cm, 10–30 cm, >30 cm.
  - Shrub height classes: <2 m, 2–4 m, >4 m.
  - Deadwood data captured for two larger DBH classes: fallen deadwood (ground) and standing deadwood (snags), plus substantial dead branches overhanging transects.
  - Counts missing for some categories indicated as no_data.
- Transect locations and methods aimed to cover the whole wood similar to 2005 with year-specific adjustments for deadwood.

## Data structure and documentation
- Dataset records include a comprehensive set of fields, enabling cross-year comparison:
  - Transect_ID and Year-level identifiers; Transect_ID_Annual for within-year tracking.
  - Spatial: X_coordinate_centroid_British_National_Grid, Y_coordinate_centroid_British_National_Grid.
  - Transect_50_m_bearing_from_centroid_1 and _2 (compass bearings for transect segments).
  - Species- and DBH-class specific counts (e.g., Ash_dbh_class_1/2/3, Ash_Total; similarly for Aspen, Elm, Field Maple, Oak, Birch, Wild Service, etc.).
  - Totals for each species group and for tree/DBH categories (Tree_Total_dbh_class_1/2/3; Tree_Total_all; Deadwood and related categories for 2006).
  - Deadwood categories: fallen and standing, with diameter classes and tallies.
  - Special notes: some fields use “no_data” to denote missing counts.
- Data quality control:
  - Records were checked and cleaned; missing values labeled as no_data.
  - An example field-recording sheet from 2006 is referenced, illustrating data capture formats.

## Data governance, access, and stewardship considerations
- Provenance and consistency:
  - Two-year dataset with a shared structure but methodological updates (notably in 2006 for deadwood and DBH/height classifications).
  - Unique transect identifiers across years enable cross-year analyses while preserving year-specific methodologies.
- Metadata and standards:
  - Clear data dictionary style field naming (e.g., species_DBH_class, total counts) supports interoperability and reuse.
  - Spatial references use the British National Grid, facilitating integration with other UK geospatial datasets.
- Data completeness and limitations:
  - 2005 lacked deadwood data; 2006 added deadwood measurements and refined height/DBH classifications.
  - Some categories may have no_data entries; users should handle missing values explicitly.
- Implications for reuse:
  - Suitable for habitat and vegetation structure analyses, temporal comparisons, and linkage to Marsh Tit territory data.
  - Requires attention to year-specific methodological differences when aggregating or comparing across years.

## References
- Broughton, R.K., Hinsley S.A., Bellamy P.E., Hill R.A. & Rothery P. (2006) Marsh Tit Territories in a British Broadleaved Wood. Ibis 148, 744-752.
- An example of the field recording sheet used in the 2006 surveys is provided (Date, Centroid grid ref, species fields, size classes, deadwood fields, etc.).