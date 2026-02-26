# Details of data structure to 'NW_N2O.csv'

- Overview
  - Supplement to the supporting documentation for data series described in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf
  - Presents the N2O emissions dataset NW_N2O.csv: 6 columns, 608 rows
  - Data originate from a grassland fertiliser trial (2016) at North Wyke Research Station (Rothamsted Research)
  - N2O fluxes measured using manual static chambers

- Dataset composition
  - 6 columns, 608 rows
  - Flux_N2O values represent N2O fluxes per chamber measurement
  - Data capture focuses on fertiliser treatments and application timing

- Variables and definitions
  - Time: Date and time of N2O sampling
  - N_app: Fertiliser application number (1, 2, or 3)
    - 1st and 2nd applications: 90 kg N ha-1
    - 3rd application: 60 kg N ha-1
  - Block: Blocking factor in the randomised block design (1–4)
  - Plot: Experimental unit
  - Treatment: N fertiliser type
    - AN = ammonium nitrate (Nitram)
    - IU = inhibited urea (agrotain)
    - U = urea
    - C = 0N Control
  - Flux_N2O: N2O flux for each chamber measurement
    - Units: g N2O-N ha-1 day-1

- Data quality and cleaning
  - Flux_N2O values with R^2 < 0.6 are flagged
  - All negative Flux_N2O values are replaced with 0

- Measurement method and design context
  - N2O fluxes measured with manual static chambers
  - Experimental design implemented as a randomised block design across blocks and plots
  - Data structured to support comparisons of fertiliser types, application timing, and their effects on N2O emissions

- Provenance and usage context
  - Part of CINAg experiments
  - Linked to supporting documentation (Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf)
  - Suitable for analyses to identify correlations, develop predictive models, and quantify the impact of fertiliser treatments on N2O emissions

- Analytical opportunities for data analysts
  - Examine relationships between N_app, Treatment, Block, Plot, and Flux_N2O
  - Compare N2O flux responses across fertiliser types and application events
  - Develop predictive models of N2O flux as a function of time, treatment, and blocking factors
  - Validate findings against other related data series within the CINAg framework