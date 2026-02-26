# Supporting Information Isle of wight data

- Purpose: Assess whether presence of an adjacent older mature neighbour affects woodland structure and height in recently created woodlands on the Isle of Wight.
- Data origin and compilation: Woodlands data from Isle of Wight; local and landscape variables calculated via GIS; canopy height and height complexity derived from LiDAR point cloud data; data compiled by Samuel Hughes, University of Leeds.

## Experimental design and generation

- LiDAR data provided by Defra (2011).
- Woodlands: all under 1 hectare; broadleaved according to the national forest inventory.
- Sample size: 65 woodlands (N = 65).
- Analysis period: November 2020 to March 2021 using R.

## Dataset structure

- Data format: single CSV file.
- Rows: observations/woodlands.
- Columns: variables (as described below).

## Variables and definitions

- Shape_area: woodland area in square meters (m^2).
- Hectares: woodland area in hectares (ha).
- Neighb: whether the woodland is adjacent to an established mature woodland neighbour (yes/no).
- Year_planted: decade when the woodland first appeared in records.
- Mean_elev: mean elevation of the woodland.
- Slope: mean slope gradient of the woodland.
- Northness: aspect variable (cosine of mean woodland radians); 1 = due north, -1 = due south.
- Soil: underlying geology with codes (e.g., SDST = sandstone; AROC+SDST = argillaceous rock mixed with sandstone; CHLK = chalkstone; AROC = argillaceous rock).
- VCI: Vertical Complexity Index normalised by the maximum height across woodland samples.
- Point_rh90: relative height at the 90th percentile of LiDAR returns.
- Entropy: foliage height diversity normalised by the maximum height for the woodland.
- Mean_crown_area: mean crown area calculated using the Dalponte algorithm in the lidr R package.
- Tree_count: number of trees in the woodland.

## Quality control and limitations

- Verification: Satellite imagery used to ensure LiDAR data aligned with polygon delineations.
- Limitations: Site visits not possible due to Covid-19 restrictions; potential alignment and data currency considerations given 2011 LiDAR data.

## Governance, provenance, and reuse considerations

- Provenance: LiDAR data from Defra (2011); woodlands defined as <1 ha and broadly consistent with national inventory.
- Data lineage: Analysis performed in R (Nov 2020–Mar 2021) by the data compiler.
- Documentation needs for reuse: the dataset is in a single CSV with a clear variable glossary; consider adding a formal metadata file (data dictionary, versioning, update plan) to support data governance, discovery, and reuse by data stewards and users.