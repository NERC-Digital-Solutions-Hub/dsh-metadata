# Supporting Information for data deposit EIDCHELP-29311

- Aim of the study
  - Investigate the combined effects of daily stochastic temperature fluctuations and resource degradation on a Plodia interpunctella – Venturia canescens host–parasitoid system.
  - Generate individual life-history data to identify patterns and potential predictions about responses under different environmental conditions.

- Experimental design and treatments
  - Life history assay conducted over a single generation to characterize individual responses.
  - Subjects: hosts from laboratory stock cultures; parasitoids from a parthenogenetic thelytokous laboratory strain.
  - Rearing conditions prior to experiments: constant 28°C, 16:8 h light cycle.
  - Temperature treatments
    - Constant temperature (Cst) with mean 26°C.
    - Variable temperature (Var) with daily fluctuations around 26°C (22.3–30.2°C), mean 26°C ± 1.5°C SD; AR(1) = 0.02 (95% CI [-0.10, 0.14]).
  - Resource degradation (diet) treatments
    - Four levels: 0, 25, 50, 75% of wheat germ replaced by methyl cellulose (indigestible bulking agent).
  - Design: full factorial crossing of Temperature (Cst, Var) and Diet (0, 25, 50, 75).
  - Timeline: life history assay started on day 5 of the temperature time series and lasted 74 days.

- Experimental subjects and data collection
  - Unparasitized hosts (Pi)
    - 40 unparasitized host larvae per temperature × diet treatment.
    - Individual tracking: each host egg kept separately under its assigned temperature and diet, monitored daily for various traits.
    - Data file: LHE-LH-Data_DQE_Pi.csv.
  - Parasitized hosts (Pi with Venturia canescens)
    - 25 parasitized hosts per temperature × diet treatment (groups of 100 eggs per day parasitized across three days; parasitized on days 8–9 of larval stage).
    - Parasitized larvae monitored individually after parasitism.
    - Data file: LHE-LH-Data_DQE_PiVc.csv.

- Datasets and key variables
  - dataset VariableTemperatureTimeSeries_DQE.csv
    - DAY, Date, Week, Temp (temperature in °C) describing the temperature time series per treatment.
  - dataset LHE-LH-Data_DQE_Pi.csv (unparasitized hosts)
    - Treatment, Individual, Diet, Temperature, Starting_Date, Egg_viability, Egg_status, Hatching date, Adult_emergence-date, Date_of_death, Sex, Egg_length, Leg_length, Date_leg_photo_taken, leg_measured, comments.
    - Additional notes on life-history measures (e.g., egg viability, hatching outcomes, growth timing, body size proxies).
  - dataset LHE-LH-Data_DQE_PiVc.csv (parasitized hosts)
    - Treatment, Diet, Temperature, Individual, Starting_Date, Vc_mother_ID, Vc_mother_stock_origin, Vc_mother_age, Pi_larval_stage_at_parasitism, Pi_larvae_mass_at_parasitism, Pi_sex, Time_at_parasitism, Adult_emergence_date, Parasitism_outcome, Date_of_death, Date_photo_taken, Leg_length, Leg_measured, Parasitism_observer, comments.
    - Includes parasitism-specific outcomes (e.g., Live Pi, Live Vc, Pi-Vc death before emergence) and size proxies for parasitoids (hind-tibia length).

- Measurements and methods
  - Life-history traits recorded daily for each individual.
  - Body size proxies
    - Host body size: Leg_length (mid-femur length) measured on the day of the experiment start.
    - Parasitoid body size: Leg_length of parasitoids measured from hind-tibia length.
  - Measurement apparatus: Nikon DS-5M camera and Nikon SMZ1500 microscope with NIS-element Dv2.3 software; leg photos recorded with date and leg side (Right/Left).

- Quality control and data management
  - Data entered with error checks; outliers rechecked during initial data analysis.
  - Datasets include metadata on treatments, dates, and observer information to support traceability and reproducibility.

- References
  - Boots, M. (2011). The evolution of resistance to a parasite is determined by resources. American Naturalist, 178, 214-220.
  - Cameron, T.C., Wearing, H.J., Rohani, P. & Sait, S.M. (2007). Two-species asymmetric competition: effects of age structure on intra- and interspecific interactions. Journal of Animal Ecology, 76, 83-93.
  - Harvey, J.A., Harvey, I.F. & Thompson, D.J. (1994). Flexible larval growth allows use of a range of host sizes by a parasitoid wasp. Ecology, 75, 1420-1428.