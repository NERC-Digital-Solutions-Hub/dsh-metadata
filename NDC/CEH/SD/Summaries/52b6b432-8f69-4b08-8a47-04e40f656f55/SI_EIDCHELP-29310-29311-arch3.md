# Supporting Information for data deposit EIDCHELP-29311

- Overview
  - Experimental study of the combined effects of daily stochastic temperature fluctuations and resource degradation on a host–parasitoid system (Plodia interpunctella and Venturia canescens).
  - One-generation life history assay using laboratory hosts and a parthenogenetic parasitoid strain to characterize individual responses.
  - Data designed to inform understanding of environmental health under climate variability and resource quality, with detailed trait measurements and temporal temperature data.

- Experimental design
  - Full factorial design with:
    - Temperature treatments: Constant (Cst) vs Variable (Var) around a mean of 26°C (Var ranges 22.3–30.2°C daily; AR(1) = 0.02).
    - Resource degradation treatments: 0, 25, 50, 75% of wheat germ replaced by methyl cellulose (MC).
  - Life history assay timeline:
    - Initiated on day 5 of the temperature time series and lasted 74 days.
    - 40 unparasitized hosts and 25 parasitized hosts per temperature–diet treatment.

- Data deposits and file contents
  - VariableTemperatureTimeSeries_DQE.csv
    - Fields: DAY, Date, Week, Temp
    - Captures daily temperature time series per treatment; Week 0 corresponds to pupae, Week 1 to adults.
  - LHE-LH-Data_DQE_Pi.csv (unparasitized hosts)
    - Fields include: Treatment, Individual, Diet, Temperature, Starting_Date, Egg_viability, Egg_status, Hatching date, Adult_emergence-date, Date_of_death, Sex, Egg_length, Leg_length, Date_leg_photo_taken, Leg_measured, comments
    - Records survival and life-history traits, plus body-size proxies (leg length, egg length) and measurement metadata.
  - LHE-LH-Data_DQE_PiVc.csv (parasitized hosts)
    - Fields include: Treatment, Diet, Temperature, Individual, Starting_Date, Vc_mother_ID, Vc_mother_stock_origin, Vc_mother_age, Pi_larval_stage_at_parasitism, Pi_larvae_mass_at_parasitism, Pi_sex, Time_at_parasitism, Adult_emergence_date, Parasitism_outcome, Date_of_death, Date_photo_taken, Leg_length, Leg_measured, Parasitism_observer, comments
    - Captures parasitism events and outcomes, parasitoid development, host and parasitoid body-size proxies, and observer information.

- Measurements and metadata
  - Biological traits recorded for hosts (unparasitized and parasitized): viability and success of eggs, hatching, emergence, survival, sex, body size proxies (leg length, egg length), and timing of key life-history events.
  - Parasitoid data include maternal stock details, larval stage at parasitism, parasitoid body size proxy (leg length), parasitism timing, and outcome categories (Live Pi, Live Vc, Pi-Vc death before emergence, or NA).
  - Measurement methods: leg lengths measured from photos using a Nikon microscope and specialized software; dates of measurements recorded for traceability.

- Quality control and data provenance
  - Data were checked for entry errors; outliers rechecked during initial analysis.
  - Comprehensive metadata accompany each dataset, including dates, measurement methods, and observational notes.
  - References cited for the experimental design and diet-resource context.

- Relevance for environmental health monitoring
  - Provides a structured example of capturing organismal responses to climate variability and resource quality, suitable for informing monitoring frameworks.
  - Demonstrates the importance of clear variable definitions (Treatment, Diet, Temperature), standardized measurement protocols, and linkage of time-series environmental context (temperature) to biological responses.
  - Highlights data governance aspects: data provenance, metadata completeness, and the need to publicly share underlying datasets to enable replication and policy-relevant analysis.

- References
  - Boots, M. 2011. The evolution of resistance to a parasite is determined by resources. American Naturalist.
  - Cameron, T.C. et al. 2007. Two-species asymmetric competition: effects of age structure on intra- and interspecific interactions. Journal of Animal Ecology.
  - Harvey, J.A. et al. 1994. Flexible larval growth allows use of a range of host sizes by a parasitoid wasp. Ecology.