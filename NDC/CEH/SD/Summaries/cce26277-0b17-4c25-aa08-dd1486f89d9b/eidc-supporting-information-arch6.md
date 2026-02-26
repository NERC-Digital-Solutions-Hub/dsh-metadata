# Hydraulic mobility of aquatic insect (Trichoptera) bioconstructions and incorporated sediments

- Purpose and scope
  - Quantify how caddisfly case construction influences sediment transport in rivers using a hydraulic flume.
  - Compare three case types: two tubular-case species (Potamophylax latipennis; Sericostoma personatum) and one domed-case species (Agapetus fuscipes).
  - Assess sediment transport by examining (i) empty cases vs (ii) individual sediment particles after case disaggregation.
  - Generate data products to enable analysis of bed shear stress thresholds and sediment entrainment for different case morphologies.

- Experimental design and timeline
  - Flume setup: cases and sediment placed in the center; hydraulic discharge increased through 11 steps.
  - Measurements: sediment eroded at each flow stage inferred from photographic analysis.
  - Sampling and collection: caddisfly specimens collected on 17 June and 18 August 2019; experiments conducted 20 Aug–20 Sep 2019.
  - Authors: Mason led collection and data interpretation with co-authors.

- Data files and their contents
  - S1_Velocimetry_data
    - Post-processed acoustic Doppler velocimetry outputs for each discharge step.
    - Recorded metrics per step: mean and standard deviation of velocity components (U, V, W); quality indicators (Signal-to-Noise Ratio, correlation); derived values (turbulent kinetic energy, bed shear stress Tb).
    - Key variables (examples): Date, Discharge_step (1–11), Umean_raw, Ustd_raw, Umean, Ustd, Vmean_raw, Vstd_raw, Vmean, Vstd, Wmean_raw, Wstd_raw, Wmean, Wstd, U_corr, U_SNR, V_corr, V_SNR, W_corr, W_SNR, TKE, Tb.
  - S2_Case-grain-size-distribution_data
    - Grain size distributions for each caddisfly case obtained by sieving.
    - Data per case: mass before sieving, mass after sieving, mass lost, loss percentage; sieve size corresponding to the smallest passing sieve; sediment masses in grams.
    - Key variables: Sample_ID (L = Potamophylax latipennis, S = Sericostoma personatum, G = Agapetus fuscipes), Sed_mass, Sieved_mass, Loss_mass, Loss_percent, Sieve_size.
  - S3_Entrainment_data
    - Percentage of sediment entrained at each flow stage, derived from photographic analysis of sediment remaining on the measurement platform.
    - Key variables: Sample_ID, State (Case or loose sediment), Discharge_step (1–11), Values (cumulative % area transported).
  - S4_Case-and-entrainment-threshold_data
    - Case characteristics (mass, axes) and entrainment thresholds; includes critical and general movement thresholds.
    - Key variables: Case/Sediment ID, State, Mass, a (long axis), b_D50 (intermediate axis or D50 for loose sediment), c (short axis), E_10 (bed shear stress critical entrainment threshold), E_90 (bed shear stress threshold for 90% movement).

- Data quality and usage notes
  - Data span from mid-2019 collection to late-2019 analysis; supports cross-comparison of case morphologies under varying flow regimes.
  - Variables provide both raw and post-processed values (e.g., velocities, TB) to facilitate quality checks and reproducible analyses.
  - Enables calculation of entrainment and movement thresholds as a function of case geometry and sediment type, supporting broader investigations into hydraulic mobility of bioconstructions.