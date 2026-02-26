# Family lineage and landscape quality data for wild bumblebee colonies across an agricultural landscape in Buckinghamshire, U.K.

- Purpose
  - A GIS-ready dataset linking bumblebee family lineages (queen and worker relationships) with landscape context to understand how habitat quality and land-use influence colony locations and foraging.
  - Enables analysis of spatial patterns across multiple scales in a real agricultural mosaic.

- Key data and components
  - Genetic and lineage data
    - Non-lethal DNA sampling from queens and workers of Bombus terrestris, B. lapidarius, and B. pascuorum.
    - Genotyped to assign full-sib groups and identify mother/sister queens (COLONY v2.0 used; low genotyping error rate 0–5% based on re-genotyping).
    - Colony locations inferred from distributions of full-sib sister workers; colonies represented by >1 worker were used.
  - Landscape and habitat data
    - Remote sensing: LiDAR (canopy height model) and hyperspectral imagery (EAGLE) from ARSF (2007), processed to 0.5 x 0.5 m grids.
    - Land-use/land-cover (LULC) map with nine classes derived from spectral and height data, supplemented by field surveys.
    - Field surveys (April–August 2011) for habitat value, flowering plant cover, and nesting habitat suitability.
  - Spatial scales and metrics
    - Data include habitat/flower cover proportions within four spatial scales around each colony: 250 m, 500 m, 1000 m, and a colony-foraging-distance-based scale.
    - Nesting habitat suitability for each species classified as high, medium, or low per land parcel.
  - Dataset and format
    - Data file: Carvell_etal_IPI_Bombus_family_lineage_and_landscape_quality_data.csv
    - CSV structure includes: SPECIES, Sp_Rel_Code, Q1, W1, Q2, Relationship, AveDIST, Colony.Specific.Foraging.Distance, and multiple habitat/flower cover proportion fields for the four spatial scales (e.g., Col.All_Summer_Flower_Cover_Prop, Col.Worker_Preferred_Summer_Flower_Cover_Prop, Col.Nesting_high, and 250./500./1000. scale equivalents).

- Data collection and processing workflow (GIS-focused)
  - Study area and sampling design
    - 1,950 ha landscape around Hillesden Estate, Buckinghamshire; 250 x 250 m grid cells with targeted sampling across habitat patches.
    - Queens sampled spring 2011 and spring 2012; workers sampled in summer 2011.
  - Remote sensing and LULC creation
    - 0.5 m resolution grids created from LiDAR and hyperspectral data; land-use classes refined by field checks.
    - Manual updates to LULC based on field surveys; spring habitat mapping via stratified sampling and adjustment from summer data.
  - Habitat and floral data
    - For each discrete habitat parcel, estimate percentage cover and percent in flower for 28 plant groups; extrapolate unsampled parcels using nearby LULC attributes.
  - Colony location estimation
    - Use mean-centre approach from queen/worker distributions to estimate colony locations.
    - Snapping colonies to the nearest suitable LULC class to avoid misclassification (e.g., roads, buildings, water).
    - Only colonies represented by two or more workers were used for nest location estimation.
  - Foraging distance metrics
    - Straight-line distance from each worker capture location to the estimated colony location; mean distance per sibship used as colony-specific foraging distance.

- Data quality and validation
  - DNA protocols and genotyping follow established standards; replication checks performed.
  - Data checks conducted by Centre for Ecology & Hydrology and Institute of Zoology; peer-reviewed analyses published ( Molecular Ecology 2014; Ecological Applications 2016).

- Analytical context and usage
  - Spatial data handling: ERDAS Imagine and ArcGIS used for remote sensing, LULC processing, and mapping; CSV for data export.
  - Data linking
    - Each family lineage is identified with a unique code; counts of Q1, W1, Q2, and habitat/land-use proportions linked to colony locations and dispersal metrics.
  - Potential GIS applications
    - Combine lineage data with landscape quality metrics to study how habitat composition at multiple scales influences colony establishment, queen dispersal, and worker foraging patterns.
    - Reuse of land-cover maps, floral availability measures, and nesting suitability layers in spatial analyses of pollinator habitat value.

- Access and references
  - Data file: Carvell_etal_IPI_Bombus_family_lineage_and_landscape_quality_data.csv
  - References for methods and data provenance:
    - Dreier et al. 2014a, 2014b
    - Redhead et al. 2014, 2016