# Two vegetation surveys of the 160 ha Monks Wood National Nature Reserve (NNR) in 2005 and 2006

- Overview
  - Data come from two vegetation surveys of Monks Wood NNR (160 ha) conducted in 2005 and 2006.
  - Purpose: originally to assess Marsh Tits habitat, but transects effectively sampled across the entire wood.
  - Transects: 100 m long, 10 m wide; centers chosen from Marsh Tit territories and nearby unoccupied wood; distributed across the wood to provide two representative surveys.

- Study design and sampling
  - Transect placement
    - 2005: 35 sampling locations; based on Marsh Tit territories (n=22) and unoccupied areas (n=13).
    - 2006: 34 sampling locations; based on Marsh Tit territories (n=21) and unoccupied areas (n=13).
  - Spatial layout
    - Transect centers spaced with a minimum of 15 m and a maximum of 159 m apart (mean 75 m, SD 37 m).
    - Transects cover all parts of Monks Wood.
  - Timeline and year-to-year differences
    - 2005 surveys conducted in February; 2006 surveys in June–July.
    - Methodological differences between years (see Data Collected) including deadwood recording and DBH/class thresholds.

- Data collected
  - Vegetation measurements
    - All shrubs (>30 cm) and trees (>1 m) within each transect; recording by species and size class.
    - Trees classified by diameter at breast height (DBH) into classes; year-specific thresholds:
      - 2005: DBH classes <5 cm, 5–30 cm, >30 cm.
      - 2006: DBH classes <10 cm, 10–30 cm, >30 cm.
    - Shrubs classified by height classes; 2005 had no size-class breakdown for shrubs, 2006 had <2 m, 2–4 m, >4 m.
  - Deadwood (introduced in 2006)
    - Fallen deadwood: 10–30 cm diameter; >30 cm diameter.
    - Standing deadwood (snags): 10–30 cm and >30 cm DBH.
    - Deadwood measurements recorded as counts within the transect.
  - Species-specific tallies
    - Extensive DBH-class counts for multiple species (e.g., Ash, Aspen, Elm, Field Maple, Oak, Birch, Wild Service, Dogwood, Goat Willow, Grey Sallow, Hawthorn, Hazel, Honeysuckle, Privet, Rose, etc.) with per-year class thresholds and total tallies.
  - Data gaps
    - Some categories marked as no_data where counts were not made.

- Data structure and metadata
  - Main fields
    - Transect_ID, Year, Transect_ID_Annual, X_coordinate_centroid (British National Grid), Y_coordinate_centroid, Transect_50m_bearing_from_centroid_1, Transect_50m_bearing_from_centroid_2.
  - Species and attribute columns
    - For each species: DBH_class_1, DBH_class_2, DBH_class_3, and total tallies; similarly for deadwood categories and broad plant groups.
  - Data quality and provenance
    - Records were checked and cleaned; missing values denoted as no_data.
  - Visualization
    - Figure 1 shows the distribution of 2005 (35 transects) and 2006 (34 transects) transects.

- Quality control and references
  - Quality control: data cleaning performed; no_data used where counts were not recorded.
  - References
    - Broughton et al. (2006) Marsh Tit Territories in a British Broadleaved Wood (Ibis 148, 744–752).
  - Field recording
    - An example field recording sheet for 2006 is provided, illustrating data capture for transect, centroid ref, species, DBH classes, and deadwood, among others.

- Implications for data management and use
  - Enables temporal comparison of vegetation structure between 2005 and 2006, despite methodological differences.
  - Provides detailed, multi-species, DBH-class and deadwood data suitable for habitat analyses relevant to Marsh Tit research and broader woodland management.
  - Metadata supports discoverability, interpretability, and potential harmonization for cross-year analyses within a wider data system.