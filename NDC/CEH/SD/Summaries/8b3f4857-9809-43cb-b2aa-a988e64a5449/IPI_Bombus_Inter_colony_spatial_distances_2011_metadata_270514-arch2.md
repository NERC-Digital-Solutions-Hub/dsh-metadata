# Geographic distances between pairs of wild bumblebee colonies across an agricultural landscape in Buckinghamshire, UK

## Aim and scope
- Quantify geographic distances between pairs of wild bumblebee colonies across a 1950 ha agricultural landscape centered on the Hillesden Estate, Buckinghamshire, UK.
- Study spatial structure for five Bombus species: Bombus terrestris, B. lapidarius, B. pascuorum, B. hortorum, and B. ruderatus.
- Report intercolony distances ranging from 7 to 5264 metres.

## Data collection and sampling regime
- Sampling conducted in summer 2011 (June–August) across all potential habitat patches in the study area.
- Worker bees sampled non-lethally; tarsal tip removed from the right mid-leg and preserved in 100% ethanol.
- Geographic locations of individual workers recorded with GPS.
- Landscape area defined as 1950 hectares in southern England.

## Laboratory methods and data processing
- DNA extracted and genotyped; workers assigned to full-sib colonies using COLONY v2.0 (Wang 2004).
- Colony locations estimated from the mean centre of worker locations within each sibship.
- Mean-centre locations snapped to the nearest land-use/land-cover class reflecting potential nesting habitat.
- Only colonies represented by two or more workers were included in analyses.

## Distance calculation and outputs
- Euclidean distances calculated between all possible pairs of colonies (two or more workers per colony).
- Distances reported in metres.

## Data structure, storage and availability
- Spatial data mapped in ArcGIS; stored in Excel; backed up as CSV.
- Data file: Dreier_etal_IPI_Bombus_Inter_colony_spatial_distances_2011.csv
- Contains 48,423 rows, each representing a pairwise distance between two colonies.
- Columns include: FROM_FID, FROM_Colony, FROM_X, FROM_Y, DISTANCE, TO_FID, TO_Colony, TO_X, TO_Y, species.
- Species codes: bter (Bombus terrestris), blap (B. lapidarius), bpas (B. pascuorum), bhor (B. hortorum), brud (B. ruderatus).

## Quality assurance and validation
- Worker DNA sampled non-lethally; samples stored, extracted, genotyped, and colonies assigned using standard protocols.
- Spatial locations generated in ArcGIS and checked for errors by staff at CEH and the Institute of Zoology.
- Analyses peer reviewed and accepted for publication in Molecular Ecology.

## Data accessibility and references
- Data submitted to the Environmental Information Data Centre (EIDC) with quality checks at multiple stages.
- Key methodological reference: Wang J (2004) Sibship reconstruction from genetic data with typing errors.