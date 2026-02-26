# Tree canopy data derived from LiDAR data for South West England 2013

- Data access and licensing
  - Available via DOI: 10.5283/78dba959-989b-43d4-b4da-efd2506e0c8e
  - License: Open Government Licence (OGPL). By downloading/using the data, you agree to the OGPL terms.
  - Acknowledgement: Must cite Scholefield, P; Trembath, P. (2022). Tree canopy data derived from LiDAR data for South West England 2013. NERC EIDC.

- Collection and generation of the dataset
  - Source: British Antarctic Survey (BAS) collected a high-resolution LiDAR survey (~1 point per m, ~25 cm vertical accuracy) over Cornwall and Devon in July–August 2013 for the Tellus South West project.
  - Processing: Raw LiDAR converted to Digital Terrain Model (DTM) and Digital Surface Model (DSM) by the Environment Agency under contract.
  - Coverage and resolution: 9,424 km² area west of Exmouth (approximately west of 3°21′W); 1 m grid cell resolution; height accuracy ~25 cm.
  - Data formats: DTMs and DSMs provided as individual files per Ordnance Survey tile (e.g., SX37ne, SX37nw, SX37se, SX37sw); coordinate system OSGB 1936 / British National Grid (EPSG:27700).
  - Outputs: DTM (bare-earth height) and DSM (height including features like buildings/vegetation).

- How canopy outlines are generated
  - Tooling: Forest Tools R package; requires DSM and DTM as inputs.
  - Detection: Dominant treetops identified with a variable window filter (dynamic window size based on local canopy height) and a minimum height threshold (minHeight = 1 m).
  - Canopy segmentation: Uses a watershed-based approach (mcws function) to outline discrete crown shapes; to reduce oversegmentation, employs marker-controlled segmentation using treetops as markers.
  - Outputs: Tree crown polygon layer and tree top point layer; saved as 25 km² geopackages.
  - Filtering: Rural feature layer created by combining UK-wide datasets (Forest Research National Forest Inventory, OS Greenspace and Urban Areas, Landcover Map 2007 Littoral) to filter out urban/offshore features (nonhedgerow layer).

- Spatial reference and coverage
  - Coordinate system: OSGB 1936 / British National Grid (EPSG:27700).
  - Geographic extent: West of Exmouth (roughly west of 3°21′W) in South West England.

- Data content and structure
  - Outputs:
    - Tree crown polygon layer
    - Tree top point layer
  - Data fields (example structure):
    - treeID: Unique identifier at 1 km scale (not unique when using 25 sq km tiles)
    - Height: Crown height in metres
    - crownAr: Crown area in square metres (integer by LiDAR resolution)
    - crwnDmt: Mean diameter from the tree top (metres)
    - habitat: Categorical descriptor (e.g., buildings/coastal, forest/woodland/urban greenspace, rural/agricultural)
    - Geometry: Point (treetop) or polygon (crown)
  - Units: All heights/distances in metres; areas in square metres.

- Data quality and controls
  - LiDAR data characteristics: 2 cm height layers for terrain and surface; 1 m grid; average height accuracy about 25 cm.
  - Output handling: Data provided as-is post-delineation; rural feature dataset used for filtering while retaining buildings and forests for contextual analysis.
  - Quality considerations: Potential oversegmentation in crown outlines; parameter tuning performed in test areas to balance full crown models versus sub-crowns or branches.

- Usage and reuse considerations for data support
  - Primary use: Facilitates exploration of tree canopy structure and related spatial analyses; supports dashboard creation, self-service data exploration, and informing policy or planning with canopy information.
  - Integration potential: Combine with other datasets (e.g., hedgerows, urban greenspace) to study canopy coverage, urban-rural interfaces, and habitat mapping.
  - Documentation and provenance: Clear methodological references and linked datasets allow reproducibility and understanding of crown delineation steps (dynamic window filter, watershed segmentation, marker-controlled segmentation).

- References for methods
  - Beucher & Meyer (1993) on marker-controlled segmentation and watershed transformations.
  - Popescu & Wynne (2004) on detecting treetops and canopy width using a dynamic window/photogrammetric approach.
  - Ferraccioli et al. (2014) on LiDAR-based DSM/DTM data for South West England.