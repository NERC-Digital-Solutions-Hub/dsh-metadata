# Locations of sampled worker bumblebees across an agricultural landscape centred on the Hillesden Estate, Buckinghamshire, UK

- Summary of content
  - Spatial locations for 2826 individual worker bumblebees (five species) across a 1,950 ha agricultural landscape centered on the Hillesden Estate, Buckinghamshire, UK, collected in 2011.
  - Individuals were non-lethally DNA sampled; species and full-sib (colony) assignments were made via genetic analysis.
  - Data are provided as an ArcGIS-ready shapefile with accompanying attribute data, suitable for map-based GIS analyses and visualization.

## What the dataset contains

- 2826 georeferenced points representing individual worker bumblebee captures.
- Five species: Bombus terrestris, B. lapidarius, B. pascuorum, B. hortorum, B. ruderatus (genetically confirmed).
- Each point linked to a colony (full-sib group) via COLONY analysis.
- GIS-friendly format: ArcGIS shapefile with associated .dbf table.

## Data collection and quality

- Field collection with handheld GPS (Garmin Etrex 10); location accuracy ~3 m.
- Non-lethal DNA sampling; standard protocols used for storage, extraction, genotyping, and species/colony assignment.
- Quality checks conducted by Centre for Ecology and Hydrology (CEH) and Institute of Zoology staff.

## Experimental design and sampling regime

- Study area: 1,950 ha agricultural landscape near Hillesden Estate, Southern England.
- Grid-based sampling: 250 x 250 m cells; sampling in every cell across all potential habitat patches.
- Sampling intensity proportional to relative habitat cover of nesting and foraging resources.
- Sampling window: 4–5 days per week from 20 June to 5 August 2011.
- Habitat management context: presence of agri-environment mitigation options targeted at pollinators implemented since 2005.

## Collection and data processing methods

- Capture method: entomological nets.
- Genetic analyses: COLONY v2.0 used to assign workers to full-sib groups (colonies).
- GIS processing: field GPS coordinates read into ArcGIS; data exported as an ESRI Shapefile.
- Projection/format: coordinates stored in Ordnance Survey grid references (British National Grid).

## Data structure and attributes

- File type: ArcGIS shapefile; underlying .dbf contains tabular attributes.
- Core attributes:
  - FID: unique feature ID
  - Shape: geometry type (point)
  - Sample_Cod: field sample code
  - Date: collection date
  - Time: collection time
  - GridRef: OS grid reference
  - Genetic_Sp: species code (Bter, Blap, Bpas, Bhor, Brud)
  - Colony: colony code from sibship assignment
  - Colony_Cod: unique colony code (concatenation of species and sibship)
- Coordinate system: British National Grid (Ordnance Survey grid)

## Spatial data considerations for GIS use

- Ready-to-use for map-based visualization and spatial analyses; shapefile readable in standard GIS software; .dbf usable in spreadsheet/database tools.
- Spatial coverage corresponds to a 1,950 ha landscape with systematic grid-based sampling across habitat patches.
- Data provenance links to genetic methodology (COLONY) and related publications.

## Access, references, and provenance

- Data validated by CEH and Institute of Zoology staff.
- References:
  - Wang J 2004 (COLONY method)
  - Dreier et al. 2014a, 2014b (microsatellite data and fine-scale spatial genetic structure)
- Dataset contributions from: Carvell, Bourke, Dreier, Heard, Jordan, Sumner, Wang, Redhead.