# Supporting Information for data deposit EIDCHELP-29311

- Project system and aim
  - Investigates combined effects of daily stochastic temperature fluctuations and resource degradation on a host–parasitoid model: Plodia interpunctella (host) and Venturia canescens (parasitoid).
  - Single-generation life history assay to characterise individual responses using lab stocks.

- Experimental design and treatments
  - Full factorial design with two factors:
    - Temperature treatment: Constant (Cst) vs Variable (Var); both target a mean of 26°C.
      - Var: temperature fluctuates daily between 22.3°C and 30.2°C (26°C ± 1.5°C SD; AR(1) = 0.02, 95% CI [-0.10, 0.14]).
      - CST: constant 26°C.
    - Resource degradation (diet): 0, 25, 50, 75% of wheat germ replaced by methyl cellulose (MC) as an indigestible bulking agent.
  - Timing and duration: experiment starts on day 5 of the temperature time series and lasts 74 days.

- Life history assays
  - Unparasitized hosts: 40 individuals per temperature×diet treatment; monitored daily at 0.3 g diet per host until death.
  - Parasitized hosts: 25 hosts per treatment; parasitism occurs over three days (days 20–22) from groups of 100 eggs; then each host is kept at 0.3 g diet and monitored until death.
  - Parasitism process involves a parasitoid from a laboratory parthenogenetic stock; most suitable host instars used for development.

- Datasets included
  - VariableTemperatureTimeSeries_DQE.csv
    - Variables: DAY (day in temperature time series), Date, Week, Temp (°C).
  - LHE-LH-Data_DQE_Pi.csv (unparasitized hosts)
    - Key fields: Treatment, Individual, Individual code, Diet, Temperature, Starting_Date, Egg_viability, Egg_status, Hatching date, Adult_emergence-date, Date_of_death, Sex, Egg_length, Leg_length, Date_leg_photo_taken, leg_measured, comments.
    - Records life history traits for unparasitized hosts across treatments.
  - LHE-LH-Data_DQE_PiVc.csv (parasitized hosts)
    - Key fields: Treatment, Diet, Temperature, Individual, Individual code, Starting_Date, Vc_mother_ID, Vc_mother_stock_origin, Vc_mother_age, Pi_larval_stage_at_parasitism, Pi_larvae_mass_at_parasitism, Pi_sex, Time_at_parasitism, Adult_emergence_date, Parasitism_outcome, Date_of_death, Date_photo_taken, Leg_measured, Leg_length, Parasitism_observer, comments.
    - Records outcomes for host and parasitoid after parasitism (e.g., Live Pi, Live Vc, Pi-Vc death before emergence, or NA).

- Data detail and measurement methods
  - Measurements collected daily during life history assays, including viability, development milestones, mortality, sex, and body size proxies.
  - Body size proxies:
    - Host: leg_length (mid-femur length) measured from leg photos; date of photo and left/right leg specified.
    - Parasitoid: hind-tibia length measured for body size proxy; date of photo and left/right leg specified.
  - Data capture equipment:
    - Nikon DS-5M camera and Nikon SMZ1500 microscope; measurements via NIS-element Dv2.3 software; precision to 0.001 mm (legs).
  - Parasitism metadata:
    - Vc_mother_ID, stock origin, and age recorded to document parasitoid source and conditions.
  - Additional notes:
    - Each treatment’s dataset includes a markers field (e.g., Treatment, Diet, Temperature) to align life history data with environmental treatments.
    - Comments field available for any relevant observations during daily monitoring.

- Quality control
  - Data entry checked for errors; outliers rechecked in initial analysis stage.

- References informing design
  - Boots (2011) on resource effects on parasite resistance.
  - Cameron et al. (2007) on resource and competition dynamics.
  - Harvey, Harvey & Thompson (1994) on flexible larval growth across host sizes.

- Governance and documentation notes
  - Data are organized into clearly labeled CSV datasets with metadata fields described above to aid discoverability and reuse.
  - The deposit follows a structured approach suitable for data sharing and cataloging within research data portals.