# WP3.2_Food_Web_Benthic_Algae_Chlorophylla_Biomass

- Overview
  - Provides quantified autotrophic resources (chlorophyll-a content and ash-free dry mass, AFDM) of benthic biofilm to support construction of quantified food webs.
  - Data presented as means with standard deviations, from multiple replicate samples per site and occasion.

- Location, scope, and timing
  - Sites: Three chalkstream sites in the Wessex chalk area — Nine Mile River, River Till, River Wylye.
  - Landscape gradient: Sites reflect varying catchment land-use intensities.
  - Temporal coverage: Sampling occurred from Oct 2012 to Oct 2013.
  - Sampling framework: Wylye and Nine Mile River sampled on seven occasions; Till on five occasions; not sampled Dec–Mar to avoid disturbing salmonid redds.

- Data collection and laboratory methods
  - Field sampling: At each site/occasion, 10 flat stones were collected from a 100 m survey reach; a 25 x 25 mm area of the stone surface was scrubbed to dislodge biofilm; material collected, labeled, frozen.
  - Laboratory analysis: Samples split into two aliquots.
    - Chlorophyll-a: Extracted with 90% cold acetone, spectrophotometrically measured after 24 h extraction.
    - AFDM: Filtration on preweighed filters, drying at 80°C, weighing, then incineration at 560°C (8–12 h) and re-weighing.
  - Standards and QA: Procedures follow Vernon (1960) and Lorenzen (1967) for chlorophyll-a and AFDM; no formal QA procedure (e.g., replicate repeat analyses); final values checked for obvious outliers (none found).

- Data structure and variables
  - Spatial/identifying fields: RIVER_ID, SITE_ID, RIVER_NAME, SITE_NAME, NGR, EASTING, NORTHING.
  - Temporal field: SAMPLE_DATE.
  - Key measured variables (per site/occasion):
    - Mean_Chla_mgperm2 (chlorophyll-a per m2)
    - StdDev_Chla_mgperm2
    - Chla_n (number of biofilm samples processed for chlorophyll-a)
    - Mean_AFDM_mgperm2 (AFDM per m2)
    - Std_Dev_AFDM_mgperm2
    - AFDM_n (number of biofilm samples processed for AFDM)

- Completeness and limitations
  - Completeness: Seven occasions for Nine Mile River and Wylye; five for River Till.
  - Gaps: No sampling during salmonid breeding season (Dec–Mar); two chlorophyll-a replicates from Nine Mile River (Mar 2013) not processed.
  - Data quality: No formal QA procedure beyond standard lab methods; no major outliers detected.

- Provenance and responsibility
  - Lead organization: Queen Mary University of London River Communities Group.
  - Responsible personnel: Dr J. Iwan Jones and team for collection, processing, analysis, interpretation, and data management.

- Potential GIS applications
  - Spatial visualization: map sampling sites with coordinates and site-level metrics.
  - Temporal analysis: compare chlorophyll-a and AFDM flux/stock across rivers and over time.
  - Integration: link biofilm resource data to land-use gradients and river-network models to support ecological network analyses. 

- References for methods
  - Vernon LP (1960) on spectrophotometric determination of chlorophylls
  - Lorenzen CJ (1967) on chlorophyll and pheophytins spectrophotometric equations