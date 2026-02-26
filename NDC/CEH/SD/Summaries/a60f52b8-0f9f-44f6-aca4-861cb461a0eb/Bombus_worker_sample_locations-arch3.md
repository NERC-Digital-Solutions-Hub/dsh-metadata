# Locations of sampled worker bumblebees across an agricultural landscape centred on the Hillesden Estate, Buckinghamshire, UK

## Purpose and scope
- Document reporting locations of worker bumblebees from five species (Bombus terrestris, B. lapidarius, B. pascuorum, B. hortorum, B. ruderatus).
- Aims to enable spatial analyses of pollinators in an agricultural landscape and to support landscape-level monitoring of pollinator populations.
- Data collected as part of the Centre for Ecology and Hydrology project, funded under the Insect Pollinators Initiative.
- Workers were non-lethally DNA sampled; species confirmed and individuals assigned to full-sib groups (colonies).

## Study area and experimental design
- Landscape area: 1,950 hectares centered on the Hillesden Estate, Buckinghamshire, Southern England, UK.
- Experimental design: landscape divided into 250 x 250 m grid cells; standardized agri-environment mitigation options for pollinators implemented in 2005 alongside conventional arable fields.
- Sampling approach: within every cell, sampling across all potential habitat patches; sampling intensity proportional to the relative cover of nesting and foraging habitats.
- Sampling period: 4–5 days per week between 20 June and 5 August 2011.

## Data collection and processing
- Specimen collection: bumblebee workers captured with entomological nets.
- Genetic analyses: samples genotyped; COLONY v2.0 used to assign workers to full-sib groups (colonies).
- Species confirmation: genetic analysis used to confirm species identity.
- Spatial data collection: GPS coordinates recorded in the field using a Garmin Etrex 10 (accuracy ~3 m); coordinates read into ArcGIS as Ordnance Survey grid references and exported as a shapefile.

## Data structure and contents
- Dataset format: ArcGIS shapefile (EIDC shapefile) containing 2,826 point records; each point represents an individual worker.
- Key attributes:
  - FID: unique feature ID
  - Shape: point geometry
  - Sample_Cod: field-assigned sample code
  - Date: collection date
  - Time: collection time
  - GridRef: Ordnance Survey grid reference
  - Genetic_Sp: species confirmed by genetics (Bter, Blap, Bpas, Bhor, Brud)
  - Colony: colony code from sibship assignment
  - Colony_Cod: unique colony code (combination of species and sibship)
- Data accessibility: underlying tabular data (.dbf) readable by Excel or similar; shapefile readable by most GIS software.

## Analytical methods
- Genetic analysis: COLONY v2.0 used for sibship/colony assignment.
- Spatial analysis: GIS processing carried out in ArcGIS to relate locations to habitat patches and landscape features.

## Quality assurance and data provenance
- Data quality: field coordinates checked; genetic data processed and validated by Centre for Ecology and Hydrology and the Institute of Zoology.
- Accuracy and standards: GPS accuracy ~3 m; standard protocols for DNA sampling, storage, extraction, and genotyping followed.
- Documentation and references: detailed methodology referenced (Dreier et al. 2014a, 2014b) and genetic analysis methods (Wang 2004); data contribute to NERC Environmental Information Data Centre.

## Data formats and reuse considerations for monitoring frameworks
- GIS-ready: shapefile with accompanying .dbf provides straightforward integration into monitoring dashboards and spatial analyses.
- Metadata and lineage: clear recording of sampling dates, locations, species, and colony assignments supports traceability and reproducibility.
- Policy relevance: enables assessment of pollinator distribution in relation to habitat patches and agri-environment measures; suitable for evaluating spatial dynamics, colony structure, and potential impacts of landscape management.
- Data governance: provenance and quality controls demonstrated; documentation supports data sharing and governance aligned with open-data practices where applicable.

## References
- Wang J (2004) Sibship reconstruction from genetic data with typing errors. Genetics, 166, 1963-1979.
- Dreier, S., Redhead, J.W., Warren, I., Bourke, A.F.G., Heard, M.S., Jordan, W.C., Sumner, S., Wang, J. & Carvell, C. (2014a) Microsatellite genotype data for five species of bumblebee across an agricultural landscape in Buckinghamshire, UK. NERC Environmental Information Data Centre.
- Dreier, S., Redhead, J.W., Warren, I.A., Bourke, A.F.G., Heard, M.S., Jordan, W.C., Sumner, S., Wang, J. & Carvell, C. (2014b) Fine-scale spatial genetic structure of common and declining bumble bees across an agricultural landscape. Molecular Ecology, Published online.