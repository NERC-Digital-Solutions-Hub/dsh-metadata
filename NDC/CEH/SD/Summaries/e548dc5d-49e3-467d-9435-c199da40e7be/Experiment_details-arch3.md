# pigAMRgenecounts.csv

- Overview and purpose
  - A dataset of quantitative PCR (qPCR) read outs for antimicrobial resistance gene (AMRG) assays, with associated metadata.
  - Represents mean gene copy numbers per microlitre of DNA extract from environmental and faecal samples.
  - Collected from a single British commercial pig unit to monitor AMR gene dynamics in response to antimicrobial use and farm management practices.
  - Two study phases: the main study (Oct 19, 2016 – Apr 5, 2017) and a depopulation study (partial depopulation, Jun 19 – Nov 13, 2017); data generated Aug 1, 2017 – May 1, 2018.

- Data collected and study design
  - Sample types: faecal samples (from sow housing, piglet pens, and weaning/growing/finishing areas) and environmental samples (slurry tanks; surrounding land).
  - Experimental setup: three pen replicates followed through weaning, growing, and finishing phases; background sampling in sow barn; slurry samples to represent on-farm AMR at a higher level.
  - Sample counts: 329 faecal/environmental samples for the main study; 45 additional samples for the depopulation study.
  - Missing values: some samples missing due to material availability or access; assumed missing at random and not informative for analysis.

- Sampling, storage and processing (high-level)
  - Detailed, protocol-driven collection for each site (farrowing crate, sow barn, slurry, and weaning/growing/finishing pens) with strict labeling, sterile equipment, and immediate freezing at -20°C on-farm.
  - On-site storage followed by transport on dry ice to a -80°C repository prior to processing.

- Quality control and sample handling
  - Avoidance of contamination and cross-contamination (use of PCR-grade water, microbiological safety cabinet, sterile consumables, dedicated lab gear).
  - Samples thawed on wet ice before processing; careful handling to maintain integrity and traceability.

- DNA extraction and processing
  - DNA extracted using the PowerSoil DNA Isolation Kit (MoBio) with bead-beating and inhibitor removal steps (C1–C6 series) to maximize yield and purity and to remove humic substances and other inhibitors.
  - Final DNA eluted in C6 buffer and stored appropriately; DNA quantified prior to qPCR.

- DNA quantification and storage
  - DNA quantified with NanoDrop; concentrations and 260/280, 260/230 ratios recorded; aliquots prepared and stored at -80°C.
  - Careful tracking of aliquots to avoid opening critical samples outside of containment.

- qPCR methodology and targets
  - Absolute quantification via qPCR with standard curves generated from cloned plasmids containing target sequences; reactions run in triplicate with no-template controls.
  - Instrument: Agilent Mx3005p; master mix: Brilliant III Ultra Fast.
  - Targets (AMRGs and controls) include tetB, ermA, ermB, dfrA1, tetQ, and 16S rRNA gene as a reference/normalization target.
  - Primer/probe sequences and amplicon sizes provided for each target.

- Data processing and structure
  - qPCR data processed using MxPro software to extrapolate gene copy numbers from standard curves.
  - Data were imported into Excel and aligned with corresponding metadata.
  - Reported metric: mean copies per microlitre of DNA extract; standardization options include normalization by percent dry matter (%DM) or by 16S copy number.
  - Dataset structure: a single CSV file, pigAMRgenecounts.csv, with 24 columns capturing sample identifiers, descriptions, and quantitative results.

- Dataset structure details (sample fields)
  - Columns include: sample identifier (short and full), category (pigs or environment), sampling date, site, DNA box ID, DNA concentration, wet/dry weights, %DM, distance from sow barn (environmental samples), copy numbers for tetB, ermA, ermB, dfrA1, tetQ, 16S; experiment type (main or depopulation); sample type; pig type; age category; pen ID; antibiotic used.
  - References and contextual notes provide sources for qPCR primer usage and methodological background.

- Reproducibility, governance and policy relevance
  - The document emphasizes rigorous metadata integration, standardized data collection, and clear documentation of laboratory procedures to support policy evaluation and monitoring framework objectives.
  - Data standardization options (e.g., %DM, 16S normalization) facilitate cross-sample comparability for environmental health monitoring.
  - Transparency about data limitations (e.g., random missingness, single-farm scope) informs policy-level interpretation and generalizability considerations.

- Limitations and data gaps
  - Missing values present in the dataset due to sampling constraints; treated as random but could affect longitudinal interpretation.
  - Data originates from a single farm, which may limit broader generalizability to other contexts or production systems.