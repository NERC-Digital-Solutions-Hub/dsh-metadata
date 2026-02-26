# Family lineage and landscape quality data for wild bumblebee colonies across an agricultural landscape in Buckinghamshire, U.K.

## Aim
- Document family lineage relationships (spring queens, daughter workers, sister queens) for three bumblebee species across the Hillesden Estate, Buckinghamshire, UK (2011–2012).
- Combine land-use/land-cover data, habitat surveys, molecular genetics, and spatial modelling to estimate colony locations and habitat context.
- Produce habitat- and landscape-scale metrics within four spatial scales around each colony for use by researchers and data users.

## Dataset scope and study design
- Study area: agricultural landscape (~1,950 ha) centered on Hillesden Estate, Buckinghamshire, UK; grid cells of 250 x 250 m.
- Species: Bombus terrestris, B. lapidarius, B. pascuorum.
- Sampling periods:
  - Queens: spring 2011 (Mar 21–Apr 18) and spring 2012 (Mar 19–May 2)
  - Workers: summer 2011 (Jun 20–Aug 5)
- Data sources:
  - DNA-based lineage assignment (non-lethal sampling)
  - Remote sensing (LiDAR and hyperspectral data) for land-use/land-cover
  - Ground-truth habitat surveys and flowering plant cover assessments
- Outcome: estimation of colony locations and foraging-distance metrics; landscape context at multiple spatial scales.

## Data collection and transformation methods
- Genetic sampling:
  - Non-lethal sampling from queens and workers using tarsi; DNA preserved in ethanol.
  - Microsatellite genotyping; COLONY v2.0 used to assign full-sib groups and identify mothers/sister queens.
  - Quality control: genotyping errors estimated (0–5%) from 10% re-genotyped subset; data checked by CEH and Institute of Zoology staff.
- Landscape and habitat data:
  - Remote sensing: ARSF data (Aug 2007) with LiDAR and hyperspectral imagery, processed to 0.5 x 0.5 m grids.
  - Land-cover classification: 30 initial classes via maximum likelihood, collapsed to nine classes; maps updated with field checks and owner information.
  - Spring habitat map: surveyed parcels in April 2011–2012; estimation of plant cover and flowering in unsampled parcels using scaling from summer data.
- Habitat suitability and nesting:
  - Parcels scored for nesting habitat suitability (high/medium/low) based on vegetation structure, litter, moss, and small mammal signs; species-specific nesting requirements inferred from literature/expert knowledge.
- Colony location estimation:
  - Colony positions inferred from distributions of full-sib sister workers using a mean-centre approach.
  - Locations snapped to nearest relevant LULC class to avoid unsuitable features.
  - Only colonies represented by two or more workers included.
- Foraging distance:
  - Distances from worker capture locations to estimated colony centers averaged per sibship.

## Data quality and validation
- Laboratory and field QA:
  - DNA handling and genotyping follow established protocols; results peer-reviewed and published.
  - Independent checks by CEH and Institute of Zoology staff.
- Documentation and reproducibility:
  - Analysis tools: COLONY for genetic data; ERDAS Imagine and ArcGIS for remote sensing and mapping.
  - Data processed in ArcGIS and Excel; submitted to the Environmental Information Data Centre (EIDC) as CSV.
- Provenance and references:
  - Related methods and data products documented in multiple peer-reviewed articles (Dreier et al. 2014a,b; Redhead et al. 2014, 2016).

## Data structure and key variables
- Data file: Carvell_etal_IPI_Bombus_family_lineage_and_landscape_quality_data.csv
- File type: comma-delimited (CSV); stored/distributed via EIDC.
- Core schema:
  - SPECIES: species code (Bter, Blap, Bpas)
  - Sp_Rel_Code: unique ID for species-family/colony
  - Q1: number of spring 2011 queens
  - W1: number of summer 2011 workers
  - Q2: number of spring 2012 queens
  - Relationship: family relationship category for each lineage
  - AveDIST: queen dispersal distance (mean across sampled queens)
  - Colony.Specific.Foraging.Distance: mean straight-line worker foraging distance
  - Foraging- and habitat-related proportions measured within four spatial scales around colony:
    - 250, 500, 1000 m (All_Summer_Flower_Cover_Prop, Worker_Preferred_Summer_Flower_Cover_Prop, All_Spring_Flower_Cover_Prop, Queen_Visited_Spring_Flower_Cover_Prop, Spring_Plus_Summer_Flower_Cover_Prop, Arable, Mixed.Vegetation, Nesting_high, etc.)
  - Layers are provided for each scale (e.g., 250.All_Summer_Flower_Cover_Prop, 500.All_Summer_Flower_Cover_Prop, 1000.All_Summer_Flower_Cover_Prop, and similarly for other metrics)
- Coverage:
  - Proportions reflect floral cover and habitat attributes within specified colony foraging distances (and within fixed radii: 250, 500, 1000 m)

## Analytical methods and software
- Genetic analyses:
  - COLONY v2.0 for sibship and maternal relationships; genotyping error estimates calculated from re-genotyped samples
- Remote sensing and GIS:
  - ERDAS Imagine for initial data processing; ArcGIS for map-making and habitat updates
- Data management:
  - Data organized in ArcGIS/Excel workflows; final export to CSV for EIDC submission

## Data access, file details, and reuse
- Access point: EIDC data submission (CSV format)
- File naming: Carvell_etal_IPI_Bombus_family_lineage_and_landscape_quality_data.csv
- Data scope and references:
  - Linked to publications detailing genetic structure, land-use maps, and landscape effects on foraging (Dreier et al. 2014a,b; Redhead et al. 2014, 2016)
- Licensing and reuse:
  - License not specified within the document; data are provided via EIDC with associated publications for methodological context

## Limitations and considerations for data stewardship
- Spatial coverage gaps:
  - About 6.5% of the study area was not surveyed due to access restrictions; floral data for these areas were imputed from similar LULC parcels
- Nesting and colony inference:
  - Colony locations are estimated only for lineages with multiple workers; single-worker lineages are excluded
- Temporal scope:
  - Data reflect a single-year sampling window (2011–2012) within a defined landscape; applicability to other years or landscapes should be considered carefully
- Habitat classification:
  - Spring habitat estimates are derived by scaling from summer data; potential uncertainties in seasonal plant-flower relationships
- Data provenance:
  - Multiple data sources (genetic, remote sensing, field surveys) require careful integration and metadata documentation to enable reproducibility

## Related resources and references
- Dreier, S. et al. (2014a). Fine-scale spatial genetic structure of common and declining bumble bees across an agricultural landscape. Molecular Ecology.
- Dreier, S. et al. (2014b). Microsatellite genotype data for five species of bumblebee across an agricultural landscape in Buckinghamshire, UK. NERC-Environmental Information Data Centre.
- Redhead, J. W. et al. (2014). Map of land-use/land-cover and floral cover across an arable landscape in Buckinghamshire, UK. NERC Environmental Information Data Centre.
- Redhead, J. W. et al. (2016). Effects of habitat composition and landscape structure on worker foraging distances of five bumble bee species. Ecological Applications.