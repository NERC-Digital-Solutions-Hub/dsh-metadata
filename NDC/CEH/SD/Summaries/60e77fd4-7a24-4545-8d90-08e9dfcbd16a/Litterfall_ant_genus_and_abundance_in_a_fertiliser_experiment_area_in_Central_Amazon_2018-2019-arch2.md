# Amazon Fertilization Experiment (AFEX)

- Study context: Research conducted within the Biological Dynamics of Forest Fragments Project (BDFFP) area, KM41 reserve, ~100 km from Manaus, in dense Terra Firme rainforest with clay soils and a humid, wet climate. Soils are highly weathered with low nutrient fertility.

- AFEX design and implementation:
  - Full factorial fertilization experiment started March 2017.
  - Treatments (7 treatments + control): N, P, cations (K, Ca, Mg), and all combinations (N+P, cat+n, cat+p, cat+n+p, plus control).
  - Plot structure: 32 plots total (4 replicates per treatment), arranged in 4 independent blocks at least 250 m apart.
  - Plot size and location: 50 x 50 m plots, each at least 100 m apart.
  - Fertilization regime: annually, split into three applications to mitigate leaching/runoff.
  - Fertilizers used: N as urea (125 kg N ha-1 yr-1), P as triple superphosphate (50 kg P ha-1 yr-1), cations as KCl (50 kg K ha-1 yr-1) and Ca/Mg as dolomitic limestone (160 kg Ca ha-1 yr-1; 160 kg Mg ha-1 yr-1).

- Ant sampling methodology:
  - Subplot sampling: five 1 x 1 m subplots within each 50 x 50 m plot, totaling 20 subplots per treatment (160 subplots overall).
  - Collection method: Winkler extractor used on litter samples to capture ants; samples kept in 90% alcohol as fixative.
  - Sample processing: 48-hour extraction per subplot; ant identification conducted using subfamily and genus keys; species-level identifications aided by AntCat (Bolton, 2020) and INPA invertebrate collection.
  - Sampling periods: two annual samplings during the dry season (October 2018 and September 2019).

- Data captured and structure:
  - Main dataset: litterfall_ants.csv deposited to the EIDC (Environmental Information/Data Center).
  - Dataset contents (column descriptors):
    - YEAR: Sampling year (2018 or 2019; 2018 in October, 2019 in September)
    - BLOCK: Block number (1–4)
    - PLOT: Plot number (1–5)
    - TRT: Treatment and combination (as listed in AFEX design)
    - SUBFAMILIES: Ant subfamilies observed
    - GENERA: Ant genera observed
    - INDIVIDUAL: Number of individuals captured
  - Example data structure includes entries for various subfamilies (e.g., Myrmicinae, Ponerinae) and genera (e.g., Crematogaster, Hypoponera).

- Data management and accessibility:
  - Data are organized for standardised analysis of richness, composition, relative abundance, and frequency.
  - Collected data are intended for integration with other environmental datasets and made accessible via the EIDC repository.

- Outputs and relevance:
  - Provides baseline and treatment-response data on litter-dwelling ant communities under different nutrient and cation additions.
  - Enables comparisons of ant community metrics across fertilization treatments, years, and plots.

- References and methodology context:
  - Sampling and taxonomic references include Baccaro et al. (2015), Bolton (AntCat, 2020), Bestelmeyer (2000), and standard soil and forest ecology literature cited in the document.
  - The study area and soil descriptions reference Quesada et al. (2010, 2011) and Laurance et al. (1999), among others.

- Alignment with environmental monitoring aims:
  - Data are collected, verified, and standardized to monitor environmental health and policy-relevant outcomes over time.
  - Outputs are designed for clear presentation (datasets, tables, and potential maps/charts) and stored in a centralized portal for reuse.
  - Highlights ongoing challenges of increasing dataset utility through data integration and broad data accessibility.