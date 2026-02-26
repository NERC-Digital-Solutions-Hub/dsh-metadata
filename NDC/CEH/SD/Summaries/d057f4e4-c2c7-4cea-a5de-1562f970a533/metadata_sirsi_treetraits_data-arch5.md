# Western Ghats tree functional trait data

## Purpose and scope
- Dataset containing thermal, hydraulic, and leaf trait measurements for trees in the Western Ghats.
- Site: Farm near Sirsi, Karnataka; coordinates 14.49 N, 74.75 E; altitude 538 m.
- Measurements conducted in summer 2021; data stored in Treetraits_Sirsi_WesternGhats.csv.

## Data file, site metadata, and scope
- File name: Treetraits_Sirsi_WesternGhats.csv
- Spatial and temporal metadata:
  - Site coordinates and altitude provided.
  - Sampling period: summer 2021; leaf measurements referenced for post-monsoon season in some analyses.
- Taxa and sampling context:
  - Includes species name (species), species code (spcode), season (Season), canopy position (cancat), and leaf habit (leafhabit).
  - Replication across individuals and leaves with multiple derived metrics.

## Measured traits and their structure
- Thermal traits
  - CO2 assimilation temperature response (Anet) and related metrics:
    - Aopt: net photosynthesis rate at optimum temperature.
    - Topt: temperature at which Anet is maximal.
    - Aopt.se, Topt.se: standard errors.
    - omega_June2004model_param, omega.se: model parameter and its SE.
    - Tspan80%: temperature range where Anet >80% of Aopt.
    - Tair_at_Topt, Tl_minus_Tair_at_Topt: air and leaf temperatures at Topt.
    - VPD_at_Topt, Cond_at_Topt, Transp_at_Topt: vapor pressure deficit, stomatal conductance, and transpiration at Topt.
    - Additional derived terms: dw, dw.se, dwslope, dwslope.se; qymax.com.
- Temperature limits of Photosystem II (T50)
  - T50: temperature at which Fv/Fm declines to 50% of maximum, estimated from dark-adapted fluorescence curves.
  - T50.com: combined (single-species) fit across replicates.
  - T5, t50: additional temperature response parameters and their standard errors (T50 and 5% thresholds).
- Hydraulic traits
  - P50: leaf water potential at which 50% of hydraulic conductivity is lost (embolism vulnerability).
  - Measurement via pneumatic method combined with bench dehydration; leaf water potential determined with Scholander pressure chamber.
- Leaf traits
  - Leaf area (from scanned leaves), leaf mass per area (LMA), and leaf dry matter content (LDMC), following standard protocols.
  - ldmc, ldmc.se; Leafarea.se; leafperimeter, leafwidth, and their standard errors.
  - TLP-related metrics: leaf turgor loss point (TLP) and related statistics (TLP_stdev, TLP_std_error, number_of_samples_TLP).

## Variable definitions and units
- Variables include: species, spcode, Season, cancat, leafhabit, Aopt, Aopt.se, Topt, Topt.se, omega_June2004model_param, omega.se, Tspan80%, Tair_at_Topt, Tl_minus_Tair_at_Topt, VPD_at_Topt, Cond_at_Topt, Transp_at_Topt, wp, wpse, P50, wood_density, t50, t50.se, t5, t5.se, dw, dw.se, dwslope, dwslope.se, T50.com, T5.com, dw.com, dwslope.com, qymax.com, ldmc, ldmc.se, Leafarea.se, leafperimeter, leafperimeter.se, leafwidth, leafwidth.se, lma, lma.se, Turgor_loss_point, TLP_stdev, TLP_std_error, number_of_samples_TLP.
- Units are provided for each variable where applicable (e.g., Aopt in micromol m-2 s-1; Topt in °C; omega in °C; P50 in MPa; VPD_at_Topt in kPa; Cond_at_Topt in mol m-2 s-1; wp and wpse in MPa; LDMC in g/g; LMA in g m-2; leaf area in cm2; temperatures in °C; etc.).

