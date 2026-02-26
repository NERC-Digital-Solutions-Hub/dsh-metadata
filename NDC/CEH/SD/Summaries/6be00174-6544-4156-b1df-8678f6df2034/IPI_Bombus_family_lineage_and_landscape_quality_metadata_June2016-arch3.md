# Dataset Title: Family lineage and landscape quality data for wild bumblebee colonies across an agricultural landscape in Buckinghamshire, U.K.

## Overview
- A dataset linking bumblebee family lineages (spring queens, daughter workers, sister queens) across three species (Bombus terrestris, B. lapidarius, B. pascuorum) with landscape quality metrics within an agricultural landscape in Buckinghamshire, UK.
- Aims to estimate colony locations, quantify habitat quality and land-use around colonies at four spatial scales, and relate lineage structure to landscape context.
- Created under the Insect Pollinators Initiative with data quality controls and public data sharing considerations.

## Study design and sampling
- Location and scale: 1,950 ha landscape around the Hillesden Estate, Buckinghamshire; divided into 250 x 250 m grid cells.
- Sampling periods: queens (spring 2011; 19 March–18 April 2011 and 19 March–2 May 2012), workers (summer 2011: 20 June–5 August 2011).
- Habitat interventions: agri-environment schemes with grass and wildflower margins in place since 2005.
- Habitat assessment: field surveys (April–August 2011) to classify nesting suitability (high/medium/low) for each species.
- Colony inference: locate colonies from distributions of full-sib sister workers; mean-centre approach snapped to nearest suitable land-use/land-cover (LULC) class; only colonies represented by >1 worker were estimated.

## Data types and structure
- Genetic data: non-lethal DNA sampling (tarsi of queens/workers), microsatellite genotyping; COLONY v2.0 used to assign full-sib groups and identify mother/sister queens.
- Landscape data: remote sensing (LiDAR and hyperspectral EAGLE data, 0.5 x 0.5 m resolution) plus field-verified LULC updates; nine primary land-use classes derived.
- Floral/foraging data: percentage cover and flowering proportion for 28 plant groups; seasonal (spring and summer) vegetation data; remaining unsurveyed areas imputed from surrounding LULC class means.
- Data outputs per colony/family: counts of Q1, W1, Q2; four scales of habitat/flower-cover proportions; nest suitability metrics; dispersal/foraging distance measures.

## Variables and scales
- Species and lineage identifiers (SPECIES, Sp_Rel_Code, Relationship).
- Counts: Q1 (spring 2011 queens), W1 (2011 workers), Q2 (spring 2012 queens).
- Spatial scales for habitat/flower-cover proportions: 250 m, 500 m, 1000 m, and a 1000 m extended set with combined metrics.
- Habitat-related proportions include: All_Summer/All_Spring flower cover, Worker_Preferred Summer flower cover, Queen_Visited Spring flower cover, Spring_Plus_Summer flower cover, Arable, Mixed.Vegetation, Nesting_high, etc.
- Foraging and nest context: AveDIST (queen dispersal distance), Colony.Specific.Foraging.Distance (mean distance from worker captures to colony).

## Analytical methods and quality assurance
- Genetic analysis: standard microsatellite genotyping; COLONY v2.0 for sibship and maternal lineage assignments; genotyping error rate 0–5% validated by re-genotyping a subset.
- Data quality: multiple verification steps by CEH and Institute of Zoology; peer-reviewed outputs published (Molecular Ecology; Ecological Applications).
- Landscape processing: ERDAS Imagine and ESRI ArcGIS used for processing and updates; field surveys for habitat validation; gap-filling in unsurveyed areas using mean values from similar LULC parcels.
- Data integration: integration of genetic data with landscape and floral data into a single CSV (EIDC) with a unique lineage identifier.

## Data structure and accessibility
- Data file: Carvell_etal_IPI_Bombus_family_lineage_and_landscape_quality_data.csv (EIDC submission).
- Columns include: SPECIES, Sp_Rel_Code, Q1, W1, Q2, Relationship, AveDIST, Colony.Specific.Foraging.Distance, and multiple habitat/flower-cover proportion variables at 250, 500, 1000 m scales.
- Access and governance: data prepared for submission to the Environmental Information Data Centre (EIDC); metadata and sharing considerations noted (public sharing of underlying data can be a barrier in some contexts).

## References and provenance
- Primary data and methods foundational papers and data centre records:
  - Dreier et al. (2014a, 2014b) on fine-scale spatial genetic structure and microsatellite data.
  - Redhead et al. (2014, 2016) on land-use/land-cover maps and habitat effects on foraging.
  - Data handling and analysis tools cited (COLONY, ERDAS Imagine, ArcGIS).