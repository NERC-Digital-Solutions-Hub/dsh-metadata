# Locations of sampled worker bumblebees across an agricultural landscape centred on the Hillesden Estate, Buckinghamshire, UK

## Overview
- Provides geo-referenced locations of worker bumblebees from five species across a 1,950 ha agricultural landscape centered on the Hillesden Estate, Buckinghamshire, UK.
- Each sampled worker is identified to species (via non-lethal DNA) and assigned to a full-sib group (colony) using standard genetic analyses.
- Data collected under the Insect Pollinators Initiative, led by the Centre for Ecology and Hydrology (CEH).

## Data scope and sampling design
- Species covered: Bombus terrestris, B. lapidarius, B. pascuorum, B. hortorum, B. ruderatus.
- Landscape and grid: study area divided into 250 x 250 m grid cells within 1,950 ha; standardized agri-environment mitigation options for pollinators implemented since 2005.
- Field sampling period: 20 June – 5 August 2011; sampling occurred 4–5 days per week.
- Sampling intensity: proportional to relative cover of suitable nesting and foraging habitats within each cell.
- Location data: geographic coordinates recorded in Ordnance Survey grid references (British National Grid) using a handheld GPS (Garmin Etrex 10; accuracy ~3 m).

## Collection, genetic analysis, and spatial processing
- Collection method: non-lethal DNA sampling of worker bumblebees via entomological nets; individuals stored and processed for genotyping.
- Genetic analysis: species confirmation and colony assignment performed with COLONY v.2.0 (Wang 2004).
- Spatial data processing: grid references read into ArcGIS (ESRI) and exported as an ESRI Shapefile; coordinates and attributes stored in associated tabular data (.dbf).

## Data structure and content
- Data format: ArcGIS shapefile containing 2,826 georeferenced points (one per worker), with an accompanying .dbf table.
- Key attributes:
  - Sample_Cod: field sample code
  - Date: collection date
  - Time: collection time
  - GridRef: Ordnance Survey grid reference
  - GenSp: genetically confirmed species (codes: Bter, Blap, Bpas, Bhor, Brud)
  - Colony: colony code derived from sibship assignment
  - Colony_Cod: unique colony code (species + sibship)
- Accessibility: shapefile readable by most GIS apps; .dbf readable by Excel or similar tools; metadata notes indicate standard protocols and quality checks.

## Quality assurance and data integrity
- Quality checks at multiple stages by CEH and Institute of Zoology.
- GPS accuracy around 3 m ensures precise localization of individuals.
- Standardized genetic analyses and lifecycle of data (collection, genotyping, species/colony assignment) documented and validated per referenced methods.

## Practical implications for environmental monitoring
- Enables monitoring of bumblebee distribution and colony structure in an agricultural landscape, supporting assessment of pollinator health and the effectiveness of pollinator-focused agri-environment schemes.
- Data are standardized and interoperable (GIS-ready), facilitating integration with habitat data, management practices, and other environmental datasets for time-series analyses and policy evaluation.
- Highlights the value of linking field observations with genetic data to understand spatial population structure over fine scales in managed landscapes.

## References and methodological foundations
- Wang J (2004) Sibship reconstruction from genetic data with typing errors.
- Dreier et al. (2014a, 2014b) related microsatellite genotype datasets and fine-scale spatial genetic structure across an agricultural landscape.