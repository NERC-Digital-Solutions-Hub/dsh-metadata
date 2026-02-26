# NW_N2O.csv data structure

- Overview
  - N2O emissions dataset from grassland fertiliser trial 2016 at North Wyke Research Station (Rothamsted Research)
  - 6 columns, 608 rows
  - N2O fluxes measured using manual static chambers

- Dataset details
  - Time: Date & time of N2O sampling
  - N_app: 1|2|3 denotes fertiliser application; 1st & 2nd applications of 90 kg N ha-1, 3rd application of 60 kg N ha-1
  - Block: 1|2|3|4 blocking factor of randomized block design
  - Plot: Experimental unit
  - Treatment: AN|IU|U|C representing N fertiliser type
    - AN = ammonium nitrate (Nitram)
    - U = urea
    - IU = inhibited urea (agrotain)
    - C = 0N Control
  - Flux_N2O: N2O flux for each chamber measurement; unit = g N2O-N ha-1 day-1

- Data quality and processing
  - Flux data with R^2 < 0.6 and all negative Flux_N2O values replaced with 0

- Context and provenance
  - Supplement to supporting documentation for CINAg experiments; linked to Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf
  - Data source: grassland fertiliser trial, 2016, North Wyke Research Station

- Usage notes for data support
  - Align analyses with randomized block design (Block) and treatment (N fertiliser type)
  - Use Time and N_app to track temporal fertiliser applications
  - Consider the R^2–based quality filter and the substitution of negative Flux_N2O values when interpreting results
  - Suitable for creating dashboards or reports to enable self-service exploration of N2O flux Dynamics across treatments and blocks