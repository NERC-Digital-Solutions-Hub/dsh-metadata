# The Glastir Monitoring and Evaluation Programme (GMEP)

- Purpose and scope
  - Wales-based monitoring programme established in 2013 to evaluate the Glastir agri-environment scheme.
  - Aims to collect evidence on the effectiveness of management interventions related to climate change, biodiversity, soil and water quality, and woodland expansion.
  - Also collects evidence to quantify overall environmental status and trends, analyzing drivers such as land use, climate, and pollution in addition to Glastir interventions.

- Data governance and stewardship context
  - Aggregates data from multiple national agencies and research partners to support environmental monitoring and policy evaluation.
  - Emphasizes provenance, interoperability, and the need to quantify changes in the Welsh environment over time.
  - Outputs are intended to be discoverable and usable by others, with documented methodologies and data sources.

- The unified peat map: objectives and significance
  - Commissioned to support the monitoring programme by mapping peat extent and condition across Wales.
  - Represents an advancement over previous peat maps, revealing widespread peatland distribution, including extensive upland blanket bog and numerous small lowland peat units.
  - Provides a detailed view of deep peat presence (generally >0.5 m) and related biodiversity significance.

- Generation methods (dataset lineage)
  - Integrated four datasets to produce a unified peat map (peat >45 cm depth):
    - BGS superficial geology map (1:50,000) identifying peat areas.
    - Forestry Commission Wales soil survey records indicating peat thickness (>45 cm).
    - Deep peat boundaries from the Lowland Peatland Survey of Wales.
    - Habitat polygons indicating deep peat from the Habitat Survey of Wales (Phase I).
  - Data integration performed by sequential union operations in ArcMap GIS to create a final multipart polygon shapefile.

- Data quality, provenance, and limitations
  - Overall quality depends on the quality of the input source datasets from national agencies.
  - Source materials are based on direct ground surveys; some peat extent inferences (e.g., deep peat from mire vegetation) are more robust in lowlands than in uplands.
  - Documentation available for each source dataset; caveats noted regarding precision and boundary delineation.

- Data product and schema
  - GMEP_Unified_Peat_Map.shp (ESRI Shapefile, multipart polygon) describing peat soils in Wales.
  - Key attributes:
    - FID/Unit: unique polygon identifiers.
    - SHAPE_AREA, SHAPE_LEN: polygon area and length.
    - DESC_: description of the polygon (e.g., 'Peat').
  - Intended to support spatial analysis of peat extent, depth, and associated greenhouse gas emissions.

- Access, usage, and attribution
  - Any product derived from the data must acknowledge source materials with:
    - "© Hawlfraint y Goron: Llywodraeth Cymru" or "© Crown copyright: Welsh Government"
    - Contains Natural Resources Wales information © NRW
    - Data includes content from British Geological Survey with appropriate attribution.
  - Clear provenance and licensing statements accompany data usage.

- Practical implications for data stewards
  - Demonstrates a multi-source data fusion approach to produce policy-relevant environmental datasets.
  - Highlights the importance of documenting data sources, methods, and limitations to ensure reuse and comparability.
  - Underlines the need for ongoing updates and versioning as inputs from national agencies evolve and as monitoring requirements change.

- Related references and context
  - Background and methodological references span peat mapping, lowland peat surveys, habitat surveys, and foundational peat mapping work (e.g., Evans et al. 2015; Lawley 2009; Pyatt 1982; Jones et al. 2011; Blackstock et al. 2010; Kenned y 2002; ECOSSE 2007; various GMEP reports).
  - Documentation supports traceability of data lineage and analytical decisions within the Glastir Monitoring and Evaluation Programme.