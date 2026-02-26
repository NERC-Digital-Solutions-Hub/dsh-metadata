# Family lineage and landscape quality data for wild bumblebee colonies across an agricultural landscape in Buckinghamshire, U.K.

- Overview
  - Purpose: Document family lineage relationships among spring queens, daughter workers, and sister queens across three bumblebee species, and relate these lineages to landscape quality around colonies for monitoring environmental health and policy performance.
  - Location and time: Hillesden Estate, Buckinghamshire, UK; sampling conducted spring 2011 to spring 2012.
  - Study landscape: 1,950 ha agricultural area with agri-environment schemes and pollinator-targeted habitat features; landscape divided into 250 × 250 m grid cells.
  - Species: Bombus terrestris, B. lapidarius, B. pascuorum.
  - Funding and leadership: Centre for Ecology & Hydrology; Insect Pollinators Initiative.

- Data and outputs
  - Biological data: Family lineage counts (founding queens Q1, workers W1, second-generation queens Q2) and sibship-derived colony locations for colonies represented by two or more workers.
  - Landscape data: Proportions of habitat quality and land-use variables within four spatial scales from each colony (including 250 m, 500 m, 1000 m radii and a colony-specific foraging distance).
  - Habitat and floral metrics: Floral cover by plant groups, nest habitat suitability, arable land, mixed vegetation, roads/buildings, water, bare soil, and land-use categories.
  - Data file: Carvell_etal_IPI_Bombus_family_lineage_and_landscape_quality_data.csv (submitted to EIDC) with a unique lineage code and a comprehensive set of habitat/foraging distance metrics.

- Methods and data collection
  - Biological sampling and genetics
    - Non-lethal DNA sampling from queen and worker bumblebees (tarsus) with microsatellite markers.
    - Genotyping used COLONY v2.0 to assign workers to full-sib groups and identify mother/sister queens.
    - Genotyping error rate estimated at 0–5% through re-genotyping; quality checks by CEH and Institute of Zoology staff.
    - Analyses of worker-only and landscape data peer-reviewed and published (Molecular Ecology, 2014; Ecological Applications, 2016).
  - Landscape and habitat data
    - Remote sensing: LiDAR (1 pulse per m²; canopy height model) and hyperspectral data (252 bands) processed to 0.5 × 0.5 m grids.
    - Land-use/land-cover (LULC): 9 classes derived from remote sensing plus manual updates from field surveys.
    - Field surveys: 2011 (July–August) and spring 2011–2012 for habitat value, flowering abundance, and plant cover; parcel-level surveys to refine nesting and floral data; adjustments for unsampled parcels using surrounding means.
    - Nesting habitat assessment: Parcel-level suitability categorized as high, medium, or low based on vegetation structure, litter, moss, and small mammal evidence.
  - Colony location estimation
    - GPS mapping of sampled queens/workers; colony locations inferred from distributions of full-sib sister workers using a mean-centre approach.
    - Colony centres snapped to the nearest suitable LULC class to avoid crops, roads, buildings, and water.
    - Colony locations estimated only for lineages represented by two or more workers; straight-line distances from worker captures to colony locations computed as colony-specific foraging distance.

- Data types, units, and structure
  - Output data per lineage/colony: counts of Q1, W1, Q2; proportions of habitat/flower cover within four extents from the colony (250 m, 500 m, 1000 m, and colony-specific foraging distance).
  - Example variables (selected): AveDIST (queen dispersal distance), Colony.Specific.Foraging.Distance, All_Summer_Flower_Cover_Prop, Worker_Preferred_Summer_Flower_Cover_Prop, All_Spring_Flower_Cover_Prop, Queen_Visited_Spring_Flower_Cover_Prop, Arable, Mixed.Vegetation, Nesting_high, across 250 m, 500 m, 1000 m radii and colony distance.
  - Data format: CSV with fields including SPECIES, Sp_Rel_Code, Q1, W1, Q2, Relationship, distances, and numerous habitat/flower-cover proportions at multiple scales.

- Analytical methods and data handling
  - Genetic analysis: DNA extraction and microsatellite genotyping procedures detailed in associated publications; error-checking and quality assurance performed by CEH and collaborating institutes.
  - Spatial analysis: GIS work in ArcGIS; remote sensing processing in ERDAS Imagine; land-cover updates and nectar/floral proxies created from field data.
  - Data processing and delivery: ArcGIS and Excel for data structuring; CSV file prepared for EIDC submission.

- Provenance, quality, and validation
  - Quality assurances: Genotyping protocols standardized; re-genotyping for error assessment; cross-site staff validation; peer-reviewed outputs verifying methods and findings.
  - Validation references: Dreier et al. (2014a, 2014b); Redhead et al. (2014, 2016); field and analytical methods published in Molecular Ecology and Ecological Applications.

- Reuse, accessibility, and references
  - Data accessibility: Data compiled for monitoring and research use; stored and accessible via the Environmental Information Data Centre (EIDC) as a CSV dataset.
  - Key references: Dreier et al. (2014a,b); Redhead et al. (2014, 2016) detailing methods and landscape associations; associated datasets and publications provide methodological context.

- Relevance to environmental monitoring
  - Demonstrates how combining lineage-level genetic data with high-resolution landscape metrics yields multi-scale insights into bumblebee colony location, foraging distance, and habitat associations.
  - Supports assessment of habitat quality, nesting opportunities, and floral resource dynamics in agricultural landscapes for pollinator monitoring and policy evaluation.