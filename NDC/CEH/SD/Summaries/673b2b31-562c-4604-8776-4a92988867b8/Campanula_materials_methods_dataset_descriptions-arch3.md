# Campanula rotundifolia cytotype determination and common garden study in the British Isles

- Overview
  - A study to determine cytotype diversity (diploid, tetraploid, pentaploid, hexaploid) and to assess phenology, growth, and fecundity through a common garden experiment using clones from field material collected across Britain and Ireland.
  - Aims include understanding how cytotype variation relates to flowering dynamics and reproductive output, and establishing a controlled comparison across cytotypes.

- Plant material
  - More than 1700 geo-referenced samples (seeds, leaves, or stem cuttings) collected, with many contributed by volunteers; focus on Britain and Ireland, plus some samples from elsewhere for context.
  - Field collection protocols ensured fresh handling and proper storage: leaves/stem cuttings kept cool; seeds air-dried and stored; leaf tissue stored at -20°C.
  - Sampling strategy aimed to minimize sampling the same clone by maintaining at least 5 m between plants; additional sampling in areas where hexaploids had been previously reported (Wanlockhead, Teesdale, Cheddar).
  - Cytotype results are catalogued in campanula_cytotype.csv with detailed location data (0.01° resolution) and sample codes; surplus material retained at CEH Edinburgh for potential reuse.

- Cytotype determination
  - Chromosome counts from previous work were validated by flow cytometry; any conflicts led to reanalysis with fresh material.
  - Flow cytometry protocol (Doležel et al. 2007) used an internal standard (Pisum sativum 'Ctirad'), propidium iodide staining, and standard gating to determine DNA content.
  - Quality control included replicates and ensuring coefficient of variation (CV) of peaks did not exceed 5%.
  - Samples were analyzed with flow cytometers (FACSCalibur or Accuri C6); DNA contents were compared to known C. rotundifolia cytotypes to assign cytotype.
  - Time since collection and sample condition affected results; desiccation and red/brown coloration yielded erratic outputs and those data were excluded from Cx analyses.
  - Cytotype assignment: genome size ranges used to classify samples as diploid (2.27–2.71 pg), tetraploid (4.22–4.96 pg), pentaploid (5.33–5.65 pg), hexaploid (6.2–7.14 pg); samples outside these ranges labeled as aneuploid.

- Common garden study
  - Clones for the common garden were produced from cuttings or seed-derived plants from field locations collected in the prior two years.
  - Plants were planted October 2008 in a raised bed near CEH Edinburgh (site naturally tetraploid) with five randomized blocks; layout included clones of tetraploid, pentaploid, and hexaploid cytotypes.
  - Each block contained multiple clones; overall design included 55 tetraploid, 1 pentaploid, and 37 hexaploid clones per block.
  - Maintenance included occasional weeding; pollination was not restricted to mimic natural conditions.
  - Phenology (first flowering date, FFD) was recorded in 2009 and 2010 via daily inspections.

- Data collection and measurements
  - Phenology: For 2009 and 2010, FFD was recorded as the date at which the first flower opened sufficiently to be visited by bees; data stored in campanula_FFD.csv.
  - Growth and fecundity (August 2009): For blocks 1 and 3, counted total flowering stems per plant; measured height and seed-related metrics for stem no. 1; repeated for stems 2 and 3; notes on plant condition recorded.
  - Growth and fecundity (September 2009): For blocks 2 and 5, harvested above-ground biomass; recorded total stem dry weight and number of flowering stems.
  - Data files and column details:
    - Campanula_cytotype.csv: Country, Location, Sample code, Latitude, Longitude, Cytotype.
    - campanula_FFD.csv: Block, Clone code, Date of first flowering (2009), Day number, plant-condition comments, Date of first flowering (2010), Day number, plant-condition comments.
    - Dest_harvest_Aug_2009_blocks_1_and_3.csv: Block, Clone code, total flowering stems, stem measurements and counts (seedheads, open flowers, buds) for multiple stems, and plant-condition comments.
    - Dest_harvest_Sept_2009_blocks_2_and_5.csv: Block, Clone code, total stem dry weight, number of flowering stems.
  - Data conventions: an asterisk (*) marks dead or missing data; clone names containing 'sd' indicate seedling-derived clones.

- Data handling, provenance and governance
  - Data are organized by clearly defined files with explicit column headings and cross-references across cytotype and phenology datasets.
  - Anonymity of sampling sites is preserved by presenting coordinates at 0.01° resolution when possible.
  - Samples and materials stored at CEH Edinburgh with sample codes enabling traceability and potential future use.
  - Data quality controls included explicit thresholds (e.g., CV for flow cytometry peaks) and re-analysis where necessary.

- Figure and supplementary notes
  - Figure 1 illustrates the layout of clonal plants across five blocks in the common garden.
  - The document notes that hexaploids were targeted for intensified sampling in certain sites to determine their distribution.
  - References provide methodological and contextual support for flow cytometry, polyploidy, and prior work on Campanula rotundifolia.

- References (selected)
  - Doležel, Greilhuber, Suda (2007). Estimation of nuclear DNA content in plants using flow cytometry.
  - McAllister (1972); Shepherd (2007); Stevens, Wilson, McAllister (2012) for cytogenetics and phylogeography context.
  - Stevens et al. (2012) Biological Flora of the British Isles: Campanula rotundifolia.