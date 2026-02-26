# Telomere heritability and parental age at conception effects in a wild avian population

- Purpose: Describe the data and methods behind a long-term study of relative telomere length (RTL) in the Seychelles warbler, including collection, processing, quality control, and data structure to support analyses of heritability and parental age effects.

## Collection and generation methods
- Study system: Seychelles warbler population on Cousin island (approx. 320 adults in 115 territories), monitored intensively since 1985.
- Sampling period: Birds caught and blood-sampled between 1995 and 2014; fieldwork data linked to major (Jun–Sep) and minor (Jan–Mar) breeding seasons.
- Sample preparation: Blood (~25 μl) stored in absolute ethanol at room temperature; DNA integrity checked before qPCR.
- Telomere measurement: Relative telomere length (RTL) estimated by qPCR (telomere and GAPDH assays); DNA integrity verified via gel electrophoresis; samples with degraded DNA excluded or re-extracted.
- Data cleaning thresholds (Spurgin et al. 2018): DNA concentration ≥15 ng/μl; 260/280 between 1.8–2.0; 260/230 > 1.8; RTL values ≥ 3; outliers with extreme cq values (>25 for telomere, >26 for GAPDH) excluded.
- Randomization: Samples assigned to qPCR plates by randomization to avoid biases related to age, sex, cohort, or environment.
- Handling of replicates: RTL values based on measurements with plate as a source of technical variation; samples with replicates across plates used to assess plate variance.

## Nature and units of recorded values
- RTL: Relative telomere length (primary quantitative outcome).

## Data structure and key variables
- BirdID: Unique identifier for each bird.
- Sex: 0 = female, 1 = male.
- AgeY: Age at capture (years).
- AgeClass: Categorical age class (e.g., A = adult, CH = chick, FL = fledgling, J = juvenile, OFL = old fledgling, SA = subadult).
- BirthFPID: Fieldwork period ID at birth.
- U_PlateID: qPCR plate ID for RTL measurements.
- RTL: Relative telomere length.
- Technician: Technician performing the qPCR (two levels).
- Terr: Territory identifier during capture.
- FPID: Fieldwork period ID of capture.
- mum/dad: Pedigree parental IDs.
- MAC/PAC: Maternal and paternal age at conception (years).
- BrF/BrM: Dominant female and male in natal territory.

## Experimental design and sampling regime
- Breeding seasons: Major (June–September) with additional minor season (January–March) in some years.
- Catching strategy: As many birds as possible captured each breeding season using mist nets; longitudinal sampling across multiple years and individuals.

## Fieldwork and laboratory instrumentation
- DNA extraction: DNeasy blood and tissue kit; overnight lysis at 37 °C; final elution of 80 μl.
- DNA quality checks: Gel electrophoresis for DNA integrity; NanoDrop 8000 for concentration quantification.
- DNA preparation for qPCR: Samples diluted to 3.3 ng/μl prior to telomere measurement.
- Quality controls: Random assignment to plates; verification that no systematic bias related to age, sex, cohort, or environment occurs.

## Quality control and data filtering details
- Within-plate repeatability: ~0.74 for GAPDH and ~0.73 for telomere cq values (see Sparks et al., 2021; Spurgin et al., 2018).
- Between-plate repeatability: RTL ~0.68 across samples measured at least twice on different plates.
- Data cleaning: Exclusion criteria applied prior to analysis (e.g., DNA quality thresholds, RTL ≥ 3, cq-based exclusions).
- Plate-based variation: Plate treated as a random effect in analyses to account for technical variance; some samples had replicates across plates (n = 388).

## Data provenance and references
- Primary data handling and QC methods detailed in Sparks et al. (2021) and Spurgin et al. (2018); related laboratory methods described in Bebbington et al. (2016).
- Key cited works provide the background on telomere measurement, sample processing, and quality thresholds used to curate the dataset.

## Data scope and availability notes for data leaders
- Final cleaned dataset: 2,664 RTL samples from 1,318 individuals.
- Longitudinal framing: Data include repeated measures and longitudinal context via plate and replicate information to enable robust assessment of technical vs. biological variation.
- Metadata richness: Comprehensive sample and pedigree metadata (sex, age, parental ages, territory, field period, etc.) supports diverse analyses of heritability, parental effects, and ecological correlates.
- Governance signals: Randomization, explicit QC thresholds, and plate-level random effects demonstrate strong data governance and reproducibility practices.