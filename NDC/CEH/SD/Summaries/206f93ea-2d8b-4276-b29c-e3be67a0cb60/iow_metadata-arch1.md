# Supporting Information Isle of wight data

- Aim
  - Investigate whether the presence of an adjacent mature woodland neighbour affects woodland structure and height in recently created woodlands on the Isle of Wight.
  - Data combine local and landscape variables using GIS; canopy height and height complexity derived from LiDAR point cloud data.
  - Dataset compiled by Samuel Hughes (University of Leeds).

- Experimental design / sampling regime
  - LiDAR data provided by Defra (2011).
  - Woodlands included: all under 1 hectare, covered by LiDAR, and classified as broadleaved according to the national forest inventory.
  - Sample size: N = 65.

- Generation (data analysis timeline)
  - Analysed in R from November 2020 through March 2021.

- Variables (descriptions)
  - Shape_area: woodland area in square meters.
  - Hectares: woodland area in hectares.
  - Neighb: whether the woodland is adjacent to an established mature woodland neighbour.
  - Year_planted: decade when the woodland first appeared in records.
  - Mean_elev: mean elevation of the woodland.
  - Slope: mean slope gradient of the woodland.
  - Northness: aspect variable (cosine of mean woodland radians); 1 = due north, -1 = due south.
  - Soil: underlying geology; categories include SDST = sandstone; AROC+SDST = argillaceous rock with sandstone; CHLK = chalkstone; AROC = argillaceous rock.
  - VCI: vertical complexity index normalized by the maximum height across all woodland samples.
  - Point_rh90: relative height at the 90th percentile of LiDAR returns (m).
  - Entropy: foliage height diversity normalized by the maximum woodland height.
  - Mean_crown_area: mean tree crown area (computed with the Dalponte algorithm in the lidr package).
  - Tree_count: number of trees in each woodland.

- Quality control
  - Satellite imagery used to verify LiDAR data alignment with polygon boundaries.
  - Site visits were not possible due to Covid-19.

- Data structure and storage
  - All data stored in a single CSV file; each row is a woodland observation and each column is a variable.

- Practical notes for analysts
  - Both local (e.g., Neighb, Year_planted, soil) and landscape variables (e.g., VCI, Entropy, Point_rh90) are available for modelling effects of neighbourhood on canopy structure.
  - The small, locally focused sample (N=65) and uniform woodland size (<1 ha) should be considered when extrapolating to broader scales.
  - Data provenance and methods (Defra LiDAR 2011; Dalponte algorithm via lidr) provide reproducible paths for replication and validation.