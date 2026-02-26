# DATA HEADER INFORMATION for Forest_inventory.csv

- Overview
  - This data describes characteristics of trees located on the Zone of Interest.

- Context and provenance
  - Programme: ESPA; Project: P4GES.
  - DOI: https://doi.org/10.5285/cbeea40f-8e35-4875-8b49-815e04f0cbd9
  - Acknowledgement required: Laboratoire des Radio Isotopes, Université d’Antananarivo for products derived from these data.
  - Reference to additional documentation: Please also see Manual 1_Classical_Survey.

- Dataset scope and design notes
  - Site_ID serves as the P4GES site code.
  - Sampling information is structured around subplots and a defined sampling area.

- Key fields and data types
  - Site_ID
    - Information: P4GES site code
    - Variable type: Text String
    - Unit: (not specified)
  - trees_subplot
    - Information: Subplot where the sample was collected, classified by radius
    - Variable type: Categorical
    - Unit: (not specified)
    - Categories: S (Small), M (Medium), L (Large)
    - Radius interpretation: 5 m < Small < 10 m; 10 m < Medium < 20 m; 20 m < Large
  - trees_area
    - Information: Surface of the sampling area (circular plot)
    - Variable type: Numeric
    - Unit: square meters (m²)
  - trees_local_name
    - Information: Vernacular/local name of the inventoried species
    - Variable type: Text String
    - Unit: (not specified)
  - trees_scientific_names
    - Information: Scientific name of the inventoried species
    - Variable type: Text String
    - Unit: (not specified)
  - trees_genera
    - Information: Genera of the selected tree
    - Variable type: Text String
    - Unit: (not specified)
  - trees_family
    - Information: Family of the selected tree
    - Variable type: Text String
    - Unit: (not specified)
  - trees_DBH
    - Information: Breast height diameter of the tree (diameter at 1.3 m from ground level)
    - Variable type: Numeric
    - Unit: Centimeter
  - trees_height
    - Information: Total height of the tree (from ground to top)
    - Variable type: Numeric
    - Unit: Meter

- Data handling and metadata notes
  - The data header includes field_materials_resources descriptors for several fields (note: implementation-specific metadata about data provenance and resources).
  - Users should reference the DOI and ESPA/P4GES project context for proper attribution and documentation.