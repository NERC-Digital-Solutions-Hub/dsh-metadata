# Telomere heritability and parental age at conception effects in a wild avian population

- Overview
  - Describes data collection, processing, and quality control for relative telomere length (RTL) measurements in Seychelles warbler, with RTL measured by qPCR and linked to individual life-history and parental data.
  - Data sources span long-term fieldwork on Cousin Island, monitoring since 1985 and blood sampling since 1990; RTL dataset uses birds caught and blood-sampled between 1995 and 2014 (most complete data).

- Collection/generation of data
  - Blood samples collected (~25 μl) since 1990 and stored in absolute ethanol; RTL dataset incorporates samples from 1995–2014.
  - RTL measured via quantitative PCR (qPCR) using standard protocols; DNA integrity and purity checked prior to analysis.
  - Sample handling includes random assignment of samples to qPCR plates to avoid bias related to age, sex, cohort, or environment.

- Nature and units of recorded values
  - Primary measurement: relative telomere length (RTL).
  - Data structured to capture individual identifiers, demographic details, and technical metadata:
    - BirdID, Sex (0=female, 1=male), AgeY, AgeClass, BirthFPID, U_PlateID, RTL, Technician, Terr, FPID, mum, dad, MAC (maternal age at conception), PAC (paternal age at conception), BrF, BrM.

- Quality control (QC)
  - Within-plate repeatability: GAPDH cq = 0.74; telomere cq = 0.73.
  - Between-plate repeatability (RTL, at least twice per sample across plates): 0.68.
  - Storage time effects on RTL: none detected.
  - Sample cleaning and inclusion criteria (based on Spurgin et al. 2018) prior to analysis:
    - DNA concentration ≥ 15 ng/μl (mean of three measurements).
    - 260/280 ratio between 1.8 and 2.0.
    - 260/230 ratio > 1.8.
    - DNA integrity validated by agarose gel; degraded samples re-extracted or excluded.
    - Samples randomly assigned to plates; outliers excluded (e.g., cq > 25 for telomere or >26 for GAPDH; RTL values ≥ 3 excluded).
  - Final cleaned dataset: 2,664 samples from 1,318 individuals passed QC and filtering.

- Data structure and formatting
  - Data include measurements and metadata necessary for analyses and replication:
    - Includes fieldwork period details (BirthFPID, FPID), plate information (U_PlateID), and family pedigree (mum, dad) to enable analyses of heritability and parental effects.
  - Use of random effects (e.g., qPCR plate) in analyses to account for technical variation.

- Experimental design and sampling regime
  - Major breeding season runs June–September; some birds breed in the minor season (January–March).
  - Field methodology involves catching as many birds as possible during the breeding season using mist nets, enabling broad sampling across individuals and cohorts.

- Fieldwork and laboratory instrumentation
  - DNA extraction conducted with DNeasy Blood & Tissue Kit (Qiagen); overnight lysis at 37°C; final elution volume 80 μL.
  - DNA integrity checked by 1.2% agarose gel; DNA concentration quantified with NanoDrop 8000.
  - Telomere measurement performed via qPCR with random plate assignment to minimize systematic bias.

- Notes on data provenance and references
  - Methodological details and QC thresholds draw on multiple studies:
    - Sparks et al. (2021) for RTL heritability and parental effects.
    - Spurgin et al. (2018) for spatio-temporal telomere dynamics and quality thresholds.
    - Bebbington et al. (2016) for DNA extraction and initial RTL associations.
  - Data are presented with explicit thresholds and quality checks to enable reproducible analyses and cross-study comparisons.