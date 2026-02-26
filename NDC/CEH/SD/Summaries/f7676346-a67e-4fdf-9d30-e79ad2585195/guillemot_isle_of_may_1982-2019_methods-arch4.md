# Data collection methods (adapted from Wanless et al. (2023) Journal of Animal Ecology ) with subheadings used in the Methods of that paper

## Overview
- Long-term, multi-year study of breeding common guillemots (Uria aalge) on the Isle of May, linking population trends, breeding biology, diet, and survival with environmental context.
- Data sources include standardized counts, detailed chick-rearing observations, diet and energy analyses, adult marking, and environmental data (sea surface temperature).

## Data collected and time frame
- Population trends: standardized counts of breeding pairs conducted in early June from 1982 to 2019.
- Environmental context: mean spring Sea Surface Temperatures (sSST) in February–March around the Isle of May (56°–57°N; 1°–3°W) using data from Bundesamt für Seeschifffahrt und Hydrographie (BSH).
- Biological measures span breeding phenology, fledging success, chick growth, parental effort, diet, adult survival, and body mass.

## Key measures and methods

- Breeding phenology, fledging, and chick growth
  - Data from 536–1014 breeding pairs annually (mean ~832 ± 114 SD) across cliff types and densities.
  - Hatching and fledging dates determined from daily visual checks (3–5 times daily).
  - Fledging: chick must reach at least 15 days old unless other evidence indicates otherwise.
  - Fledging metrics include mass-based indices (for chicks with wing ≥60 mm) and a growth rate index (g/mm) computed from weights and age at fledging; wings 25–59 mm used for linear-growth growth rate estimates.
  - Wing length and mass data underpin fledging readiness.

- Parental effort
  - Daily attendance tracked during chick-rearing; categories include both parents present, one parent present, or neither.
  - An annual parental-effort index (weighted sum, WS) ranges from 0 (all chicks attended by both parents) to 2.0 (all chicks unattended), incorporating the observed state proportions.
  - Occasional subset (32 days over 22 years) with detailed observations of pair co-attendance after chick feeding.

- Guillemot chick diet
  - All-day watches recorded prey species and qualitative length classes (very small to very large) fed to chicks in two plots during the chick-rearing period.
  - Prey lengths converted to actual measurements using fish collected from the colony during ringing.
  - Diet largely comprised Ammodytidae (lesser sandeel) and Clupeidae (sprat, with some herring); fish samples used for species-specific calorific values.
  - Calorific values determined via calorimetry (1985–1987) and later via body composition analyses; energy content computed from fat and protein content.
  - Systematic watches quantified frequency of feeds; annual estimates of prey-species proportions and mean prey length; energy-value relationships derived from species-specific data; annual relative calorific values estimated as deviations from species-specific length-energy curves.

- Adult survival and body mass
  - Marked adults: up to 1,025 individuals tracked; mean annual observed marked birds ~326.
  - Overwinter survival estimated with Bayesian Cormack–Jolly–Seber (CJS) models implemented in JAGS within R; full time dependence assumed for parameters; non-informative priors (Uniform 0–1) for survival and recapture probabilities; three independent MCMC chains run with burn-in and thinning.

## Data processing and analysis

- Energetics and diet processing
  - Fat and protein contents of prey used to compute energy (fat: 39.6 kJ g⁻¹; protein: 23.7 kJ g⁻¹).
  - Energy values tied to dry mass measurements, fat-free mass, mineral content, and elemental composition to derive total energy per prey item.
  - Yearly energy estimates for prey in chick diet produced by integrating calorific value with prey length data.

- Growth and growth-rate indices
  - Growth rate index calculated as the ratio of mean fledging mass (for wings ≥60 mm) to mean age at fledging (days).
  - Annual growth-rate estimates also derived from chicks with wing lengths 25–59 mm.

- Demography and behavior
  - Adult survival modeled with Bayesian CJS; chick-attendance and parental effort analyzed as part of understanding demographic rates.
  - 32-day detailed behavioral dataset used to quantify time spent together after chick feeding.

## Data quality, governance, and metadata considerations

- Standardization and comparability
  - Use of standardized counts, consistent procedures for hatching/fledging determination, and uniform definitions of metrics (e.g., fledging age, WS index) across years.
  - Long-running time series enabling robust trend analyses and cross-year comparisons.

- Documentation and transparency
  - Clear methodological descriptions for data collection and processing, including reference to multiple supporting studies and calibration efforts (calorimetry, body composition, and energy calculations).

- Data limitations and variability
  - Acknowledgment of annual variability in sample sizes (e.g., chick counts, adult samples) and potential seasonal/daily variation affecting observations.
  - Observer effort and exact timing of checks discussed as factors influencing accuracy of certain estimates (e.g., breeding success).

## References
- Methods adapted from Wanless et al. (2023) Journal of Animal Ecology; additional foundational references include Allen (1989), Ashbrook et al. (2008, 2010), Cormack (1964), Crisp (1971), Harris et al., Thaxter et al. (2009, 2010), Wanless & Harris (1986), Wanless et al. (2023), and related statistical software documentation (JAGS, R).