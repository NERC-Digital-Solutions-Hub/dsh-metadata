# The Analysis of Immunological Profiles in Wild Animals: A Case Study on Immunodynamics in the Field Vole, Microtus agrestis

- Context and study aims
  - Investigates immunological profiles in wild voles to understand how immune gene expression relates to host variables and infection.
  - Data combine field-derived measurements with lab-measured immune gene expression and pathogen presence to explore correlations and potential predictive relationships.

- Study system and location
  - Species: field vole, Microtus agrestis.
  - Location: Kielder Forest, Northumberland, UK.

- Sampling design and field methods
  - Timeframe: 2015–2017.
  - Sites: seven sampling sites within forest clear-cuts; traps laid in grids with approximately 3–5 m spacing.
  - Trapping regime: longitudinal components with individuals sampled repeatedly and a cross-sectional component after culling; sessions occurred roughly every two weeks over March–October each year.
  - Trap effort: large grids using Ugglan traps; each session involved trapping at multiple sites over three days; animals marked with PIT tags.
  - Field data collected per capture: species identification, unique chip ID, capture date, sex, reproductive state, body mass, body length, and various fat scores.

- Biological samples and measurements
  - Blood sampling: up to 50 µL collected from tail and stored in RNAlater for RNA-based analyses.
  - Additional measurements: sex, reproductive status (various male/female states), scrotal status, pregnancy/lactation/perforation indicators, and general body condition indicators.
  - Parasitology and other measurements: recorded counts of mites, ticks, fleas, and anti-parasitic treatment data (e.g., Frontline, Profender).

- Data structure and recorded values
  - Primary dataset: long_blood_qpcr_FV.2.csv with fields such as:
    - Metadata: bloodNum, blood tube ID, site, dateCapt, session, gridTreat, trapsOut, trapsWorking, operator.
    - Capture info: timeGrid, timeOut, trap, species, chip, NRW, alive, age, sex, repro, scrotal, preg, perforate, lact, year.
    - Morphology and condition: bodyW (mass), bodyLen (length), pelvCond, dorsalCond, bodyCond.
    - Parasitic/vector data: miteLaela, miteListro, miteMyo, tick, flea; treatment details (treat, frontline dose, profender dose).
    - Molecular data: qPCR.plate1, plate2, plate.3 with gene targets (AR, CD8A, FOXP3, IL10, IL17, IL1B, IL4, INFG, ORAI1, and many others), plus relative concentrations for numerous immune-related genes.
    - Calibration and control: entryDate, calibrator references, MT (control) notes, comments, etc.

- Immunogenetics and laboratory methods
  - Target: immune-associated genes informed by known mouse immunology and prior vole studies.
  - RNA processing: RNA extracted from splenocytes preserved in RNAlater; DNase treatment; cDNA synthesis with RNA-to-cDNA kit.
  - qPCR platform and setup: SYBR Green chemistry on 384-well plates; robot-assisted pipetting; standard plate layouts ensuring matched triplets of animals across plates.
  - Endogenous controls: Ywhaz and Actb for normalization.
  - Plate design: three standard layouts containing fixed sets of target gene assays and endogenous controls; unknown samples run in duplicate; calibrator samples run in triplicate; no-template controls included per plate.
  - Dilution and calibration: cDNA diluted 1/20; main calibrator pool created from splenocyte cDNA; additional synthetic calibrator fragments used for low-representation genes (Tollip, IL1RAP, IRF2).
  - Expression quantification: relative expression values computed as RQ via the ∆∆Ct method using machine software; quality checks include melting curves and amplification plots for each well.

- Pathogen detection and validation
  - Pathogens measured: Babesia microti (18S) and Bartonella spp. (16S) by SYBR Green qPCR.
  - Validation: subset cross-validation with RNA-Seq pathogen reads from cross-sectional samples (n = 44); strong concordance observed (B. microti r^2 = 0.81; Bartonella spp. r^2 = 0.81; p < 0.001).

- Experimental design notes
  - Longitudinal component: repeated sampling of individuals to track immune expression and infection status over time.
  - Cross-sectional component: data from post-culling individuals to complement longitudinal findings.
  - Field, lab, and data management practices integrated to enable robust analyses of immunological profiles in a wild mammal population.

- Data quality, standardization, and reproducibility
  - Primer design and validation performed in-house with attention to specificity and PCR efficiency (target 100 ± 10%).
  - Use of consistent calibrators and plate layouts to minimize plate effects; replication strategy (duplicates for samples, triplicates for calibrators) supports reliability of expression measures.
  - Cross-method validation for pathogen data enhances confidence in infection status assignments.

- References to related work and data context
  - Jackson et al. 2011. The Analysis of Immunological Profiles in Wild Animals: A Case Study on Immunodynamics in the Field Vole, Microtus agrestis. Molecular Ecology.
  - Wanelik et al. 2019. IgE receptor polymorphism and inflammatory dynamics in wild rodents. bioRxiv.
  - Wanelik et al. 2021. Early-life immune expression profiles predict later health and fitness in a wild rodent. bioRxiv.

- Practical considerations for analysts
  - Data fusion: integration of field captures, morphometrics, parasitology, longitudinal sampling metadata, and lab-derived gene expression and pathogen data enables multifaceted analyses of immune function, infection dynamics, and host condition.
  - Scale and accessibility: complex, multi-source data with many derived variables; attention needed for data cleaning, standardization across plates, and careful interpretation of expression metrics.
  - Analytic opportunities: correlations among immune gene expression panels, host traits (sex, age, reproductive status), parasite burdens, and infection outcomes; predictive modeling of immune states or infection risk under environmental or experimental conditions.