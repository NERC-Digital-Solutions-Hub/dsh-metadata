# Abstract: Microsatellite data for five species of common and declining bumblebee ( Bombus terrestris, B. lapidarius, B. pascuorum, B. hortorum and B. ruderatus ) collected across the Hillesden Estate, Buckinghamshire, UK, in summer 2011.

## Overview
- Dataset of microsatellite genotypes for five Bombus species collected in 2011 in Buckinghamshire, UK.
- Part of a Centre for Ecology and Hydrology project funded by the Insect Pollinators Initiative.
- Data suitable for governance, discovery, and reuse with proper metadata and provenance.

## Data Collection and Experimental Design
- Study area: agricultural landscape spanning 1,950 ha around the Hillesden Estate; 250 x 250 m grid cells.
- Sampling window: 20 June – 5 August 2011; 4–5 days per week.
- Habitat context: standardized agri-environment mitigation options (grass and wildflower margins) implemented since 2005.
- Sampling strategy: workers collected across habitat patches; intensity proportional to habitat availability.
- Biological design: five bumblebee species; workers genotyped non-lethally; queen genotypes reconstructed from worker offspring.

## Data and Metadata Content
- Data types:
  - Worker genotypes: 2,577 individuals genotyped at 10–14 microsatellite loci per species; reduced data option available for diversity analyses.
  - Queen reconstructed genotypes: reconstructed queen multilocus genotypes from worker data; per-colony family size and queen IDs recorded.
- Data formats and structure:
  - Primary format: CSV files; Excel-based processing prior to submission.
  - Files (example naming):
    - Worker genotypes: per species (bter, blap, bpas, bhor, brud)
    - Queen genotypes: per species (bter, blap, bpas, bhor, brud)
  - Key columns for workers: Count, Date collected, CEH-ID, Reduced data, Colony, followed by 10–14 locus alleles.
  - Key columns for queens: Colony, Family size, Queen ID, followed by 10–14 locus alleles.
- Loci and species codes:
  - Species codes: bter (Bombus terrestris), blap (B. lapidarius), bpas (B. pascuorum), bhor (B. hortorum), brud (B. ruderatus).
  - Loci lists and locus-specific data vary by species.

## Methods and Standards
- DNA sampling and preservation: non-lethal sampling from the terminal tarsus; material preserved in 100% ethanol.
- DNA extraction and amplification: HotSHOT protocol; 8 μl PCR reactions; amplification of 10–14 microsatellite loci per species.
- Genotyping and analysis:
  - Capillary sequencing (ABI 3130xl) with LIZ 500 internal size standards.
  - Genotypes determined with GENEMAPPER v4.1.6.
  - Colwing of workers into full-sib groups using COLONY v2.0, with assumed monogamy for both sexes and a genotyping error rate of 0–5%.
  - Queen genotypes reconstructed from worker genotypes using COLONY v2.0.
- Documentation of data processing:
  - Data entry in Excel; submission to European Biodiversity Data Centre (EIDC) as CSV.
  - Data files include raw worker genotypes and queen reconstructed genotypes.

## Provenance, Documentation, and Reuse
- Data provenance:
  - Collected under a defined experimental design with explicit sampling regime and habitat context.
  - Quality checks performed at CEH and Institute of Zoology; genotyping error rate assessed via re-genotyping 10% of samples.
- Quality assurance:
  - Standard molecular methods and software validated for accuracy.
  - Analyses subjected to peer review and published in Molecular Ecology.
- Documentation and metadata:
  - Comprehensive notes on sample collection, lab protocols, loci, species-specific details, and file naming.
  - Data structure described (CSV format, column headers, and missing data coded as 0).
- Data sharing and accessibility considerations:
  - Data intended for sharing via appropriate portals and catalogues; potential limitations include disclosure risks, proprietary concerns, or embargoes.
  - Documentation supports reproducibility and re-use, including detailed methods and locus information.

## Data Stewardship Considerations and Challenges
- Governance considerations:
  - Clear lineage from field collection to genetic analysis; well-documented processing steps facilitate auditability.
  - Availability of both raw worker genotypes and queen reconstructions supports various reuse scenarios (e.g., population structure, mating system analyses).
- Usability and interoperability:
  - Standardized microsatellite loci and consistent file naming enhance interoperability across systems and portals.
  - Metadata includes sampling dates, locations, and colony identifiers to enable discoverability and re-use.
- Potential challenges for data stewards:
  - Incomplete or evolving user needs for metadata and data integration.
  - Ensuring timely data availability and compliance with data sharing restrictions.
  - Managing data across multiple formats and species-specific locus sets.
  - Handling large genotype matrices and ensuring robust linking of worker and queen data per colony.