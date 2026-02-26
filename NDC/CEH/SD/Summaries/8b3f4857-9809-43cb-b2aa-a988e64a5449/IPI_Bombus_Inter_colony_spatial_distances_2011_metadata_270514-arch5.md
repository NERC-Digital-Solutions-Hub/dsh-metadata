# Geographic distances between pairs of wild bumblebee colonies across an agricultural landscape in Buckinghamshire, UK

## Purpose and scope
- Documents geographic distances between pairs of wild bumblebee colonies in an agricultural landscape centered on the Hillesden Estate, Buckinghamshire, UK.
- Studies spatial structure across five Bombus species (B. terrestris, B. lapidarius, B. pascuorum, B. hortorum, B. ruderatus) with intercolony distances ranging from 7 to 5264 metres.
- Data collected as part of a project led by the Centre for Ecology and Hydrology, funded under the Insect Pollinators Initiative.

## Data provenance and sampling design
- Location: 1950 ha landscape around Hillesden Estate, Southern England (coordinates provided in data).
- Sampling period: June–August 2011.
- Target taxa: five bumblebee species.
- Non-lethal DNA sampling from worker bees; right mid-leg tarsal tips removed and preserved in 100% ethanol.
- Worker locations recorded with GPS; colony assignments derived from genotyped workers.

## Data collection, transformation, and processing
- Laboratory workflow: DNA extraction and genotyping following recognized standard protocols.
- Colony grouping: workers assigned to full-sib groups (colonies) using COLONY v.2.0.
- Spatial processing: colony locations estimated as mean-centre of worker locations; final locations snapped to the nearest land-use/land-cover class that could form suitable nesting habitat.
- Inclusion criteria: colonies represented by two or more workers.
- Distance calculation: geographic (Euclidean) distances computed between all colony pairs; expressed in metres.

## Data products and structure
- Primary data product: a CSV file containing pairwise inter-colony distances.
- File: Dreier_etal_IPI_Bombus_Inter_colony_spatial_distances_2011.csv, stored in EIDC as CSV; 48,423 rows.
- Data rows describe a pair of colonies with fields:
  - FROM_FID, FROM_Colony, FROM_X, FROM_Y
  - DISTANCE
  - TO_FID, TO_Colony, TO_X, TO_Y
  - species (four-letter code)
- Species codes:
  - bter = Bombus terrestris
  - blap = B. lapidarius
  - bpas = B. pascuorum
  - bhor = B. hortorum
  - brud = B. ruderatus

## Metadata, documentation, and data quality
- Provenance: data generated in ArcGIS; backed up as Excel files; then shared as CSV.
- Quality assurance: data checked for errors at Centre for Ecology and Hydrology and Institute of Zoology.
- Validation: analyses derived from the data have undergone peer review and were published in Molecular Ecology.
- Metadata completeness: explicit column definitions provided; species coding documented.

## Technical validation and reproducibility
- Location accuracy and sampling integrity supported by GPS recording and non-lethal DNA methods.
- Colony assignments based on standard genetic analysis (COLONY v.2.0) with an established reference (Wang 2004).
- Analytical methods (mean-centre colony estimation; snapping to land-use class) documented for reproducibility.

## Data stewardship, accessibility, and reuse considerations
- Data are stored and backed up in multiple formats (ArcGIS project, Excel, CSV) and archived with the EIDC.
- Clear documentation of data structure and field meanings facilitates reuse and interoperability with GIS and population genetics workflows.
- Sharing constraints and update mechanisms are acknowledged in the project context (data sharing respects limitations; systems for updates are in place as applicable).
- Users should reference the original study and the COLONY method when reanalyzing genetic assignments and colony delineations.

## Supporting references
- Wang J (2004) Sibship reconstruction from genetic data with typing errors. Genetics, 166, 1963-1979.