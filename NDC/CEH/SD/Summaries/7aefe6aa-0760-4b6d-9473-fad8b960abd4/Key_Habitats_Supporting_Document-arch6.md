# Habitat data from an ecological survey of terrestrial key habitats in England, 1992-1993

- Overview of the dataset and its purpose
  - A national-scale ecological survey focusing on key habitats perceived to be under threat or of concern to the Department for the Environment.
  - Builds on earlier Countryside Surveys (since 1978) but uses a targeted habitat-focused approach for reporting.
  - England-wide in scope, covering Lowland heath, Chalk and limestone calcareous grasslands, Coasts, Uplands, with supplementary lowland river valleys from Countryside Survey 1990.
  - Data collected 1992-1993; some supplementary lowland data from Countryside Survey 1990.

- Geographic and temporal scope
  - Geographic coverage: England.
  - Time period: 1992-1993 (with supplementary data referenced from 1990 Countryside Survey for reporting purposes).

- Data collected and content areas
  - Vegetation data
    - Detailed plant information: vascular plants, bryophytes, and lichens.
    - Plots used: Main (X) plots, Targeted (Y) plots, Streamside (S) and Waterside (W) plots, Roadside/Verge (R/V) plots.
    - Plot sizes and placement varied by landscape/habitat type; multiple plots per 1km square.
  - Boundary data
    - Description of the nearest boundary at grid points (within 100 m) with codes for hedgerows, walls, fences, earth/stone banks, etc.
  - Land cover data
    - Land cover at grid points within each 1km square using Countryside Survey 1990 Codes.
    - Minimum mappable unit: 400 m2; boundaries recorded as nearest boundary segment of at least 20 m.
  - Habitat data and structure
    - Codes and descriptions for habitat/landscape types; vegetation data from multiple plot types; boundary features descriptions.
  - Data management and quality
    - All data collected by trained surveyors; checked and verified where possible.
    - Field handbooks and key Barr et al. documentation guided methods (1992, 1993; 1973 standardized survey methods).

- Data structure and key datasets/files
  - Datasets/Payload
    - Key_Habitat_Survey_Squares.csv: list of 1km survey squares with county, end date, and habitat type.
    - Key_Habitat_Plot_Headers.csv: vegetation plot header information and location (including plot type, size, and classification codes).
    - Key_Habitat_Plot_Species.csv: species recorded within each vegetation plot (species codes, cover, age, height, etc.).
    - Key_Habitat_LC_Features.csv: land cover data mapped at each grid point within survey squares (HAB_TYPE, land-use codes, canopy, weed properties, etc.).
    - Key_Habitat_LC_Species.csv: species details pertaining to land cover features (species, cover, age, height, management, etc.).
    - Key_Habitat_BD_Features.csv: boundary data mapped at each boundary nearest to grid points (habitat/feature codes, land use, canopy/height, and related descriptors).
    - Key_Habitat_BD_Species.csv: species details pertaining to boundary features (species, proportion covers, descriptions).
  - Appendices and code tables
    - Appendix I: List of square codes and habitats/landscape types.
    - Appendix II: Land Cover Codes (descriptions and codes).
    - Appendix III: Boundary Codes (descriptions and codes) and associated boundary feature interpretations.
    - Appendix IV: Land Use (LUSE) Codes (and descriptions).
  - Data relationships
    - Linkages between squares, plots, and species via series IDs, REP_ID, GRIDCODE, and SP_LINK fields, enabling reconstruction of plots within squares and associated vegetation or boundary features.

- Sampling design and coverage
  - Stratified sampling across 1km survey squares, with plots distributed to capture calcareous, coastal, upland, and heath habitats.
  - Multiple plot types per square to capture core vegetation and adjacent features (streams, roadsides, verges, boundaries).
  - Vegetation plots include main X plots and targeted Y plots, plus S/W and R/V plots for broader habitat characterization.
  - Data include both within-square vegetation data and boundary/land-cover context around grid points.

- Data quality, provenance, and references
  - Field data collected by trained surveyors; efforts made to verify data where possible.
  - Methods and data management linked to established field handbooks (Barr 1992, Barr 1993) and the Countryside Survey lineage.
  - Supplementary reporting data drawn from Countryside Survey 1990 to aid reporting for river valleys and lowlands.
  - Key habitat survey outputs include both raw plot-level data and structured feature tables (land cover, boundaries) with descriptive codes to support reproducibility and re-use.

- Potential data products and uses (Data Support perspective)
  - Self-service exploration of habitat distribution and vegetation composition across England for the 1992-1993 period.
  - Dashboards or pivot-table style summaries by habitat type, 1km square, or plot type (X/Y/S/W/R/V).
  - Comparative analysis against Countryside Survey baselines (1990) for trend assessment in key habitats.
  - Spatial-temporal investigations of land-cover and boundary changes at grid-point or plot level.
  - Data can underpin policy reporting, conservation planning, and public-data outreach with clearly defined habitat and vegetation codes.
  - Documentation of data structures and codes supports data ingestion into GIS, statistical analysis, and metadata-driven reuse.

- Practical considerations and challenges for data support
  - Complex code systems (habitat, land cover, boundary, land use) require careful interpretation using the provided appendices.
  - Some squares have no plot data; patchy data across habitat types necessitates awareness of gaps when aggregating.
  - Data exist in multiple related CSVs with cross-references; accurate linking is essential for coherent analysis.
  - Variation in data collection formats across plot types and years (1990s context) may require harmonization for certain longitudinal analyses.

- Documentation and sources for further context
  - Related key publications: Barr C.J. (1992, 1993, 1997) on changes in key habitats; Bunce R.G.H. & Shaw M.W. (1973) standardized survey procedures.
  - Countryside Survey datasets and resources: Countryside Survey website.
  - Management and data contributors: Institute of Terrestrial Ecology, Centre for Ecology & Hydrology; field team and data management staff listed in the dataset description.