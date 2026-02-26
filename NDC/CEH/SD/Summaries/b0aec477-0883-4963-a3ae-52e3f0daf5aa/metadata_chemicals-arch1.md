# Experimental design/sampling method

- Objective
  - Track changing chemical profiles of Maculinea rebeli caterpillars from different regions when reared with each ant species, observing changes from uncontaminated pre-adoption instars to six weeks with ants, and then after a 5-day isolation to dissipate acquired semio-chemicals and elicit the caterpillars’ own secretions.

- Experimental design
  - Timepoints and treatment conditions
    - (i) Unparasitized Myrmica schencki and Myrmica sabuleti on study sites (Pyrenees, Poland) and naïve French ants with no prior experience of M. rebeli.
    - (ii) Pre-adoption final-instar M. rebeli larvae after leaving Gentiana cruciata, before contact with ants.
    - (iii) M. rebeli larvae after living 6 weeks with naïve French ants.
    - (iv) M. rebeli larvae from (iii) then isolated from ants and kept unfed, singly in sterile conditions for 5 days.
  - Scope and locality
    - Regions include Spain (Es/Es), Poland (Pl/Pl), and France (Fr) with multiple nest/colony sources.
  - Sample counts (illustrative)
    - Vary by stage and pairing, e.g., initial ant/region combinations with n ranging from 3 to 5 per group, multiple batches and nested sampling across localities.

- Specimens and sampling categories
  - Ants: unmated, naïve workers from M. schencki and M. sabuleti colonies; naïve ants in France that had not experienced M. rebeli.
  - Caterpillars: pre-adoption M. rebeli larvae (ending Gentiana cruciata visitation), and M. rebeli larvae after 6 weeks with ants, plus larvae after 5-day post-ant-isolation.
  - Localities and pairings: combinations of Spanish/Polish origins with sabuleti or schencki ants; French naïve ants included for some comparisons.

- Analytical methods and quality assurance
  - Chemical analysis
    - Hexane extracts of surface chemicals prepared for Maculinea rebeli and ants.
    - Gas chromatography–mass spectrometry (GC-MS) using HP 5890II GC and HP 5971A MSD; full scan 40–600 m/z; helium as carrier gas.
    - Data processing: screen hydrocarbons via ion m/z 57; integrate peaks with threshold 12; use Equivalent Chain Length (ECL) based on n-C20 to n-C36 alkane standards; peaks tentatively identified by ECL + full spectra against NIST-97/08.
    - Quality control: inspect chromatograms for interferences; exclude column bleed, siloxanes, phthalates (noted by m/z 149); express each peak area as a proportion of the total peak area.
  - Data handling
    - Data stored in CSV text files.

- Data format and column labels
  - Column labels follow a detailed scheme indicating species, region, sample type, and sample number (examples include Rebeli_sab_0_ES_1141, Rebeli_sab_5_ES_1155, Rebeli_sch_0_Es_1111, rebeli_none_pre_PL_1029, etc.).
  - Descriptions attached to labels indicate: species reared with a specific Myrmica ant (sabuli/ schencki), country/origin (ES/PL/FR), sample number, and whether the sample is pre-adoption, post-adoption, or post-isolation.
  - The dataset includes samples from pre-adoption M. rebeli, M. rebeli reared with various ants, and after 5 days isolation, across Spain, Poland, and France, along with corresponding ant-only and naïve ant controls.

- Data management and accessibility notes
  - The study uses standardized extraction, GC-MS analysis, and data normalization (proportions of peak areas) to enable cross-condition comparisons.
  - A structured CSV format with explicit metadata in the sample labels supports traceability across regions, ant species, and treatment stages.