## Data collection and processing methods
- Thermal traits (A-T curves)
  - In situ measurements with portable IRGA Li-6400 XT and leaf chamber Li-6400-40.
  - High irradiance (~1000 μmol m-2 s-1), CO2 ~400 ppm, RH ~60%.
  - Temperature steps from ~20 to ~48 °C with stabilization criteria (stability thresholds for Anet, gs, Rh, and Tleaf).
  - Leaf samples taken from sunlit terminal branches along the slope; starting leaf temperatures constrained by equipment and leaf response.
  - Curve fitting: Anet = Aopt × exp(-((Tiet - Topt)/Ω)^2) as per June et al. 2004; derived parameters include Aopt, Topt, Ω, Tspan80%.
- Temperature limits of PSII (T50)
  - Leaf discs heated in a temperature-controlled water bath (25, 40, 45, 47.5, 50 °C) for 30 min.
  - Post-treatment, leaves dark-adapted 30 min; Fv/Fm measured with PAM 2500 fluorometer.
  - Four-parameter logistic model fitted (lower asymptote fixed at zero) to estimate T50.
  - Five discs per temperature per individual; replicated across 5–6 individuals per species.
- Hydraulic traits (P50)
  - Pneumatic method with bench dehydration to produce embolism vulnerability curve.
  - Xylem air discharge measured with a partial vacuum; leaf water potential determined via Scholander pressure chamber.
  - Repeated across the dehydration process to map air discharge vs. leaf water potential.
- Leaf turgor loss point (TLP)
  - Bench-dry pressure-volume method; relative water content vs leaf water potential to identify the transition point (non-linear to linear) indicating TLP.
- Leaf traits (area, LMA, LDMC)
  - Leaf area measured from scanned leaves; LMA and LDMC derived using standard protocols (Wilson et al. 1999).
  - Image processing with ImageJ (v1.52p).

## Data quality, replication, and provenance
- Replication:
  - 5–6 individuals per species for T50; multiple leaves/discs per temperature for PSII measurements.
  - Combined fits (com) used for some PSII-derived metrics.
- Quality indicators:
  - Standard errors reported for key estimates (Aopt.se, Topt.se, T50.se, t50.se, t5.se, dw.se, dwslope.se, ldmc.se, Leafarea.se, leafperimeter.se, leafwidth.se, lma.se, etc.).
  - Clear documentation of measurement protocols and data processing steps.
- Provenance and references:
  - Methodological references cited for temperature response modeling, PSII thermotolerance, pneumatic embolism measurement, and leaf trait protocols.
  - Author list includes June, Evans, and Farquhar; multiple supporting literature cited for context and methods.

## Access, sharing, and documentation considerations for reuse
- Metadata depth:
  - Detailed variable explanations included for each column, enabling understanding of the dataset’s structure and derivation.
  - Instrumentation and measurement conditions explicitly described (instruments, irradiance, CO2, RH, temperature steps).
  - Sampling site and date provided to support georeferencing and temporal analyses.
- Reuse readiness:
  - CSV format with explicit variable names and explanations supports integration into data portals and catalogues.
  - References and provenance included to support methodological reproducibility and traceability.
- Governance considerations for Data Stewards:
  - Ensure versioning and licensing information accompany data releases.
  - Maintain and publish a data dictionary capturing all variable definitions, units, and units changes over time.
  - Track data provenance: site, sampling date, instrument models, measurement protocols, and processing steps.

## Author, references, and provenance
- Author list: June, Evans, and Farquhar (and collaborators on underlying protocols).
- Key references:
  - June et al. 2004: temperature dependence model for photosynthesis.
  - Sastry et al. 2018; Curtis et al. 2014: leaf thermotolerance and recovery.
  - Ritz & Streibig 2005; Baz et al. protocols for data analysis.
  - Bittencourt et al. 2018; Pereira et al. 2016; Sperry et al. 1988: pneumatic embolism methods and plant hydraulics.
  - Hazir et al. 2022; Bartlett et al. 2012; Schneider et al. 2012; Wilson et al. 1999: leaf traits and analytical methods.