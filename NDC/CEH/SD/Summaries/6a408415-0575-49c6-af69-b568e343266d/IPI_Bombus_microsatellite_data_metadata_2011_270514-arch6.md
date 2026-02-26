# Microsatellite data for five species of common and declining bumblebee ( Bombus terrestris, B. lapidarius, B. pascuorum, B. hortorum and B. ruderatus ) collected across the Hillesden Estate, Buckinghamshire, UK, in summer 2011

## Overview
- Dataset of microsatellite data for five Bombus species collected in 2011 from the Hillesden Estate, Buckinghamshire, UK.
- Worker genotypes are direct observations; queen genotypes are reconstructed from worker offspring.
- Led by the Centre for Ecology and Hydrology; funded under the Insect Pollinators Initiative.
- Aims to enable population/genetic analyses and data use by others (e.g., self-serve exploration, re-use in broader studies).

## Quality and validation
- Non-lethal DNA sampling from the terminal tarsus of workers; samples stored in 100% ethanol.
- Genotyped using recognized standard microsatellite protocols; data checked for errors by CEH and Institute of Zoology staff.
- Genotyping error rate estimated at 0–5% based on re-genotyping 10% of samples.
- COLONY v2.0 used to assign workers to full-sib groups and to reconstruct mother queen genotypes.
- Analyses arising from the data peer-reviewed and published in Molecular Ecology.

## Experimental design and sampling regime
- Study area: 1,950 ha agricultural landscape around Hillesden Estate; standardized agri-environment mitigations present since 2005.
- Sampling framework: 250 x 250 m grid cells; within each cell, sampling across habitat patches proportional to habitat availability.
- Sampling period: 4–5 days per week from 20 June to 5 August 2011.

## Collection, generation, and transformation methods
- Non-lethal worker DNA sampling via a small distal tarsus piece; preserved in ethanol until extraction.
- DNA extraction: HotSHOT protocol; PCR amplified across 10–14 microsatellite loci.
- Genotyping: PCR products measured as base pairs; capillary sequencing on ABI 3130xl; allele calling with GENEMAPPER.
- Loci: standardized across species (BL03, BL11, BT10, BT26, BTMS0125) with additional species-specific loci listed in the dataset description.
- Species and loci: 
  - Bombus terrestris (bter): multiple additional loci listed
  - Bombus lapidarius (blap): multiple additional loci listed
  - Bombus pascuorum (bpas): multiple additional loci listed
  - Bombus hortorum (bhor): multiple additional loci listed
  - Bombus ruderatus (brud): multiple additional loci listed
- Sample size: 2,577 workers genotyped across the five species.
- Data processing: COLONY v2.0 used for sibship analysis and queen reconstruction; haplo-diploid system; assumed monogamy; full-likelihood method; allele frequencies not updated; moderate likelihood precision.

## Data structure and content
- Data stored as Excel-derived CSV files submitted to EIDC in two main groups:
  1) Worker genotypes (one file per species)
     - File names: 
       - Dreier etal_IPI_Bombus_microsatellite_bter_worker genotypes.csv
       - Dreier etal_IPI_Bombus_microsatellite_blap_worker genotypes.csv
       - Dreier etal_IPI_Bombus_microsatellite_bpas_worker genotypes.csv
       - Dreier etal_IPI_Bombus_microsatellite_bhor_worker genotypes.csv
       - Dreier etal_IPI_Bombus_microsatellite_brud_worker genotypes.csv
     - Columns include: Count (unique sample), Date collected, CEH-ID, Reduced data (one worker per colony for diversity analyses), Colony (full-sib group code), and alleles for 10–14 loci (missing data coded as 0).
     2) Queen reconstructed genotypes (one file per species)
     - File names:
       - Dreier etal_IPI_Bombus_microsatellite_bter_queen genotypes.csv
       - Dreier etal_IPI_Bombus_microsatellite_blap_queen genotypes.csv
       - Dreier etal_IPI_Bombus_microsatellite_bpas_queen genotypes.csv
       - Dreier etal_IPI_Bombus_microsatellite_bhor_queen genotypes.csv
       - Dreier etal_IPI_Bombus_microsatellite_brud_queen genotypes.csv
     - Columns include: Colony (full-sib group), Family size (number of worker offspring sampled per colony), Queen ID, and alleles for the same 10–14 loci.
- Species codes:
  - bter = Bombus terrestris
  - blap = Bombus lapidarius
  - bpas = Bombus pascuorum
  - bhor = Bombus hortorum
  - brud = Bombus ruderatus

## Metadata and references
- Locus and methodology references provided for standard microsatellite panels and COLONY-based analyses (e.g., monoandry/polyandry in Bombus, microsatellite loci development, and genotype reconstruction).
- Data structure notes: raw worker genotypes and queen genotypes are provided; reduced data subset is indicated for diversity analyses.
- Data collection and analysis documented to support reproducibility and re-use in related pollinator genetics studies.

## Potential uses for data support
- Reconstruct mating system dynamics and queen–offspring relationships within and among colonies.
- Population genetic structure, gene flow, and colony-level diversity across a managed landscape with pollinator enhancements.
- Cross-species comparisons of microsatellite diversity in Bombus species.
- Integration with ecological or landscape data to assess effects of habitat management on pollinator genetics.