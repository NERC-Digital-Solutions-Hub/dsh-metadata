# The Glastir Monitoring and Evaluation Programme (GMEP)

- Purpose and scope
  - Wales-wide monitoring programme (established 2013) to assess the effects of the Glastir agri-environment scheme on climate change, biodiversity, soil and water quality, and woodland expansion.
  - Aims to quantify status and trends in the environment and identify how drivers of change (land use, climate, pollution) interact with Glastir interventions.
  - Produces evidence to evaluate the effectiveness of bundles of management interventions.

- The unified peat map: purpose and context
  - Commissioned to update the extent and condition of Welsh peatlands; described in Evans et al. (2015).
  - Represents an advancement over previous peat maps, revealing a widespread and detailed distribution of peat across Wales, including large upland peat areas and numerous small lowland peat units.
  - Highlights both upland peat (e.g., Migneint, Berwyn, Cambrian Mountains) and lowland peat with significant biodiversity interest.

- Generation methods (how the unified peat map was created)
  - Data sources combined (via UNION in ArcMap) to map peat >45 cm thick:
    1) Areas mapped as peat in the British Geological Survey (BGS) superficial geology map (1:50,000).
    2) Forests and Lands soil mapping from Forestry Commission Wales records (soil codes 8a–14w indicating peat >45 cm).
    3) Deep peat boundary (>0.5 m) from the Lowland Peatland Survey of Wales (CCW/NRW).
    4) Habitat polygons indicative of deep peat (E class, excluding E2) from Habitat Survey of Wales Phase I.
  - Output is GMEP_Unified_Peat_Map.shp (multipart polygon) with polygon-level attributes.

- Quality Control and limitations
  - Quality depends on input data quality from national agencies; the derived peat map inherits their limitations.
  - Ground-survey based delineations support reliability, but upland boundaries may be less precise due to mosaics of mire and non-mire vegetation.
  - Source documents provide details on data provenance and reliability for each input dataset.

- Output data product and structure
  - File: GMEP_Unified_Peat_Map.shp (ESRI Shapefile, multipart polygon).
  - Attributes include:
    - FID: Unique polygon identifier (Objectid).
    - SHAPE_AREA: Area in square metres.
    - SHAPE_LEN: Perimeter/length in metres.
    - DESC_: Description of polygons (e.g., 'Peat').
  -Designed to show the outline location of peat soils across Wales and support subsequent analyses of peat extent and condition.

- Usage, attribution, and licensing
  - Any product derived from or incorporating the data must acknowledge the sources with statements such as:
    - "© Hawlfraint y Goron: Llywodraeth Cymru" or "© Crown copyright: Welsh Government"; Contains Natural Resources Wales information © NRW.
    - "Derived in part from British Geological Survey geology data 1:50,000 scale. BGS © UKRI."
  - Data uses are tied to the Glastir Monitoring & Evaluation Programme and related Welsh Government agreements.

- References and context
  - Evans et al. (2015): Glastir Monitoring & Evaluation Programme. Mapping the extent and condition of Welsh peat.
  - Related Welsh Government and CEH/NCER publications detailing the data sources, surveys, and methodologies referenced for peat mapping and GMEP reporting.