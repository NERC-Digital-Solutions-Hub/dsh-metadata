# Vegetation surveys of the Monks Wood National Nature Reserve (2005 and 2006)

## Overview
- Data from two vegetation surveys of the 160 ha Monks Wood National Nature Reserve (NNR) in 2005 and 2006.
- Each survey used 100 m long transects (10 m wide) spread across the wood, with locations centered on Marsh Tit territories and similar-sized unoccupied woodland blocks.
- Transects are distributed across the wood to provide two representative surveys of the entire area.
- Spatial coordinates are provided in the British National Grid; transect centers are the primary spatial units.

## Study design and sampling
- Transect setup:
  - 2005: 35 sampling locations; transects formed by a central centroid with a 100 m transect (50 m on either side) at ~10 m width.
  - 2006: 34 sampling locations; similar centroid-based layout across the wood.
- Distance between transects: minimum 15 m, maximum 159 m, mean 75 m (SD 37 m).
- Sampling locations chosen from Marsh Tit territory centroids (2004 for 2005; 2006 breeding season for 2006) and unoccupied areas approximating territory sizes.
- Purpose: assess vegetation around transects; originally linked to Marsh Tit habitat but effectively covers the entire woodland.

## Survey methods by year
- 2005 surveys (February 2005):
  - Record all shrubs (>30 cm tall) and trees (>1 m tall) within each 100 m transect.
  - Trees categorized by DBH (<5 cm, 5–30 cm, >30 cm).
  - Shrubs counted as individuals unless forming dense patches; multi-stemmed species counted as separate individuals if >1 m apart.
  - Deadwood not surveyed in 2005.
- 2006 surveys (June–July 2006):
  - Similar transect approach; all shrubs and trees recorded with updated height classes.
  - Trees categorized by DBH (<10 cm, 10–30 cm, >30 cm); shrubs by height (<2 m, 2–4 m, >4 m).
  - Deadwood recorded, including fallen deadwood (10–30 cm and >30 cm) and standing deadwood (snags) and large broken branches; categorized as on-ground fallen, standing, and total.
  - Deadwood is included for two larger tree classes and other specifics differ from 2005.
- Data with missing counts are denoted as no_data.

## Data structure and attributes
- Core fields (examples):
  - Transect_ID, Description; Year, Transect_ID_Annual
  - X_coordinate_centroid_British_National_Grid, Y_coordinate_centroid_British_National_Grid
  - Transect_50_m_bearing_from_centroid_1, Transect_50_m_bearing_from_centroid_2
- Species/DBH-class variables (examples):
  - Ash_dbh_class_1, Ash_dbh_class_2, Ash_dbh_class_3, Ash_Total
  - Aspen_dbh_class_1, Aspen_dbh_class_2, Aspen_dbh_class_3, Aspen_Total
  - Elm_dbh_class_1, Elm_dbh_class_2, Elm_dbh_class_3, Elm_Total
  - Field_Maple_dbh_class_1, Field_Maple_dbh_class_2, Field_Maple_dbh_class_3, Field_Maple_Total
  - Oak_dbh_class_1, Oak_dbh_class_2, Oak_dbh_class_3, Oak_Total
  - Birch_dbh_class_1, Birch_dbh_class_2, Birch_dbh_class_3, Birch_Total
  - Wild_Service_dbh_class_1, Wild_Service_dbh_class_2, Wild_Service_dbh_class_3, Wild_Service_Total
  - Tree_Total_dbh_class_1, Tree_Total_dbh_class_2, Tree_Total_dbh_class_3, Tree_Total_all
  - Species-specific height-class totals for groups such as Blackthorn, Bramble, Crab Apple, Dogwood, Goat Willow, Grey Sallow, Hawthorn, Hazel, Honeysuckle, Privet, Rose
  - Deadwood_Fallen_10-30_cm_diameter, Deadwood_Fallen_>30_cm_diameter, Deadwood_Fallen_Total
  - Deadwood_Standing_10-30_cm_dbh, Deadwood_Standing_>30_cm_dbh, Deadwood_Standing_Total
- Data quality:
  - Records were checked and cleaned; missing values are listed as no_data.

## Spatial context and visualization
- Figure 1 (referenced) shows the distribution of transects:
  - 2005 transects (white squares)
  - 2006 transects (black squares)
  - Each square marks the transect center (100 m long, 10 m wide).

## Quality control and references
- Quality control: data records cleaned; missing values flagged as no_data.
- References:
  - Broughton, R.K. et al. (2006) Marsh Tit Territories in a British Broadleaved Wood. Ibis 148, 744-752.
  - An example field recording sheet for the 2006 surveys is provided in the accompanying documentation.

## GIS and data usage implications
- Spatially explicit dataset: transect centroids with grid coordinates and bearings enable map-based analyses and visualization in GIS.
- Multi-year data support: allows cross-year comparisons of species counts, DBH class distributions, and deadwood indicators.
- Data integration considerations:
  - Different DBH and height class schemes between 2005 and 2006 require careful harmonization for cross-year analysis.
  - Some categories (e.g., deadwood) were introduced or extended in 2006; alignment needed for time-series work.
- Practical GIS workflows:
  - Map transect centers and bearings to reproduce sampling design.
  - Join species/DBH class counts by transect and year for thematic maps and hot-spot analyses.
  - Use no_data entries to handle missing data during rasterization or aggregation.