# Family lineage and landscape quality data for wild bumblebee colonies across an agricultural landscape in Buckinghamshire, U.K.

## Overview
- Integrates family lineage data, habitat surveys, molecular genetics, and spatial modelling to estimate colony locations and habitat quality around wild bumblebee colonies.
- Focuses on three species (Bombus terrestris, B. lapidarius, B. pascuorum) across an agricultural landscape in Buckinghamshire, UK, collected between spring 2011 and spring 2012.
- Aims to relate colony lineage information to landscape-scale habitat quality and floral resources at multiple spatial scales.

## Study Area and Sampling
- Area: 1,950 ha landscape centered on the Hillesden Estate, Buckinghamshire, Southern England, UK.
- Grid: 250 x 250 m cells; standardized pollinator-targeted agri-environment options implemented since 2005.
- Sampling windows:
  - Queens: 21 March–18 April 2011 and 19 March–2 May 2012.
  - Workers: 20 June–5 August 2011 (continuous 4–5 days per week).
- Non-lethal DNA sampling of queens and workers (terminal tarsus) with ethanol preservation for microsatellite analysis.

## Data Collected
- Genetic data: microsatellite genotypes used to assign workers to full-sib groups and identify mothers/sister queens (COLONY v2.0), with genotyping error rate 0–5%.
- Colony data: counts of founding queens (Q1), workers (W1), and second-generation spring queens (Q2).
- Habitat and land-use data: landscape quality measures and land-use/land-cover (LULC) classifications at multiple scales.
- Floral data: estimated percentage cover and flowering for 28 plant groups, collected in spring and summer; field surveys for habitat value of different parcels.
- Landscape data: remote sensing from LiDAR (canopy height model) and hyperspectral data (EAGLE) to create a 0.5 x 0.5 m LULC map, later refined with field updates.

## Methods and Data Processing
- Remote sensing: LiDAR and hyperspectral data processed in ERDAS Imagine and ArcGIS to produce a nine-class LULC map; manual updates based on field surveys and landowner information.
- Floral/habitat assessment: for each mapped habitat parcel, estimated percent cover and percent in flower for plant groups; exclusions for inaccessible areas with mean values from surrounding parcels of the same LULC class.
- Nesting habitat suitability: parcels classified as high/medium/low suitability for each species based on vegetation structure, litter, moss, and signs of small mammal activity.
- Colony localisation: colonies inferred from distributions of full-sib sister workers using a mean-centre approach; locations snapped to nearest suitable LULC class; only colonies represented by two or more workers were estimated.
- Foraging distance: straight-line distance from worker capture location to the estimated colony location; mean distance per sibship used as colony-specific foraging distance.

## Landscape, Habitat and Floral Data
- Floral cover calculations:
  - All summer flowers, worker-preferred summer flowers, spring flowers, and spring-visited flowers; computed within defined colony foraging radii.
  - Distances tracked at four scales: 250 m, 500 m, 1000 m around each colony.
- Habitat variables (proportional cover) at multiple scales:
  - Arable, mixed vegetation, nesting suitability (high) within 250, 500, 1000 m radii.
  - Additional categories for all/spring/summer flower cover and queen-visited plant groups.

## Colony Location and Foraging Distances
- Foraging distance metrics:
  - AveDIST: average distance of 2012 spring queens from their estimated natal colony locations (for families with two or more queens).
  - Colony.Specific.Foraging.Distance: mean straight-line distance of all workers in a sibship from capture to estimated colony location.

## Data Structure and Key Variables
- Data file: Carvell_etal_IPI_Bombus_family_lineage_and_landscape_quality_data.csv.
- Core fields:
  - SPECIES: Bter (Bombus terrestris), Blap (B. lapidarius), Bpas (B. pascuorum).
  - Sp_Rel_Code: unique code for species and family/colony.
  - Q1: number of spring 2011 queens; W1: number of 2011 workers; Q2: number of spring 2012 queens.
  - Relationship: family relation category for each lineage.
  - AveDIST: dispersal distance for queens (when multiple sampled).
  - Colony.Specific.Foraging.Distance: mean foraging distance for the colony.
  - Proportional cover fields: Col.* and 250/500/1000 scales for summer/all/spring flowers, Queen-Visited Spring, Worker-Preferred Summer, and habitat categories (Arable, Mixed.Vegetation, Nesting_high) within each radius.
- Coverage scales: 250 m, 500 m, 1000 m, each with multiple plant-habitat variables.

## Analytical Methods and Validation
- Genetic methods described in full in Dreier et al. (2014a, 2014b); data handling with ERDAS Imagine and ArcGIS.
- LULC mapping and updates guided by field surveys and expert knowledge; quality checks at CEH and Institute of Zoology.
- Data and analyses associated with peer-reviewed publications: Molecular Ecology (Dreier et al. 2014) and Ecological Applications (Redhead et al. 2016).

## Data Availability and References
- Data submitted to the Environmental Information Data Centre (EIDC) as a CSV file; includes metadata on data structure and variable definitions.
- Core references:
  - Dreier et al. 2014a, Molecular Ecology.
  - Dreier et al. 2014b, NERC Environmental Information Data Centre.
  - Redhead et al. 2014, EIDC.
  - Redhead et al. 2016, Ecological Applications.