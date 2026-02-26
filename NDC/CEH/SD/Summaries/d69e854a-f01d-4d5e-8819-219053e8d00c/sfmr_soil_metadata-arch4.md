# Soil data from the South Fork McKenzie River in Oregon, USA.

- Purpose and scope
  - Monitoring data to assess soil variable responses to wildfire in restored, unrestored, and reference sites (near Horse Creek unburned site to the East).

- Data content and structure
  - Data type: Monitoring; Dataset size: 22 KB.
  - Interpreted by: All authors.
  - Collection: 1 CSV file named SFMR_Soil_Data containing:
    - Sampling_Date, FieldID, SampleID, SampNum, Site_Type (restored, unrestored, reference), Depth
    - Moisture, Microtopography, Sand, Silt, Clay, Clay_Silt_Pct, Texture
    - Longitude, Latitude, OrganicCarbon_pct, TotalCarbon_pct
    - DateRecd, DateRept, Total_N_ppm, Nitrite_N_ppm, Nitrate_N_ppm
  - Overall dataset structure emphasizes spatial (long/lat) and environmental variables (grain size, texture, C and N forms).

- Collection purpose and methodology
  - Field campaigns:
    - 2020: targeted 22 soil locations per site (A restored floodplain, B unrestored degraded floodplain, C undegraded reference at Horse Creek); sampling included 0–30 cm horizon, with 30–60 cm and 60–90 cm if feasible.
    - 2021: follow-up sampling; July 2021 planned.
  - Sampling approach:
    - 0–30 cm surface samples collected with a T-bar probe; deeper horizons sampled where feasible.
    - Samples placed in bags, frozen, then shipped to Ward Lab for analyses (total carbon, organic carbon, grain size).
  - Sample counts:
    - 53 samples (July 2020)
    - 27 samples (February 2021)
    - 34 samples (June 2021)

- Variables and data standards
  - Site_Type labels: restored, unrestored, reference (Horse Creek).
  - Depth, moisture (wet/dry locations), and microtopography (high/low) are recorded.
  - Grain size distribution: Sand, Silt, Clay with Ward Lab size definitions; Clay_Silt_Pct combines clay+silt.
  - Texture category follows USGS classification.
  - Carbon and nitrogen metrics: OrganicCarbon_pct, TotalCarbon_pct, Total_N_ppm, Nitrite_N_ppm, Nitrate_N_ppm.
  - Geographic coordinates (Longitude, Latitude) included for each sample.
  - Temporal data: Sampling_Date, DateRecd (date received for processing), DateRept (date results reported).

- Data quality and provenance
  - Quality Control (QC): Detailed QC conducted by Moffett Lab (Washington State University).
  - Procedures include retaining duplicate samples and cross-checking parameters (e.g., texture) for accuracy.

- Data lineage and discoverability
  - Dataset identifier: SFMR_Soil_Data (1.csv file) with explicit field definitions and campaign references.
  - Data collected across multiple campaigns and locations to enable comparative analyses of restored, unrestored, and reference areas.

- Gaps, challenges, and considerations for data strategy
  - Incomplete moisture data for some samples; not always available.
  - Depth coverage limited by feasibility; some deeper samples may be missing.
  - Potential variability in data collection timing and site access between campaigns.
  - Metadata could be enhanced with a data dictionary, data provenance notes, and licensing terms to improve reuse.

- Potential uses and value for data leadership
  - Enables assessment of how soil properties respond to wildfire under different restoration statuses.
  - Supports cross-site comparisons and restoration efficacy evaluations.
  - Provides a structured dataset for integrating soil physical and chemical properties with spatial context for policy, planning, and research collaborations.
  - Can inform data governance practices by illustrating standardized fields, QA/QC workflows, and metadata conventions for soil monitoring data.