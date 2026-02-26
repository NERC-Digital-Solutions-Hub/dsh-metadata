# Details of data structure to 'HF_NH3.csv'

- Overview
  - NH3 emissions dataset from a grassland fertiliser trial (2016) at Henfaes Research Station (Bangor University)
  - 7 columns, 476 rows
  - Data collected using wind tunnels to measure NH3 emissions for 3 weeks after fertiliser applications (daily sampling)
  - Treatments involve urea and inhibited urea (agrotain); applications: first two at 90 kg ha-1, third at 60 kg ha-1

- Dataset contents
  - Data source noted as a supplement to supporting documentation for CINAg experiments (final check v2.1)

- Column definitions and units
  - Time_Start: Date and time at start of sampling period
  - Time_End: Date and time at end of sampling period
  - N_app: 1|2|3 indicating fertiliser application number; first two applications at 90 kg ha-1, third at 60 kg ha-1
  - Plot: 1–16, the plot measured (plot size 2 × 4 m)
  - Block: 1–4, blocking factor of the randomised block design
  - Treatment: AN|U|IU, where AN = ammonium nitrate, U = urea, IU = inhibited urea (agrotain)
  - Emission_rate_kghad: emission rate of NH3 from plot for 1 day (kg NH3-N ha-1 d-1)

- Data quality and handling notes
  - Wind tunnel anemometers on plot 3 (during first and second fertiliser applications) and plot 14 (during the third application) failed
  - Failed anemometer values were replaced with the mean of surrounding wind tunnels
  - Limit of detection: 0.1 mg NH4-N L-1
  - Negative NH3 flux values were replaced with 0

- Usage context
  - Provides structured metadata for analysis and the creation of data products; supports data cleaning, alignment with study design, and subsequent exploration of NH3 emission patterns across plots, treatments, and application events