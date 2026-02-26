# Vegetation plot data from a survey of Moor House National Nature Reserve, 2008-09

- Scope and purpose
  - Re-survey of part of Moor House National Nature Reserve (Troutbeck catchment) to update vegetation data after a 50-year gap.
  - Focus on Calluna vulgaris and Eriophorum vaginatum-dominated areas within a grid-based sample.

- Data collection and design
  - Time period: June–August 2008 and July–August 2009 (with some plots surveyed in 2012).
  - Sampling design: grid-based, plots spaced at 200 m (some 100 m) intervals; GPS-located.
  - Plot size: 2 x 2 meters.
  - What was recorded per plot:
    - General/header information: plot number/name, location type, slope, aspect, altitude, vegetation height, peat depth.
    - Vegetation data: presence/absence of species and percentage cover (to the nearest 5%).
  - Data collection process: field staff coordinated by the Centre for Ecology and Hydrology, Lancaster; full training provided; accuracy checks performed on species lists.
  - Data capture: vegetation cover recorded for each species; data entered via an electronic tablet with software adapted from Countryside Survey 2007.

- Data structure and contents
  - Data stored in two CSV files:
    - MH08_VEGETATION_PLOTS.csv
      - Plot header data: REP_ID, SLOPE, ASPECT, VEG_HT_AVE, PEAT_DEPTH, ALT, LOCATION, X_COORD, Y_COORD, YEAR.
      - Year of survey.
    - Vegetation species information
      - REP_ID, BRC_NUMBER, BRC_NAMES, COMMON_NAME, TOTAL_COVER.
  - Spatial reference: OSGB36 easting/northing coordinates.
  - Taxonomic standardization: species names aligned with Stace (1997); BRC codes used for species identification.
  - Documentation: survey field handbook; data interpretation aligned with Centre for Ecology and Hydrology practices.

- Provenance and lifecycle
  - Originators/Surveyors: Rose, W.C. et al.; University of Cumbria; survey coordinated by CEH, Lancaster.
  - Key context: Moor House is England’s highest and largest terrestrial NNR; study area focused on the Troutbeck catchment within blanket bog habitats.
  - Related publications and references:
    - Eddy, Welch & Rawes (1969) for prior vegetation work at Moor House.
    - Maskell et al. (2008) Vegetation Plots Handbook (CS Technical Report No. 2/07).
    - Stace (1997) New Flora of the British Isles.
  - Data lifecycle notes: some additional plots surveyed in 2012; grid-based method chosen due to inability to locate exact 1960s plot positions.

- Data quality, standards, and governance
  - Standards and metadata: explicit plot-level and species-level metadata; clear field definitions for slope, aspect, altitude, peat depth, vegetation height, and cover.
  - Quality assurance: full training provided; species lists checked for accuracy; data structured for interoperability (CSV with defined headers and codes).
  - Governance considerations: dataset described with originator details and publications; designed to be shared via relevant portals and catalogues, with documentation permitting reuse by others.

- Access, reuse, and potential use
  - Data format and access: CSV files with explicit field definitions, suitable for ingestion into data portals and catalogues.
  - Reuse potential: enables temporal vegetation trend analyses, bog/peatland vegetation studies, and habitat assessments within Moor House NNR; supports metadata-driven data discovery and interoperability.
  - Documentation references available to support understanding of methods, taxonomy, and data interpretation.