# Supporting Information Isle of wight data

## Aim
- Determine whether the presence of an adjacent older neighbour affects woodland structure and height in recently created woodlands.

## Data source and scope
- Location: Isle of Wight woodlands
- Sample size: 65 woodlands (N = 65)
- Woodland size: all under 1 hectare
- Type: broadleaved woodlands per the national forest inventory
- Data sources: LiDAR data provided by Defra (2011); GIS-derived local and landscape variables; canopy height and height complexity from LiDAR point cloud data
- Data compilation: Samuel Hughes, University of Leeds
- Data format: single CSV file with rows as observations/woodlands and columns as variables

## Experimental design / sampling
- Selection: woodlands under 1 ha, covered by LiDAR
- Adjacent condition: adjacent to an established mature woodland neighbour or not (Neighb variable)

## Generation and analysis
- Analysis period: November 2020 to March 2021
- Software: R

## Variables (and interpretations)
- Shape_area: woodland area in square meters
- Hectares: woodland area in hectares
- Neighb: adjacency to an established mature woodland neighbour (yes/no)
- Year_planted: decade when the woodland first appeared on records
- Mean_elev: mean elevation of the woodland
- Slope: mean slope gradient of the woodland
- Northness: aspect metric; cos of mean woodland radian (1 = due north, -1 = due south)
- Soil: underlying geology (categories include SDST = sandstone, AROC+SDST = argillaceous rock mixed with sandstone, CHLK = chalkstone, AROC = argillaceous rock)
- VCI: vertical complexity index normalized by the maximum height among all woodland samples
- Point_rh90: relative height at the 90th percentile of LiDAR returns (m)
- Entropy: foliage height diversity normalized by the maximum woodland height
- Mean_crown_area: mean area of tree crowns (calculated using the Dalponte algorithm in the lidr package)
- Tree_count: number of trees in each woodland

## Quality control
- Satellite imagery used to verify LiDAR data matched with polygon boundaries
- Site visits were not possible due to COVID-19 restrictions

## Data structure
- All data stored in a single CSV file; rows represent woodlands and columns represent variables

## Additional notes
- Data include both GIS-derived and LiDAR-derived metrics to assess structural characteristics and complexity
- The adjacency variable enables analysis of how proximity to an older neighbour influences woodland development and structure