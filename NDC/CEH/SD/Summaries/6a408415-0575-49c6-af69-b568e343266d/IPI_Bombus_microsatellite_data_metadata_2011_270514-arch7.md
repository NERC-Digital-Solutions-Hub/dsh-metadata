# Microsatellite data for five species of common and declining bumblebee ( Bombus terrestris, B. lapidarius, B. pascuorum, B. hortorum and B. ruderatus ) collected across the Hillesden Estate, Buckinghamshire, UK, in summer 2011

## Overview
- Dataset of microsatellite genotypes for five bumblebee species collected in a 1,950 ha agricultural landscape around the Hillesden Estate, Southern England, UK, during summer 2011.
- Part of a project led by the Centre for Ecology and Hydrology under the Insect Pollinators Initiative.
- Includes worker genotypes and reconstructed queen genotypes derived from worker offspring.

## Spatial sampling design and context
- Landscape divided into 250 x 250 m grid cells; sampling targeted habitat patches within each cell.
- Sampling period: 20 June – 5 August 2011, with 4–5 days of collection per week.
- Sampling area and activity linked to standardized agri-environment mitigation options (grass and wildflower strips along field margins).
- Central study coordinates: 1°00'01" W, 51°57'16" N (Hill esden Estate).

## Data collection and laboratory methods
- Non-lethal DNA sampling from worker bumblebees; terminal portion of the tarsus (mid-leg) used, preserved in 100% ethanol.
- DNA extraction and microsatellite genotyping performed; 10–14 loci genotyped per species.
- Genotyping conducted using PCR, capillary electrophoresis, and allele sizing; software GENEMAPPER used for genotype calls.
- Genome-wide data quality validated by re-genotyping a subset (0–5% error rate estimated from re-genotyped samples); data checked by CEH and Institute of Zoology staff.
- Queen genotypes reconstructed from worker genotypes using COLONY v2.0; monoandrous/mating system assumptions applied in analyses.

## Data structure and files
- Data stored as comma-delimited (CSV) files and submitted to the European DNA Data Center (EIDC).
- Two main data types per species:
  - Worker genotypes: Dreier etal_IPI_Bombus_microsatellite_<species>_worker genotypes.csv
  - Queen reconstructed genotypes: Dreier etal_IPI_Bombus_microsatellite_<species>_queen genotypes.csv
- Species codes:
  - bter = Bombus terrestris
  - blap = B. lapidarius
  - bpas = B. pascuorum
  - bhor = B. hortorum
  - brud = B. ruderatus
- Columns and data:
  - Worker file: Count, Date collected, CEH-ID, Reduced data, Colony, followed by 10–14 loci alleles; missing data indicated by 0.
  - Queen file: Colony, Family size, Queen ID, followed by 10–14 loci alleles.
- Data volume: 2,577 workers genotyped across the five species.

## Experimental design and analysis details
- Worker sampling across all relevant habitat patches within each 250 x 250 m cell.
- COLONY v2.0 used to assign workers to full-sib groups (colonies) under a monogamous mating assumption for both sexes; genotyping error rate set at 0–5%.
- Queen genotypes reconstructed from worker data using COLONY with specified parameters (haplo-diploid system, full-likelihood method, no allele frequency updates, etc.).

## Quality assurance and peer review
- DNA sampling, storage, extraction, and genotyping followed recognized standard protocols.
- Data checks performed by CEH and Institute of Zoology staff.
- Analyses based on the data peer-reviewed and accepted for publication in Molecular Ecology.

## Reuse potential for GIS and spatial analyses
- Grid-based sampling provides a clear spatial framework suitable for GIS analyses of genetic diversity and structure across the landscape.
- Spatially explicit integration with habitat data (field margins, restoration strips, habitat patches) to assess spatial patterns of relatedness, colony distribution, and potential impacts of landscape features on pollinator genetics.
- The 1,950 ha study area and documented sampling design enable landscape-scale analyses and cross-referencing with environmental covariates.

## References and standard methods
- Estoup et al. (1995, 1996) on monoandry/polyandry and population differentiation in Bombus.
- Reber Funk et al. (2006); Stolle et al. (2009) on microsatellite loci for Bombus spp.
- Truett et al. (2000) HotSHOT DNA extraction protocol.
- Wang (2004) COLONY program for sibship reconstruction with typing errors.