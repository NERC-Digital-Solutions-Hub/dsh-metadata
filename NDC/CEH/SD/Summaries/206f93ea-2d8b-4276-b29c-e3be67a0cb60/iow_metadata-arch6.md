# Supporting Information Isle of wight data

- Overview
  - Data were collected to assess whether the presence of an adjacent older neighbour affects woodland structure and height in recently created woodlands.
  - Based on woodlands in the Isle of Wight.
  - Local and landscape variables calculated using GIS; canopy height and height complexity derived from LiDAR point cloud data.
  - Data compiled by Samuel Hughes, University of Leeds.

- Experimental design / sampling regime
  - LiDAR data provided by Defra, 2011.
  - Woodlands used: all under 1 hectare and covered by LiDAR; broadleaved woodlands according to the national forest inventory.
  - Sample size: N = 65.

- Generation
  - Data analysed from November 2020 through March 2021 using R.

- Variable explanations
  - Shape area: Area in m^2 of the woodland.
  - Hectares: Area in hectares of the woodland.
  - Neighb: Whether the woodland was created adjacent to an established mature woodland neighbour or not.
  - Year_planted: The decade in which the woodland first appeared on records.
  - Mean_elev: Mean elevation of the woodland.
  - Slope: Mean slope gradient of the woodland.
  - Northness: Aspect variable calculated from the cosine of the mean woodland radians; 1 = due north, -1 = due south.
  - Soil: Underlying geology of the woodland (codes include SDST = sandstone, AROC+SDST = argillaceous rock mixed with sandstone, CHLK = chalkstone, AROC = argillaceous rock).
  - VCI: Vertical Complexity Index normalised by the maximum height across woodland samples.
  - Point_rh90: Relative height at the 90th percentile of LiDAR returns (units listed as m^2 in the data description).
  - Entropy: Foliage height diversity normalised by the maximum height of the woodland.
  - Mean_crown_area: Mean area of tree crowns in a woodland (calculated via the Dalponte algorithm in the lidr package).
  - Tree_count: The number of trees in each woodland.

- Quality control
  - Satellite imagery used to verify LiDAR data alignment with polygons.
  - Site visits were not possible due to COVID-19 restrictions.

- Data structure
  - All data are contained in a single CSV file.
  - Rows represent observations/woodlands; columns represent variables.