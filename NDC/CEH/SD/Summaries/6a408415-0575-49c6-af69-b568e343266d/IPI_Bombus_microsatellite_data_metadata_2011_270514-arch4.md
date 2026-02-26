# Microsatellite data for five species of common and declining bumblebee ( Bombus terrestris, B. lapidarius, B. pascuorum, B. hortorum and B. ruderatus ) collected across the Hillesden Estate, Buckinghamshire, UK, in summer 2011.

- What the dataset contains
  - Microsatellite genotype data for five Bombus species from worker bees, with queen genotypes reconstructed from worker offspring.
  - 2,577 workers genotyped across the five species; queen identities reconstructed using COLONY v2.0.
  - Non-lethal sampling of worker DNA, with subsequent genetic analyses to infer colony structure and maternal genotypes.

- Context and aims
  - Study conducted on the Hillesden Estate, Buckinghamshire, UK, within a 1,950 ha agricultural landscape.
  - Part of a project led by the Centre for Ecology and Hydrology, funded under the Insect Pollinators Initiative.
  - Data support analyses of mating systems, colony structure, and genetic diversity across species and landscape contexts.

- Experimental design and sampling regime
  - Landscape divided into 250 x 250 m grid cells; sampling targeted habitat patches and was proportionate to available nesting/foraging habitats.
  - Standard agri-environment mitigation options present in 2005 (grass and wildflower margins).
  - Sampling period: 20 June – 5 August 2011; 4–5 days per week.
  - Workers collected across all habitat patches in each cell to capture spatial variation.

- Collection, generation, and transformation methods
  - Non-lethal DNA collection from the terminal tarsus of a mid-leg; preserved in 100% ethanol.
  - DNA extraction via HotSHOT protocol; PCR amplified 10–14 microsatellite loci.
  - Genotyping performed on an ABI 3130xl capillary sequencer; allele calling with GENEMAPPER v4.1.6.
  - Loci used: standard set for Bombus spp.; species-specific additional loci listed per species.
  - Data processed with COLONY v2.0 to assign workers to full-sib groups (colonies) under a monogamous mating system assumption; genotyping error rate estimated at 0–5% from re-genotyping 10% of samples.

- Queen reconstruction
  - COLONY v2.0 used to reconstruct mother queen multilocus genotypes from worker genotypes.
  - Haplo-diploid species system; assumptions include monogamy for males and females; full-likelihood analysis with specified parameters.

- Data structure and formats
  - Data organized in Excel during processing and submitted to EIDC as CSV files.
  - Two main data groups per species:
    - Worker genotypes (CSV files named for each species, e.g., Dreier etal_IPI_Bombus_microsatellite_bter_worker genotypes.csv)
    - Queen reconstructed genotypes (CSV files named for each species, e.g., Dreier etal_IPI_Bombus_microsatellite_bter_queen genotypes.csv)
  - Key columns for workers: Count (sample ID), Date collected, CEH-ID, Reduced data (one worker per colony for diversity analyses), Colony (colony code), and alleles for 10–14 loci; missing data coded as 0.
  - Key columns for queens: Colony (colony code), Family size (number of worker offspring sampled per colony), Queen ID, and locus alleles.
  - Species codes: bter = Bombus terrestris; blap = B. lapidarius; bpas = B. pascuorum; bhor = B. hortorum; brud = B. ruderatus.

- Data quality, validation, and provenance
  - DNA sampling, storage, extraction, and genotyping followed recognized standard protocols; high-level quality checks conducted by CEH and Institute of Zoology staff.
  - Analyses (including colony reconstruction) peer-reviewed and accepted for publication in Molecular Ecology.
  - Quality statement notes verification at multiple stages and estimation of genotyping error via re-genotyping.

- Data accessibility and metadata
  - Data are organized with explicit metadata, including sample IDs, collection dates, colony assignments, and locus data.
  - Detailed locus lists provided per species, with references to established microsatellite markers and methods.

- Reuse and governance implications for Data Leaders
  - Demonstrates robust data lifecycle: design-informed sampling, non-lethal collection, standardized lab methods, transparent data processing, and traceable provenance.
  - Emphasizes the importance of clear data structures, naming conventions, and metadata (e.g., reduced data option for diversity analyses).
  - Useful for cross-species comparative studies, population genetics, and colony dynamics in managed landscapes.
  - Highlights need for careful documentation of loci, software parameters, and error rate assumptions to enable reproducibility and cross-network collaboration.

- References and standard methods
  - Standard microsatellite markers and protocols cited (Estoup et al. 1995, 1996; Reber Funk et al. 2006; Stolle et al. 2009; Truett et al. 2000; Wang 2004), with software and methodological details provided (COLONY v2.0, GENEMAPPER, HotSHOT).