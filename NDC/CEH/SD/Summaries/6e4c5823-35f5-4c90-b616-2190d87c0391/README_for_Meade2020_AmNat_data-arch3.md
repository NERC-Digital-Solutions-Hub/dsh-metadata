# Maintenance of fertility in the face of meiotic drive

- Purpose and scope
  - Investigates differences in fertility (egg hatch) when Teleopsis dalmanni females are mated to males with SR vs ST genotype.
  - Experimental setup: males mated with either one (low mating rate) or five (high mating rate) females; unmated males included; males and related tissues dissected to measure organ sizes.
  - Rationale: organ sizes are known to correlate with fertility and mating rate in wild-type males.

- Data and measures
  - Data file: Meade2020_AmNat_data.csv
  - Key columns and meanings
    - male_id: unique identifier for each male
    - females: number of females the male mated with over a 10-hour period (1 or 5 for mated; 0 for unmated)
    - batch: experimental batch identifier
    - eyespan: male eyespan (mm)
    - thorax: male thorax length (mm)
    - testis: testis area (mm^2)
    - accessory_gland: accessory gland area (mm^2)
    - total_eggs: total eggs laid by female(s) (fecundity)
    - fertile_eggs: fertilised eggs laid (fertility)
    - comp162710, ms395, cnv395: allele sizes (bp) from genetic markers
    - genotype: male genotype (SR or ST) assigned using the marker sizes
  - Data provenance
    - The dataset is linked to the study by Meade et al. (2020) and published as a Note in The American Naturalist
    - Contact emails provided for data origin: a.pomiankowski@ucl.ac.uk, lara.meade.13@ucl.ac.uk

- Experimental design details
  - Males categorized by mating exposure (1, 5, or unmated) and genotype (SR or ST)
  - Morphological measurements (eyespan, thorax) and reproductive organ sizes (testis, accessory gland) collected
  - Reproductive output captured via total and fertilised eggs
  - Genotype assignment based on specific genetic markers (INDEL and microsatellite markers)

- Provenance, metadata and data governance
  - Clear variable definitions, units, and measurement types (e.g., mm, mm^2, bp)
  - Unique identifiers and batch information support traceability and reproducibility
  - Genotype determination method documented via allele sizes
  - Metadata provided to facilitate reuse and verification of data quality

- Relevance to monitoring frameworks
  - Demonstrates rigorous data management: explicit variable definitions, units, provenance, and versionable data file
  - Highlights importance of accessible, well-documented data for evaluating biological hypotheses and informing future research directions
  - Illustrates challenges in data sharing and metadata completeness that monitoring frameworks aim to address (e.g., enabling data governance, reproducibility)

- Limitations and considerations
  - Data derive from a single study and organism; generalizability may be limited
  - Fertility assessment based on egg hatch outcomes; may not capture all facets of reproductive success
  - Some barriers to data reuse may arise if metadata beyond what is described is needed for broader analyses

- Practical uses
  - Enable analyses linking mating rate, genotype, morphology, and reproductive output
  - Serve as a model for documenting data provenance, measurement definitions, and governance in monitoring-related datasets