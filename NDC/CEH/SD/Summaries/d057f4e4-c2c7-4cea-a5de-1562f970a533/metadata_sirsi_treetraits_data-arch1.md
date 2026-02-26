# Western Ghats tree functional trait data

## Overview
- Dataset collected from a farm near Sirsi, Karnataka (latitude 14.49 N, longitude 74.75 E; altitude 538 m).
- Measurements conducted in summer 2021.
- Focus on thermal, hydraulic, and leaf-trait data across multiple species.
- Variables include species name, species code, season, canopy position, leaf habit, and a wide set of trait measurements with replicates.

## Thermal traits
- 1.1.1 CO2 assimilation temperature relationship (A-T curves)
  - Measure net CO2 assimilation (A_net) versus leaf temperature using LICOR 6400 with a Li-6400 XT chamber.
  - Conditions: irradiance ~1000 μmol m^-2 s^-1, CO2 ~400 ppm, relative humidity ~60±5%.
  - Procedure: stable readings at each temperature; target leaf temperatures sampled across 20–48 °C (with leaf temperatures often limited by instrument/physiology).
  - Data modeling: fit A_net = A_opt × exp[-((T_iets − T_opt)/Ω)^2] to derive:
    - T_opt: temperature of maximum A_net
    - A_opt: A_net at T_opt
    - Ω: temperature difference between T_opt and the 37% A_opt drop point
    - Tspan80%: width of the temperature range where A_net > 80% of A_opt
    - T_air_at_Topt, T_leaf_at_Topt, VPD_at_Topt, Cond_at_Topt
- 1.1.2 Temperature limits of Photosystem II (PSII) functioning (T50)
  - Assess PSII thermotolerance via chlorophyll a fluorescence (Fv/Fm) after leaf discs are heated in a water bath (temperatures: 25, 40, 45, 47.5, 50 °C for 30 min).
  - Post-treatment, leaves dark-adapt 30 min; measure Fv/Fm with PAM fluorometer.
  - Fit four-parameter logistic curve (R package drc) to estimate T50: temperature at which Fv/Fm drops to 50% of the upper asymptote.
  - Sampling: 5 independent leaf discs per temperature per individual; 5–6 individuals per species.

## Hydraulic traits
- 1.2.1 P50 (water potential at 50% loss of hydraulic conductivity)
  - Embolism vulnerability curves measured with pneumatic method combined with bench dehydration.
  - Process: discharge xylem air into a vacuum reservoir, measure air discharge; determine leaf water potential (Scholander pressure chamber) on leaves cut from measured branches.
  - Repeated across dehydration until a sigmoidal air-discharge vs. leaf water potential curve is obtained; P50 is the leaf water potential at 50% air discharge.
- 1.2 Leaf turgor loss point (TLP)
  - Bench-dry method (pressure-volume approach).
  - Measure relative water content (RWC) and leaf water potential during drying; determine TLP as the transition point from curved to linear in Ψ_leaf vs 100−RWC plot.

## Leaf traits
- 1.3.1 Leaf area, LMA, LDMC
  - Fresh leaves scanned (LiDE scanner); processed in ImageJ to obtain leaf area.
  - Leaf mass per area (LMA) and leaf dry mass per unit leaf fresh mass (LDMC) determined per standard protocols.
- Data sources and references
  - Protocols and methods adapted from Hazir et al. 2022; foundational methods from June et al. (2004) for temperature dependence of photosynthetic electron transport; Sastry et al. (2018); Curtis et al. (2014); and standard analyses (Ritz & Streibig 2005; related methodological papers listed in the document).
  - Author list for the trait compilation includes June, Evans, and Farquhar (photophysiology context) and other cited contributors.

## Data structure and variables
- Dataset contains: species, spcode, Season, cancat (canopy position/topography), leafhabit (deciduousness), plus a comprehensive set of trait variables.
- Example and replicate structure
  - Many trait fields have paired entries (e.g., VPD_at_Topt_1 and VPD_at_Topt_2; Cond_at_Topt_1 and Cond_at_Topt_2), indicating replicates or alternate measurements.
- Key thermal/hydraulic/leaf variables
  - Aopt, Aopt.se, Topt, Topt.se, omega (Ω), omega.se, Tspan80%, Tair_at_Topt, Tleaf_at_Topt, VPD_at_Topt, Cond_at_Topt, Transp_at_Topt, wp, wpse, P50, wood_density, t50, t5, dw, dwslope, dwslope.se, qymax.com, ldmc, ldmc.se, Leafarea.se, leafperimeter, leafperimeter.se, leafwidth, leafwidth.se, lma, lma.se, Turgor_loss_point, TLP_stdev, TLP_std_error, number_of_samples_TLP.
- Data capture details
  - In situ, high-irradiance, controlled humidity conditions for thermal curves.
  - Replicated measurements across individuals and species for robust estimation.

## Sampling design and context
- Location and environment
  - Farm near Sirsi, Karnataka, India; site coordinates and elevation provided.
- Temporal scope
  - Summer 2021 for thermal measurements; PSII, P50, TLP measured across multiple individuals/species with specified sampling cadence.
- Organismal scope
  - Multi-species hardwoods typical of Western Ghats forest; species-level trait data intended for cross-species comparisons and trait-based analyses.

## Data quality, usage, and potential applications
- Quality assurance and traceability
  - Detailed measurement protocols, stabilization criteria, and explicit model fittings documented.
  - Data are designed for cross-dataset comparability and potential integration into trait portals with metadata.
- Analytical uses
  - Identify correlations among thermal optima (T_opt, A_opt) and drought tolerance (P50, TLP).
  - Develop predictive models linking leaf traits (LMA, LDMC) with photosynthetic temperature responses and hydraulic safety.
  - Explore species-specific strategies for heat tolerance and water transport under climate stress.
- Data integration and discoverability
  - Variables are well-labelled with explanations; replicates explicitly indicated, aiding data merging and meta-analyses.
  - Potential to combine with other trait datasets from the Western Ghats or broader tropical datasets.

## Considerations and limitations
- Local scale and sample scope
  - Data are site- and season-specific (Sirsi, summer 2021); extrapolation to other regions or seasons requires caution.
- Replication and variability
  - Some traits have multiple replicates; exact sample sizes per species for each trait should be consulted in the dataset metadata.
- Environmental context
  - Thermal measurements are conducted on sunlit terminal leaves with controlled chamber conditions; real-world leaf temperatures may differ in situ.

## Summary of key takeaways
- The Western Ghats tree functional trait data provide comprehensive thermal, hydraulic, and leaf-trait measurements for multiple tree species, with detailed methodological documentation.
- Thermal traits include A_opt and T_opt from in situ A-T curves and PSII T50 from fluorescence thermotolerance assays.
- Hydraulic traits include P50 and leaf turgor loss point, obtained through pneumatic vulnerability assessments and bench-dry pressure-volume methods.
- Leaf traits include leaf area, LMA, and LDMC derived from scanned leaves.
- The dataset emphasizes replicability, methodological transparency, and utility for correlational analyses and predictive modelling of plant responses to temperature and water stress.