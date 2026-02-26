# Details of data structure to ' Digestate_HF_and_NW_N_concentration.csv '

- Overview
  - Supplement to supporting documentation for data series; details the structure of the Digestate_HF_and_NW_N_concentration.csv dataset.
  - 7 columns, 90 rows of data from a 2017 digestate wheat trial conducted at Henfaes Research Center (HF) and North Wyke (NW) research stations.
  - Measurements are nitrogen (N) concentrations in winter wheat components (grain, chaff, straw) at harvest across multiple treatments and N-application rates.

- Dataset scope and origin
  - Trials located at HF and NW with contributions from Bangor University and Rothamsted Research.
  - Treatments include zero N control and various digestate-based amendments, with and without nitrification inhibition.
  - N concentrations measured in grain (and chaff for HF; not measured for NW) and straw.

- Columns and layout (7 columns)
  - Site: HF or NW.
  - Plot: plot number from which yield measurements were derived (with exceptions noted for monthly sampling).
  - Block: blocking factor of the randomized block design (1–5).
  - Treatment: C (control), D (digestate), AD (acidified digestate), DNI (digestate with DMPP), ADNI (acidified digestate with DMPP), N-75, N-150, N-225, N-300 (NH4NO3 application rates).
  - Grain_concentration_g_N_kg: concentration of N in grain at harvest (g N per kg).
  - Chaff_concentration_g_N_kg: concentration of N in chaff at harvest (g N per kg; Not Assessed for NW).
  - Straw_concentration_g_N_kg: concentration of N in straw at harvest (g N per kg).

- Measurements and units
  - Concentrations given in grams of N per kilogram of plant tissue (g N kg-1).
  - Grain data available for HF and, where applicable, NW data for grain is implied; chaff data absent for NW.

- Treatments and nitrogen rates
  - C = zero N control.
  - D = digestate; AD = acidified digestate; DNI = digestate with nitrification inhibitor (DMPP); ADNI = acidified digestate with nitrification inhibitor (DMPP).
  - N-75, N-150, N-225, N-300 correspond to NH4NO3 applications at 75, 150, 225, and 300 kg N ha-1, respectively.

- Site and plot details
  - Plot sizes differ by site:
    - HF: plots 1.2 m x 6.5 m (harvest area) for nitrogen addition rates; possibly larger for some treatments.
    - NW: plots 1.2 m x 14 m (harvest area) for nitrogen addition rates; separate dimensions for certain treatments.
  - Specific notes: plots 1, 19, 25, 31, and 47 at HF were used for monthly samplings for the 150 kg N ha-1 treatment.

- Data quality and caveats
  - NA indicates Not Assessed where data are unavailable.
  - Chaff N concentration not measured for NW.
  - The document provides the data structure and metadata to support data discoverability, provenance, and reuse within broader data-management and data-cataloging efforts.