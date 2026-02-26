# Hydraulic mobility of aquatic insect (Trichoptera) bioconstructions and incorporated sediments

## Objective
- Quantify how caddisfly case construction affects sediment transport in rivers.
- Compare bed shear stress required to move (1) empty caddisfly cases and (2) sediment after disaggregation.
- Examine three species with two tubular case styles and one domed case; assess differences in hydraulic mobility across cases and incorporated sediments.

## Experimental design and timeline
- Hydraulic flume experiments with cases placed at the center; hydraulic forcing increased over 11 discharge steps.
- Sediment erosion quantified from photographs at each flow stage.
- Species and cases:
  - Tubular cases: Potamophylax latipennis and Sericostoma personatum
  - Domed case: Agapetus fuscipes
- Field/lab timeline:
  - Data collected August 20 – September 20, 2019
  - Caddisfly specimens collected on June 17 and August 18, 2019
- Data collection led by Richard Mason with co-authors.

## Data assets and contents

### S1_Velocimetry_data
- Post-processed acoustic Doppler velocimetry outputs for each discharge step.
- Includes: mean and standard deviation of velocities (U, V, W), data quality metrics (Signal-to-Noise Ratio, correlation), turbulent kinetic energy (TKE), and bed shear stress (Tb).
- Variables (examples):
  - Date, Discharge_step (1–11)
  - Umean_raw, Ustd_raw, Umean, Ustd
  - Vmean_raw, Vstd_raw, Vmean, Vstd
  - Wmean_raw, Wstd_raw, Wmean, Wstd
  - U_corr, U_SNR, V_corr, V_SNR, W_corr, W_SNR
  - TKE, Tb

### S2_Case-grain-size-distribution_data
- Grain size distributions for each caddisfly case obtained by sieving case sediment.
- Variables per sample: Sample_ID (G, S, L + individual number), Sed_mass, Sieved_mass, Loss_mass, Loss_percent.
- Sieve-related details: smallest sieve size passed (mm); sediment masses in grams.

### S3_Entrainment_data
- Percentage of sediment entrained during each flow stage.
- Measured as cumulative percent area of sediment transported from photography.
- Variables: Sample_ID, State (Case or loose sediment), Discharge_step (1–11), Values (cumulative % area entrained).

### S4_Case-and-entrainment-threshold_data
- Case characteristics, thresholds, and movement data.
- Variables:
  - Case/Sediment ID, State (Case or loose sediment)
  - Mass (g), a (long axis, mm), b_D50 (intermediate axis, mm), c (short axis, mm)
  - E_10 (bed shear stress threshold for critical entrainment), E_90 (threshold for general movement)
- Note: E axes provide a priori estimates of mobility thresholds for cases and loose sediment.

## Data quality, processing, and metadata
- Velocimetry data include post-processed values with explicit raw vs. adjusted velocities, and data quality indicators (SNR, correlation) to support reliability assessments.
- Variables and units are clearly defined, supporting reproducibility and metadata discoverability.
- Multiple complementary datasets (velocities, grain-size distributions, entrainment percentages, and physical thresholds) enable integrated analysis of hydraulic forcing and sediment mobilization.

## Provenance and publication context
- Data originate from a controlled flume study investigating the interaction of caddisfly bioconstructions with sediment transport.
- Primary contributors: Mason, Rice, Johnson, Wood, and Vettori.
- Data capture and interpretation built around a coherent set of S1–S4 files, with explicit dates of collection and experiment.

## Potential uses for Data Leaders
- Assessing data strategy around ecological hydraulics: integrating biological constructions with physical transport data.
- Evaluating data completeness, metadata definitions, and variable provenance for cross-domain reuse.
- Informing data governance on multidisciplinary environmental datasets (measurement methods, post-processing, and thresholds).
- Enabling reproducible analyses of sediment transport influenced by bioconstructions across species and case morphologies.
- Identifying data gaps (e.g., geographic or temporal generalizability) and opportunities for data standardization (metadata schemas, units, and naming conventions).