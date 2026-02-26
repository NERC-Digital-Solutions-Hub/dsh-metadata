# Microsatellite data for five species of common and declining bumblebee ( Bombus terrestris, B. lapidarius, B. pascuorum, B. hortorum and B. ruderatus ) collected across the Hillesden Estate, Buckinghamshire, UK, in summer 2011

## Overview and Aim
- Provides microsatellite genotypic data for five bumblebee species collected in 2011 across a 1,950 ha agricultural landscape centered on the Hillesden Estate, Buckinghamshire, UK.
- Part of a project led by the Centre for Ecology and Hydrology, funded under the Insect Pollinators Initiative.
- Worker genotypes were obtained directly; queen genotypes were reconstructed from worker offspring.
- Data support analyses of genetic structure, mating systems, and colony diversity using standardized methods; intended for use in monitoring environmental health and policy performance over time.

## Study area and sampling design
- Landscape: 1,950 ha agricultural area with standardized agri-environment mitigation options (grass and wildflower field margins) established in 2005.
- Sampling grid: 250 × 250 m cells; within each cell, workers were sampled across all habitat patches with effort proportional to habitat availability.
- Sampling window: 4–5 days per week from 20 June to 5 August 2011.
- Species: Bombus terrestris, B. lapidarius, B. pascuorum, B. hortorum, B. ruderatus.
- Total bees genotyped: 2,577 workers across the five species.

## Methods and laboratory workflow
- Sample collection: Non-lethal DNA sampling from the terminal portion of the bee tarsus; samples preserved in 100% ethanol.
- DNA extraction: HotSHOT protocol.
- Genotyping: 8 µl PCR reactions with 10–14 microsatellite loci; PCR conditions specified; products resolved on an ABI 3130xl Capillary Sequencer; genotypes determined with GENEMAPPER v4.1.6.
- Loci: All species genotyped at BL03, BL11, BT10, BT26, BTMS0125; species-specific additional loci listed per species.
- Colony assignment and queen reconstruction: COLONY v2.0 used to assign workers to full-sib groups (colonies) under a monogamous mating assumption for both sexes; queen multilocus genotypes reconstructed from worker genotypes.
- Data handling: Excel-based processing; data stored and submitted to EIDC in CSV format.

## Data structure and contents
- Worker genotypes files (CSV) per species:
  - Dreier etal_IPI_Bombus_microsatellite_bter_worker genotypes.csv
  - Dreier etal_IPI_Bombus_microsatellite_blap_worker genotypes.csv
  - Dreier etal_IPI_Bombus_microsatellite_bpas_worker genotypes.csv
  - Dreier etal_IPI_Bombus_microsatellite_bhor_worker genotypes.csv
  - Dreier etal_IPI_Bombus_microsatellite_brud_worker genotypes.csv
- Queen reconstructed genotypes files (CSV) per species:
  - Dreier etal_IPI_Bombus_microsatellite_bter_queen genotypes.csv
  - Dreier etal_IPI_Bombus_microsatellite_blap_queen genotypes.csv
  - Dreier etal_IPI_Bombus_microsatellite_bpas_queen genotypes.csv
  - Dreier etal_IPI_Bombus_microsatellite_bhor_queen genotypes.csv
  - Dreier etal_IPI_Bombus_microsatellite_brud_queen genotypes.csv
- Column headings and data:
  - Worker files include: Count, Date collected, CEH-ID, Reduced data (one worker per colony), Colony, followed by 10–14 loci alleles; missing data indicated by 0.
  - Queen files include: Colony, Family size, Queen ID, followed by 10–14 loci alleles.
- Species codes: bter = Bombus terrestris; blap = B. lapidarius; bpas = B. pascuorum; bhor = B. hortorum; brud = B. ruderatus.

## Quality control and validation
- Non-lethal sampling and standardized protocols used for DNA extraction and genotyping.
- Genotyping error rate estimated at 0–5% based on re-genotyping 10% of randomly selected individuals.
- Data checked for errors by staff at CEH and the Institute of Zoology.
- Analyses derived from the data have been peer reviewed and accepted for publication in Molecular Ecology.

## Data availability and formats
- Raw worker genotypes and queen reconstructed genotypes processed in Excel and submitted to the European Insect Data Centre (EIDC) as CSV files.
- Dataset structure supports replication and cross-study comparisons; reduced data option selects one worker per colony for diversity analyses.

## Relevance for environmental monitoring
- Provides a standardized, quality-controlled genetic dataset suitable for monitoring pollinator population structure, colony dynamics, and mating systems in an agricultural landscape.
- Enables integration with habitat, management, and policy data to evaluate environmental health and pollinator support measures over time.
- Data accessibility via a centralized data portal (EIDC) facilitates broader use and data linkage by researchers and policymakers.

## References
- Foundational methods and loci development references (Estoup et al. 1995, 1996; Reber Funk et al. 2006; Stolle et al. 2009; Truett et al. 2000; Wang 2004) underpin the microsatellite markers, colony reconstruction, and data processing approaches cited in the dataset.