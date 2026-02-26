# Western Ghats tree functional trait data

## Overview
- Dataset from a farm near Sirsi, Karnataka (latitude 14.49 N, longitude 74.75 E; altitude 538 m).
- Measurements conducted in summer 2021.
- Focuses on tree functional traits organized into thermal, hydraulic, and leaf trait categories.
- Data collected on sunlit terminal branches; multiple individuals per species; includes a comprehensive set of derived parameters (e.g., Topt, Aopt, P50, TLP, LMA, LDMC).

## Spatial and Sampling Context
- Location: Farm close to Sirsi, Karnataka; coordinates 14.49 N, 74.75 E; altitude 538 m.
- Sampling design: leaves collected from sunlit terminal branches along the slope; measurements span summer and post-monsoon periods.
- Replication: 5–6 individuals per species for some traits (e.g., PSII T50); data includes multiple measurements per species and season.
- Temporal coverage: measurements reported for summer 2021; partial seasonal context with post-monsoon values for certain thermal traits.

## Data Variables and Schema
- Core fields (examples): 
  - species, spcode, Season, cancat, leafhabit
  - Thermal traits: Aopt, Aopt.se, Topt, Topt.se, omega_June2004model_param, omega.se, Tspan80%, Tair_at_Topt, Tleaf_at_Topt, VPD_at_Topt, Cond_at_Topt, Transp_at_Topt
  - Hydraulic traits: P50, P50.se
  - Leaf traits: ldmc, ldmc.se, Leafarea.se, leafperimeter, leafperimeter.se, leafwidth, leafwidth.se, lma, lma.se, Turgor_loss_point, TLP_stdev, TLP_std_error, number_of_samples_TLP
  - Additional derived/related metrics: dw, dw.se, dwslope, dwslope.se, T50.com, T5.com, dw.com, dw.se, dwslope.com, qymax.com
- Units and descriptions:
  - Many fields are dimensionless (e.g., spcode, Season) or have clearly defined units (e.g., Aopt in μmol m−2 s−1, Topt in °C, VPD_at_Topt in kPa, Cond_at_Topt in mol m−2 s−1, LMA in g m−2, etc.).
  - Variable explanations provided for most columns (e.g., what Aopt, Topt, P50 represent, and how T50 for PSII was estimated).
- Data scope:
  - Thermal traits include CO2 assimilation temperature response and PSII thermal tolerance (T50).
  - Hydraulic trait includes water potential at 50% conductivity loss (P50) and leaf turgor loss point (TLP).
  - Leaf trait includes leaf area, LMA, LDMC, and related leaf characteristics.

## Measurements & Methods
- Thermal traits:
  - CO2 assimilation vs temperature (A-T curve) measured in situ with a Li-6400 XT IRGA and leaf chamber; high irradiance (~1000 μmol m−2 s−1), CO2 ~400 μmol mol−1, RH ~50–60%.
  - Temperature range sample points typically: 20–48 °C; stabilization criteria defined (steady-state thresholds) and data logged after stabilization.
  - Model applied: A_net = A_opt × exp(-((T_leaf - T_opt)/Ω)^2); parameters include A_opt, T_opt, Ω, and derived Tspan80%.
  - Outcome: estimates of T_opt, A_opt, and related thermal response metrics (e.g., Tair_at_Topt, VPD_at_Topt, Cond_at_Topt).
- PSII thermal tolerance (T50):
  - Leaf discs heated in water bath to set temperatures (25, 40, 45, 47.5, 50 °C) for 30 min; Fv/Fm measured after dark adaptation.
  - Four-parameter logistic curve fitted to Fv/Fm vs temperature to estimate T50 (50% loss of maximum PSII efficiency); 5–6 individuals per species.
- Hydraulic traits (P50) and leaf turgor:
  - P50: pneumatic method to measure xylem embolism with bench dehydration; air discharge vs leaf water potential yields a sigmoidal curve; P50 is the point of 50% air discharge.
  - Turgor loss point (TLP): bench-dry method using pressure-volume curves; TLP determined from the transition point in a plot of leaf water potential vs 100−RWC.
- Leaf traits:
  - Leaf area measured from scanned leaves (ImageJ analysis); LMA and LDMC computed following standard protocols.
- Documentation and sources:
  - Method descriptions and references cited for each trait (e.g., June et al. 2004 model, Sastry et al. 2018, Pneumatic method literature, Prometheus/pressure-volume references, standard leaf-trait protocols).

## Data Quality, Standards, and Limitations
- Data organized with explicit variable explanations and units, facilitating GIS integration (e.g., spcode for species, season, and canopy position).
- Multi-method data with several derived metrics; measurement uncertainty captured via standard errors in several fields (e.g., Aopt.se, Topt.se, P50.se, LMA.se, etc.).
- Spatial resolution is at a single site with detailed trait data per species and individual-level replication for some traits; broader geographic extrapolation should consider site-specific conditions.
- Temporal coverage limited to the reported seasons (summer 2021 and notes on post-monsoon for thermal curves); seasonality may affect some trait values.
- Data availability note: dataset file named Treetraits_Sirsi_WesternGhats.csv; no direct access link provided in the text.

## Potential GIS Applications
- Spatial visualization of trait distributions across the Western Ghats by species or functional groups.
- Mapping key functional trait gradients (e.g., T_opt, A_opt, P50, TLP, LMA) in relation to climate layers, elevation, and habitat types.
- Integration with species distribution data to model vulnerability to drought and heat stress (via P50, TLP, T50).
- Creation of map-ready attribute tables linking trait profiles to individual trees or populations for policy or public-facing dashboards.
- Data can support habitat suitability analyses, climate change impact assessments, and conservation prioritization by trait-based functional diversity.

## Access and Availability
- File: Treetraits_Sirsi_WesternGhats.csv
- Site/context: Farm near Sirsi, Karnataka; precise coordinates and altitude provided; measurements in summer 2021.