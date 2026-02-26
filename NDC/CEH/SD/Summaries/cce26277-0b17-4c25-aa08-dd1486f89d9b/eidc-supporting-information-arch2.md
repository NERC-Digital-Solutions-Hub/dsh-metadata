# Hydraulic mobility of aquatic insect (Trichoptera) bioconstructions and incorporated sediments

## Purpose and scope
- Quantify how caddisfly case construction affects sediment transport in rivers using a hydraulic flume study.
- Compare three caddisfly species with different case styles: two tubular cases (Potamophylax latipennis and Sericostoma personatum) and one domed case (Agapetus fuscipes).
- Determine bed shear stress required to transport (1) empty cases and (2) sediment after disaggregation from cases.

## Experimental design and timeline
- Centered placement of cases and sediment in the flume; hydraulic force increased across 11 discharge steps.
- Sediment erosion measured from photographs taken at each stage.
- Flume experiments conducted 20 August–20 September 2019.
- Caddisflies collected 17 June and 18 August 2019.
- Richard Mason led data collection and interpretation with assistance from co-authors.

## Data files and structure

- S1_Velocimetry_data
  - Post-processed acoustic Doppler velocimetry data for each discharge step.
  - Includes mean and standard deviation of velocity in three directions (U, V, W), data quality metrics (Signal to Noise Ratio and correlation), turbulent kinetic energy (TKE), and bed shear stress (Tb).
  - Key variables: Date, Discharge_step, Umean_raw/Ustd_raw/Umean/Ustd, Vmean_raw/Vstd_raw/Vmean/Vstd, Wmean_raw/Wstd_raw/Wmean/Wstd, U_corr, U_SNR, V_corr, V_SNR, W_corr, W_SNR, TKE, Tb.

- S2_Case-grain-size-distribution_data
  - Grain size distributions for each caddisfly case obtained by sieving case sediment.
  - Variables: Sample_ID (G/S/L for Agapetus fuscipes / Sericostoma personatum / Potamophylax latipennis, with individual number), Sed_mass, Sieved_mass, Loss_mass, Loss_percent; sieve size references; sediment masses in grams.

- S3_Entrainment_data
  - Percentage of sediment entrained during each flow stage (1–11) measured via photography of sediment remaining on the platform.
  - Variables: Sample_ID, State (Case or loose sediment), Discharge_step, Values (cumulative % area transported).

- S4_Case-and-entrainment-threshold_data
  - Case characteristics (mass, axes a, b, c) and entrainment thresholds (E_10 and E_90) with general movement data.
  - Variables: Case/Sediment ID, State, Mass, a (long axis), b_D50 (intermediate axis / D50 of sediment), c (short axis), E_10 (bed shear stress threshold for initial entrainment), E_90 (bed shear stress threshold for 90% sediment transport).

## Data quality, processing, and interpretation
- Post-processed velocity fields include corrected mean velocities and standard deviations, along with quality indicators (correlation, SNR) and derived metrics (TKE, bed shear stress).
- Case-sediment size data include mass balance (losses during sieving) to ensure accurate grain-size distributions.
- Entrainment data capture sediment mobility across flow stages, enabling assessment of transport thresholds.
- Case and threshold data summarize physical properties essential for linking case morphology to hydraulic stability and movement.

## Relevance for environmental monitoring and policy
- The dataset uses standardized, auditable measurements (velocimetry, grain-size analysis, entrainment thresholds) suitable for temporal comparisons and cross-site synthesis.
- Outputs align with common monitoring products (reports, maps, charts) to visualize how bioconstructions influence sediment dynamics under varying hydrodynamic conditions.
- Data management practices imply storage and potential portal upload, supporting transparency and reuse in environmental health assessments and policy evaluation.

## Opportunities for data integration and reuse
- Increasing value by combining these hydraulic and sediment-transport measurements with broader riverine data (flow regimes, sediment supply, ecological metrics).
- Potential to enable broader access to underlying data to support comparative analyses, meta-analyses, and policy performance monitoring across multiple sites or time periods.