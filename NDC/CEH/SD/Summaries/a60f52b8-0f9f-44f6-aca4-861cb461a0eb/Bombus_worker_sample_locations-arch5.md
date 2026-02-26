# Locations of sampled worker bumblebees across an agricultural landscape centred on the Hillesden Estate, Buckinghamshire, UK

## Overview
- Dataset documenting 2,826 individual worker bumblebee locations across a 1,950 ha agricultural landscape centered on the Hillesden Estate, Buckinghamshire, UK.
- Five species studied: Bombus terrestris, B. lapidarius, B. pascuorum, B. hortorum, B. ruderatus.
- Non-lethal DNA sampling used to confirm species identity and assign individuals to full-sib groups (colonies).
- Project led by the Centre for Ecology and Hydrology; funded under the Insect Pollinators Initiative.
- Data quality and validation performed by CEH and the Institute of Zoology.

## Data provenance and collection context
- Geographic data collected with a handheld GPS (Garmin Etrex 10) accuracy ~3 m.
- Sampling conducted 20 June–5 August 2011, 4–5 days per week.
- Landscape design includes standardized agri-environment mitigation options and conventionally farmed arable fields, organized into a 250 × 250 m grid.
- Sampling intensity in each cell proportional to the relative cover of nesting and foraging habitats.

## Methods and processing
- Specimens captured using entomological nets.
- DNA genotyping performed; individuals assigned to species and full-sib groups using COLONY v2.0 (Wang 2004).
- Geographic coordinates recorded in the field and processed into GIS formats (ArcGIS).

## Geographic information and data formats
- Location data stored as an ESRI ArcGIS shapefile (EIDC shapefile) with 2,826 point records.
- Underlying tabular data stored in a .dbf file; both formats widely readable in GIS and spreadsheet software.
- Coordinates recorded as Ordnance Survey grid references (British National Grid projection).

## Data structure and attributes
- Each record represents a single worker bee capture with associated attributes:
  - FID: unique feature ID
  - Shape: geometry type (point)
  - Sample_Cod: field-assigned sample code
  - Date: collection date
  - Time: collection time
  - GridRef: Ordnance Survey grid reference
  - Genetic_Sp: species identification confirmed by genetic analysis
    - Codes: Bter = Bombus terrestris, Blap = B. lapidarius, Bpas = B. pascuorum, Bhor = B. hortorum, Brud = B. ruderatus
  - Colony: colony code from sibship assignment
  - Colony_Cod: unique colony code (combination of species and sibship)

## Data quality, validation and scope
- Quality statement: GPS accuracy ~3 m; non-lethal DNA sampling; standard protocols for storage, extraction, genotyping; species and colony assignments made with established methods.
- Data checked for errors at all stages by CEH and the Institute of Zoology.

## Experimental design and sampling regime (in brief)
- Study area: 1,950 ha landscape around Hillesden Estate, Southern England.
- Grid-based sampling: 250 × 250 m cells; sampling across all habitat patches within each cell.
- Temporal window: 20 June–5 August 2011; targeted sampling aligned with habitat availability.

## Availability, access, and reuse notes
- Data available as ArcGIS shapefile (EIDC) containing 2,826 point records, with accompanying .dbf table.
- Shapefile and its tabular data are suitable for integration into GIS workflows and basic data analysis tools (e.g., Excel for .dbf).
- Data use references: primary genetic and spatial analyses published (Dreier et al. 2014a, 2014b) and foundational COLONY methodology (Wang 2004); associated data centre: NERC Environmental Information Data Centre.

## References for provenance and methods
- Wang J (2004) Sibship reconstruction from genetic data with typing errors. Genetics, 166, 1963-1979.
- Dreier, S. et al. (2014a, 2014b) Microsatellite genotype data and fine-scale spatial genetic structure across an agricultural landscape.
- Data centre and project documentation: NERC Environmental Information Data Centre.