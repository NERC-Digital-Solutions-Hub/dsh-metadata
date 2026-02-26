# Supporting Documentation
Effects of low-dose ionising radiation on reproduction and DNA damage in marine and freshwater amphipod crustaceans

- Aim and scope
  - Provide first assessments of the impacts of chronic radiation exposure on male fertility and DNA damage in aquatic invertebrates (amphipods).
  - Include both marine (Echinogammarus marinus) and freshwater (Gammarus pulex) species.
  - Examine multiple endpoints: sperm quality and quantity, DNA damage in sperm, and reproductive outcomes.

- Datasets included
  - Crustacean_Sperm_Data_NF.csv (marine Echinogammarus marinus)
    - Sperm quality and quantity across dose rates: 0, 0.1, 1, 10 mGy/d
    - Covariate: weight (mg)
    - Data from two exposures: Oct 2015 and Nov 2016
    - 148 individuals; seven columns: weight, experiment number, arc-sin transformed % sperm viable, dose rate, fourth root transformed sperm numbers, raw sperm numbers, raw sperm viability
  - Crustacean_Sperm_Data_Freshwater.csv (freshwater Gammarus pulex)
    - Sperm parameters across dose rates: 0, 0.1, 1, 10 mGy/d
    - Covariate: weight (mg)
    - Single exposure: Aug 2016
    - 63 individuals; six columns: weight, arc-sin transformed % sperm viable, dose rate, fourth root transformed sperm numbers, raw sperm numbers, raw sperm viability
  - Crustacean_DNA_Damage_Sperm_Data_NF.csv
    - DNA damage in E. marinus sperm after radiation (tail DNA %)
    - Dose rates: 0, 0.1, 1, 10 mGy/d
    - Two-column dataset: dose rate, % tail DNA
    - Analyzed with OpenComet software (v1.3)
  - Crustacean_Egg_Numbers_and_Breeding_Dates.csv
    - Reproductive outcomes after exposure: eggs produced, time to reproduction, % abnormal embryos, embryo diameters
    - Female weight included; mating with radiation-exposed males
    - Dose rate of male exposure; six columns: female weight (mg), eggs produced, time to reproduction after male addition, dose rate, % abnormal embryos, embryo diameter (µm)

- Methods and data collection
  - Radiation exposure
    - Phosphorus-32 beta radiation (ATP γ32P) applied to exposure media and organisms
    - Dose rates: 0, 0.1, 1, 10 mGy/d
    - Marine exposure: two-week duration; Oct 2015 and Nov 2016
    - Freshwater exposure: two-week duration; Aug 2016
  - Biological measurements
    - Sperm counts and viability using LIVE/DEAD sperm viability kit
    - Sperm visualization with fluorescence microscopy
    - DNA damage assessment via alkaline comet assay; OpenComet analysis
    - Embryo/egg measurements after pairing exposed males with unexposed females; blind analysis with random coding
  - Quality and provenance
    - Activity concentrations measured with HIDEX 300SL counter
    - Analyses performed and interpreted by Neil Fuller; support from Prof. Alex T. Ford
    - Funded under TREE project by NERC, Environment Agency, and Radioactive Waste Management

- Data structure and transformations
  - Sperm datasets
    - Columns include weight, experiment number, transformed sperm viability (arc-sin), dose rate, transformed sperm numbers (fourth root), raw sperm numbers, and raw sperm viability
  - DNA damage dataset
    - Dose rate and % tail DNA
  - Reproduction dataset
    - Female weight, eggs produced, time to reproduction, dose rate, % abnormal embryos, embryo diameter
  - Transformations noted to aid analysis
    - Arc-sin transformed percentages for sperm viability
    - Fourth root transformation for sperm numbers

- Purpose, context, and relevance
  - Establish baseline effects of environmentally relevant radiation levels on male fertility, DNA integrity, and reproductive success in aquatic amphipods
  - Provide datasets suitable for cross-study comparisons, modelling, and potential meta-analyses
  - Relevant to toxicology, radiobiology, and environmental risk assessment

- Data provenance and access
  - Data generated under TREE project; publicly documented with methodological details
  - Datasets accompanied by methodological descriptions, measurement techniques, and software used (OpenComet)
  - Metadata and study context prepared to support reuse and discoverability

- References
  - Gyori et al. OpenComet software for comet assay analysis
  - Lacaze et al. DNA damage assessment in freshwater amphipods
  - Sundelin & Eriksson embryo abnormalities in amphipods
  - Sundelin et al. use of embryo abnormalities for environmental stress assessment