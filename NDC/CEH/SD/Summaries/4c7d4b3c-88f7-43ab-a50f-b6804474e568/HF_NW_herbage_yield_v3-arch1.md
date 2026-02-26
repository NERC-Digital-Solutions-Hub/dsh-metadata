# Details of data structure to ' HF_NW_herbage_yield.csv '

- Dataset scope
  - 7 columns and 96 rows
  - Grassland herbage yield data from 2016 fertiliser trials
  - Sites: Henfaes Research Station (HF) and North Wyke Research Station (NW) of the referenced institutions
  - Purpose: supplementary to the supporting documentation for CINAg experiments

- Columns and coding
  - Date: Date of grass cut
  - Site: HF or NW (location of the trial)
  - N_app: Fertiliser application level
    - 1, 2, or 3
    - 1st & 2nd applications: 90 kg ha-1
    - 3rd application: 60 kg ha-1
  - Block: Blocking factor (1, 2, 3, or 4) in the randomised block design
  - Plot: Plot identifier (1–16)
  - Treatment: Nitrogen fertiliser type
    - AN = ammonium nitrate
    - U = urea
    - IU = inhibited urea (agrotain)
    - C = 0N control
  - Dry_tonnes_ha: Grass yield on a dry weight basis (tonnes per hectare)

- Experimental context
  - Data derived from grassland fertiliser trials conducted in 2016 at HF and NW research stations
  - Structured as a randomised block design to enable comparison across treatments and application rates

- Data provenance and structure notes
  - This file forms part of the data structure documentation referenced by Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf
  - Clear units and coded categories support reproducible analysis and modelling

- Potential uses for analysis
  - Comparing yield responses across fertiliser types (AN, U, IU) and the 0N control
  - Assessing the effect of different N application rates (N_app levels)
  - Modelling yield while accounting for block effects and site differences
  - Preparing data for reporting, visualization, or predictive modelling of fertiliser responses in grassland systems