# The Glastir Monitoring and Evaluation Programme (GMEP)

- Purpose and aims
  - Wales-wide monitoring programme established in 2013 to assess the effects of the Glastir agri-environment scheme on the environment.
  - Seeks evidence on the effectiveness of management interventions related to climate change, biodiversity, soil and water quality, and woodland expansion.
  - Collects data to quantify status and trends in the environment, and to identify how drivers of change (e.g., land use, climate, pollution) impact the environment beyond Glastir interventions.

- The unified peat map: purpose and significance
  - Welsh Government commissioned a unified map to map peat extent and condition in support of GMEP.
  - Represents a major advance over previous peat maps and provides a more detailed picture of peat distribution, including many small lowland peat units.
  - Highlights extensive upland peat in NE and NC Wales and central Wales, and significant lowland peatlands with notable biodiversity interest.
  - Useful for understanding carbon dynamics (greenhouse gas emissions) and environmental status across the country.

- Data sources and integration (Generation Methods)
  - Four datasets combined to create the unified peat map (peat > 45 cm depth):
    - Areas mapped as peat in the British Geological Survey (BGS) superficial geology map (1:50,000).
    - Soil data from Forestry Commission Wales digital soil records (codes indicating peat > 45 cm).
    - Deep peat boundary from Lowland Peatland Survey of Wales.
    - Habitat polygons indicating deep peat presence from Habitat Survey of Wales (Phase I).
  - Datasets were merged sequentially using the UNION operation in ArcMap GIS to form a final multipart polygon shapefile.

- Data quality and limitations (Quality Control/Assurance)
  - Final quality depends on the input data quality and the reliability of the national datasets.
  - Most data are based on direct ground surveys; where peat presence is inferred from vegetation boundaries, especially in uplands, boundaries are less precise.
  - Lowland peat mapping is fairly reliable; upland boundaries may be more uncertain due to mosaic vegetation and mapping resolution.

- Data product details
  - GMEP_Unified_Peat_Map.shp: ESRI Shapefile containing the outline location of peat soils in Wales.
  - Attributes include:
    - FID: Unique polygon identifier
    - SHAPE_AREA: Polygon area (square metres)
    - SHAPE_LEN: Polygon length (metres)
    - DESC_: Description of polygons (peat)
  - Provides a comprehensive spatial representation of deep peat (≥0.5 m) and peat bodies.

- Usage, references, and licensing
  - References include multiple Welsh and UK data sources and reports (e.g., Evans et al. 2015; Jones et al. 2011; Blackstock et al. 2010; Kennedy 2002; Lawley 2009; Pyatt 1982; ECOSSE 2007; and others).
  - Any product derived from or incorporating the data must acknowledge sources with explicit statements such as:
    - "© Hawlfraint y Goron: Llywodraeth Cymru" or "© Crown copyright: Welsh Government"
    - "Contains Natural Resources Wales information © NRW" and "Derived in part from British Geological Survey geology data 1:50,000 scale. BGS © UKRI."
  - Notes that the mapping and data are intended to support environment monitoring and policy assessment through integrated datasets.

- Implications for Data Leaders
  - Emphasizes the importance of an integrated data system spanning multiple agencies and datasets to monitor environmental outcomes.
  - Highlights benefits of co-ownership and collaboration for data products (e.g., unified peat map) to support decision making, reporting, and policy evaluation.
  - Underlines need for clear metadata, data provenance, and quality controls when combining diverse datasets.
  - Demonstrates practical data governance considerations: transparency about data sources, methodological choices (e.g., peat thickness threshold, union-based integration), and clear licensing/acknowledgement requirements.
  - Encourages ongoing data updates and iteration to keep monitoring outputs relevant for policy and management, while maintaining discoverability and accessibility of data assets.