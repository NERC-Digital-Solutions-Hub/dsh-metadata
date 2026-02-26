# Supporting Information Isle of wight data

- Purpose and scope
  - Data collected to assess whether the presence of an adjacent older neighbour affects woodland structure and height in recently created woodlands on the Isle of Wight.
  - Combines local and landscape variables calculated via GIS with canopy height and height complexity derived from LiDAR point cloud data.
  - Compiled by Samuel Hughes, University of Leeds.

- Experimental design and sampling
  - LiDAR data provided by Defra (2011).
  - Woodlands: all under 1 hectare and classified as broadleaved according to the national forest inventory.
  - Sample size: 65 woodlands (N = 65).

- Generation and analysis
  - Data analysed from November 2020 to March 2021 using R.

- Variable explanations (selected key variables)
  - Shape area: woodland area in square meters.
  - Hectares: woodland area in hectares.
  - Neighb: whether the woodland is adjacent to an established mature woodland neighbour.
  - Year_planted: decade when the woodland first appeared on records.
  - Mean_elev: mean elevation of the woodland.
  - Slope: mean slope gradient of the woodland.
  - Northness: aspect metric (cosine of mean woodland radians; 1 = due north, -1 = due south).
  - Soil: underlying geology (e.g., SDST = sandstone; CHLK = chalkstone; combinations listed).
  - VCI: vertical complexity index normalized by the maximum height among samples.
  - Point_rh90: relative height at the 90th percentile of LiDAR returns.
  - Entropy: foliage height diversity normalized by maximum woodland height.
  - Mean_crown_area: mean area of tree crowns (via Dalponte algorithm in lidr package).
  - Tree_count: number of trees in the woodland.

- Quality control
  - Satellite imagery used to verify alignment between LiDAR data and polygon boundaries.
  - Site visits were not possible due to the Covid pandemic.

- Data structure and accessibility
  - Data stored in a single CSV file.
  - Rows represent individual woodlands; columns represent the variables described above.