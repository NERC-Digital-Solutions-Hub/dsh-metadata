# Locations of sampled worker bumblebees across an agricultural landscape centred on the Hillesden Estate, Buckinghamshire, UK

## Overview
- Dataset of worker bumblebee samples from five species (Bombus terrestris, B. lapidarius, B. pascuorum, B. hortorum, B. ruderatus) across a 1,950 ha agricultural landscape centered on Hillesden Estate, Buckinghamshire, UK.
- Non-lethal DNA sampling of workers; genetic analysis confirms species and assigns individuals to full-sib groups (colonies).
- Collected under the Insect Pollinators Initiative; data collection period: 20 June–5 August 2011.
- Data intended to support spatial and genetic analyses of pollinators in agricultural mosaics.

## Data collection scope and design
- Location data recorded with handheld GPS (Garmin Etrex 10); precision ~3 m.
- Landscape divided into 250 x 250 m grid cells; sampling across all potential habitat patches within each cell.
- Sampling intensity roughly proportional to relative habitat cover of nesting and foraging resources.
- Environmental context includes standardised pollinator-friendly mitigation options implemented since 2005.
- Sampling cadence: 4–5 days per week during the sampling window.

## Collection, generation and transformation methods
- Capture method: entomological nets.
- Genetic analysis: genotyped workers; COLONY v2.0 used to assign individuals to full-sib groups (colonies).
- Geographic data: coordinates captured in OS grid references, read into ArcGIS, exported as an ESRI Shapefile.

## Data content and format
- ArcGIS shapefile (EIDC) containing 2,826 point records; each point represents a single worker’s capture location.
- Underlying table (.dbf) readable in Excel or similar tools.
- Key attributes:
  - FID: unique feature ID
  - Sample_Cod: field-assigned sample code
  - Date, Time: collection timestamp
  - GridRef: Ordnance Survey grid reference
  - Genetic_Sp: genetically confirmed species (codes: Bter, Blap, Bpas, Bhor, Brud)
  - Colony: colony code from sibship assignment
  - Colony_Cod: unique colony identifier (species + sibship)
- Species assignments and colony codes derived from genetic analysis (COLONY v2.0).

## Analytical methods
- Genetic analyses performed with COLONY v2.0.
- Spatial analyses conducted in ArcGIS (GIS software) to map and analyze sample locations and colony structure.

## Data quality and provenance
- Data checked for errors at all stages by the Centre for Ecology and Hydrology (CEH) and the Institute of Zoology.
- Location accuracy and data integrity documented; explicit quality statements accompany the data.

## Data structure and accessibility
- Shapefile widely readable by GIS applications; associated .dbf table accessible in spreadsheet/database programs.
- Documentation available within the dataset detailing fields, codes, and processing steps.

## Potential applications for data support
- Create interactive maps and dashboards to explore spatial distribution of bumblebee species and colonies.
- Analyze fine-scale spatial genetic structure and habitat associations in an agricultural landscape.
- Support policy or conservation planning by illustrating pollinator distribution relative to habitat patches and mitigation options.
- Combine with other data sources (habitat, flowering resource maps, landscape features) to produce data products for non-specialist end users and policymakers.

## Notes and references
- Data collection and analysis follow referenced workflows (Dreier et al. 2014; Wang 2004) for genetic sibship reconstruction.
- Data packaged as both GIS shapefile and accompanying metadata to enable re-use and integration with other datasets.