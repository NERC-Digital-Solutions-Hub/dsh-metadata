# Soil data from the South Fork McKenzie River in Oregon, USA. Lat/Long: 44.17, -122.30.

- Purpose and scope
  - Monitoring dataset to assess soil variable responses to wildfire across restored, unrestored, and reference sites near South Fork McKenzie River, Oregon.
  - Collected to compare soil properties (carbon, nitrogen, texture) across treatment types and depths.

- Dataset overview
  - Data type: Monitoring; File: SFMR_Soil_Data (1 CSV file, ~22 KB).
  - Samples: 53 (July 2020), 27 (February 2021), 34 (June 2021).
  - Dataset columns include Sampling_Date, FieldID, SampleID, SampNum, Site_Type, Depth, moisture, Microtopography, Sand, Silt, Clay, Clay_Silt_Pct, Texture, Longitude, Latitude, OrganicCarbon_pct, TotalCarbon_pct, DateRecd, DateRept, Total_N_ppm, Nitrite_N_ppm, Nitrate_N_ppm.

- Site design and sampling
  - Site types: Restored floodplain, Unrestored degraded floodplain, Reference area (Horse Creek).
  - Depths sampled: 0-30 cm; additional 30-60 cm and 60-90 cm where feasible.
  - Sampling plan (2020): target 22 locations per site (11 wet, 11 dry) with T-bar probes; subset limitations in degraded site.
  - Spatial data: coordinates provided for each sample; pairings indicated (Site_Pairs), and microtopography (high/low).

- Collection methodology and handling
  - Field approach (2021 notes): 0-30 cm bulk samples collected with T-bar; samples bagged, frozen, and sent to Ward Labs or Colorado partners for analyses.
  - Workflow: samples placed in Ziplocs, shipped to processing labs; parameters analyzed include total carbon, organic carbon, and grain-size analyses.

- Data structure and variables
  - Core measurements: texture (USGS classification), grain-size percentages (Sand, Silt, Clay), Clay_Silt_Pct, OrganicCarbon_pct, TotalCarbon_pct, Total_N_ppm, Nitrite_N_ppm, Nitrate_N_ppm.
  - Metadata: Sampling_Date, DateRecd, DateRept, Location (Longitude, Latitude), SampleID, FieldID, SampNum, Site_Type, Depth, moisture, Microtopography.

- Quality assurance and limitations
  - QA/QC conducted by Moffett Lab (Washington State University); duplicate samples retained; cross-checks of select parameters (e.g., texture) for accuracy.
  - Notable data considerations: moisture data may be incomplete (wet/dry selected by eye); data patchiness across sites and depths; reliance on USGS texture classifications.

- How to use
  - Suitable for analyses of soil carbon and nitrogen content by site type and depth, texture distribution, and spatial patterns.
  - Enables comparisons across restored, unrestored, and reference conditions; supports data-driven exploration and visualization (e.g., dashboards, pivot tables).
  - Provides provenance through detailed collection dates, field campaigns, and processing dates for traceability.