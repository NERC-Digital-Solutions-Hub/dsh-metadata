# Locations of sampled worker bumblebees across an agricultural landscape centred on the Hillesden Estate, Buckinghamshire, UK

## Purpose and scope
- Document the locations of worker bumblebees across a 1,950 ha agricultural landscape centred on the Hillesden Estate, Buckinghamshire, UK, covering five Bombus species.

## Data collected
- Non-lethal DNA sampling of workers; genetic analysis to confirm species and assign individuals to full-sib groups (colonies).
- Species confirmation and colony assignment performed using established genetic protocols.
- Geographic data collected in the field using a handheld GPS (Garmin Etrex 10) with approximately 3 m accuracy.

## Sampling design
- Landscape divided into 250 x 250 m grid cells.
- Within each cell, sampling across potential habitat patches with effort proportional to the relative cover of nesting and foraging habitats.
- Sampling conducted on 4–5 days per week from 20 June to 5 August 2011.
- The study sits within a context of standardised agri-environment mitigation options established in 2005.

## Genetic and spatial analyses
- Genotyping performed to assign individuals to species and colonies.
- COLONY v2.0 used to determine full-sib groupings (colonies).
- Spatial analyses conducted in ArcGIS; coordinates stored in Ordnance Survey grid references and British National Grid projection.

## Data structure and content
- Data provided as an ArcGIS shapefile containing 2,826 points, each representing a single worker.
- Underlying tabular data stored in a .dbf file readable by Excel or similar software.
- Key attributes:
  - FID: unique feature ID
  - Shape: geometry type (point)
  - Sample_Cod: field-assigned sample code
  - Date: collection date
  - Time: collection time
  - GridRef: Ordnance Survey grid reference
  - Genetic_Sp: species confirmed by genetic analysis (codes: Bter, Blap, Bpas, Bhor, Brud)
  - Colony: colony code from sibship assignment
  - Colony_Cod: unique colony code (combination of species and sibship)

## Data quality and provenance
- Data checked for errors at all stages by the Centre for Ecology and Hydrology (CEH) and the Institute of Zoology.
- DNA sampling, storage, extraction, genotyping, and assignment to species/colonies performed using recognised standard protocols.

## Data availability and lineage
- Data collected as part of a project led by CEH and funded under the Insect Pollinators Initiative.
- Dataset comprises 2,826 georeferenced worker locations, with associated genetic and colony information, provided as a GIS-ready shapefile and accompanying tabular data.

## Practical notes for data leaders
- Emphasises the importance of integrating genetic and spatial data with clear, machine-readable metadata.
- Highlights need for robust data quality checks and documentation of data lineage to support reuse in broader pollinator and landscape studies.