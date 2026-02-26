# Supporting Information Isle of wight data

## Objective and scope
- Investigates whether the presence of an adjacent older neighbour influences woodland structure and height in recently created woodlands on the Isle of Wight.
- Focuses on local and landscape variables derived via GIS; canopy height and height complexity derived from LiDAR point cloud data.
- Data compiled by Samuel Hughes, University of Leeds.

## Data sources and study design
- LiDAR data provided by Defra (2011).
- Woodlands: all under 1 hectare, broadleaved per national forest inventory.
- Sample size: N = 65 woodlands.
- Spatial scope: woodlands located on the Isle of Wight; adjacent to mature neighbouring woodland considered as a factor.
- Data processing uses GIS-based calculations to derive local and landscape variables.

## Generation and analysis
- Data analysed from November 2020 through March 2021 using R.
- LiDAR-derived metrics used to quantify canopy height and height complexity.

## Variables and measurements
- Shape_area: woodland area in square meters.
- Hectares: woodland area in hectares.
- Neighb: whether the woodland is adjacent to a mature neighbouring woodland (yes/no).
- Year_planted: decade when the woodland first appeared on records.
- Mean_elev: mean elevation of the woodland.
- Slope: mean slope gradient.
- Northness: aspect metric (cosine of mean aspect); 1 = due north, -1 = due south.
- Soil: underlying geology with categories:
  - SDST = sandstone
  - AROC+SDST = argillaceous rock + sandstone
  - CHLK = chalkstone
  - AROC = argillaceous rock
- VCI: vertical complexity index, normalized by the maximum height across woodlands.
- Point_rh90: relative height at the 90th percentile of LiDAR returns.
- Entropy: foliage height diversity, normalized by the maximum height for the woodland.
- Mean_crown_area: average crown area derived via the Dalponte algorithm (via the lidr R package).
- Tree_count: number of trees in each woodland.

## Data quality and limitations
- QA: Satellite imagery used to ensure LiDAR data aligned with polygon boundaries.
- Limitations: site visits were not possible due to Covid-19 restrictions.

## Data structure and accessibility
- Data stored in a single CSV file.
- Rows represent individual woodlands; columns represent the variables listed above.