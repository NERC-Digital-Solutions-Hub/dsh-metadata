# Experimental design/sampling method

- Objective
  - Track changing chemical profiles of Maculinea rebeli caterpillars when reared with different Myrmica ant species, from pre-adoption to post-ant interaction and after isolation, to identify surface/semiochemical cues.

- Experimental design and sampling
  - Regions/localities: study sites in the Pyrenees, Poland, and naïve French ants; additional samples from Spain and Poland as indicated.
  - Subjects and treatments:
    - Unparasitized ants (Myrmica schencki and M. sabuleti) and naïve ants (France) that have not experienced M. rebeli.
    - M. rebeli larvae sampled at multiple stages:
      - Pre-adoption final instars after leaving Gentiana cruciata
      - After 6 weeks living with naïve French ants
      - After isolation from ants for 5 days
  - Sampling details:
    - Hexane extracts of surface chemicals prepared for each group.
    - Sample sizes (n) per group vary:
      - (i) n = 5 workers from 5 nests per locality
      - (ii) eight batches per region (n = 5 larvae per batch; total 40 per larval type)
      - (iii) n values differ by region (Spain/Poland; values provided in the text)
      - (iv) after isolation/sterile 5-day period (n = 5, 4, or 3 depending on group)

- Analytical method and quality assurance
  - Instrumentation and run conditions:
    - Gas chromatography with mass spectrometric detection (GC-MS) using HP 5890II GC and HP 5971A MSD; helium carrier gas; 10 psi column head pressure; full-scan m/z 40–600.
  - Data processing and QC:
    - Screen hydrocarbons via ion m/z 57; integrate peaks (threshold 12 on HP integrator) to obtain total ion areas.
    - Use Equivalent Chain Length (ECL) based on n-C20 to n-C36 for peak positioning.
    - Check chromatograms for interferences; ensure peaks are distinct and symmetrical; exclude column bleed, siloxanes, and phthalate plastics via characteristic ion m/z 149.
    - Tentative identification by ECL and full-scan MS; cross-check with NIST-97/08 database.
  - Quantification approach:
    - Express each peak area as a proportion of the sum of all peak areas in the chromatogram.

- Data storage and metadata
  - Format: CSV text file
  - Column label explanations:
    - Example labels indicate sample origin, host ant, country, sample number, and treatment stage.
    - Examples: Rebeli_sab_0_ES_1141 (M. rebeli reared with M. sabuleti, Spain, sample 1141); Rebeli_sab_5_ES_1155 (same group after 5 days isolation, Spain, sample 1155); Rebeli_sch_0_PL_1106 (M. rebeli with M. schencki, Poland, sample 1106); Sabuleti_Fr_1082 (M. sabuleti ants from France, sample 1082).
  - Label conventions cover host ant species, country, sample number, stage (pre/adoption vs after 5 days isolation), and regional origin.

- Relevance for monitoring/frameworks
  - Demonstrates a structured, metadata-rich approach to environmental/biological chemical monitoring: explicit sampling design across regions and conditions, standardized analytical workflow, clear data formatting, and comprehensive documentation of sample identifiers to enable data sharing, reuse, and audit trails.