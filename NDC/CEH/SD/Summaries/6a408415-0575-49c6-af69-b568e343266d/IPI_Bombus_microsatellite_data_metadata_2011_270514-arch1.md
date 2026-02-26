# Microsatellite data for five species of common and declining bumblebee ( Bombus terrestris, B. lapidarius, B. pascuorum, B. hortorum and B. ruderatus ) collected across the Hillesden Estate, Buckinghamshire, UK, in summer 2011

## Overview
- Objective: provide microsatellite data to study genetic structure, colony relationships, and potential mating patterns in five bumblebee species.
- Scope: 2011 field study on Hillesden Estate, Buckinghamshire, UK, within an agricultural landscape with agri-environment measures.
- Species: Bombus terrestris, B. lapidarius, B. pascuorum, B. hortorum, B. ruderatus.
- Scale: landscape-level sampling across 1,950 ha with a 250 x 250 m grid.

## Sampling design and collection
- Sampling frame: standardized habitat patches within each grid cell; sampling intensity proportional to available nesting and foraging habitats.
- Time frame: 4–5 days per week, 20 June – 5 August 2011.
- Specimen type: non-lethal DNA sampling from bumblebee workers (terminal tarsus) preserved in 100% ethanol.
- Sample coverage: 2,577 workers genotyped across the five species.

## Laboratory methods and quality control
- DNA extraction: HotSHOT protocol from small tarsus tissue.
- Genotyping: 10–14 microsatellite loci per species; PCR products analyzed on an ABI 3130xl capillary sequencer; allele calling with GENEMAPPER v4.1.6.
- Loci: species-specific sets (e.g., common loci BL03, BL11, BT10, BT26, BTMS0125 used across all; additional loci specified per species).
- Quality checks: DNA sampling, genotyping, and data checks performed by CEH and Institute of Zoology staff; genotyping error rate estimated at 0–5% via re-genotyping 10% of samples.
- Data processing: haplo-diploid sibship reconstruction using COLONY v2.0 (monogamy assumed for both sexes; full-likelihood analysis; specified error rates).

## Data structure and content
- Data organization: Excel-based data processed and exported to CSV for EIDC submission.
- Worker genotypes: one CSV per species containing unique sample IDs, collection dates, colony codes (full-sib groups), and alleles across 10–14 loci.
- Queen reconstructed genotypes: one CSV per species containing colony code, family size, queen ID, and alleles across the same loci.
- Reduced data: within-colony samples selected to represent genetic diversity.
- File naming conventions (examples):
  - Worker genotypes: Dreier etal_IPI_Bombus_microsatellite_bter_worker genotypes.csv, etc.
  - Queen genotypes: Dreier etal_IPI_Bombus_microsatellite_bter_queen genotypes.csv, etc.
- Data fields: includes Count (sample number), Date collected, CEH-ID, Reduced data, Colony; loci columns contain allele sizes in base pairs; missing data indicated by 0.

## Analytical framework and potential use
- Primary analyses enabled: assignment of workers to full-sib colonies, reconstruction of mother queen genotypes, estimation of colony structure and mating patterns in haplo-diploid Bombus.
- Cross-species comparisons: ability to compare colony dynamics, sibship, and genetic diversity across five Bombus species within a shared landscape.
- Links to ecology and management: data can inform how habitat features and agri-environment measures relate to genetic structure, mating behavior, and potential gene flow.

## Validation, references, and provenance
- Standard methods and references for microsatellite work and COLONY-based sibship reconstruction documented (e.g., Estoup et al. on polyandry/monoandry, Reber Funk et al., Stolle et al., Truett et al., Wang).
- Data quality and peer review: analyses arising from the data have been peer reviewed and accepted for publication in Molecular Ecology.

## Practical considerations for analysts
- Data accessibility: stored as CSVs with clearly labeled loci; dataset is multi-species and multi-file, requiring careful merging by species and data type.
- Data consistency: cross-species locus sets vary; allele coding must align to reference loci per species.
- Limitations: snapshot from summer 2011 in a specific landscape; missing data present as zeros; interpretation should consider local habitat context and temporal scope.
- Data integration: potential to combine with habitat, management, and temporal data to model drivers of genetic structure and colony dynamics.