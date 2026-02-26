# Fish abundance, habitat, water quality, flow and climate data from English rivers,1975-2017.

- Purpose and aim
  - Aims to use data to demonstrate environmental condition in a consistent format, enabling scrutiny of environmental health and policy performance over time.
  - Analysts typical role: interpret monitoring data from established sources, apply standardised methods, and present outputs for policy and management evaluation.

- Scope and location
  - Geographic focus: England.
  - Temporal coverage: fish abundance, habitat, water quality, flow and climate data spanning 1975–2017 (dataset described in the readme with updates up to 2022/2024).

- Data provenance and funding
  - Data authors: Ainsworth, Nunn, Bachiller-Jareno, Rizzo, Scarlett, Antoniou, and colleagues.
  - Funding: NERC Chempop grant NE/S000100/2.
  - Citation: Ainsworth et al. (2024) Fish abundance, habitat, water quality, flow and climate data from English rivers, 1975-2017. NERC EDS Environmental Information Data Centre. DOI provided.

- Access, licensing, and related data
  - Licensing: NFPD data and RHS are open; Crown copyright and database rights; specific licenses and links to ancillary data provided.
  - Public links: NFPD fish data, land cover maps, altitude data, and EDF model references are publicly accessible; citations to related methodologies and tools are provided.
  - Data citation and DOI: dataset has an official DOI; emphasizes reproducibility and traceability.

- Dataset structure and contents
  - File organization: site-level and data tables are organized as regional files (Anglian, Midlands, North East, North West, Thames, Southern, South West); a single Species table accompanies the data.
  - Primary data file: CP_Fish_SiteVariables_region.csv
    - Contains 18 variables per region.
    - Key covariates include:
      - HQA_Score (Habitat Quality Assessment) and HMS_Score (Habitat Modification/Quality) from River Habitat Survey (RHS).
      - Fish_Altitude (site elevation).
      - Land use covariates: LC_Woodland_Per, LC_Arable_Per, LC_Seminatural_Per, LC_Urban_Per and their corresponding Area measures (km2) upstream from each fish site.
      - BFI (Base Flow Index) representing upstream hydrology.
      - EDF_Mean, EDF_SD, EDF_Q90, EDF_Q95 (Effluent Dilution Factor metrics) for wastewater influence.
      - ED_SITE_ID (associated effluent dilution site identifiers).
      - Spatial identifiers: Fish_SiteID, Fish_Name, Fish_River, Fish_Catchment, Fish_Easting, Fish_Northing.
  - Data relationships: Fish_SiteID links to entries in DataTable, Hydrology, and chemical determinand files.

- Data sources and derivation
  - RHS data: HQA/HMS scores linked to fish sites via IRN extension; RHS scores from RHS survey sites approximate alignment within 5 km along the river.
  - Land use: derived from CEH Land Cover Map 2015 (LCM2015) and CEH IHDTM (50 m) elevations; 21 land cover categories collapsed into four macro-categories (Woodland, Arable, Sem natural, Urban) for upstream catchments.
  - Altitude: extracted from CEH IHDTM; two values computed per site (cell-centre value and bilinear-interpolated average); centre value used.
  - EDF (wastewater influence): computed with LowFlows2000-WQX model; matches fish sites to the closest river network reach; provides distribution of wastewater influence as mean, SD, 90th and 95th percentiles.
  - Data processing tools: ArcGIS (10.6.1+ for elevation extraction; 10.7+ or Pro for interpretation); GRASS GIS (r.accumulate) for land-use accumulation; DataLabs for land-use extraction; Python 3 for EDF and land-use processing.

- Data processing and quality assurance
  - Processing steps:
    - RHS: minimal transformation; some sites may not match to RHS sites.
    - Land use: generation of 21 category rasters; aggregation into four macro-categories; extraction of upstream area/percentages for each fish site.
    - EDF: association to closest river network reach; mean and percentile statistics produced; sites with discrepancies set to no data.
    - Altitude: calculation using IHDTM with attention to NoData cells (treated as 0 m where appropriate).
  - Quality assurance:
    - Independent checks by Nunn (distance criteria, within 1 km acceptable).
    - Sum of macro-category percentages checked to 99.96–100.04%.
    - NoData handling documented for EDF and altitude.
  - Documentation of processing requirements:
    - Software: ArcGIS 10.7+ or Pro; GRASS GIS; DataLabs; Python 3.
    - Data interpretation notes and scripts referenced for reproducibility.

- Versioning and updates
  - Multiple versions and file updates:
    - 20211116_HIFI_JuvenileFish_England_SiteTable: split of site covariates; removal of HMS, HQA land use, and BFI from the data table and regional file split.
    - Updates on 2022/05/31 and 2022/08/12 noted for specific file changes and structure.

- Practical implications for Analysts monitoring the environment
  - Enables standardized, comparable indicators of habitat quality, hydrology, and wastewater influence across English rivers over multiple decades.
  - Facilitates integrated analysis by linking site-level fish data with habitat scores, land-use context, and hydrological/wastewater influence metrics.
  - Supports cross-site and longitudinal monitoring, with clear provenance and methodological documentation to assess performance against environmental standards.

- Notes on limitations and usage considerations
  - Some sites may lack RHS matches; EDF data may be blank where network matching issues occur.
  - Land-use covariates are upstream-catchment derived and aggregated into macro-categories; spatial interpolation and raster processing require specific software environments.
  - Data availability and structure reflect regional segmentation; users should join regional files via Fish_SiteID and ED_SITE_ID as needed.