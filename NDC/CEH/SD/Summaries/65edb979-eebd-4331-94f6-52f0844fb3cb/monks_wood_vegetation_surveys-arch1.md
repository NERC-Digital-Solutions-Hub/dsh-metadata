# Two vegetation surveys of the 160 ha Monks Wood National Nature Reserve (NNR) in 2005 and 2006

- Overview
  - Data from two vegetation surveys of Monks Wood NNR (160 ha) conducted in 2005 and 2006.
  - Transects: 100 m long, 10 m wide, distributed across the wood to cover both Marsh Tit territories and unoccupied areas, effectively representing the entire wood.
  - Transect centers ranged from 15 m to 159 m apart (mean 75 m, sd 37 m).

- Survey design and methods
  - 2005 survey (February): 35 sampling locations; transects centered on Marsh Tit territories (n=22) and unoccupied-wood areas (n=13); shrubs >30 cm and trees >1 m tall recorded; trees classified by DBH: <5 cm, 5–30 cm, >30 cm; shrubs counted as individuals unless forming dense patches; deadwood not surveyed.
  - 2006 survey (June–July): 34 sampling locations; centroids based on Marsh Tit territories (n=21) and unoccupied areas (n=13); methodology largely similar but with additional deadwood recording; trees DBH classes: <10 cm, 10–30 cm, >30 cm; shrubs height classes: <2 m, 2–4 m, >4 m; deadwood categorized as fallen (ground) or standing (snags) and further by diameter class; counts for many species expanded with DBH-classed tallies.
  - Transect bearing data collected for 50 m segments from each centroid.

- Data captured and structure
  - Core identifiers: Transect_ID, Year, Transect_ID_Annual, X/Y coordinates (British National Grid), transect bearings.
  - Per-year vegetation data by species and size class (examples include):
    - Wood-wide tree and shrub counts by DBH classes for multiple species (e.g., Ash, Aspen, Elm, Field Maple, Oak, Birch, Wild Service, Hawthorn, Hazel, Honeysuckle, Privet, Rose, etc.).
    - Species totals (e.g., Ash_Total, Oak_Total, Tree_Total_all, etc.).
    - DBH class breakdowns (e.g., <5 cm, 5–30 cm, >30 cm) and annual adjustments in thresholds (e.g., 1.3 m high reference).
    - Deadwood components (Deadwood_Fallen and Deadwood_Standing) subdivided by diameter ranges and by whether fallen/standing; separate counts for small to large diameter classes and for specific categories like Deadwood_Fallen_Total and Deadwood_Standing_Total.
  - Data quality: some counts denoted as no_data where not recorded; 2005 and 2006 datasets share a consistent field structure with added deadwood fields in 2006.
  - Data availability: transect locations mapped (Figure 1 in the source).

- Quality control and provenance
  - Records checked and cleaned; missing values recorded as no_data.
  - References: Broughton et al. (2006) Marsh Tit Territories in a British Broadleaved Wood; field recording sheet example provided (2006).

- Potential analyses and use for analysts
  - Cross-year comparisons of vegetation structure (DBH distributions, shrub height classes, deadwood presence) across transects.
  - Spatial analyses linking vegetation structure to habitat features associated with Marsh Tit territories and unoccupied areas.
  - Modeling relationships between structural habitat metrics (e.g., large-diameter trees, deadwood) and ecological outcomes.
  - Data can support meta-analyses of habitat change at local scales, including assessments of broader habitat quality and potential drivers of vegetation change.
  - Considerations and caveats:
    - 2005 lacks deadwood data; 2006 includes it, enabling before/after assessment but with different metric granularity.
    - Feb 2005 vs Jul 2006 sampling windows may introduce phenological differences.
    - Local-scale transect design centered on bird territories may bias representation toward particular habitat features.
    - Missing data (no_data) must be handled in analyses; numerous per-species, per-DBH fields require careful preprocessing.