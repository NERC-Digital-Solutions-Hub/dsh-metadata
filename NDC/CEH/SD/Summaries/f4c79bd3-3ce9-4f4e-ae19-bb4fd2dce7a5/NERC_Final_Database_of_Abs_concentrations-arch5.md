# Brief description of the dataset

- Focus: Weekly concentrations of fluoroquinolones and resistance qnrS gene in the South West UK.
- Analytes: Includes numerous fluoroquinolones (e.g., ofloxacin, desmethyl-ofloxacin, lomefloxacin, moxifloxacin, besifloxacin, prulifloxacin, ciprofloxacin, norfloxacin, nalidixic acid, etc.) and related compounds listed; abbreviations provided (n.d., MQL, Conc., influent, effluent, river upstream/downstream).
- Format: Concentrations reported in ng/L for influent and effluent wastewater and for the receiving river environment.

- Study area and sampling design
  - Timeframe: 7 consecutive days (Wednesday to Tuesday) between June and October 2015.
  - Locations: Five major wastewater treatment plants (WWTPs) contributing to one river catchment in South-West UK, covering ~2,000 km² and ~1.5 million people (over 75% of catchment population).
  - Matrices and sampling:
    - Influent wastewater: 24 h volume-proportional composites with ~15-minute subsamples.
    - Effluent wastewater: time-proportional samples.
    - River water: grab samples upstream and downstream of discharge points; site E not sampled (discharges directly to estuary).
  - Handling: Samples cooled on ice during collection; transported to laboratory on ice.

- Analytical workflow
  - Preparation: Filtration (GF/F 0.7 µm), spiking with isotopically-labeled internal standards, SPE using Oasis HLB cartridges, elution with methanol, evaporation, reconstitution, filtration.
  - Instrumentation: UPLC-MS/MS with chiral CHIRALCEL OZ-RH column; positive ESI; Xevo TQD triple quadrupole; internal standard-based quantification; isocratic mobile phase (10 mM ammonium formate/methanol 1:99 with 0.05% formic acid).
  - QA/QC: Analyses performed in duplicate; method fully validated; validation described in Castrignano et al. 2018.
  - Data processing: MassLynx control; TargetLynx for data processing.

- Data provenance and references
  - Primary method validation and related studies cited (Castrignano et al. 2018; Castrignano et al. 2020; Petrie et al. 2016).
  - Data format notes indicate concentrations in ng/L; adaptation of methods for enantioselective analysis. 

- Data governance and usability considerations for stewarding
  - Metadata and standards: Clearly defined analytes, abbreviations, matrices, sampling schemes, and units; links to detailed methodological references.
  - Data quality and lineage: Detailed sampling procedures, preparation, and instrument parameters; duplicate analyses; fully validated method.
  - Reuse caveats: Incomplete river sampling at one site (Site E); sample collection methods (volume- vs time-proportional) differ by matrix, which can affect cross-matrix comparability.
  - Documentation: Explicit reporting of analytical workflow and references supports traceability and reproducibility.

- Limitations and site-specific notes
  - Site E excluded due to estuary discharge pathway.
  - Temporal and spatial scope limited to one 7-day week in 2015; results require careful temporal/spatial generalization.

- References for methods and context
  - Castrignano, E., et al. 2018. Enantioselective fractionation of fluoroquinolones in the aqueous environment using chiral LC-MS/MS. Chemosphere.
  - Castrignano, E., et al. 2020. (Fluoro)quinolones and quinolone resistance genes in the aquatic environment: A river catchment perspective. Water Research.
  - Petrie, B., et al. 2016. Multi-residue analysis of 90 emerging contaminants... J Chrom A.