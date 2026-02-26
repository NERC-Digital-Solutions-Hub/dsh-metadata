# Western Ghats tree functional trait data

- Overview: A dataset capturing thermal, hydraulic, and leaf traits for trees in the Western Ghats to support environmental monitoring and policy evaluation over time.
- Purpose for analysts: Provides standardized trait measures that can be used to assess environmental health, species responses to temperature and drought, and to monitor policy-related environmental performance.

## Location, timing, and sampling context
- Site: Farm near Sirsi, Karnataka, India.
- Coordinates: 14.49 N, 74.75 E; altitude 538 m.
- Sampling period: Summer 2021.
- Data format: CSV file named Treetraits_Sirsi_WesternGhats.csv.

## Measurements and trait groups

### 1.1 Thermal traits
- 1.1.1 CO2 assimilation versus temperature (A-T) to define temperature response and optima for photosynthesis.
  - Method: In situ measurements with LI-COR 6400XT (leaf chamber LI-6400-40); irradiance ~1000 µmol m-2 s-1; CO2 ~400 ppm; RH ~50–60%.
  - Key outputs: Aopt (net assimilation at optimum), Topt (temperature of peak A net), omega (temperature difference between Topt and 37% of Aopt), Tspan80% (temperature range above 80% of Aopt), and related parameters with standard errors (e.g., Aopt.se, Topt.se, omega.se).
  - Data range: Tleaf at opt approx 21.4–45.0 °C in summer; 23.2–41.1 °C post-monsoon.

- 1.1.2 Temperature limits of Photosystem II (PSII) function (T50) from chlorophyll a fluorescence (Fv/Fm).
  - Method: Leaf discs heated in a water bath (temperature-controlled) and measured after dark adaptation; Fv/Fm response curves fitted with four-parameter logistic model.
  - Output: T50 (temperature at which Fv/Fm declines to 50% of maximum), with per-individual estimates across 5–6 individuals per species.

### 1.2 Hydraulic traits
- 1.2.1 P50: Water potential at 50% loss of hydraulic conductivity.
  - Method: Pneumatic method combined with bench dehydration to generate air-discharge vs leaf water potential curves; leaf water potential measured with Scholander chamber.
  - Output: P50 values (and associated sampling details) representing embolism susceptibility.

- 1.2.2 Leaf turgor loss point (TLP)
  - Method: Bench-dry/pressure-volume approach; plot Ψleaf vs (100 − RWC) to identify TLP.
  - Output: Turgor loss point with related statistics (stdev, std_error, number of samples).

### 1.3 Leaf traits
- Leaf area (from scanned leaves, processed with ImageJ).
- Leaf mass per area (LMA) and leaf dry matter content (LDMC).
- Data provenance: Standard protocols referenced (Hazir et al. 2022); leaf trait metrics include area, LMA, LDMC, and related derivatives.

## Variables and data structure
- Core fields: species, spcode, Season, cancat (canopy position/topography), leafhabit (deciduousness), plus a comprehensive suite of trait variables across thermal, hydraulic, and leaf domains.
- Thermal outputs include Aopt, Topt, omega, Tspan80%, Tair_at_Topt, Tleaf_at_Topt, VPD_at_Topt, Cond_at_Topt, Transp_at_Topt, wp, wpse, and related SEs.
- Hydraulic outputs include P50, P50-related metrics, and leaf water potential data.
- Leaf traits include leaf area (and SE), LMA (and SE), LDMC (and SE), Turgor metrics, and related descriptive statistics (e.g., number_of_samples_TLP).
- All values accompanied by standard errors where provided; dataset combines species-level and individual-level measurements.

## Data quality, provenance, and usage
- Collected using standardized, publishable protocols; measurements conducted in situ where feasible and paired with controlled lab measurements (e.g., fluorescence, pneumatic method, pressure-volume curves).
- Documentation includes model equations and references for trait calculations (e.g., Anet temperature response model from June et al. 2004; PSII T50 methodology; pneumatic embolism methods).
- Data management practices align with environmental monitoring norms: verification, quality assurance, data cleaning, transformation, and storage/upload to appropriate data portals.

## How this dataset supports environmental monitoring
- Enables time-series assessment of species’ thermal and hydraulic tolerance in the Western Ghats.
- Facilitates cross-species comparisons of photosynthetic temperature responses and PSII stability under heat stress.
- Supports drought vulnerability analyses through P50 and leaf turgor metrics.
- Can be integrated with climate, soil, and ecosystem datasets to map and chart environmental health indicators across regions and over time.
- Suitable for creating maps, dashboards, and analytic reports that inform policy performance and conservation planning.

## References and methodological notes
- Primary methods and analyses grounded in established literature (e.g., June et al. 2004; Sastry et al. 2018; Curtis et al. 2014; Sperry et al. 1988; Bittencourt et al. 2018; Bartlett et al. 2012; Wilson et al. 1999) as cited in the data documentation.
- Author list for dataset: June, T.; Evans, J. R.; Farquhar, G. D.