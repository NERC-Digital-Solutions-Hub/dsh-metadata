# Data collection methods (adapted from Wanless et al. (2023) Journal of Animal Ecology ) with subheadings used in the Methods of that paper

- Overview
  - Longitudinal ecological study of common guillemots Uria aalge on the Isle of May covering 1982–2019.
  - Data collected to support understanding of population trends, breeding success, parental effort, chick development, diet, and adult survival.
  - Data sources include standardized field counts, behavioral observations, biometric measurements, prey sampling, and mark–recapture data analyzed with Bayesian models.

## Population trends and environmental data
- Breeding pair counts
  - Standardized counts conducted in early June to estimate breeding pairs; time span 1982–2019.
- Environmental context
  - Mean spring sea surface temperatures (sSST) in February–March calculated for a defined area around the Isle of May that encompasses foraging regions during the breeding season (Feb–Mar data used).
  - SST data sourced from Bundesamt fȕr Seeschifffahrt und Hydographie (BSH).

## Breeding phenology, fledging success and chick growth index
- Chick rearing observations
  - Data from 536–1014 pairs annually (mean ~832 ± 114 SD) across various cliff types and bird densities at ~250 m of cliff.
  - Visual checks 3–5 times daily to determine hatching and fledging dates.
- Fledging criteria
  - A chick is considered fledged if it is at least 15 days old and absent from the breeding site, with dates known to within one day.
- Fledging mass index
  - Weights of fledgling chicks with wing length ≥ 60 mm used to index fledging mass; annual growth rate (g/mm) calculated from mean mass and mean age at fledging for these chicks.
  - Growth during the linear period estimated using chicks with wing lengths 25–59 mm.
- Sample sizes
  - Annual chick weights: average n ≈ 59 (range 6–140).

## Parental effort
- Attendance monitoring
  - Daily checks during the chick-rearing period (annual mean number of days ~27; range 7–37) to determine proportion of chicks attended by both parents, one parent, or neither.
- Parental effort index
  - Weighted sum (WS) index computed over time, ranging from 0 (all chicks attended by both parents) to 2.0 (all chicks unattended).
  - State coding: both parents (i=0, X0=0), one parent (i=1, X1=1), neither (i=2, X2=2); weights Wi correspond to state proportions by year.
- Detailed behavioral observations
  - Subset analysis of time spent together by pairs after chick feeding conducted over 32 days across 22 years.

## Guillemot chick diet
- Diet data collection
  - All-day watches in two plots to record frequency of chick feeds (annual mean ~57 chicks observed; range 19–158) across 2–8 days per year.
- Prey identification and sizing
  - Recorded fish species and qualitative length class (very small to very large) relative to parent’s bill; length classes converted to actual lengths using measurements from captured fish.
- Key prey categories
  - Primarily Ammodytidae (lesser sandeel) and Clupeidae (sprat; with some herring).
- Nutritional analysis
  - Fish samples analyzed to derive species-specific length–calorific value relationships; calorific values calculated from body composition (fat and protein) with standard energy conversions.
- Energy value estimation
  - Energy values estimated from calorific content; prey length and calorific values used to derive annual energy-value contrasts (relative calorific values) as deviations from species-specific length–calorific curves.

## Adult survival and body mass
- Adult sampling
  - Marked adults (color rings) tracked across years; mean annual marked count ~326 (range 101–418) with a focal sample of 1025 unique individuals observed over time.
- Survival estimation
  - Overwinter adult survival estimated with Bayesian Cormack–Jolly–Seber models implemented in JAGS within R; full time dependence among parameters; non-informative priors (Uniform 0–1).
  - Model specifics: three independent MCMC chains (9,000 iterations; burn-in 900; thinning by 10).
- Chick-rearing mass measurements
  - Adults with chicks weighed (nearest 5 g) to estimate mean mass of chick-rearing adults (annual sample mean ~41; range 1–130) in proximity to breeding data.

## References and methodological foundation
- The dataset and methods draw on a broad set of historical and contemporary references for breeding biology, energy content analyses, and Bayesian survival modeling, including Harris & Wanless, Thaxter et al., Wanless et al., and standard statistical sources for Bayesian capture–recapture analysis (JAGS, Cormack–Jolly–Seber).