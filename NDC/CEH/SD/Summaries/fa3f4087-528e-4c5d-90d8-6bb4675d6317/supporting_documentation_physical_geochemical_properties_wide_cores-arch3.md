# Physical_geochemical_properties_wide_cores_essex.csv

- Overview
  - Dataset documenting physical and geochemical properties of saltmarsh soils from 19 wide-diameter gouge cores across 8 Essex sites, collected in 2019.
  - Marsh types represented: natural, historic breach, and managed realignment.
  - Purpose aligned with monitoring environmental health and informing coastal and carbon-management decisions within the Carbon Storage in Intertidal Environments (C-SIDE) project.

- What is included
  - Site and sample identifiers: Core_ID; Saltmarsh; Marsh_type.
  - Location data: Lat_dec_deg, Long_dec_deg (WGS84); X_easting, Y_northing (local projected coordinates).
  - Elevation: Elevation_above_OD__m (meters).
  - Subsampling details: Sample_depth_cm; Mid_Point_depth_cm.
  - Physical and geochemical attributes: Substrate; Dry_bulk_density_g_cm_3; OC_perc (organic carbon percentage).
  - Data structure: Described as a CSV with a defined header, including field descriptions (Description; Cell Format) and data types (Text; Number).

- Methods and procedures
  - Sampling: 19 gouge cores (60 mm diameter) collected from eight sites; cores sectioned at 1 cm intervals (n = 1952 sub-samples).
  - Location and sampling controls: DGPS used for precise site locations; samples frozen at -20°C until analysis.
  - Core description and classification: Troels-Smith framework used for substrate descriptions.
  - Laboratory analyses: Organic carbon quantified using Elementar Soli TOC with the temperature gradient method (DIN 19539); calibration with CaCO3 and standard soils; isotopic QC via high OC sediment standard.
  - Quality assurance: Laboratory equipment calibrated per standard practices; data quality controlled and traceable to equipment and standards.

- Data formatting and metadata
  - Primary format: .csv (with additional data resource description detailing headers and data types).
  - Key fields and definitions are explicitly described, enabling data reuse and integration with other datasets.
  - Metadata supports traceability from field sampling to laboratory analysis and data outputs.

- Data governance and sharing
  - Data are generated under the C-SIDE project (funded by NERC) with an emphasis on data quality, openness, and clear provenance.
  - Public sharing of underlying data is possible but can be subject to governance considerations; metadata and methodological details are provided to facilitate transparency and reuse.
  - Standardized procedures (Troels-Smith classification; DIN 19539) support consistent data governance and comparability with other datasets.

- Relevance for monitoring environmental health
  - Provides baseline measurements of saltmarsh soil physical properties and organic carbon content across different marsh origins, enabling assessment of carbon stocks and status over time.
  - Supports spatially explicit monitoring and modeling of coastal carbon storage, aiding policy evaluation of managed realignment and restoration scenarios.
  - Methodological transparency enhances replication, aggregation, and cross-site comparisons essential for monitoring frameworks.

- References and standards
  - Sampling and density methods: Dadey, Janecek, and Klaus (1992).
  - TOC measurement methodology: DIN 19539 (2015).
  - Soil carbon context and thermochemical considerations: Natali et al. (2020); Smeaton et al. (2021).
  - Troels-Smith sediment classification: Troels-Smith (1955).