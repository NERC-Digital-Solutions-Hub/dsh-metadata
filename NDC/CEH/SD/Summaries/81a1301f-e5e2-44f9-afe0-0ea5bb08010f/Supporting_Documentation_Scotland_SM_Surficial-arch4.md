# Supporting documentation for data resource Scotland_SM_Surficial.csv

- Project and team
  - Project: Carbon Storage in Intertidal Environments (C-SIDE)
  - Funding: NERC (NE/R010846/1)
  - Staff Responsible: William Austin
  - Research Team: Paulina Ruranska (U. of St Andrews), Lucy C. Miller (U. of St Andrews), Carolyn Hindle (U. of St Andrews), Cai J.T. Ladd (U. of Glasgow/Bangor University), Craig Smeaton (U. of St Andrews), Martin W. Skov (Bangor University), William E.N. Austin (U. of St Andrews/Scottish Association of Marine Science), C-SIDE Citizen Science Team

- Data resource at a glance
  - Name: Scotland_SM_Surficial.csv
  - Description: Dry bulk density, loss on ignition (LOI), and organic carbon content of surficial soils from Scottish salt marshes (top 10 cm)
  - Timeframe: 2018–2020 (Scottish portion of C-SIDE sampling program and the CarbonQuest Citizen Science sampling program; Jan 2018–Dec 2019)
  - Coverage: Scotland (excluding Outer Hebrides and Shetland Islands); 471 soil samples from 46 salt marshes
  - Data resource focus: Soil properties relevant to carbon storage and marsh soil characterization

- What the dataset contains
  - Observations: Dry bulk density (g cm-3), LOI (%), organic carbon content (% by weight) derived from surficial soil samples
  - Depth: Top 10 cm of soil
  - Sample count and sites: 471 samples across 46 salt marshes
  - Spatial identifiers: Site names, Lat_dec_deg and Long_dec_deg (WGS84), plus OSGB grid references, X_easting, Y_northing
  - Additional attributes: Soil_Texture (Sandy/Not-Sandy), Year of sampling, Year Lat/Long were recorded, Saltmarsh_Name, Grid_Reference Location

- Sampling and data collection methods
  - Field sampling: 
    - Methods include 50 ml syringe (modified) to 10 cm depth or a 30 mm gouge corer with top 10 cm subsampled
    - GPS locations recorded via mobile devices or RTK systems
    - Samples frozen at -20°C until analysis
  - Lab analyses:
    - Dry Bulk Density calculated from dry mass and pre-drying volume
    - LOI determined by combusting dried, milled samples at 450°C for 4 hours
    - Organic carbon measured by Elemental Analysis (CN) after acidification to remove carbonates
    - Calibration: Elemental Analyzer calibrated with Acetanilide; repeated analysis of standard materials ensures measurement consistency
  - Soil texture: classified as Sandy or Not-Sandy (method based on Ford et al., 2019) with expert judgement
  - Data handling: Multiple procedures described for QA/QC and metadata capture

- Quality control and data validation
  - Citizen Science QC: samples from citizen scientists visually checked by experienced salt marsh scientists before drying
  - Geographic validation: sample coordinates cross-checked against habitat maps and aerial imagery to confirm salt marsh origin
  - Team-based verification: four team members independently classified grid references and validated location data
  - Metadata integrity: detailed header/descriptions for fields (e.g., Lat_dec_deg, Long_dec_deg, X_easting, Y_northing, Year, Depth_cm, Sampling_Method, File formats)

- Data formats and metadata
  - Primary format: CSV (scotland_SM_Surficial.csv)
  - Location references: decimal degrees (WGS84) and OS grid (OSGB 1936) with easting/northing
  - Key fields include: Saltmarsh_Name, Lat_dec_deg, Long_dec_deg, Year, Grid_Reference, X_easting, Y_northing, Sampling_Method, Depth_cm, Dry_Bulk_Density_g_cm_3, OC_Perc, LOI_Perc, Soil_Texture
  - Header and data descriptions are included as part of the resource documentation to support discoverability and interpretation

- Data management and governance
  - Data coverage is limited to Scotland (excluding specific islands) with explicit site selection to capture contrasting habitats and sediment types
  - No planned repeat sampling for this dataset
  - Emphasizes data discovery, format consistency, and metadata richness to support reuse and integration with broader data systems
  - References provided for methodologies and calibration practices

- Uses and relevance for data leadership
  - Supports assessment of carbon storage potential in Scottish salt marshes and spatial comparisons across sites
  - Demonstrates end-to-end data pipeline: field collection, laboratory analysis, QA/QC, geospatial validation, and documentation
  - Highlights practical considerations for data access, discoverability, and metadata standards to enable cross-network collaboration and broader data sharing
  - Provides a model for coordinating university researchers with citizen science contributions and ensuring data quality and provenance

- References
  - Craft et al. 1991; Dadey et al. 1992; Ford et al. 2019; Kennedy et al. 2005; Nieuwenhuize et al. 1994; Verardo et al. 1990