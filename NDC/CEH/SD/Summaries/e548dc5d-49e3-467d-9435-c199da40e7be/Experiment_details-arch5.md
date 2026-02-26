# Overview of data

- What the dataset is
  - pigAMRgenecounts.csv contains quantitative PCR (qPCR) read outs from antimicrobial resistance gene (AMRG) assays and associated metadata.
  - Data represent mean gene copy numbers per microlitre of DNA extract for each sample.
  - Target genes include tetB, ermA, ermB, dfrA1, tetQ, and 16S, with per-sample copy numbers recorded as copies/µl.

- Context and sampling scope
  - Samples collected from a single British commercial pig unit, including faecal and environmental materials (soil, slurry).
  - Two study phases: the main study (Oct 19, 2016 – Apr 5, 2017) and a depopulation study (Jun 19, 2017 – Nov 13, 2017).
  - Data generation period: Aug 1, 2017 – May 1, 2018.
  - Purpose: monitor dynamics of antimicrobial resistance gene dynamics on-farm in response to antimicrobial administration and management practices (including partial depopulation).

- Sampling design and content
  - Main study: 329 faecal and environmental samples; weekly sampling across three piglet pens during weaning, growing, and finishing phases; background sow barn samples and slurry samples for farm-wide context.
  - Depopulation study: 45 additional samples to track AMR gene dynamics after depop.
  - Sample types: faeces (piglets and sows), soil/environment, and slurry.
  - Experimental framework includes three pen replicates, multiple farm locations, and a timeline tied to production phases and antimicrobial exposure (acidified water, chlortetracycline in feed, tylosin in-feed).

- Metadata and data structure
  - The dataset comprises 24 columns with structured metadata and gene-copy measurements.
  - Columns include: Short sample identifier, sample description, full sample identifier, category of pigs, sampling date, sampling site, DNA box ID, DNA concentration, sample wet/dry weight, percentage dry matter, distance from sow barn (environmental samples), copy numbers for tetB, ermA, ermB, dfrA1, tetQ, 16S, experiment type (main or depop), sample type, pig type, pig age, pen ID, and antibiotic used.
  - Data can be standardized or normalized post hoc (e.g., by % dry matter or by 16S copies) according to metadata.

- Laboratory methods and standards
  - DNA extraction: PowerSoil DNA Isolation Kit (MoBio) with specified lysis and inhibitor-removal steps; detailed handling of soil-like samples and preservation of DNA purity.
  -DNA quantification: NanoDrop measurements (260/280 and 260/230 ratios) and aliquoting into multiple 20 µL aliquots for storage at -80°C.
  - qPCR: Absolute quantification using a standard curve (dilution series of cloned plasmid) with triplicate reactions; controls included (no-template controls and replicates).
  - Reagents and protocols: Agilent Brilliant III Ultra Fast Mastermix; specified cycling program; primer/probe sets for target genes and 16S; references to supporting literature.

- Data processing and reporting
  - Copy numbers derived by extrapolating from the standard curve using the qPCR instrument (Mx3005p/Mx3000P).
  - Data imported into Excel, aligned with corresponding metadata; reported as mean copies/µl per sample.
  - The dataset notes potential standardization options using %DM or 16S copy numbers for cross-sample comparability.

- Data provenance and documentation
  - Data and protocols linked to the pigAMRgenecounts.csv dataset with explicit references to sample collection, DNA extraction, qPCR methods, and data processing steps.
  - The accompanying text provides comprehensive details on sample handling, storage conditions (-20°C on-farm, -80°C in-lab), QC practices, and the structure of the dataset.

- Data governance and stewardship implications
  - The dataset includes extensive procedural metadata (collection site, sample type, pig category, pen IDs, dates, antibiotic exposure) essential for reproducibility and governance.
  - Documentation covers data quality considerations (random missing values due to sampling limitations) and normalization options, aiding transparent data sharing and reuse.
  - For data stewards, the clear column definitions and lab protocols support data discoverability, interoperability, and potential re-use in meta-analyses of AMR dynamics on production animals.