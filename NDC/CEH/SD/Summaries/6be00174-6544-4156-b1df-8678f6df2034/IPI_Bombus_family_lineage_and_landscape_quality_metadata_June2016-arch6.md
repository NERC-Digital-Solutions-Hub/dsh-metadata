# Family lineage and landscape quality data for wild bumblebee colonies across an agricultural landscape in Buckinghamshire, U.K.

## Overview
- Dataset describing family lineage relationships among spring queens, daughter workers, and sister queens for three bumblebee species (Bombus terrestris, B. lapidarius, B. pascuorum) in Buckinghamshire, UK (Hillesden Estate).
- Combines genetic data, field-based habitat surveys, and high-resolution remote sensing to estimate colony locations and quantify landscape quality around colonies.
- Collected across 2011–2012, with landscape context derived from LiDAR and hyperspectral data and ground-truth habitat surveys.

## Data collected and scope
- Biological data:
  - Queen and worker samples for three species; lineage information (full-sib groups) established using COLONY v2.0.
  - Counts: Q1 (spring 2011 queens), W1 (2011 workers), Q2 (spring 2012 queens); relationships within family lineages.
  - Dispersal and foraging metrics (AveDIST, Colony.Specific.Foraging.Distance).
- Landscape data:
  - Land-use/land-cover (LULC) map with nine classes (e.g., arable, short grass, mixed vegetation, field margins, woody vegetation, urban vegetation, roads/buildings, water, bare soil).
  - Floral cover estimates for 28 plant groups across spring and summer, plus derived measures like "all flowers" and "worker preferred" groups within defined radii.
  - Nesting habitat suitability (high/medium/low) per parcel for each species.
- Spatial scale context:
  - Four nested spatial scales from colony location: 250 m, 500 m, 1000 m, with corresponding floral and nesting metrics.
- Location and mapping:
  - GPS-based colony locations; colonies inferred from distributions of full-sib sister workers; coordinates snapped to nearby habitat features to avoid non-habitat areas.

## Data processing and quality
- Non-lethal DNA sampling from queens and workers; microsatellite genotyping with standard protocols.
- Genotyping validated with 0–5% error rate based on repeat genotyping.
- QA performed by Centre for Ecology & Hydrology (CEH) and Institute of Zoology; analyses published in peer-reviewed journals (Molecular Ecology, Ecological Applications).
- Geospatial processing performed in ERDAS Imagine and ArcGIS; data structured and stored as CSV with unique lineage identifiers.

## Experimental design
- Landscape: 1,950 ha study area within Hillesden Estate, divided into 250 x 250 m grid cells.
- Sampling intensity proportional to habitat patch availability to capture colonies in potential nesting and foraging habitats.
- Temporal windows:
  - Queens: spring 2011 (Mar–Apr) and spring 2012 (Mar–May).
  - Workers: summer 2011 (Jun–Aug).
- Remote sensing: LiDAR and hyperspectral data (2007) at ~0.5 x 0.5 m resolution; used to derive detailed LULC with height-based discrimination of spectrally similar classes.

## Data structure and key variables
- Data file: Carvell_etal_IPI_Bombus_family_lineage_and_landscape_quality_data.csv
- Core columns:
  - SPECIES: Bter, Blap, Bpas
  - Sp_Rel_Code: unique code linking lineage/colony
  - Q1, W1, Q2: counts of queens/workers sampled
  - Relationship: family relationship category
  - AveDIST: dispersal distance for queens (2012) within lineage
  - Colony.Specific.Foraging.Distance: mean distance from worker captures to colony location
  - Col.All_Summer_Flower_Cover_Prop, Col.Worker_Preferred_Summer_Flower_Cover_Prop, Col.All_Spring_Flower_Cover_Prop, Col.Queen_Visited_Spring_Flower_Cover_Prop, Col.Spring_Plus_Summer_Flower_Cover_Prop: proportional floral cover metrics within colony foraging distance
  - Col.Arable, Col.Mixed.Vegetation, Col.Nesting_high: habitat composition indicators within foraging distance
  - 250.*, 500.*, 1000.*: analogous floral cover and habitat metrics within 250 m, 500 m, and 1000 m radii
- Multi-scale structure enables analysis of habitat and floral resources around colonies at nested radii.

## Spatial scales and metrics
- Four radii used for landscape and floral metrics: 250 m, 500 m, 1000 m, plus all flowers within the colony's foraging distance.
- For each scale, metrics cover:
  - Floral cover (all/worker-preferred/queen-visited)
  - Arable area
  - Mixed vegetation
  - Nesting habitat suitability (high/low/medium)
- Colony-level foraging distance (distance between captured workers and estimated natal colony) used to anchor landscape metrics to each colony.

## Potential data products and use cases (Data Support perspective)
- Interactive dashboards or self-serve analyses linking colony genetics to landscape quality and floral resource availability.
- Habitat association analyses:
  - How nesting habitat quality and floral abundance across scales relate to colony genetics and foraging behavior.
- Landscape-quality indices:
  - Composite metrics at 250, 500, and 1000 m that summarize nesting suitability and floral resources for pollinator support.
- Foraging ecology insights:
  - Relationships between colony foraging distance and habitat composition, including effects of arable vs. semi-natural vegetation and field margins.
- Policy and conservation support:
  - Evidence on the effectiveness of agri-environment schemes (e.g., field margins) in supporting wild bumblebee colonies.
- Data integration opportunities:
  - Combine with other pollinator datasets, DNA-based lineage information, or additional habitat/remotely-sensed layers to extend cross-study analyses.

## Data access and format considerations
- Primary data delivered as a single CSV with a unique Sp_Rel_Code linkage across lineage and colony records.
- Rich metadata within the dataset description and linked references; suitable for import into GIS, statistical software, or dashboards.
- Provenance and quality controls documented (non-lethal sampling, genotyping protocol, QA steps, peer-reviewed outputs).

## Limitations and considerations for use
- Patchy data coverage exists for portions of the landscape; for missing areas, floral data were imputed from surrounding LULC parcels.
- Colony location estimates rely on mean-centre approaches based on sibships; single-worker lineages do not provide meaningful nest locations.
- Temporal scope is restricted to 2011–2012; considerations needed when comparing to year-to-year variation or longer-term trends.
- Data complexity requires careful alignment of scale-specific metrics when integrating with other datasets.

## References
- Dreier, S., et al. (2014a). Fine-scale spatial genetic structure of common and declining bumble bees across an agricultural landscape. Molecular Ecology.
- Dreier, S., et al. (2014b). Microsatellite genotype data for five species of bumblebee across an agricultural landscape in Buckinghamshire, UK. NERC Environmental Information Data Centre.
- Redhead, J. W., et al. (2014). Map of land-use/land-cover and floral cover across an arable landscape in Buckinghamshire, UK. NERC Environmental Information Data Centre.
- Redhead, J. W., et al. (2016). Effects of habitat composition and landscape structure on worker foraging distances of five bumble bee species. Ecological Applications.