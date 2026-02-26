# Family lineage and landscape quality data for wild bumblebee colonies across an agricultural landscape in Buckinghamshire, U.K.

## Purpose and scope
- Describes a dataset linking bumblebee family lineages (spring queens, daughter workers, sister queens) of three species (Bombus terrestris, B. lapidarius, B. pascuorum) with landscape quality metrics across an agricultural landscape in Buckinghamshire, UK.
- Integrates genetic data, land-use/land-cover (LULC), and habitat/flowering data to estimate colony locations and examine habitat associations at multiple spatial scales.
- Collected during 2011–2012 within the Hillesden Estate area (1,950 ha) as part of the Insect Pollinators Initiative led by the Centre for Ecology & Hydrology.

## Data composition
- Genetic data: non-lethal DNA sampling of queens and workers; microsatellite genotyping to identify full-sib groups and maternal/sister queens; COLONY v2.0 used for sibship assignment with 0–5% genotyping error rate (validated by re-genotyping 10% of samples).
- Landscape and habitat data: remote-sensing–derived LULC with 9 classes (arable, short grass, semi-natural vegetation, environmental field margins, woody vegetation, garden/urban vegetation, roads/buildings, water, bare soil); canopy height from LiDAR; field- and ground-survey–based floral cover for 28 plant groups across spring and summer.
- Foraging and nesting variables: colony-specific foraging distance; nesting habitat suitability (high/medium/low) for each species based on habitat features.
- Data output: a single CSV file (Carvell_etal_IPI_Bombus_family_lineage_and_landscape_quality_data.csv) with a unique family/colony identifier, Q1/W1/Q2 counts, and a set of proportional habitat/flower cover metrics across multiple spatial scales.

## Data generation and quality assurance
- Experimental design: 1,950 ha study area grid (250 x 250 m); sampling within habitat patches proportional to habitat availability; queen sampling March–April (2011, 2012); worker sampling June–August (2011).
- Landscape data processing: LiDAR-based canopy height; hyperspectral imagery; land-cover classification into nine classes; manual field updates in ArcGIS to refine parcel boundaries and habitat values.
- Flower/vegetation data: field surveys in July–August 2011; spring survey subset in April 2011–2012 to estimate flowering cover; missing parcels imputed from neighboring LULC classes.
- Data quality documentation: analyses peer-reviewed and published (Dreier et al. 2014a,b; Redhead et al. 2016); data checked by CEH and Institute of Zoology; extensive methodological references provided.

## Spatial and landscape data
- Remote sensing: ARSF data (LiDAR and hyperspectral) from August 2007; 0.5 x 0.5 m grid resolution; LiDAR-derived canopy height model integrated with land-cover classes.
- Habitat mapping: annual to perennial flower mixtures and field margins; field verges and non-woody linear habitats included in vegetation categories.
- Habitat and floral metrics: calculated as proportional cover within colony-specific radii (250, 500, 1000 m) and within all-summer and spring periods; multiple derived indicators (e.g., All_Summer_Flower_Cover_Prop, Col.Worker_Preferred_Summer_Flower_Cover_Prop, Col.Nesting_high).

## Data structure and access
- Data format: comma-delimited CSV submitted to the Environmental Information Data Centre (EIDC).
- Key columns (highlights):
  - SPECIES: Bter, Blap, Bpas
  - Sp_Rel_Code: unique code per species-family/colony
  - Q1, W1, Q2: counts of queens/workers in respective cohorts
  - Relationship: family relationship category
  - AveDIST: queen dispersal distance (averaged across a sibship)
  - Colony.Specific.Foraging.Distance: mean straight-line worker foraging distance
  - Multiple columns for floral cover and nesting indicators across scales (e.g., 250.All_Summer_Flower_Cover_Prop, 500.Nesting_high, 1000.Queen_Visited_Spring_Flower_Cover_Prop, etc.)
- Data handling tools: ArcGIS, ERDAS Imagine for remote-sensing data; Excel for processing; final CSV structured for broad reuse.
- Availability and citation: linked references provided; dataset designed for reuse in ecological, landscape-genetics, and pollinator-habitat research.

## Provenance, publications, and references
- Primary data collection and analysis underpinning two main peer-reviewed works:
  - Dreier et al. (2014a, Molecular Ecology) on fine-scale spatial genetic structure
  - Dreier et al. (2014b, NERC-EDI) on microsatellite genotype data
  - Redhead et al. (2016, Ecological Applications) on habitat and landscape effects on worker foraging distances
- Additional methodological and dataset context:
  - Redhead et al. (2014) map of LULC and floral cover for Buckinghamshire
- Data hosted with EIDC; associated DOIs and data references provided in the metadata.

## Practical implications for Data Leaders
- Demonstrates successful integration of genetic, ecological, and high-resolution landscape data across multiple spatial scales to model colony locations and foraging dynamics.
- Supports co-ownership and cross-team collaboration by aligning genetic data with environmental context, enabling broader reuse for policy, pollinator conservation, and landscape planning.
- Highlights data governance considerations: explicit data standards, rich metadata, versioning through field updates, validation of remote-sensing products, and transparent quality assurance across institutions.
- Provides a scalable example of multi-layer data architecture (genetic data, LULC, floral/phenology data, nesting suitability) with clear provenance, documentation, and published validation.