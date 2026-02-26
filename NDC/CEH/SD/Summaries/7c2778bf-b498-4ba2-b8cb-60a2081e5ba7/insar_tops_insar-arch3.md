# Interferometric Synthetic Aperture Radar (InSAR) measurements over Caithness and Sutherland to measure peatland surface motion in the Flow Country using APSIS

- Overview
  - Uses InSAR to measure peatland surface motion across the Flow Country (Caithness and Sutherland) with the APSIS (Intermittent Small Baseline Subset) technique.
  - Produces timeseries of peat surface height and long-term mean motion in the survey area.
  - Data collected on a 6–12 day cycle from 12 March 2015 to 1 June 2019; missing pixels excluded due to low coherence; processing conducted by Terra Motion Ltd.

- Survey Area and Coverage
  - Area processed: approximately 930 km² of blanket bog in the Flow Country.
  - Excludes water bodies and the sea; focused on land surfaces across multiple vegetation types.
  - Ground motion measured relative to a stable reference point at Wick Airport (58.4533° N, 3.0879° W).

- Methodology and Processing
  - Data source: 410 Sentinel-1A and Sentinel-1B SAR images (orbit 125) gathered every 6–12 days between March 2015 and June 2019.
  - Processing framework: APSIS, an adapted low-resolution SBAS DInSAR time-series approach to improve density and spatial coverage in vegetated areas.
  - Software: Terra Motion Limited’s Punnet for co-registration and time-series generation; SNAPHU-based phase unwrapping (in-house implementation).
  - Coherence and baselines: maximum horizontal baseline 250 m; maximum temporal separation 1 year; coherence threshold 0.25; point threshold 360.
  - Outputs per georeferenced pixel: motion time series (multiannual average line-of-sight velocity, m/yr) and mean velocity in the line-of-sight.

- Data Products and Formats
  - Primary products (per pixel, ~80 × 90 m resolution):
    - Motion time series (line-of-sight velocity, m/yr).
    - Mean velocity in the line-of-sight (evv-corrected product).
  - Additional supporting files:
    - ortho_velocity_utm_isbas.tif: Mean line-of-sight motion over the study period (m/yr).
    - ortho_velocity_utm_isbas_evv.tif: Corrected mean vertical motion over the study period (m/yr).
    - ortho_cohcount.tif: Number of coherent interferograms per pixel (quality indicator).
    - ortho_velocity_utm_verror.tif: Standard error of the line-of-sight motion (m/yr).
  - Reference frame and projections:
    - Coordinate reference system: WGS84 UTM Zone 29N.
    - No_data value: -999.
  - Time-series and height data:
    - Time-series files: individual .tif with corresponding .aux files; filenames dated (e.g., 20190701.tif, 20190701.tif.aux).
    - Height information: relative land-surface height files associated with specific dates.
  - Data naming conventions and units:
    - Height in meters; timeseries files named by date; a consistent, replicable naming convention is used for both velocity and height datasets.

- Data Provenance and Access
  - Data sources: Copernicus Sentinel data (S1A/S1B) from the European Space Agency Open Access Hub (scihub.copernicus.eu) (2015–2019).
  - Processing provenance: Terra Motion Ltd. (APSIS/isbas) with in-house Punnet software; SNAPHU for phase unwrapping.
  - Datasets cover multiple landcover types within the Flow Country peatlands and provide long-term motion metrics as well as near-term time-series.

- Quality, Gaps and Limitations
  - Gaps and missing data: pixels with low coherence removed; missing survey dates correspond to processing issues or persistent coherence problems.
  - Data quality indicators: ortho_cohcount.tif provides the number of coherent interferograms per pixel; ortho_velocity_utm_verror.tif provides standard errors.
  - Data transformation: some processing steps and data transformations are required to render the time-series usable for analysis, which can pose barriers if metadata are incomplete.
  - Coverage limitations: data quality and density are influenced by vegetation, surface water presence, and atmospheric conditions.

- Relevance for Monitoring Frameworks
  - Provides a quantitative, spatially explicit measure of peatland surface motion, useful for evaluating peatland stability, hydrological changes, drainage effects, and subsidence risk.
  - Demonstrates how to identify and fill data gaps through satellite-based monitoring, leveraging public Sentinel data and a transparent processing chain.
  - Supports reporting and decision-making through clear outputs (velocity time-series, mean velocities, and vertical motion corrections) and accompanying metadata indicators (coherence counts, errors).
  - Highlights data governance considerations relevant to monitoring frameworks:
    - Data provenance and processing transparency (documented methodology and software).
    - Metadata adequacy and accessibility (structured file naming, coordinate reference systems, and auxiliary data).
    - Open data sources (Sentinel data) and the need to share derived outputs and underlying data where feasible.
    - The balance between data sharing and data quality assurance (publicly sharing datasets, while ensuring metadata and data governance standards are met).

- Practical Implications and Use
  - Can inform policy and management decisions related to peatland conservation, climate resilience, and land-use planning by providing evidence of surface motion dynamics over time.
  - Enables monitoring authorities to assess temporal trends and spatial patterns of movement, contributing to risk assessment and adaptation planning.
  - The dataset’s structure (georeferenced rasters, accompanying QA metrics) facilitates integration into dashboards, reports, and governance processes.

- References and Data Sources
  - Sentinel data (2015–2019) processed by ESA; APSIS/ISBAS methodology and related literature cited.
  - Core references include ISBAS-based InSAR processing and time-series analysis methods (Bateson et al., Cigna & Sowter, Gong et al., Osmanoğlu et al., Sowter et al.).