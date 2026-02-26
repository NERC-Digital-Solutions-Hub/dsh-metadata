# Hydraulic mobility of aquatic insect (Trichoptera) bioconstructions and incorporated sediments

## Overview
- Investigates how caddisfly (Trichoptera) case construction influences sediment transport in rivers.
- Uses a hydraulic flume to compare bed shear stress needed to move:
  - empty caddisfly cases
  - individual sediment grains released from cases
- Three caddisfly species/case types examined: two tubular cases (Potamophylax latipennis and Sericostoma personatum) and one domed case (Agapetus fuscipes).
- Study period: flume experiments Aug 20–Sep 20, 2019; collection of specimens on Jun 17 and Aug 18, 2019.

## Experimental design
- Center-mounted cases and sediment in the flume; hydraulic discharge increased through 11 steps.
- At each discharge step, sediment eroded was quantified from photographs.
- Objectives include: determining how case morphology affects sediment transport and establishing entrainment thresholds for cases and loose sediment.

## Data files and key variables

- S1_Velocimetry_data
  - Contains post-processed Acoustic Doppler Velocimetry (ADV) outputs for each discharge step.
  - Includes mean and standard deviation of velocity components (U, V, W), data quality metrics (SNR, correlation), turbulent kinetic energy (TKE), and bed shear stress (Tb).
  - Variables include: Date, Discharge_step, raw and adjusted velocities (Umean, Ustd, Vmean, Vstd, Wmean, Wstd), correlations (U_corr, V_corr, W_corr), SNR values, TKE, Tb.

- S2_Case-grain-size-distribution_data
  - Grain size distributions for each caddisfly case from sieving case sediment.
  - Variables: Sample_ID (G, S, L followed by individual number), Sed_mass (pre-sieving), Sieved_mass, Loss_mass, Loss_percent; sieve size references for passing sizes; mass values in grams.

- S3_Entrainment_data
  - Percentage of sediment entrained at each flow stage (1–11), determined by photography of sediment remaining on the measurement platform.
  - Variables: Sample_ID, State (Case or loose sediment), Discharge_step, Values as cumulative percentage area transported.

- S4_Case-and-entrainment-threshold_data
  - Case characteristics (mass, axes a, b, c) and entrainment thresholds for movement of cases and loose sediment.
  - Variables: Case/Sediment ID, State (Case or loose sediment), Mass, a (long axis), b_D50 (intermediate axis or D50 for loose sediment), c (short axis), E_10 (bed shear stress threshold for entrainment), E_90 (bed shear stress threshold for general movement).

## How the data can be used (analytical aims)
- Correlate case morphology (mass, a, b, c axes) with entrainment thresholds (E_10, E_90) and with observed sediment transport.
- Link hydraulic conditions (U, V, W, TKE, Tb) from S1 to entrainment and sediment loss in S3 and S4.
- Compare transport dynamics of empty cases versus sediment released from cases to understand how bioconstructions alter bed stability.
- Integrate grain-size distributions (S2) with entrainment data to assess selective transport or preservation of particular sediment sizes.
- Explore species- and morphology-specific differences in mobility and thresholds to infer ecological and hydraulic implications.

## Context and collection details
- Specimens collected: 17 June and 18 August 2019.
- Experiment duration: 20 August–20 September 2019.
- Data collection focused on central flume placements and controlled discharge increments to capture a range of hydraulic conditions.

## Data quality and accessibility notes
- S1 provides both raw and adjusted velocity measurements with accompanying quality metrics (SNR, correlation) and derived turbulence metrics (TKE) and bed shear stress.
- S2–S4 provide structured, labeled datasets with explicit identifiers linking case morphology, sediment properties, transport observations, and thresholds.
- Datasets are organized to enable reconstruction of flow-stage–dependent transport dynamics and cross-dataset analyses (velocity fields, sediment entrainment, and morphological thresholds).