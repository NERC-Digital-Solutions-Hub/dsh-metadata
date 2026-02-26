# Monks Wood NNR vegetation surveys 2005 and 2006

- The dataset comprises two vegetation surveys of the 160 ha Monks Wood National Nature Reserve (NNR) conducted in 2005 and 2006, originally aimed at Marsh Tit habitat assessment. Transects were distributed across the wood to represent the entire area.

- Survey design and locations
  - 2005: conducted in February at 35 sampling locations. Locations selected from Marsh Tit territory centroids (2004) and unoccupied woodland centroids approximating territory sizes.
  - 2006: conducted in June–July at 34 sampling locations, using Marsh Tit territory centroids from 2006 and unoccupied centroids, ensuring broad woodland coverage.
  - Transects: 100 m long, 10 m wide; transect centers (centroids) spaced with minimum 15 m and maximum 159 m between centers (mean ~75 m, SD ~37 m).
  - Transects were distributed to sample across all parts of the wood.

- Data collected and how it varied by year
  - 2005 methodology
    - Recordings for all shrubs (>30 cm) and trees (>1 m) with stems rooted within the transect.
    - Trees classified by DBH: <5 cm, 5–30 cm, >30 cm.
    - Shrubs counted as single individuals if in dense patches; multi-stemmed species counted separately if stems were >1 m apart.
    - Deadwood not surveyed in 2005.
  - 2006 methodology
    - Similar transect approach; shrubs (>30 cm) and trees (>1 m) recorded.
    - Trees DBH classes: <10 cm, 10–30 cm, >30 cm.
    - Shrubs height classes added: <2 m, 2–4 m, >4 m tall.
    - Deadwood recorded, including: fallen (10–30 cm and >30 cm diameter) and fallen >30 cm diameter; standing deadwood (snags) and tall dead wood categories also recorded.
    - Deadwood and some other categories introduced where counts were previously not made (design changes from 2005 to 2006).
- Data structure and fields
  - Core identifiers: Transect_ID, Year, Transect_ID_Annual, X_coordinate_centroid (British National Grid), Y_coordinate_centroid (British National Grid).
  - Transect bearings for each 50 m section from centroid (two bearing fields).
  - Species/DBH-class counts (example fields shown for multiple species, e.g., Ash, Aspen, Elm, Field Maple, Oak, Birch, Wild Service, Dogwood, Goat Willow, Grey Sallow, Hawthorn, Hazel, Honeysuckle, Privet, Rose, etc.) with year-specific DBH-class definitions.
  - Total counts by species and height/DBH class (e.g., Tree_Total_all, Tree_Total_dbh_class_1/2/3, Shrub totals, Deadwood categories).
  - Data quality notes: missing values are recorded as no_data; some counts were not made in a given year (denoted as no_data).
- Data quality, provenance, and references
  - Records were checked and cleaned; missing values labeled as no_data.
  - References include Broughton et al. (2006) Marsh Tit Territories in a British Broadleaved Wood, and field recording sheet examples showing how data were captured (2006).
- Spatial and practical notes
  - Transects provide two representative surveys of Monks Wood (2005 and 2006), enabling cross-year comparisons of vegetation structure and composition.
  - An example field sheet is included in the documentation, illustrating data capture fields such as date, transect, species, size categories, and deadwood measurements.
- Potential uses for data support and analysis
  - Cross-year comparison of tree/shrub composition and structure.
  - Habitat assessment and monitoring for Marsh Tit or broader woodland management objectives.
  - Creation of self-serve data products (e.g., dashboards, pivot tables) to explore species composition by DBH/height class and deadwood metrics across transects.
  - Data quality assessment and methodological evaluation of changes between 2005 and 2006 (e.g., inclusion of deadwood, revised DBH/height class thresholds).