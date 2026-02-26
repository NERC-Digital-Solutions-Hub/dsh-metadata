# Supporting Information Isle of wight data

- Purpose
  - Data collected to assess whether an adjacent older neighbouring woodland influences structure and height in recently created woodlands on the Isle of Wight.
  - Uses local and landscape variables derived from GIS; canopy height and height complexity derived from LiDAR data.
  - Compiled to explore interactions between land-use history and woodland attributes.

- Experimental design / Sampling regime
  - LiDAR data provided by Defra (2011).
  - Woodlands: less than 1 hectare, covered by LiDAR, broadleaved as defined by the national forest inventory.
  - Sample size: 65 woodlands.

- Generation / Analysis
  - Data analysis conducted from November 2020 to March 2021 using R.

- Variable explanations
  - Shape area: woodland area in square metres (m^2).
  - Hectares: woodland area in hectares (ha).
  - Neighb: whether the woodland is adjacent to an established mature woodland neighbour.
  - Year_planted: decade in which the woodland first appeared on records.
  - Mean_elev: mean elevation of the woodland.
  - Slope: mean slope gradient of the woodland.
  - Northness: aspect variable (cosine of mean woodland radians; 1 = due north, -1 = due south).
  - Soil: underlying geology (categories: SDST = sandstone; AROC+SDST = argillaceous rock mixed with sandstone; CHLK = chalkstone; AROC = argillaceous rock).
  - VCI: vertical complexity index normalized by the maximum height across all woodlands.
  - Point_rh90: relative height at the 90th percentile of LiDAR returns (m).
  - Entropy: foliage height diversity normalized by the maximum height of the woodland.
  - Mean_crown_area: mean area of tree crowns, calculated with the Dalponte algorithm (lidr package).
  - Tree_count: number of trees in each woodland.

- Quality control
  - Satellite imagery used to confirm LiDAR data alignment with polygon boundaries; site visits were not possible due to Covid restrictions.

- Data structure
  - All data stored in a single CSV file: rows represent individual woodlands; columns represent the variables listed above.

- Provenance
  - Data compiled by Samuel Hughes, University of Leeds.
  - LiDAR data provided by Defra (2011).