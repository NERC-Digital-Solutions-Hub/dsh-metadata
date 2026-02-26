# Experimental design/sampling method

- Objective: Track changing surface chemical profiles of Maculinea rebeli caterpillars across regional contexts and social environments (with ants), from uncontaminated pre-adoption instars through six weeks with ants, then isolation to allow semiochemical dissipation.
- Sample categories and contexts:
  - (i) Unparasitized ants (Myrmica schencki and M. sabuleti) on study sites in Pyrenees, Poland; naïve ants in France. Sampled as 5 workers from 5 nests of each ant per locality.
  - (ii) Eight batches per region of pre-adoption final instar M. rebeli larvae sampled after leaving Gentiana cruciata but before contact with ants (5 larvae per batch; total 40 larvae per type).
  - (iii) M. rebeli larvae after six weeks living with naïve French ants. Sample sizes reported as n = 5 for some groupings and n = 3 for others, depending on regional–ant pairing (Spanish+sabuleti and Polish+schencki vs. Spanish+schencki and Polish+sabuleti).
  - (iv) M. rebeli larvae reared as in (iii), then isolated from ants and kept unfed and singly in sterile conditions for 5 days (n = 5 for Spanish+schencki; n = 4 for Polish+schencki; n = 3 for Spanish+sabuleti and Polish+sabuleti).
- Regions and species involved: Pyrenees (Spain/France), Poland, and France; ant partners include Myrmica sabuleti and Myrmica schencki.
- Outcome measures: Hexane surface chemical extracts from each sample category to assess semiochemical profiles over time and treatment conditions.

# Analytical method/Quality Assurance

- Analytical workflow:
  - Concentration: Maculinea extracts to 20 ml; ant workers to 50 ml.
  - Instrumentation: Gas chromatography–mass spectrometry (GC-MS) with HP 5890II GC and HP 5971A MSD; ultra-high purity helium as carrier gas at 10 psi column head pressure.
  - Detection: Full-scan mass spectra from 40 to 600 m/z; initial screening for hydrocarbons via m/z 57.
  - Quantification: Peak areas integrated with threshold 12 (HP integrator); expressed as proportions of total peak area in each chromatogram.
- Compound identification:
  - Use of alkane standards (n-C20 to n-C36) to calculate Equivalent Chain Length (ECL) for peaks.
  - Peak validation to avoid interferences (column bleed, siloxanes, phthalates identified by characteristic ions such as m/z 149).
  - Tentative identifications based on ECL and full-scan MS spectra, cross-referenced with NIST-97/08 databases.
- Data quality considerations:
  - Consistency across sample sequences, with standard QC checks for peak distinctness and chromatographic symmetry.
  - Exclusion of dubious peaks and interferences to maintain robust comparative analyses.

# Format of stored data

- Data format: CSV text file.

# Explanation of column labels

- Example explanations:
  - Rebeli_sab_0_ES_1141: Sample from Maculinea rebeli reared with Myrmica sabuleti; country Spain; sample number 1141.
  - Rebeli_sab_5_ES_1155: Sample from Maculinea rebeli reared with Myrmica sabuleti; after 5 days isolation; country Spain; sample number 1155.
  - Rebeli_sch_0_PL_1106: Sample from Maculinea rebeli reared with Myrmica schencki; country Poland; sample number 1106.
  - Rebeli_none_pre_PL_1029: Sample from pre-adoption Maculinea rebeli; country Poland; sample number 1029.
  - Sabuleti_Fr_1082: Sample taken from Myrmica sabuleti; country France; sample number 1082.
  - Schencki_Es_1042: Sample taken from Myrmica schencki; country Spain; sample number 1042.
- Structure: The label encodes the organism (Rebeli), the ant partner (sab/schencki), the time point (0 for pre-adoption or 5 for post-isolation), country code, and sample number, enabling cross-group comparisons and regional tracking.

# Relevance to environmental monitoring and data management

- Standardized, multi-regional data collection enables temporal and spatial comparisons of caterpillar–ant chemical interactions, contributing to understanding ecosystem chemical ecology as an environmental health indicator.
- Data are prepared for integration with other datasets and portals, aligning with the aim of increasing dataset value and enabling access to underlying data for broader scrutiny and reuse.
- The CSV format and explicit metadata facilitate transparency, quality assurance, and reuse in monitoring programs that track ecological interactions and environmental policy performance over time.