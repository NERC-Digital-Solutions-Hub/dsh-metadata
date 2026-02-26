# Western Ghats tree functional trait data

## Overview
- Dataset from a farm near Sirsi, Karnataka (14.49 N, 74.75 E; altitude 538 m) with measurements conducted in summer 2021.
- Focuses on tree functional traits across thermal, hydraulic, and leaf characteristics.
- Data collected at the site include in situ physiological measurements and leaf/wood traits for multiple species.

## Data Content
- File: Treetraits_Sirsi_WesternGhats.csv
- Site metadata: location, altitude, season.
- Trait categories:
  - Thermal traits
  - Hydraulic traits
  - Leaf traits
- Key variables and derived parameters (examples):
  - Thermal: Aopt (net photosynthesis at optimum temperature), Topt (temperature of max A net), Aopt.se, Topt.se, omega-related parameters, Tspan80%, Tair_at_Topt, Tleaf_at_Topt, VPD_at_Topt, Cond_at_Topt, Transp_at_Topt, etc.
  - PSII tolerance: T50 (temperature causing 50% loss of PSII function) with references to PSII fluorescence curves (Fv/Fm).
  - Hydraulic: P50 (water potential at 50% loss of hydraulic conductivity) via pneumatic method; wp (daytime water potential) and wpse (standard error).
  - Leaf turgor: Turgor loss point (TLP) with standard metrics and sample counts.
  - Leaf traits: leaf area, leaf mass per area (LMA), leaf dry matter content (LDMC), leaf dimensions (perimeter, width), ldmc.se, Leafarea.se, lma.se, and related standard errors.
  - Derived/combined metrics: com variants (e.g., T50.com, dw.com, etc.) for species-level syntheses across replicates.
- Data structure notes: includes species name (species), species code (spcode), season, canopy position (cancat), and leaf habit; many columns include standard errors or “com” (combined) estimates.

## Methods
- Thermal traits (1.1)
  - 1.1.1 CO2 assimilation vs temperature (A-T) curves measured in situ with a Li-6400 XT IRGA connected to a leaf chamber; conditions: irradiance ~1000 μmol m^-2 s^-1, CO2 ~400 μmol mol^-1, RH ~60%.
  - Leaves sampled from sunlit terminal shoots along the slope; measurements spanned typically 20–48°C chamber air temperatures with leaf temperatures constrained by equipment and leaf regulation; stabilization criteria defined for steady-state data.
  - Temperature response modeled with an equation from June et al. (2004) to estimate Topt, Aopt, and related parameters (omega, Tspan80%, etc.).
  - 1.1.2 PSII thermal limits (T50) from fluorescence (Fv/Fm) curves using leaf discs heated in a temperature-controlled water bath at specified temperatures; 30 min exposures; Fv/Fm measured after dark adaptation and curves fitted with a four-parameter logistic model (R drc package) to estimate T50 per individual; 5–6 individuals per species.
- Hydraulic traits (1.2)
  - 1.2.1 P50 estimated from branch xylem vulnerability curves using the pneumatic method combined with bench dehydration; air discharge is measured as leaf water potential is recorded with a Scholander pressure chamber.
  - 1.2.2 Leaf turgor loss point estimated with the bench-dry method using pressure-volume curves; Ψleaf vs (100 − RWC) to identify the transition point.
- Leaf traits (1.3)
  - Fresh leaves scanned; leaf area measured with ImageJ; LMA and LDMC calculated following standard protocols.
- Data derivation and reporting
  - References include June et al. (2004), Sastry et al. (2018), Curtis et al. (2014), and methodological sources for hydraulic and leaf traits.
  - Several derived metrics are reported with standard errors to reflect measurement uncertainty.

## Data Quality and Metadata
- Site-specific dataset from a single location with summer 2021 collection; sample sizes reported for PSII and P50 components (e.g., 5–6 individuals per species for T50).
- Variables include both raw measurements and model-derived estimates, with associated standard errors (e.g., Aopt.se, Topt.se, T50.se, leaf trait standard errors).
- Metadata and methods are described to enable reproducibility and cross-study comparability, with explicit instrument settings and measurement protocols.

## Usage and Considerations for Data Leaders
- Comprehensive, multi-trait dataset suitable for analyzing trait correlations across thermal, hydraulic, and leaf dimensions in tropical trees.
- Rich metadata supports data discoverability and potential integration with broader trait databases; attention needed for unit consistency and method-specific caveats (e.g., in situ A-T measurements versus lab-based protocols).
- Data can inform comparative analyses of species-specific drought and heat tolerance, as well as synthesis across sites if similar datasets exist.
- Potential limitations include single-site coverage and season-specific sampling; derived parameters (e.g., com metrics) should be interpreted with awareness of replicate aggregation.

## Author and References
- Author list: June, Evans, and Farquhar (and collaborators noted in referenced protocols).
- Key references include: June et al. (2004); Sastry et al. (2018); Curtis et al. (2014); and methodological sources on pneumatic hydraulic measurements, pressure-volume curves, and ImageJ-based leaf trait measurements.